This repository contains the whole (technical, commercial, communication, and so on) roadmap of my games not to forget things to do.

This roadmap applies to all of my three Steam games:
- [Extortion](https://store.steampowered.com/app/2299430/Extortion/)
- [Alchemistry](https://store.steampowered.com/app/1730540/Alchemistry/)
- [Manufactur'inc](https://store.steampowered.com/app/2146380/Manufactur_inc/)

But this can be forked and used for your games as well!

# Table of content
1. [Repositories setup](#repositories-setup)
2. [Steam page](#steam-page)
3. [Platform-agnostic technical features](#platform-agnostic-technical-features)
4. [Steam integration](#steam-integration)
5. [Public databases](#public-databases)
6. [Steam Deck compatibility](#steam-deck-compatibility)

# Repositories setup

| Id                         | Task                                            | Tags | Links | Needs | Extortion | Alchemistry | Manufactur'inc |
| -------------------------- | ----------------------------------------------- | ---- | ----- | ---- | ---- | ---- | ---- |
| <span id="1">#1</span>     | Create game client repository                   | game-client, technical | - | - | ✅ | ✅ | ✅ |
| <span id="2">#2</span>     | CI: tests on game client                        | game-client, automation, technical | - | [#1](#user-content-1) | ✅ | ✅ | ✅ |
| <span id="3">#3</span>     | CI: run sonarqube on game client code           | game-client, automation, technical | - | [#1](#user-content-1) | ✅ | ✅ | ✅ |
| <span id="4">#4</span>     | CI: sonarqube quality gate on game client code  | game-client, automation, technical | - | [#1](#user-content-1), [#3](#user-content-3) | ✅ | ✅ | ✅ |
| <span id="5">#5</span>     | CI: build windows x64 version                   | game-client, automation, technical | - | [#1](#user-content-1) | ✅ | ✅ | ✅ |
| <span id="6">#6</span>     | CI: build linux x64 version                     | game-client, automation, technical | - | [#1](#user-content-1) | ✅ | ✅ | ✅ |
| <span id="7">#7</span>     | CI: build macos x64 version                     | game-client, automation, technical | - | [#1](#user-content-1) | ✅ | ✅ | ✅ |
| <span id="8">#8</span>     | CI: build macos arm64 version                   | game-client, automation, technical | - | [#1](#user-content-1) | ❌ | ❌ | ❌ |
| <span id="9">#9</span>     | CI: publish to steam (dev)                      | game-client, automation, technical, steam | - | [#1](#user-content-1), [#5](#user-content-5) | ✅ | ✅ | ✅ |
| <span id="10">#10</span>   | CI: publish to steam (demo)                     | game-client, automation, technical, steam | - | [#1](#user-content-1), [#5](#user-content-5) | ✅ | ✅ | ❌ |
| <span id="11">#11</span>   | CI: publish to itch.io (prod)                   | game-client, automation, technical, itch | - | [#1](#user-content-1), [#5](#user-content-5) | ❌ | ❌ | ❌ |
| <span id="12">#12</span>   | CI: publish to itch.io (demo)                   | game-client, automation, technical, itch | - | [#1](#user-content-1), [#5](#user-content-5) | ✅ | ✅ | ❌ |
| <span id="21">#21</span>   | Create game server repostiory                   | game-server, technical | - | - | - | - | ✅ |
| <span id="22">#22</span>   | CI: tests on game server                        | game-server, automation, technical | - | [#21](#user-content-21) | - | - | ✅ |
| <span id="23">#23</span>   | CI: run sonarqube on game client code           | game-client, automation, technical | - | [#21](#user-content-21) | - | - | ✅ |
| <span id="24">#24</span>   | CI: sonarqube quality gate on game server code  | game-client, automation, technical | - | [#21](#user-content-21), [#23](#user-content-23) | - | - | ✅ |
| <span id="31">#31</span>   | Create game i18n public repostiory              | localization | - | - | ✅ | ✅ | ✅ |
| <span id="32">#32</span>   | Setup Contributor License Agreements            | localization, legal | - | [#31](#user-content-31) | ✅ | ✅ | ❌ |
| <span id="33">#33</span>   | Add i18n repo as a game repo submodule          | game-client, localization | - |  [#1](#user-content-1), [#31](#user-content-31) | ✅ | ❌ | ✅ |

[Back to the top](#table-of-content)

# Steam page

[Back to the top](#table-of-content)

# Platform-agnostic technical features

| Id                         | Task                                            | Tags | Links | Needs | Extortion | Alchemistry | Manufactur'inc |
| -------------------------- | ----------------------------------------------- | ---- | ----- | ---- | ---- | ---- | ---- |
| <span id="201">#201</span> | Setup a translation system                      | game-client, localization, technical | - | - | ✅ | ✅ | ✅ |
| <span id="202">#202</span> | Setup end-to-end tests                          | game-client, automation, technical | - | - | ✅ | ✅ | ⚠️ |
| <span id="203">#203</span> | Credits page                                    | game-client, legal, technical | - | - | ✅ | ✅ | ✅ |
| <span id="204">#204</span> | Settings page                                   | game-client, accessibility, technical | - | - | ✅ | ✅ | ❌ |
| <span id="205">#205</span> | Settings page - Keyboard remapping              | game-client, accessibility, technical | [#204](#user-content-204) | - | - | - | ❌ |
| <span id="206">#206</span> | Settings page - Change language                 | game-client, accessibility, technical | [#204](#user-content-204), [#201](#user-content-201) | - | - | - | ❌ |
| <span id="206">#207</span> | Tutorial                                        | game-client, accessibility, technical | - | - | ✅ | ⚠️ | ❌ |

# Steam integration

| Id                         | Task                                            | Tags | Links | Needs | Extortion | Alchemistry | Manufactur'inc |
| -------------------------- | ----------------------------------------------- | ---- | ----- | ---- | ---- | ---- | ---- |
| <span id="301">#301</span> | Integrate steam dll/so files                    | game-client, technical, steam | - | - | ✅ | ✅ | ✅ |
| <span id="302">#302</span> | Unlock at least 1 achievement                   | game-client, technical, steam | - | [#301](#user-content-301) | ✅ | ✅ | ✅ |
| <span id="303">#303</span> | Save data to steam cloud                        | game-client, technical, steam | - | [#301](#user-content-301) | ✅ | ✅ | ❌ |
| <span id="304">#304</span> | Setup steam leaderboards                        | game-client, technical, steam | - | [#301](#user-content-301) | ❌ | ✅ | ❌ |
| <span id="305">#305</span> | Setup steam authentication                      | game-client, technical, steam | - | [#301](#user-content-301) | - | - | ✅ |
| <span id="306">#306</span> | Ensure steam overlay works                      | game-client, technical, steam | - | [#301](#user-content-301) | ✅ | ✅ | ❌ |
| <span id="307">#307</span> | Get language from Steam                         | game-client, technical, steam | - | [#301](#user-content-301) | ✅ | ✅ | ❌ |
| <span id="308">#308</span> | Setup steam enhanced rich presence              | game-client, technical, steam | [Steam official documentation](https://partner.steamgames.com/doc/features/enhancedrichpresence) | [#301](#user-content-301) | ❌ | ✅ | ❌ |

[Back to the top](#table-of-content)

# Public databases

| Id                         | Task                                            | Tags | Links | Needs | Extortion | Alchemistry | Manufactur'inc |
| -------------------------- | ----------------------------------------------- | ---- | ----- | ---- | ---- | ---- | ---- |
| <span id="401">#401</span> | Create game page on IGDB                        | community, visibility | [Dysnomia's Blog](https://blog.dysnomia.studio/posts/add-your-game-to-twitch/) | - | ✅ | ✅ | ✅ |
| <span id="402">#402</span> | Claim game page on Twitch                       | community, visibility | [Dysnomia's Blog](https://blog.dysnomia.studio/posts/add-your-game-to-twitch/) | [#401](#user-content-401) | ✅ | ✅ | ✅ |
| <span id="403">#403</span> | Create youtube category                         | community, visibility | - | ? | ✅ | ✅ | ✅ |
| <span id="404">#404</span> | Create IndieDB page                             | community, visibility | - | - | ❌ | ❌ | ❌ |
| <span id="405">#405</span> | Dump tokens to SteamDB to ensure full data there | community, visibility | [SteamDB Official page about token dumper](https://steamdb.info/tokendumper/) | - | ✅ | ✅ | ✅ |

[Back to the top](#table-of-content)

# Steam Deck compatibility

| Id                         | Task                                            | Tags | Links | Needs | Extortion | Alchemistry | Manufactur'inc |
| -------------------------- | ----------------------------------------------- | ---- | ----- | ---- | ---- | ---- | ---- |
| <span id="501">#501</span> | Ensure you can navigate UI with gamepad         | steam-deck, accessibility, technical | - | - | ❌ | ✅ | ❌ |
| <span id="502">#502</span> | Ensure virtual keyboard show automatically when needed | steam-deck, accessibility, technical | - | - | ❌ | - | ❌ |
| <span id="503">#503</span> | Ensure resolution/font-size is okay on Steam deck | steam-deck, accessibility, technical | - | - | ✅ | ✅ | ✅ |
| <span id="504">#504</span> | Ensure steam input configuration is correct     | steam-deck, accessibility, technical | - | - | ❌ | ✅ | ❌ |
| <span id="505">#505</span> | Ensure performances on steam deck are correct   | steam-deck, accessibility, technical | - | - | ✅ | ✅ | ✅ |
| <span id="506">#506</span> | Ensure display settings are local and not clouded | steam-deck, accessibility, technical | - | - | ❌ | ✅ | ✅ |
| <span id="507">#507</span> | Ensure steam cloud work | steam-deck, accessibility, technical | - | [#303](#user-content-303) | ✅ | ✅ | ❌ |

---

# To do

Things to detail here later:
- Twitch extension
- Discord app and/or bot
- Discord rich presence
- Wiki/Guides
- Next Fest and other festivals
- Analyze other games for:
	- ideas (e.g. reviews)
	- languages
	- tags
- Visibility of steam page:
	- mutliple languages
	- follow/wishlist button GIF
	- tags
- Trailer (and where/when showing it)
- Demo (+ Big banner) 
- Playtests
- Audio (effects and music)
- Touchscreen support
- Social networks links
- Images lossless compression
- Steam community forum setup
- Devblog
- Reporting (grafana & co)
- Accessibiltiy checkup
- Daily deals
- Community-organized events
- Steam release: not round date (e.g. 14:58) so before the other ones in "popular upcoming" - Link: https://gdcvault.com/play/1034567/Independent-Games-Summit-The-Steam
- Press kit
- Steam page translation
- Release announcements (1 week before, 3 days before, 1 day before, day, 3 days, 1 week after a few hours before the end of the sale)
- Form to get feedback on demo/playtest (on graphics, gameplay, ux, fun, ..., not too long)
- Bundle with other games (from the dev or other devs)
- Streamers/news outlets spreadsheet (list contacts, and attempts (max 3))
