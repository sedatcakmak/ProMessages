# ProMessages

A join / leave / welcome message plugin for Spigot/Paper. Replace the default join and leave broadcasts, send a personal title, action bar and chat message to the joining player, and optionally play sounds.

## Features

- Custom join, first-join and leave broadcast messages.
- Per-player welcome title and subtitle with configurable fade timings.
- Per-player action bar message on join.
- Per-player chat lines on join (separate list for first-join), with a configurable delay and `%center%` support.
- Optional join sound for the joining player and a separate sound broadcast to everyone on join / leave.
- Built-in placeholders (`%player%`, `%health%`, `%hunger%`, `%online%`, `%ping%`, `%world%`, `%location_x/y/z%`, etc.) plus PlaceholderAPI support.
- Hex / RGB color support (`#RRGGBB`) in addition to standard `&` color codes.

## Requirements

- Minecraft / Spigot 1.16+ (built against Spigot API 1.16.4).
- Java 8 or newer.
- Optional: PlaceholderAPI for extended placeholders.

## Commands

- `/promessages` (alias: `/promessage`) — base command.
  - `info` — show current message configuration.
  - `reload` — reload `config.yml`.

## Permissions

- `promessages.command` — use the base command.
- `promessages.reload` — use `/promessages reload`.

(Permission nodes are configurable under `settings.permissions` in `config.yml`.)

## Installation

1. Drop `ProMessages.jar` into `plugins/`.
2. Start (or restart) the server to generate `config.yml`.
3. Edit `plugins/ProMessages/config.yml`, then `/promessages reload`.

## Configuration

`config.yml` controls:

- `settings.title` — welcome title / subtitle and fade timings.
- `settings.actionBar` — action bar message on join.
- `settings.firstJoin`, `settings.join`, `settings.leave` — broadcast messages (set to `""` to disable).
- `settings.player` — per-player chat lines, with `firstJoin` and `join` lists and a delay.
- `settings.sound.join` and `settings.sound.players` — per-event sounds.
- `messages` — command-related messages.
