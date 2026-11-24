---
name: tutti
description: Read and control Tutti on this Mac. Use for Tutti volume, mute, display brightness, Presets, audio output or microphone selection, per-app audio, Now Playing, and CLI or MCP troubleshooting.
---

# Tutti

Use the installed Tutti MCP tools when your client provides them. Otherwise,
use the bundled CLI. Find it with `command -v tutti` or use
`/Applications/Tutti.app/Contents/Helpers/tutti` when the app is installed there.
Run `tutti --help` for the command syntax.

## Before acting

1. Read `tutti_get_status`, `tutti://status`, or `tutti status --json` for the live
   Remote Snapshot. It includes master volume and mute, outputs, Presets,
   displays, inputs, sounding apps, Now Playing, and Pro status.
2. Use an exact target ID from that snapshot. A full name works when it matches
   one target. On `ambiguousTarget`, use the returned `candidateIDs` to identify
   the requested target. Ask the user if the ID still cannot be determined.
3. Match the action to the request. Absolute levels take integer percentages
   from 0 to 100. Master volume and display brightness also accept signed
   percentage-point changes. For CLI writes, use `--dry-run --json` to check
   the resolved target and permission before submitting the command.
4. Read status after an accepted write when you need to verify the resulting
   state. Check the current state before repeating a toggle, step, or track
   change after a timeout.

## Common workflows

| Goal | CLI |
| --- | --- |
| Check the endpoint, permissions, and available hardware | `tutti doctor --json` |
| Wait for a state change | Run `tutti watch` and read one JSON snapshot per line |
| Set the master volume or lower it by five points | `tutti volume 35` or `tutti volume -5` |
| Set one display's brightness | `tutti brightness display "$display_id" 65` |
| Preview a Preset | `tutti preset "$preset_uuid" --dry-run --json` |
| Choose a microphone, then set its volume | `tutti input select "$input_uid"` followed by `tutti input volume 40` |
| Set a sounding app's volume | `tutti app volume "$bundle_id" 25` |
| Seek in Apple Music or Spotify | `tutti media seek 45.5` |

Quote names with spaces. Put flags before the `--` delimiter when a target
begins with `--`.

## Output and recovery

Commands use readable output in a terminal where applicable. Use `--json` for
machine-readable output regardless of the terminal. Piped data commands output
compact JSON. `watch` emits newline-delimited JSON. `skill` prints this Markdown
offline. Read diagnostic errors from stderr, and use the recovery `hint`.
`doctor` writes its diagnostic report to stdout even when it exits nonzero.

| Exit | Meaning |
| --- | --- |
| `0` | Success |
| `2` | `invalidArguments` |
| `3` | `appNotRunning` |
| `4` | `localControlDisabled` |
| `5` | `unauthorized` |
| `6` | `protocolMismatch` |
| `7` | `unavailable` |
| `8` | `proRequired` |
| `9` | `notFound` |
| `10` | `ambiguousTarget` |

For `appNotRunning`, ask the user to open Tutti. For `localControlDisabled`,
ask them to enable **CLI & MCP** under **Settings → Controllers**. Status,
watch, and diagnostics are free. Writes and CLI dry runs require Tutti Pro.
Use `doctor` to investigate a connection or permission issue.

## MCP

Configure a local stdio server with the absolute path to `tutti` as its command
and `["mcp"]` as its arguments. Use `tools/list` to discover the current input
schemas. Read `structuredContent.snapshot`,
`structuredContent.report`, or `structuredContent.plan` on success. When
`isError` is true, read `structuredContent.error.code` and its `hint`.
