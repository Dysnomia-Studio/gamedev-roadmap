This repository contains the whole (technical, commercial, communication, ...) roadmap of my games in order to not forget things to do.

This roadmap applies to all of my three Steam games:
- [Extortion](https://store.steampowered.com/app/1299430/Extortion/)
- [Alchemistry](https://store.steampowered.com/app/1730540/Alchemistry/)
- [Manufactur'inc](https://store.steampowered.com/app/2146380/Manufactur_inc/)

But this can be forked and used for your own games as well!


TODO: table of content

# Repositories setup

| Id                         | Task                                            | Tags | Links | Extortion | Alchemistry | Manufactur'inc | Needs |
| -------------------------- | ----------------------------------------------- | ---- | ----- | ---- | ---- | ---- | ---- |
| <span id="1">#1</span>     | Create game client repository                   | game-client, technical | - | ✅ | ✅ | ✅ | - |
| <span id="2">#2</span>     | CI: tests on game client                        | game-client, automation, technical | - | ✅ | ✅ | ✅ | [#1](#user-content-1) |
| <span id="3">#3</span>     | CI: run sonarqube on game client code           | game-client, automation, technical | - | ✅ | ✅ | ✅ | [#1](#user-content-1) |
| <span id="4">#4</span>     | CI: sonarqube quality gate on game client code  | game-client, automation, technical | - | ✅ | ✅ | ✅ | [#1](#user-content-1), [#3](#user-content-3) |
| <span id="5">#5</span>     | CI: build windows x64 version                   | game-client, automation, technical | - | ✅ | ✅ | ✅ | [#1](#user-content-1) |
| <span id="6">#6</span>     | CI: build linux x64 version                     | game-client, automation, technical | - | ✅ | ✅ | ✅ | [#1](#user-content-1) |
| <span id="7">#7</span>     | CI: build macos x64 version                     | game-client, automation, technical | - | ✅ | ✅ | ✅ | [#1](#user-content-1) |
| <span id="8">#8</span>     | CI: build macos arm64 version                   | game-client, automation, technical | - | ❌ | ❌ | ❌ | [#1](#user-content-1) |
| <span id="9">#9</span>     | CI: publish to steam (dev)                      | game-client, automation, technical, steam | - | ✅ | ✅ | ✅ | [#1](#user-content-1), [#5](#user-content-5) |
| <span id="11">#11</span>   | Create game server repostiory                   | game-server, technical | - | - | - | ✅ | - |
| <span id="12">#12</span>   | CI: tests on game server                        | game-server, automation, technical | - | - | - | ✅ | [#11](#user-content-11) |
| <span id="13">#13</span>   | CI: run sonarqube on game client code           | game-client, automation, technical | - | - | - | ✅ | [#11](#user-content-11) |
| <span id="14">#14</span>   | CI: sonarqube quality gate on game server code  | game-client, automation, technical | - | - | - | ✅ | [#11](#user-content-11), [#13](#user-content-13) |
| <span id="21">#21</span>   | Create game i18n public repostiory              | localization | - | ✅ | ✅ | ✅ | - |
| <span id="22">#22</span>   | Setup Contributor License Agreements            | localization, legal | - | ✅ | ✅ | ❌ | [#21](#user-content-21) |
| <span id="23">#23</span>   | Add i18n repo as a game repo submodule          | game-client, localization | - | ✅ | ❌ | ✅ |  [#1](#user-content-1), [#21](#user-content-21) |

# Steam page

# Steam integration

| Id                         | Task                                            | Tags | Links | Extortion | Alchemistry | Manufactur'inc | Needs |
| -------------------------- | ----------------------------------------------- | ---- | ----- | ---- | ---- | ---- | ---- |
| <span id="201">#201</span> | Integrate steam dll/so files                    | game-client, technical, steam | - | ✅ | ✅ | ✅ | - |
| <span id="202">#202</span> | Unlock at least 1 achievement                   | game-client, technical, steam | - | ✅ | ✅ | ✅ | [#201](#user-content-201) |
| <span id="203">#203</span> | Save data to steam cloud                        | game-client, technical, steam | - | ✅ | ✅ | ❌ | [#201](#user-content-201) |
| <span id="204">#204</span> | Setup steam leaderboards                        | game-client, technical, steam | - | ❌ | ✅ | ❌ | [#201](#user-content-201) |
| <span id="205">#205</span> | Setup steam authentication                      | game-client, technical, steam | - | - | - | ✅ | [#201](#user-content-201) |
| <span id="206">#206</span> | Ensure steam overlay works                      | game-client, technical, steam | - | ✅ | ✅ | ❌ | [#201](#user-content-201) |
| <span id="207">#207</span> | Get language from Steam                         | game-client, technical, steam | - | ✅ | ✅ | ❌ | [#201](#user-content-201) |
