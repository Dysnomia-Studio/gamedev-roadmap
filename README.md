
This repository contains the whole (technical, commercial, communication, and so on) roadmap of my games not to forget things to do.

This roadmap applies to all of my three Steam games:
- [Extortion](https://store.steampowered.com/app/1299430/Extortion/)
- [Alchemistry](https://store.steampowered.com/app/1730540/Alchemistry/)
- [Manufactur'inc](https://store.steampowered.com/app/2146380/Manufactur_inc/)

But this can be forked and used for your games as well!

# Table of content
1. [Pre-development](#pre-development)
2. [Repositories setup](#repositories-setup)
3. [Steam page](#steam-page)
4. [Platform-agnostic technical features](#platform-agnostic-technical-features)
5. [Steam integration](#steam-integration)
6. [Public databases](#public-databases)
7. [Steam Deck compatibility](#steam-deck-compatibility)

# Pre-development
 | Id                         | Task                                            | Tags | Links | Needs | Extortion | Alchemistry | Manufactur'inc |
| -------------------------- | ----------------------------------------------- | ---- | ----- | ---- | ---- | ---- | ---- |
| <span id="1">#1</span>     | Write GDD                   |  | - | - | - | - | ✅ |

# Repositories setup

| Id                         | Task                                            | Tags | Links | Needs | Extortion | Alchemistry | Manufactur'inc |
| -------------------------- | ----------------------------------------------- | ---- | ----- | ---- | ---- | ---- | ---- |
| <span id="101">#101</span> | Create game client repository                   | game-client, technical | - | - | ✅ | ✅ | ✅ |
| <span id="102">#102</span> | CI: tests on game client                        | game-client, automation, technical | - | [#101](#user-content-101) | ✅ | ✅ | ✅ |
| <span id="103">#103</span> | CI: run sonarqube on game client code           | game-client, automation, technical | - | [#101](#user-content-101) | ✅ | ✅ | ✅ |
| <span id="104">#104</span> | CI: sonarqube quality gate on game client code  | game-client, automation, technical | - | [#101](#user-content-101), [#103](#user-content-103) | ✅ | ✅ | ✅ |
| <span id="105">#105</span> | CI: build windows x64 version                   | game-client, automation, technical | - | [#101](#user-content-101) | ✅ | ✅ | ✅ |
| <span id="106">#106</span> | CI: build linux x64 version                     | game-client, automation, technical | - | [#101](#user-content-101) | ✅ | ✅ | ✅ |
| <span id="107">#107</span> | CI: build macos x64 version (Deprecated)        | game-client, automation, technical | - | [#101](#user-content-101) | ✅ | ✅ | - |
| <span id="108">#108</span> | CI: build macos arm64 version                   | game-client, automation, technical | - | [#101](#user-content-101) | ❌ | ❌ | ✅ |
| <span id="109">#109</span> | CI: publish to steam (dev)                      | game-client, automation, technical, steam | - | [#101](#user-content-101), [#105](#user-content-105), [#221](#user-content-221) | ✅ | ✅ | ✅ |
| <span id="110">#110</span> | CI: publish to steam (demo)                     | game-client, automation, technical, steam | - | [#101](#user-content-101), [#105](#user-content-105), [#223](#user-content-223) | ✅ | ✅ | ❌ |
| <span id="111">#111</span> | CI: publish to itch.io (prod)                   | game-client, automation, technical, itch | - | [#101](#user-content-101), [#105](#user-content-105) | ❌ | ❌ | ❌ |
| <span id="112">#112</span> | CI: publish to itch.io (demo)                   | game-client, automation, technical, itch | - | [#101](#user-content-101), [#105](#user-content-105) | ✅ | ✅ | ❌ |
| <span id="121">#121</span> | Create game server repostiory                   | game-server, technical | - | - | - | - | ✅ |
| <span id="122">#122</span> | CI: tests on game server                        | game-server, automation, technical | - | [#121](#user-content-121) | - | - | ✅ |
| <span id="123">#123</span> | CI: run sonarqube on game client code           | game-client, automation, technical | - | [#121](#user-content-121) | - | - | ✅ |
| <span id="124">#124</span> | CI: sonarqube quality gate on game server code  | game-client, automation, technical | - | [#121](#user-content-121), [#123](#user-content-123) | - | - | ✅ |
| <span id="131">#131</span> | Create game i18n public repostiory              | localization | - | - | ✅ | ✅ | ✅ |
| <span id="132">#132</span> | Setup Contributor License Agreements            | localization, legal | - | [#131](#user-content-131) | ✅ | ✅ | ❌ |
| <span id="133">#133</span> | Add i18n repo as a game repo submodule          | game-client, localization | - |  [#101](#user-content-101), [#131](#user-content-131) | ✅ | ❌ | ✅ |

[Back to the top](#table-of-content)

# Steam page

| Id                         | Task                                            | Tags | Links | Needs | Extortion | Alchemistry | Manufactur'inc |
| -------------------------- | ----------------------------------------------- | ---- | ----- | ---- | ---- | ---- | ---- |
| <span id="201">#201</span> | Create Steamworks account (incl. administrative/tax setup) | administrative | - | - | ✅ | ✅ | ✅ |
| <span id="202">#202</span> | Pay Steam Fee to get our own Steam app | administrative | - | [#201](#user-content-201) | ✅ | ✅ | ✅ |
| <span id="203">#203</span> | [Basic Info] Fill game name, app type | administrative | - | [#202](#user-content-202) | ✅ | ✅ | ✅ |
| <span id="204">#204</span> | [Basic Info] Fill developer and publisher name | administrative | - | [#202](#user-content-202) | ✅ | ✅ | ✅ |
| <span id="204">#205</span> | [Basic Info] Fill franchise name | administrative | - | [#202](#user-content-202) | ✅ | ✅ | ✅ |
| <span id="206">#206</span> | Create developer/publisher/franchise homepage | administrative, seo | [Steam Official Documentation](https://partner.steamgames.com/doc/store/creator_homepage) | [#204](#user-content-204) | ✅ | ✅ | ✅ |
| <span id="207">#207</span> | [Basic Info] Fill external links (website, forum, stats, online manual, Metacritic) and social media links (Discord, Youtube, Facebook, Twitter, Twitch) | administrative, social-medias | - | [#202](#user-content-202) | ✅ | ✅ | ✅ |
| <span id="208">#208</span> | [Basic Info] Fill search keywords (add a lot of them!) | administrative, seo | - | [#202](#user-content-202) | ✅ | ✅ | ✅ |
| <span id="209">#209</span> | [Basic Info] Fill supported platforms and requirements | administrative, technical | - | [#202](#user-content-202), [#105](#user-content-105), [#106](#user-content-106), [#108](#user-content-108)  | ✅ | ✅ | ✅ |
| <span id="210">#210</span> | [Basic Info] Fill supported languages | administrative, seo | - | [#202](#user-content-202) | ✅ | ✅ | ✅ |
| <span id="211">#211</span> | [Basic Info] Fill "players" (single/multi/coop), and supported features (achievements, cloud, stats, ...) | administrative | - | [#202](#user-content-202) | ✅ | ✅ | ✅ |
| <span id="212">#212</span> | [Basic Info] Fill genre and tags | administrative, seo | - | [#202](#user-content-202) | ✅ | ✅ | ✅ |
| <span id="213">#213</span> | [Basic Info] Fill controller support | administrative, game-client, seo | - | [#202](#user-content-202) | ❌ | ❌ | ✅ |
| <span id="214">#214</span> | [Basic Info] Fill 3rd party DRM/Accounts, legal lines | administrative, legal | - | [#202](#user-content-202) | - | - | - |
| <span id="215">#215</span> | [Basic Info] Fill support contact info | administrative, legal | - | [#202](#user-content-202) | ✅ | ✅ | ✅ |
| <span id="216">#216</span> | [Description] Fill short description, long description, reviews, awards | administrative, seo | - | [#202](#user-content-202) | ✅ | ✅ | ✅ |
| <span id="217">#217</span> | [Rewards] Fill rating if you have some | administrative, legal | - | [#202](#user-content-202) | - | - | - |
| <span id="218">#218</span> | [Early Access] Fill early access informations if relevant | administrative, seo | - | [#202](#user-content-202) | - | - | ✅ |
| <span id="219">#219</span> | [Graphical Assets] Add all assets, including optional ones | administrative, seo | - | [#202](#user-content-202), Logos | ⚠️ | ⚠️ | ⚠️ |
| <span id="220">#220</span> | [Trailer] Add trailer | administrative, seo | - | [#202](#user-content-202), Trailer | ✅ | ✅ | ❌ |
| <span id="221">#221</span> | Translate steam page to other languages | administrative, seo | - | [#202](#user-content-202) | ✅ | ✅ | ⚠️ |
| <span id="222">#222</span> | Setup steam depots, packages and launch options | technical, game-client | - | [#202](#user-content-202) | ✅ | ✅ | ✅ |
| <span id="223">#223</span> | Setup demo the same way as app | technical, game-client | - | [#202](#user-content-202) | ✅ | ✅ | ✅ |
| <span id="224">#224</span> | Setup steam demo depots, packages and launch options | technical, game-client | - | [#202](#user-content-202) | ✅ | ✅ | ✅ |
| <span id="225">#225</span> | Fill pricing | administrative | - | [#202](#user-content-202) | ✅ | ✅ | ❌ |
| <span id="226">#226</span> | Fill "More from (Franchise/Developer/Publisher)" | administrative, seo | - | [#202](#user-content-202) | ✅ | ✅ | ✅ |
| <span id="227">#227</span> | [Basic Info] Fill "Accessibility" | acessibility, seo | [Official announcemet](https://steamcommunity.com/groups/steamworks/announcements/detail/536595840131663919) | [#202](#user-content-202) | ✅ | ✅ | ✅ |


[Back to the top](#table-of-content)

# Platform-agnostic technical features

| Id                         | Task                                            | Tags | Links | Needs | Extortion | Alchemistry | Manufactur'inc |
| -------------------------- | ----------------------------------------------- | ---- | ----- | ---- | ---- | ---- | ---- |
| <span id="301">#301</span> | Setup a translation system                      | game-client, localization, technical | - | - | ✅ | ✅ | ✅ |
| <span id="302">#302</span> | Setup end-to-end tests                          | game-client, automation, technical | - | - | ✅ | ✅ | ✅ |
| <span id="303">#303</span> | Credits page                                    | game-client, legal, technical | - | - | ✅ | ✅ | ✅ |
| <span id="304">#304</span> | Settings page                                   | game-client, accessibility, technical | - | - | ✅ | ✅ | ❌ |
| <span id="305">#305</span> | Settings page - Keyboard remapping              | game-client, accessibility, technical | [#304](#user-content-304) | - | - | - | ❌ |
| <span id="306">#306</span> | Settings page - Change language                 | game-client, accessibility, technical | [#304](#user-content-304), [#301](#user-content-301) | - | - | - | ❌ |
| <span id="307">#307</span> | Tutorial                                        | game-client, accessibility, technical | - | - | ✅ | ⚠️ | ❌ |

# Steam integration

| Id                         | Task                                            | Tags | Links | Needs | Extortion | Alchemistry | Manufactur'inc |
| -------------------------- | ----------------------------------------------- | ---- | ----- | ---- | ---- | ---- | ---- |
| <span id="401">#401</span> | Integrate steam dll/so files                    | game-client, technical, steam | - | - | ✅ | ✅ | ✅ |
| <span id="402">#402</span> | Unlock at least 1 achievement                   | game-client, technical, steam | - | [#401](#user-content-401) | ✅ | ✅ | ✅ |
| <span id="403">#403</span> | Save data to steam cloud                        | game-client, technical, steam | - | [#401](#user-content-401) | ✅ | ✅ | ❌ |
| <span id="404">#404</span> | Setup steam leaderboards                        | game-client, technical, steam | - | [#401](#user-content-401) | ❌ | ✅ | ❌ |
| <span id="405">#405</span> | Setup steam authentication                      | game-client, technical, steam | - | [#401](#user-content-401) | - | - | ✅ |
| <span id="406">#406</span> | Ensure steam overlay works                      | game-client, technical, steam | - | [#401](#user-content-401) | ✅ | ✅ | ❌ |
| <span id="407">#407</span> | Get language from Steam                         | game-client, technical, steam | - | [#401](#user-content-401) | ✅ | ✅ | ❌ |
| <span id="408">#408</span> | Setup steam enhanced rich presence              | game-client, technical, steam | [Steam official documentation](https://partner.steamgames.com/doc/features/enhancedrichpresence) | [#401](#user-content-401) | ❌ | ✅ | ❌ |

[Back to the top](#table-of-content)

# Public databases

| Id                         | Task                                            | Tags | Links | Needs | Extortion | Alchemistry | Manufactur'inc |
| -------------------------- | ----------------------------------------------- | ---- | ----- | ---- | ---- | ---- | ---- |
| <span id="501">#501</span> | Create game page on IGDB                        | community, visibility | [Dysnomia's Blog](https://blog.dysnomia.studio/posts/add-your-game-to-twitch/) | - | ✅ | ✅ | ✅ |
| <span id="502">#502</span> | Claim game page on Twitch                       | community, visibility | [Dysnomia's Blog](https://blog.dysnomia.studio/posts/add-your-game-to-twitch/) | [#501](#user-content-501) | ✅ | ✅ | ✅ |
| <span id="503">#503</span> | Create youtube category                         | community, visibility | - | ? | ✅ | ✅ | ✅ |
| <span id="504">#504</span> | Create IndieDB page                             | community, visibility | - | - | ❌ | ❌ | ❌ |
| <span id="505">#505</span> | Dump tokens to SteamDB to ensure full data there | community, visibility | [SteamDB Official page about token dumper](https://steamdb.info/tokendumper/) | - | ✅ | ✅ | ✅ |

[Back to the top](#table-of-content)

# Steam Deck compatibility

| Id                         | Task                                            | Tags | Links | Needs | Extortion | Alchemistry | Manufactur'inc |
| -------------------------- | ----------------------------------------------- | ---- | ----- | ---- | ---- | ---- | ---- |
| <span id="601">#601</span> | Ensure you can navigate UI with gamepad         | steam-deck, accessibility, technical | - | - | ❌ | ✅ | ❌ |
| <span id="602">#602</span> | Ensure virtual keyboard show automatically when needed | steam-deck, accessibility, technical | - | - | ❌ | - | ❌ |
| <span id="603">#603</span> | Ensure resolution/font-size is okay on Steam deck | steam-deck, accessibility, technical | - | - | ✅ | ✅ | ✅ |
| <span id="604">#604</span> | Ensure steam input configuration is correct     | steam-deck, accessibility, technical | - | - | ❌ | ✅ | ❌ |
| <span id="605">#605</span> | Ensure performances on steam deck are correct   | steam-deck, accessibility, technical | - | - | ✅ | ✅ | ✅ |
| <span id="606">#606</span> | Ensure display settings are local and not clouded | steam-deck, accessibility, technical | - | - | ❌ | ✅ | ✅ |
| <span id="607">#607</span> | Ensure steam cloud work | steam-deck, accessibility, technical | - | [#403](#user-content-403) | ✅ | ✅ | ❌ |
| <span id="608">#608</span> | [Basic Info] Fill Steam Deck Compatibility Info (Steamworks back-end) | administrative | - | [#202](#user-content-202) | ❌ | ✅ | ❌ |

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
- Trailer (and where/when showing it)
- Demo (+ Big banner) 
- Playtests
- Audio (effects and music)
- Touchscreen support
- Images lossless compression
- Steam community forum setup
	- Social network posts
	- Translation post
 	- Subscribe to all the forums  
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
- Create Discord server
- Make an influencer list
- Make a press list
- Analyse other games for: tags, price, language, things to have/not have
- Feedback form
- Social medias in game
  Wishlist button in Demo
