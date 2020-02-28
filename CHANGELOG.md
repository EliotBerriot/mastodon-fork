# Changelog

This changelog will only include differences from upstream Mastodon. [You can find the upstream
changelog here.](https://github.com/tootsuite/mastodon/blob/master/CHANGELOG.md)

Please note that this project doesn't follow semantic versioning— for details please have a look at
our [README file].
## [2.9.4] - 2020-02-27
### Security

- Fix leak of arbitrary statuses through unfavourite action in REST API ([Gargron](https://github.com/tootsuite/mastodon/pull/13161))

## [2.9.3] - 2019-08-10
### Added

- Add GIF and WebP support for custom emojis ([Gargron](https://github.com/tootsuite/mastodon/pull/11519))
- Add logout link to dropdown menu in web UI ([koyuawsmbrtn](https://github.com/tootsuite/mastodon/pull/11353))
- Add indication that text search is unavailable in web UI ([ThibG](https://github.com/tootsuite/mastodon/pull/11112), [ThibG](https://github.com/tootsuite/mastodon/pull/11202))
- Add `suffix` to `Mastodon::Version` to help forks ([clarfon](https://github.com/tootsuite/mastodon/pull/11407))
- Add on-hover animation to animated custom emoji in web UI ([ThibG](https://github.com/tootsuite/mastodon/pull/11348), [ThibG](https://github.com/tootsuite/mastodon/pull/11404), [ThibG](https://github.com/tootsuite/mastodon/pull/11522))
- Add custom emoji support in profile metadata labels ([ThibG](https://github.com/tootsuite/mastodon/pull/11350))

### Changed

- Change default interface of web and streaming from 0.0.0.0 to 127.0.0.1 ([Gargron](https://github.com/tootsuite/mastodon/pull/11302), [zunda](https://github.com/tootsuite/mastodon/pull/11378), [Gargron](https://github.com/tootsuite/mastodon/pull/11351), [zunda](https://github.com/tootsuite/mastodon/pull/11326))
- Change the retry limit of web push notifications ([highemerly](https://github.com/tootsuite/mastodon/pull/11292))
- Change ActivityPub deliveries to not retry HTTP 501 errors ([Gargron](https://github.com/tootsuite/mastodon/pull/11233))
- Change language detection to include hashtags as words ([Gargron](https://github.com/tootsuite/mastodon/pull/11341))
- Change terms and privacy policy pages to always be accessible ([Gargron](https://github.com/tootsuite/mastodon/pull/11334))
- Change robots tag to include `noarchive` when user opts out of indexing ([Kjwon15](https://github.com/tootsuite/mastodon/pull/11421))

### Fixed

- Fix account domain block not clearing out notifications ([Gargron](https://github.com/tootsuite/mastodon/pull/11393))
- Fix incorrect locale sometimes being detected for browser ([Gargron](https://github.com/tootsuite/mastodon/pull/8657))
- Fix crash when saving invalid domain name ([Gargron](https://github.com/tootsuite/mastodon/pull/11528))
- Fix pinned statuses REST API returning pagination headers ([Gargron](https://github.com/tootsuite/mastodon/pull/11526))
- Fix "cancel follow request" button having unreadable text in web UI ([Gargron](https://github.com/tootsuite/mastodon/pull/11521))
- Fix image uploads being blank when canvas read access is blocked ([ThibG](https://github.com/tootsuite/mastodon/pull/11499))
- Fix avatars not being animated on hover when not logged in ([ThibG](https://github.com/tootsuite/mastodon/pull/11349))
- Fix overzealous sanitization of HTML lists ([ThibG](https://github.com/tootsuite/mastodon/pull/11354))
- Fix block crashing when a follow request exists ([ThibG](https://github.com/tootsuite/mastodon/pull/11288))
- Fix backup service crashing when an attachment is missing ([ThibG](https://github.com/tootsuite/mastodon/pull/11241))
- Fix account moderation action always sending e-mail notification ([Gargron](https://github.com/tootsuite/mastodon/pull/11242))
- Fix swiping columns on mobile sometimes failing in web UI ([ThibG](https://github.com/tootsuite/mastodon/pull/11200))
- Fix wrong actor URI being serialized into poll updates ([ThibG](https://github.com/tootsuite/mastodon/pull/11194))
- Fix statsd UDP sockets not being cleaned up in Sidekiq ([Gargron](https://github.com/tootsuite/mastodon/pull/11230))
- Fix expiration date of filters being set to "never" when editing them ([ThibG](https://github.com/tootsuite/mastodon/pull/11204))
- Fix support for MP4 files that are actually M4V files ([Gargron](https://github.com/tootsuite/mastodon/pull/11210))
- Fix `alerts` not being typecast correctly in push subscription in REST API ([Gargron](https://github.com/tootsuite/mastodon/pull/11343))
- Fix some notices staying on unrelated pages ([ThibG](https://github.com/tootsuite/mastodon/pull/11364))
- Fix unboosting sometimes preventing a boost from reappearing on feed ([ThibG](https://github.com/tootsuite/mastodon/pull/11405), [Gargron](https://github.com/tootsuite/mastodon/pull/11450))
- Fix only one middle dot being recognized in hashtags ([Gargron](https://github.com/tootsuite/mastodon/pull/11345), [ThibG](https://github.com/tootsuite/mastodon/pull/11363))
- Fix unnecessary SQL query performed on unauthenticated requests ([Gargron](https://github.com/tootsuite/mastodon/pull/11179))
- Fix incorrect timestamp displayed on featured tags ([Kjwon15](https://github.com/tootsuite/mastodon/pull/11477))
- Fix privacy dropdown active state when dropdown is placed on top of it ([ThibG](https://github.com/tootsuite/mastodon/pull/11495))
- Fix filters not being applied to poll options ([ThibG](https://github.com/tootsuite/mastodon/pull/11174))
- Fix keyboard navigation on various dropdowns ([ThibG](https://github.com/tootsuite/mastodon/pull/11511), [ThibG](https://github.com/tootsuite/mastodon/pull/11492), [ThibG](https://github.com/tootsuite/mastodon/pull/11491))
- Fix keyboard navigation in modals ([ThibG](https://github.com/tootsuite/mastodon/pull/11493))
- Fix image conversation being non-deterministic due to timestamps ([Gargron](https://github.com/tootsuite/mastodon/pull/11408))
- Fix web UI performance ([ThibG](https://github.com/tootsuite/mastodon/pull/11211), [ThibG](https://github.com/tootsuite/mastodon/pull/11234))
- Fix scrolling to compose form when not necessary in web UI ([ThibG](https://github.com/tootsuite/mastodon/pull/11246), [ThibG](https://github.com/tootsuite/mastodon/pull/11182))
- Fix save button being enabled when list title is empty in web UI ([ThibG](https://github.com/tootsuite/mastodon/pull/11475))
- Fix poll expiration not being pre-filled on delete & redraft in web UI ([ThibG](https://github.com/tootsuite/mastodon/pull/11203))
- Fix content warning sometimes being set when not requested in web UI ([ThibG](https://github.com/tootsuite/mastodon/pull/11206))

### Security

- Fix invites not being disabled upon account suspension ([ThibG](https://github.com/tootsuite/mastodon/pull/11412))
- Fix blocked domains still being able to fill database with account records ([Gargron](https://github.com/tootsuite/mastodon/pull/11219))

## [v3.1.2] - 2020-02-27
### Added

- Add `--reset-password` option to `tootctl accounts modify` ([ThibG](https://github.com/tootsuite/mastodon/pull/13126))
- Add source-mapped stacktrace to error message in web UI ([ThibG](https://github.com/tootsuite/mastodon/pull/13082))

### Fixed

- Fix dismissing an announcement twice raising an obscure error ([ThibG](https://github.com/tootsuite/mastodon/pull/13124))
- Fix misleading error when attempting to re-send a pending follow request ([ThibG](https://github.com/tootsuite/mastodon/pull/13133))
- Fix backups failing when files are missing from media attachments ([ThibG](https://github.com/tootsuite/mastodon/pull/13146))
- Fix duplicate accounts being created when fetching an account for its key only ([ThibG](https://github.com/tootsuite/mastodon/pull/13147))
- Fix `/web` redirecting to `/web/web` in web UI ([ThibG](https://github.com/tootsuite/mastodon/pull/13128))
- Fix previously OStatus-based accounts not being detected as ActivityPub ([ThibG](https://github.com/tootsuite/mastodon/pull/13129))
- Fix account JSON/RSS not being cacheable due to wrong mime type comparison ([ThibG](https://github.com/tootsuite/mastodon/pull/13116))
- Fix old browsers crashing because of missing `finally` polyfill in web UI ([ThibG](https://github.com/tootsuite/mastodon/pull/13115))
- Fix account's bio not being shown if there are no proofs/fields in admin UI ([ThibG](https://github.com/tootsuite/mastodon/pull/13075))
- Fix sign-ups without checked user agreement being accepted through the web form ([ThibG](https://github.com/tootsuite/mastodon/pull/13088))
- Fix non-x64 architectures not being able to build Docker image because of hardcoded Node.js architecture ([SaraSmiseth](https://github.com/tootsuite/mastodon/pull/13081))
- Fix invite request input not being shown on sign-up error if left empty ([ThibG](https://github.com/tootsuite/mastodon/pull/13089))
- Fix some migration hints mentioning GitLab instead of Mastodon ([saper](https://github.com/tootsuite/mastodon/pull/13084))

### Security

- Fix leak of arbitrary statuses through unfavourite action in REST API ([Gargron](https://github.com/tootsuite/mastodon/pull/13161))

## [3.1.1] - 2020-02-10
### Fixed

- Fix yanked dependency preventing installation ([mayaeh](https://github.com/tootsuite/mastodon/pull/13059))

## [3.1.0] - 2020-02-09
### Added

- Add bookmarks ([ThibG](https://github.com/tootsuite/mastodon/pull/7107), [Gargron](https://github.com/tootsuite/mastodon/pull/12494), [Gomasy](https://github.com/tootsuite/mastodon/pull/12381))
- Add announcements ([Gargron](https://github.com/tootsuite/mastodon/pull/12662), [Gargron](https://github.com/tootsuite/mastodon/pull/12967), [Gargron](https://github.com/tootsuite/mastodon/pull/12970), [Gargron](https://github.com/tootsuite/mastodon/pull/12963), [Gargron](https://github.com/tootsuite/mastodon/pull/12950), [Gargron](https://github.com/tootsuite/mastodon/pull/12990), [Gargron](https://github.com/tootsuite/mastodon/pull/12949), [Gargron](https://github.com/tootsuite/mastodon/pull/12989), [Gargron](https://github.com/tootsuite/mastodon/pull/12964), [Gargron](https://github.com/tootsuite/mastodon/pull/12965), [ThibG](https://github.com/tootsuite/mastodon/pull/12958), [ThibG](https://github.com/tootsuite/mastodon/pull/12957), [Gargron](https://github.com/tootsuite/mastodon/pull/12955), [ThibG](https://github.com/tootsuite/mastodon/pull/12946), [ThibG](https://github.com/tootsuite/mastodon/pull/12954))
- Add number animations in web UI ([Gargron](https://github.com/tootsuite/mastodon/pull/12948), [Gargron](https://github.com/tootsuite/mastodon/pull/12971))
- Add `kab`, `is`, `kn`, `mr`, `ur` to available locales ([Gargron](https://github.com/tootsuite/mastodon/pull/12882), [BoFFire](https://github.com/tootsuite/mastodon/pull/12962), [Gargron](https://github.com/tootsuite/mastodon/pull/12379))
- Add profile filter category ([ThibG](https://github.com/tootsuite/mastodon/pull/12918))
- Add ability to add oneself to lists ([ThibG](https://github.com/tootsuite/mastodon/pull/12271))
- Add hint how to contribute translations to preferences page ([Sasha-Sorokin](https://github.com/tootsuite/mastodon/pull/12736))
- Add signatures to statuses in archive takeout ([noellabo](https://github.com/tootsuite/mastodon/pull/12649))
- Add support for `magnet:` and `xmpp` links ([ThibG](https://github.com/tootsuite/mastodon/pull/12905), [ThibG](https://github.com/tootsuite/mastodon/pull/12709))
- Add `follow_request` notification type ([ThibG](https://github.com/tootsuite/mastodon/pull/12198))
- Add ability to filter reports by account domain in admin UI ([ThibG](https://github.com/tootsuite/mastodon/pull/12154))
- Add link to search for users connected from the same IP address to admin UI ([ThibG](https://github.com/tootsuite/mastodon/pull/12157))
- Add link to reports targeting a specific domain in admin view ([ThibG](https://github.com/tootsuite/mastodon/pull/12513))
- Add support for EventSource streaming in web UI ([BenLubar](https://github.com/tootsuite/mastodon/pull/12887))
- Add hotkey for opening media attachments in web UI ([ThibG](https://github.com/tootsuite/mastodon/pull/12498), [Kjwon15](https://github.com/tootsuite/mastodon/pull/12546))
- Add relationship-based options to status dropdowns in web UI ([Gargron](https://github.com/tootsuite/mastodon/pull/12377), [ThibG](https://github.com/tootsuite/mastodon/pull/12535), [Gargron](https://github.com/tootsuite/mastodon/pull/12430))
- Add support for submitting media description with `ctrl`+`enter` in web UI ([ThibG](https://github.com/tootsuite/mastodon/pull/12272))
- Add download button to audio and video players in web UI ([NimaBoscarino](https://github.com/tootsuite/mastodon/pull/12179))
- Add setting for whether to crop images in timelines in web UI ([duxovni](https://github.com/tootsuite/mastodon/pull/12126))
- Add support for `Event` activities ([tcitworld](https://github.com/tootsuite/mastodon/pull/12637))
- Add basic support for `Group` actors ([noellabo](https://github.com/tootsuite/mastodon/pull/12071))
- Add `S3_OVERRIDE_PATH_STYLE` environment variable ([Gargron](https://github.com/tootsuite/mastodon/pull/12594))
- Add `S3_OPEN_TIMEOUT` environment variable ([tateisu](https://github.com/tootsuite/mastodon/pull/12459))
- Add `LDAP_MAIL` environment variable ([madmath03](https://github.com/tootsuite/mastodon/pull/12053))
- Add `LDAP_UID_CONVERSION_ENABLED` environment variable ([madmath03](https://github.com/tootsuite/mastodon/pull/12461))
- Add `--remote-only` option to `tootctl emoji purge` ([ThibG](https://github.com/tootsuite/mastodon/pull/12810))
- Add `tootctl media remove-orphans` ([Gargron](https://github.com/tootsuite/mastodon/pull/12568), [Gargron](https://github.com/tootsuite/mastodon/pull/12571))
- Add `tootctl media lookup` command ([irlcatgirl](https://github.com/tootsuite/mastodon/pull/12283))
- Add cache for OEmbed endpoints to avoid extra HTTP requests ([Gargron](https://github.com/tootsuite/mastodon/pull/12403))
- Add support for KaiOS arrow navigation to public pages ([nolanlawson](https://github.com/tootsuite/mastodon/pull/12251))
- Add `discoverable` to accounts in REST API ([trwnh](https://github.com/tootsuite/mastodon/pull/12508))
- Add admin setting to disable default follows ([ArisuOngaku](https://github.com/tootsuite/mastodon/pull/12566))
- Add support for LDAP and PAM in the OAuth password grant strategy ([ntl-purism](https://github.com/tootsuite/mastodon/pull/12390), [Gargron](https://github.com/tootsuite/mastodon/pull/12743))
- Allow support for `Accept`/`Reject` activities with a non-embedded object ([puckipedia](https://github.com/tootsuite/mastodon/pull/12199))
- Add "Show thread" button to public profiles ([Sasha-Sorokin](https://github.com/tootsuite/mastodon/pull/13000))

### Changed

- Change `last_status_at` to be a date, not datetime in REST API ([ThibG](https://github.com/tootsuite/mastodon/pull/12966))
- Change followers page to relationships page in admin UI ([Gargron](https://github.com/tootsuite/mastodon/pull/12927), [Gargron](https://github.com/tootsuite/mastodon/pull/12934))
- Change reported media attachments to always be hidden in admin UI ([Gargron](https://github.com/tootsuite/mastodon/pull/12879), [ThibG](https://github.com/tootsuite/mastodon/pull/12907))
- Change string from "Disable" to "Disable login" in admin UI ([nileshkumar](https://github.com/tootsuite/mastodon/pull/12201))
- Change report page structure in admin UI ([Sasha-Sorokin](https://github.com/tootsuite/mastodon/pull/12615))
- Change swipe sensitivity to be lower on small screens in web UI ([umonaca](https://github.com/tootsuite/mastodon/pull/12168))
- Change audio/video playback to stop playback when out of view in web UI ([Gargron](https://github.com/tootsuite/mastodon/pull/12486))
- Change media description label based on upload type in web UI ([ThibG](https://github.com/tootsuite/mastodon/pull/12270))
- Change large numbers to render without decimal units in web UI ([noellabo](https://github.com/tootsuite/mastodon/pull/12706))
- Change "Add a choice" button to be disabled rather than hidden when poll limit reached in web UI ([ThibG](https://github.com/tootsuite/mastodon/pull/12319), [hinaloe](https://github.com/tootsuite/mastodon/pull/12544))
- Change `tootctl statuses remove` to keep statuses favourited or bookmarked by local users ([ThibG](https://github.com/tootsuite/mastodon/pull/11267), [Gomasy](https://github.com/tootsuite/mastodon/pull/12818))
- Change domain block behavior to update user records (fast) before deleting data (slower) ([ThibG](https://github.com/tootsuite/mastodon/pull/12247))
- Change behaviour to strip audio metadata on uploads ([hugogameiro](https://github.com/tootsuite/mastodon/pull/12171))
- Change accepted length of remote media descriptions from 420 to 1,500 characters ([ThibG](https://github.com/tootsuite/mastodon/pull/12262))
- Change preferences pages structure ([Sasha-Sorokin](https://github.com/tootsuite/mastodon/pull/12497), [mayaeh](https://github.com/tootsuite/mastodon/pull/12517), [Sasha-Sorokin](https://github.com/tootsuite/mastodon/pull/12801), [Sasha-Sorokin](https://github.com/tootsuite/mastodon/pull/12797), [Sasha-Sorokin](https://github.com/tootsuite/mastodon/pull/12799), [Sasha-Sorokin](https://github.com/tootsuite/mastodon/pull/12793))
- Change format of titles in RSS ([devkral](https://github.com/tootsuite/mastodon/pull/8596))
- Change favourite icon animation from spring-based motion to CSS animation in web UI ([ThibG](https://github.com/tootsuite/mastodon/pull/12175))
- Change minimum required Node.js version to 10, and default to 12 ([Shleeble](https://github.com/tootsuite/mastodon/pull/12791), [mkody](https://github.com/tootsuite/mastodon/pull/12906), [Shleeble](https://github.com/tootsuite/mastodon/pull/12703))
- Change spam check to exempt server staff ([ThibG](https://github.com/tootsuite/mastodon/pull/12874))
- Change to fallback to to `Create` audience when `object` has no defined audience ([ThibG](https://github.com/tootsuite/mastodon/pull/12249))
- Change Twemoji library to 12.1.3 in web UI ([koyuawsmbrtn](https://github.com/tootsuite/mastodon/pull/12342))
- Change blocked users to be hidden from following/followers lists ([ThibG](https://github.com/tootsuite/mastodon/pull/12733))
- Change signature verification to ignore signatures with invalid host ([Gargron](https://github.com/tootsuite/mastodon/pull/13033))

### Removed

- Remove unused dependencies ([ykzts](https://github.com/tootsuite/mastodon/pull/12861), [mayaeh](https://github.com/tootsuite/mastodon/pull/12826), [ThibG](https://github.com/tootsuite/mastodon/pull/12822), [ykzts](https://github.com/tootsuite/mastodon/pull/12533))

### Fixed

- Fix some translatable strings being used wrongly ([Sasha-Sorokin](https://github.com/tootsuite/mastodon/pull/12569), [Sasha-Sorokin](https://github.com/tootsuite/mastodon/pull/12589), [Sasha-Sorokin](https://github.com/tootsuite/mastodon/pull/12502), [mayaeh](https://github.com/tootsuite/mastodon/pull/12231))
- Fix headline of public timeline page when set to local-only ([ykzts](https://github.com/tootsuite/mastodon/pull/12224))
- Fix space between tabs not being spread evenly in web UI ([Sasha-Sorokin](https://github.com/tootsuite/mastodon/pull/12944), [Sasha-Sorokin](https://github.com/tootsuite/mastodon/pull/12961), [Sasha-Sorokin](https://github.com/tootsuite/mastodon/pull/12446))
- Fix interactive delays in database migrations with no TTY ([Gargron](https://github.com/tootsuite/mastodon/pull/12969))
- Fix status overflowing in report dialog in web UI ([ThibG](https://github.com/tootsuite/mastodon/pull/12959))
- Fix unlocalized dropdown button title in web UI ([Sasha-Sorokin](https://github.com/tootsuite/mastodon/pull/12947))
- Fix media attachments without file being uploadable ([Gargron](https://github.com/tootsuite/mastodon/pull/12562))
- Fix unfollow confirmations in profile directory in web UI ([ThibG](https://github.com/tootsuite/mastodon/pull/12922))
- Fix duplicate `description` meta tag on accounts public pages ([ThibG](https://github.com/tootsuite/mastodon/pull/12923))
- Fix slow query of federated timeline ([notozeki](https://github.com/tootsuite/mastodon/pull/12886))
- Fix not all of account's active IPs showing up in admin UI ([Gargron](https://github.com/tootsuite/mastodon/pull/12909), [Gargron](https://github.com/tootsuite/mastodon/pull/12943))
- Fix search by IP not using alternative browser sessions in admin UI ([Gargron](https://github.com/tootsuite/mastodon/pull/12904))
- Fix “X new items” not showing up for slow mode on empty timelines in web UI ([ThibG](https://github.com/tootsuite/mastodon/pull/12875))
- Fix OEmbed endpoint being inaccessible in secure mode ([Gargron](https://github.com/tootsuite/mastodon/pull/12864))
- Fix proofs API being inaccessible in secure mode ([Gargron](https://github.com/tootsuite/mastodon/pull/12495))
- Fix Ruby 2.7 incompatibilities ([ThibG](https://github.com/tootsuite/mastodon/pull/12831), [ThibG](https://github.com/tootsuite/mastodon/pull/12824), [Shleeble](https://github.com/tootsuite/mastodon/pull/12759), [zunda](https://github.com/tootsuite/mastodon/pull/12769))
- Fix invalid poll votes being accepted in REST API ([ThibG](https://github.com/tootsuite/mastodon/pull/12601))
- Fix old migrations failing because of strong migrations update ([ThibG](https://github.com/tootsuite/mastodon/pull/12787), [ThibG](https://github.com/tootsuite/mastodon/pull/12692))
- Fix reuse of detailed status components in web UI ([ThibG](https://github.com/tootsuite/mastodon/pull/12792))
- Fix base64-encoded file uploads not being possible in REST API ([Gargron](https://github.com/tootsuite/mastodon/pull/12748), [Gargron](https://github.com/tootsuite/mastodon/pull/12857))
- Fix error due to missing authentication call in filters controller ([Gargron](https://github.com/tootsuite/mastodon/pull/12746))
- Fix uncaught unknown format error in host meta controller ([Gargron](https://github.com/tootsuite/mastodon/pull/12747))
- Fix URL search not returning private toots user has access to ([ThibG](https://github.com/tootsuite/mastodon/pull/12742), [ThibG](https://github.com/tootsuite/mastodon/pull/12336))
- Fix cache digesting log noise on status embeds ([Gargron](https://github.com/tootsuite/mastodon/pull/12750))
- Fix slowness due to layout thrashing when reloading a large set of statuses in web UI ([panarom](https://github.com/tootsuite/mastodon/pull/12661), [panarom](https://github.com/tootsuite/mastodon/pull/12744), [Gargron](https://github.com/tootsuite/mastodon/pull/12712))
- Fix error when fetching followers/following from REST API when user has network hidden ([Gargron](https://github.com/tootsuite/mastodon/pull/12716))
- Fix IDN mentions not being processed, IDN domains not being rendered ([Gargron](https://github.com/tootsuite/mastodon/pull/12715), [Gargron](https://github.com/tootsuite/mastodon/pull/13035), [Gargron](https://github.com/tootsuite/mastodon/pull/13030))
- Fix error when searching for empty phrase ([Gargron](https://github.com/tootsuite/mastodon/pull/12711))
- Fix backups stopping due to read timeouts ([chr-1x](https://github.com/tootsuite/mastodon/pull/12281))
- Fix batch actions on non-pending tags in admin UI ([ThibG](https://github.com/tootsuite/mastodon/pull/12537))
- Fix sample `SAML_ACS_URL`, `SAML_ISSUER` ([orlea](https://github.com/tootsuite/mastodon/pull/12669))
- Fix manual scrolling issue on Firefox/Windows in web UI ([ThibG](https://github.com/tootsuite/mastodon/pull/12648))
- Fix archive takeout failing if total dump size exceeds 2GB ([scd31](https://github.com/tootsuite/mastodon/pull/12602), [Gargron](https://github.com/tootsuite/mastodon/pull/12653))
- Fix custom emoji category creation silently erroring out on duplicate category ([ThibG](https://github.com/tootsuite/mastodon/pull/12647))
- Fix link crawler not specifying preferred content type ([ThibG](https://github.com/tootsuite/mastodon/pull/12646))
- Fix featured hashtag setting page erroring out instead of rejecting invalid tags ([ThibG](https://github.com/tootsuite/mastodon/pull/12436))
- Fix tooltip messages of single/multiple-choice polls switcher being reversed in web UI ([acid-chicken](https://github.com/tootsuite/mastodon/pull/12616))
- Fix typo in help text of `tootctl statuses remove` ([trwnh](https://github.com/tootsuite/mastodon/pull/12603))
- Fix generic HTTP 500 error on duplicate records ([Gargron](https://github.com/tootsuite/mastodon/pull/12563))
- Fix old migration failing with new status default scope ([ThibG](https://github.com/tootsuite/mastodon/pull/12493))
- Fix errors when using search API with no query ([Gargron](https://github.com/tootsuite/mastodon/pull/12541), [trwnh](https://github.com/tootsuite/mastodon/pull/12549))
- Fix poll options not being selectable via keyboard in web UI ([ThibG](https://github.com/tootsuite/mastodon/pull/12538))
- Fix conversations not having an unread indicator in web UI ([Gargron](https://github.com/tootsuite/mastodon/pull/12506))
- Fix lost focus when modals open/close in web UI ([ThibG](https://github.com/tootsuite/mastodon/pull/12437))
- Fix pending upload count not being decremented on error in web UI ([ThibG](https://github.com/tootsuite/mastodon/pull/12499))
- Fix empty poll options not being removed on remote poll update ([ThibG](https://github.com/tootsuite/mastodon/pull/12484))
- Fix OCR with delete & redraft in web UI ([ThibG](https://github.com/tootsuite/mastodon/pull/12465))
- Fix blur behind closed registration message ([ThibG](https://github.com/tootsuite/mastodon/pull/12442))
- Fix OEmbed discovery not handling different URL variants in query ([Gargron](https://github.com/tootsuite/mastodon/pull/12439))
- Fix link crawler crashing on `<a>` tags without `href` ([ThibG](https://github.com/tootsuite/mastodon/pull/12159))
- Fix whitelisted subdomains being ignored in whitelist mode ([noiob](https://github.com/tootsuite/mastodon/pull/12435))
- Fix broken audit log in whitelist mode in admin UI ([ThibG](https://github.com/tootsuite/mastodon/pull/12303))
- Fix unread indicator not honoring "Only media" option in local and federated timelines in web UI ([ThibG](https://github.com/tootsuite/mastodon/pull/12330))
- Fix error when rebuilding home feeds ([dariusk](https://github.com/tootsuite/mastodon/pull/12324))
- Fix relationship caches being broken as result of a follow request ([ThibG](https://github.com/tootsuite/mastodon/pull/12299))
- Fix more items than the limit being uploadable in web UI ([ThibG](https://github.com/tootsuite/mastodon/pull/12300))
- Fix various issues with account migration ([ThibG](https://github.com/tootsuite/mastodon/pull/12301))
- Fix filtered out items being counted as pending items in slow mode in web UI ([ThibG](https://github.com/tootsuite/mastodon/pull/12266))
- Fix notification filters not applying to poll options ([ThibG](https://github.com/tootsuite/mastodon/pull/12269))
- Fix notification message for user's own poll saying it's a poll they voted on in web UI ([ykzts](https://github.com/tootsuite/mastodon/pull/12219))
- Fix polls with an expiration not showing up as expired in web UI ([noellabo](https://github.com/tootsuite/mastodon/pull/12222))
- Fix volume slider having an offset between cursor and slider in Chromium in web UI ([ThibG](https://github.com/tootsuite/mastodon/pull/12158))
- Fix Vagrant image not accepting connections ([shrft](https://github.com/tootsuite/mastodon/pull/12180))
- Fix batch actions being hidden on small screens in admin UI ([ThibG](https://github.com/tootsuite/mastodon/pull/12183))
- Fix incoming federation not working in whitelist mode ([ThibG](https://github.com/tootsuite/mastodon/pull/12185))
- Fix error when passing empty `source` param to `PUT /api/v1/accounts/update_credentials` ([jglauche](https://github.com/tootsuite/mastodon/pull/12259))
- Fix HTTP-based streaming API being cacheable by proxies ([BenLubar](https://github.com/tootsuite/mastodon/pull/12945))
- Fix users being able to register while `tootctl self-destruct` is in progress ([Kjwon15](https://github.com/tootsuite/mastodon/pull/12877))
- Fix microformats detection in link crawler not ignoring `h-card` links ([nightpool](https://github.com/tootsuite/mastodon/pull/12189))
- Fix outline on full-screen video in web UI ([hinaloe](https://github.com/tootsuite/mastodon/pull/12176))
- Fix TLD domain blocks not being editable ([ThibG](https://github.com/tootsuite/mastodon/pull/12805))
- Fix Nanobox deploy hooks ([danhunsaker](https://github.com/tootsuite/mastodon/pull/12663))
- Fix needlessly complicated SQL query when performing account search amongst followings ([ThibG](https://github.com/tootsuite/mastodon/pull/12302))
- Fix favourites count not updating when unfavouriting in web UI ([NimaBoscarino](https://github.com/tootsuite/mastodon/pull/12140))
- Fix occasional crash on scroll in Chromium in web UI ([hinaloe](https://github.com/tootsuite/mastodon/pull/12274))
- Fix intersection observer not working in single-column mode web UI ([panarom](https://github.com/tootsuite/mastodon/pull/12735))
- Fix voting issue with remote polls that contain trailing spaces ([ThibG](https://github.com/tootsuite/mastodon/pull/12515))
- Fix dynamic elements not working in pgHero due to CSP rules ([ykzts](https://github.com/tootsuite/mastodon/pull/12489))
- Fix overly verbose backtraces when delivering ActivityPub payloads ([zunda](https://github.com/tootsuite/mastodon/pull/12798))
- Fix rendering `<a>` without `href` when scheme unsupported ([Gargron](https://github.com/tootsuite/mastodon/pull/13040))
- Fix unfiltered params error when generating ActivityPub tag pagination ([Gargron](https://github.com/tootsuite/mastodon/pull/13049))
- Fix malformed HTML causing uncaught error ([Gargron](https://github.com/tootsuite/mastodon/pull/13042))
- Fix native share button not being displayed for unlisted toots ([ThibG](https://github.com/tootsuite/mastodon/pull/13045))
- Fix remote convertible media attachments (e.g. GIFs) not being saved ([Gargron](https://github.com/tootsuite/mastodon/pull/13032))
- Fix account query not using faster index ([abcang](https://github.com/tootsuite/mastodon/pull/13016))
- Fix error when sending moderation notification ([renatolond](https://github.com/tootsuite/mastodon/pull/13014))

### Security

- Fix OEmbed leaking information about existence of non-public statuses ([Gargron](https://github.com/tootsuite/mastodon/pull/12930))
- Fix password change/reset not immediately invalidating other sessions ([Gargron](https://github.com/tootsuite/mastodon/pull/12928))
- Fix settings pages being cacheable by the browser ([Gargron](https://github.com/tootsuite/mastodon/pull/12714))

## [3.0.1] - 2019-10-10
### Added

- Add `tootctl media usage` command ([Gargron](https://github.com/tootsuite/mastodon/pull/12115))
- Add admin setting to auto-approve trending hashtags ([Gargron](https://github.com/tootsuite/mastodon/pull/12122), [Gargron](https://github.com/tootsuite/mastodon/pull/12130))

### Changed

- Change `tootctl media refresh` to skip already downloaded attachments ([Gargron](https://github.com/tootsuite/mastodon/pull/12118))

### Removed

- Remove auto-silence behaviour from spam check ([Gargron](https://github.com/tootsuite/mastodon/pull/12117))
- Remove HTML `lang` attribute from individual statuses in web UI ([Gargron](https://github.com/tootsuite/mastodon/pull/12124))
- Remove fallback to long description on sidebar and meta description ([Gargron](https://github.com/tootsuite/mastodon/pull/12119))

### Fixed

- Fix preloaded JSON-LD context for identity not being used ([Gargron](https://github.com/tootsuite/mastodon/pull/12138))
- Fix media editing modal changing dimensions once the image loads ([Gargron](https://github.com/tootsuite/mastodon/pull/12131))
- Fix not showing whether a custom emoji has a local counterpart in admin UI ([Gargron](https://github.com/tootsuite/mastodon/pull/12135))
- Fix attachment not being re-downloaded even if file is not stored ([Gargron](https://github.com/tootsuite/mastodon/pull/12125))
- Fix old migration trying to use new column due to default status scope ([Gargron](https://github.com/tootsuite/mastodon/pull/12095))
- Fix column back button missing for not found accounts ([trwnh](https://github.com/tootsuite/mastodon/pull/12094))
- Fix issues with tootctl's parallelization and progress reporting ([Gargron](https://github.com/tootsuite/mastodon/pull/12093), [Gargron](https://github.com/tootsuite/mastodon/pull/12097))
- Fix existing user records with now-renamed `pt` locale ([Gargron](https://github.com/tootsuite/mastodon/pull/12092))
- Fix hashtag timeline REST API accepting too many hashtags ([Gargron](https://github.com/tootsuite/mastodon/pull/12091))
- Fix `GET /api/v1/instance` REST APIs being unavailable in secure mode ([Gargron](https://github.com/tootsuite/mastodon/pull/12089))
- Fix performance of home feed regeneration and merging ([Gargron](https://github.com/tootsuite/mastodon/pull/12084))
- Fix ffmpeg performance issues due to stdout buffer overflow ([hugogameiro](https://github.com/tootsuite/mastodon/pull/12088))
- Fix S3 adapter retrying failing uploads with exponential backoff ([Gargron](https://github.com/tootsuite/mastodon/pull/12085))
- Fix `tootctl accounts cull` advertising unused option flag ([Kjwon15](https://github.com/tootsuite/mastodon/pull/12074))

## [3.0.0] - 2019-10-03
### Added

- Add "not available" label to unloaded media attachments in web UI ([Gargron](https://github.com/tootsuite/mastodon/pull/11715), [Gargron](https://github.com/tootsuite/mastodon/pull/11745))
- **Add profile directory to web UI** ([Gargron](https://github.com/tootsuite/mastodon/pull/11688), [mayaeh](https://github.com/tootsuite/mastodon/pull/11872))
  - Add profile directory opt-in federation
  - Add profile directory REST API
- Add special alert for throttled requests in web UI ([ThibG](https://github.com/tootsuite/mastodon/pull/11677))
- Add confirmation modal when logging out from the web UI ([ThibG](https://github.com/tootsuite/mastodon/pull/11671))
- **Add audio player in web UI** ([Gargron](https://github.com/tootsuite/mastodon/pull/11644), [Gargron](https://github.com/tootsuite/mastodon/pull/11652), [Gargron](https://github.com/tootsuite/mastodon/pull/11654), [ThibG](https://github.com/tootsuite/mastodon/pull/11629), [Gargron](https://github.com/tootsuite/mastodon/pull/12056))
- **Add autosuggestions for hashtags in web UI** ([Gargron](https://github.com/tootsuite/mastodon/pull/11422), [ThibG](https://github.com/tootsuite/mastodon/pull/11632), [Gargron](https://github.com/tootsuite/mastodon/pull/11764), [Gargron](https://github.com/tootsuite/mastodon/pull/11588), [Gargron](https://github.com/tootsuite/mastodon/pull/11442))
- **Add media editing modal with OCR tool in web UI** ([Gargron](https://github.com/tootsuite/mastodon/pull/11563), [Gargron](https://github.com/tootsuite/mastodon/pull/11566), [ThibG](https://github.com/tootsuite/mastodon/pull/11575), [ThibG](https://github.com/tootsuite/mastodon/pull/11576), [Gargron](https://github.com/tootsuite/mastodon/pull/11577), [Gargron](https://github.com/tootsuite/mastodon/pull/11573), [Gargron](https://github.com/tootsuite/mastodon/pull/11571))
- Add indicator of unread notifications to window title when web UI is out of focus ([Gargron](https://github.com/tootsuite/mastodon/pull/11560), [Gargron](https://github.com/tootsuite/mastodon/pull/11572))
- Add indicator for which options you voted for in a poll in web UI ([ThibG](https://github.com/tootsuite/mastodon/pull/11195))
- **Add search results pagination to web UI** ([Gargron](https://github.com/tootsuite/mastodon/pull/11409), [ThibG](https://github.com/tootsuite/mastodon/pull/11447))
- **Add option to disable real-time updates in web UI ("slow mode")** ([Gargron](https://github.com/tootsuite/mastodon/pull/9984), [ykzts](https://github.com/tootsuite/mastodon/pull/11880), [ThibG](https://github.com/tootsuite/mastodon/pull/11883), [Gargron](https://github.com/tootsuite/mastodon/pull/11898), [ThibG](https://github.com/tootsuite/mastodon/pull/11859))
- Add option to disable blurhash previews in web UI ([ThibG](https://github.com/tootsuite/mastodon/pull/11188))
- Add native smooth scrolling when supported in web UI ([ThibG](https://github.com/tootsuite/mastodon/pull/11207))
- Add scrolling to the search bar on focus in web UI ([Kjwon15](https://github.com/tootsuite/mastodon/pull/12032))
- Add refresh button to list of rebloggers/favouriters in web UI ([Gargron](https://github.com/tootsuite/mastodon/pull/12031))
- Add error description and button to copy stack trace to web UI ([Gargron](https://github.com/tootsuite/mastodon/pull/12033))
- Add search and sort functions to hashtag admin UI ([mayaeh](https://github.com/tootsuite/mastodon/pull/11829), [Gargron](https://github.com/tootsuite/mastodon/pull/11897), [mayaeh](https://github.com/tootsuite/mastodon/pull/11875))
- Add setting for default search engine indexing in admin UI ([brortao](https://github.com/tootsuite/mastodon/pull/11804))
- Add account bio to account view in admin UI ([ThibG](https://github.com/tootsuite/mastodon/pull/11473))
- **Add option to include reported statuses in warning e-mail from admin UI** ([Gargron](https://github.com/tootsuite/mastodon/pull/11639), [Gargron](https://github.com/tootsuite/mastodon/pull/11812), [Gargron](https://github.com/tootsuite/mastodon/pull/11741), [Gargron](https://github.com/tootsuite/mastodon/pull/11698), [mayaeh](https://github.com/tootsuite/mastodon/pull/11765))
- Add number of pending accounts and pending hashtags to dashboard in admin UI ([Gargron](https://github.com/tootsuite/mastodon/pull/11514))
- **Add account migration UI** ([Gargron](https://github.com/tootsuite/mastodon/pull/11846), [noellabo](https://github.com/tootsuite/mastodon/pull/11905), [noellabo](https://github.com/tootsuite/mastodon/pull/11907), [noellabo](https://github.com/tootsuite/mastodon/pull/11906), [noellabo](https://github.com/tootsuite/mastodon/pull/11902))
- **Add table of contents to about page** ([Gargron](https://github.com/tootsuite/mastodon/pull/11885), [ykzts](https://github.com/tootsuite/mastodon/pull/11941), [ykzts](https://github.com/tootsuite/mastodon/pull/11895), [Kjwon15](https://github.com/tootsuite/mastodon/pull/11916))
- **Add password challenge to 2FA settings, e-mail notifications** ([Gargron](https://github.com/tootsuite/mastodon/pull/11878))
- **Add optional public list of domain blocks with comments** ([ThibG](https://github.com/tootsuite/mastodon/pull/11298), [ThibG](https://github.com/tootsuite/mastodon/pull/11515), [Gargron](https://github.com/tootsuite/mastodon/pull/11908))
- Add an RSS feed for featured hashtags ([noellabo](https://github.com/tootsuite/mastodon/pull/10502))
- Add explanations to featured hashtags UI and profile ([Gargron](https://github.com/tootsuite/mastodon/pull/11586))
- **Add hashtag trends with admin and user settings** ([Gargron](https://github.com/tootsuite/mastodon/pull/11490), [Gargron](https://github.com/tootsuite/mastodon/pull/11502), [Gargron](https://github.com/tootsuite/mastodon/pull/11641), [Gargron](https://github.com/tootsuite/mastodon/pull/11594), [Gargron](https://github.com/tootsuite/mastodon/pull/11517), [mayaeh](https://github.com/tootsuite/mastodon/pull/11845), [Gargron](https://github.com/tootsuite/mastodon/pull/11774), [Gargron](https://github.com/tootsuite/mastodon/pull/11712), [Gargron](https://github.com/tootsuite/mastodon/pull/11791), [Gargron](https://github.com/tootsuite/mastodon/pull/11743), [Gargron](https://github.com/tootsuite/mastodon/pull/11740), [Gargron](https://github.com/tootsuite/mastodon/pull/11714), [ThibG](https://github.com/tootsuite/mastodon/pull/11631), [Sasha-Sorokin](https://github.com/tootsuite/mastodon/pull/11569), [Gargron](https://github.com/tootsuite/mastodon/pull/11524), [Gargron](https://github.com/tootsuite/mastodon/pull/11513))
  - Add hashtag usage breakdown to admin UI
  - Add batch actions for hashtags to admin UI
  - Add trends to web UI
  - Add trends to public pages
  - Add user preference to hide trends
  - Add admin setting to disable trends
- **Add categories for custom emojis** ([Gargron](https://github.com/tootsuite/mastodon/pull/11196), [Gargron](https://github.com/tootsuite/mastodon/pull/11793), [Gargron](https://github.com/tootsuite/mastodon/pull/11920), [highemerly](https://github.com/tootsuite/mastodon/pull/11876))
  - Add custom emoji categories to emoji picker in web UI
  - Add `category` to custom emojis in REST API
  - Add batch actions for custom emojis in admin UI
- Add max image dimensions to error message ([raboof](https://github.com/tootsuite/mastodon/pull/11552))
- Add aac, m4a, 3gp, amr, wma to allowed audio formats ([Gargron](https://github.com/tootsuite/mastodon/pull/11342), [umonaca](https://github.com/tootsuite/mastodon/pull/11687))
- **Add search syntax for operators and phrases** ([Gargron](https://github.com/tootsuite/mastodon/pull/11411))
- **Add REST API for managing featured hashtags** ([noellabo](https://github.com/tootsuite/mastodon/pull/11778))
- **Add REST API for managing timeline read markers** ([Gargron](https://github.com/tootsuite/mastodon/pull/11762))
- Add `exclude_unreviewed` param to `GET /api/v2/search` REST API ([Gargron](https://github.com/tootsuite/mastodon/pull/11977))
- Add `reason` param to `POST /api/v1/accounts` REST API ([Gargron](https://github.com/tootsuite/mastodon/pull/12064))
- **Add ActivityPub secure mode** ([Gargron](https://github.com/tootsuite/mastodon/pull/11269), [ThibG](https://github.com/tootsuite/mastodon/pull/11332), [ThibG](https://github.com/tootsuite/mastodon/pull/11295))
- Add HTTP signatures to all outgoing ActivityPub GET requests ([Gargron](https://github.com/tootsuite/mastodon/pull/11284), [ThibG](https://github.com/tootsuite/mastodon/pull/11300))
- Add support for ActivityPub Audio activities ([ThibG](https://github.com/tootsuite/mastodon/pull/11189))
- Add ActivityPub actor representing the entire server ([ThibG](https://github.com/tootsuite/mastodon/pull/11321), [rtucker](https://github.com/tootsuite/mastodon/pull/11400), [ThibG](https://github.com/tootsuite/mastodon/pull/11561), [Gargron](https://github.com/tootsuite/mastodon/pull/11798))
- **Add whitelist mode** ([Gargron](https://github.com/tootsuite/mastodon/pull/11291), [mayaeh](https://github.com/tootsuite/mastodon/pull/11634))
- Add config of multipart threshold for S3 ([ykzts](https://github.com/tootsuite/mastodon/pull/11924), [ykzts](https://github.com/tootsuite/mastodon/pull/11944))
- Add health check endpoint for web ([ykzts](https://github.com/tootsuite/mastodon/pull/11770), [ykzts](https://github.com/tootsuite/mastodon/pull/11947))
- Add HTTP signature keyId to request log ([Gargron](https://github.com/tootsuite/mastodon/pull/11591))
- Add `SMTP_REPLY_TO` environment variable ([hugogameiro](https://github.com/tootsuite/mastodon/pull/11718))
- Add `tootctl preview_cards remove` command ([mayaeh](https://github.com/tootsuite/mastodon/pull/11320))
- Add `tootctl media refresh` command ([Gargron](https://github.com/tootsuite/mastodon/pull/11775))
- Add `tootctl cache recount` command ([Gargron](https://github.com/tootsuite/mastodon/pull/11597))
- Add option to exclude suspended domains from `tootctl domains crawl` ([dariusk](https://github.com/tootsuite/mastodon/pull/11454))
- Add parallelization to `tootctl search deploy` ([noellabo](https://github.com/tootsuite/mastodon/pull/12051))
- Add soft delete for statuses for instant deletes through API ([Gargron](https://github.com/tootsuite/mastodon/pull/11623), [Gargron](https://github.com/tootsuite/mastodon/pull/11648))
- Add rails-level JSON caching ([Gargron](https://github.com/tootsuite/mastodon/pull/11333), [Gargron](https://github.com/tootsuite/mastodon/pull/11271))
- **Add request pool to improve delivery performance** ([Gargron](https://github.com/tootsuite/mastodon/pull/10353), [ykzts](https://github.com/tootsuite/mastodon/pull/11756))
- Add concurrent connection attempts to resolved IP addresses ([ThibG](https://github.com/tootsuite/mastodon/pull/11757))
- Add index for remember_token to improve login performance ([abcang](https://github.com/tootsuite/mastodon/pull/11881))
- **Add more accurate hashtag search** ([Gargron](https://github.com/tootsuite/mastodon/pull/11579), [Gargron](https://github.com/tootsuite/mastodon/pull/11427), [Gargron](https://github.com/tootsuite/mastodon/pull/11448))
- **Add more accurate account search** ([Gargron](https://github.com/tootsuite/mastodon/pull/11537), [Gargron](https://github.com/tootsuite/mastodon/pull/11580))
- **Add a spam check** ([Gargron](https://github.com/tootsuite/mastodon/pull/11217), [Gargron](https://github.com/tootsuite/mastodon/pull/11806), [ThibG](https://github.com/tootsuite/mastodon/pull/11296))
- Add new languages ([Gargron](https://github.com/tootsuite/mastodon/pull/12062))
  - Breton
  - Spanish (Argentina)
  - Estonian
  - Macedonian
  - New Norwegian
- Add NodeInfo endpoint ([Gargron](https://github.com/tootsuite/mastodon/pull/12002), [Gargron](https://github.com/tootsuite/mastodon/pull/12058))

### Changed

- **Change conversations UI** ([Gargron](https://github.com/tootsuite/mastodon/pull/11896))
- Change dashboard to short number notation ([noellabo](https://github.com/tootsuite/mastodon/pull/11847), [noellabo](https://github.com/tootsuite/mastodon/pull/11911))
- Change REST API `GET /api/v1/timelines/public` to require authentication when public preview is off ([ThibG](https://github.com/tootsuite/mastodon/pull/11802))
- Change REST API `POST /api/v1/follow_requests/:id/(approve|reject)` to return relationship ([ThibG](https://github.com/tootsuite/mastodon/pull/11800))
- Change rate limit for media proxy ([ykzts](https://github.com/tootsuite/mastodon/pull/11814))
- Change unlisted custom emoji to not appear in autosuggestions ([Gargron](https://github.com/tootsuite/mastodon/pull/11818))
- Change max length of media descriptions from 420 to 1500 characters ([Gargron](https://github.com/tootsuite/mastodon/pull/11819), [ThibG](https://github.com/tootsuite/mastodon/pull/11836))
- **Change deletes to preserve soft-deleted statuses in unresolved reports** ([Gargron](https://github.com/tootsuite/mastodon/pull/11805))
- **Change tootctl to use inline parallelization instead of Sidekiq** ([Gargron](https://github.com/tootsuite/mastodon/pull/11776))
- **Change account deletion page to have better explanations** ([Gargron](https://github.com/tootsuite/mastodon/pull/11753), [Gargron](https://github.com/tootsuite/mastodon/pull/11763))
- Change hashtag component in web UI to show numbers for 2 last days ([Gargron](https://github.com/tootsuite/mastodon/pull/11742), [Gargron](https://github.com/tootsuite/mastodon/pull/11755), [Gargron](https://github.com/tootsuite/mastodon/pull/11754))
- Change OpenGraph description on sign-up page to reflect invite ([Gargron](https://github.com/tootsuite/mastodon/pull/11744))
- Change layout of public profile directory to be the same as in web UI ([Gargron](https://github.com/tootsuite/mastodon/pull/11705))
- Change detailed status child ordering to sort self-replies on top ([ThibG](https://github.com/tootsuite/mastodon/pull/11686))
- Change window resize handler to switch to/from mobile layout as soon as needed ([ThibG](https://github.com/tootsuite/mastodon/pull/11656))
- Change icon button styles to make hover/focus states more obvious ([ThibG](https://github.com/tootsuite/mastodon/pull/11474))
- Change contrast of status links that are not mentions or hashtags ([ThibG](https://github.com/tootsuite/mastodon/pull/11406))
- **Change hashtags to preserve first-used casing** ([Gargron](https://github.com/tootsuite/mastodon/pull/11416), [Gargron](https://github.com/tootsuite/mastodon/pull/11508), [Gargron](https://github.com/tootsuite/mastodon/pull/11504), [Gargron](https://github.com/tootsuite/mastodon/pull/11507), [Gargron](https://github.com/tootsuite/mastodon/pull/11441))
- **Change unconfirmed user login behaviour** ([Gargron](https://github.com/tootsuite/mastodon/pull/11375), [ThibG](https://github.com/tootsuite/mastodon/pull/11394), [Gargron](https://github.com/tootsuite/mastodon/pull/11860))
- **Change single-column mode to scroll the whole page** ([Gargron](https://github.com/tootsuite/mastodon/pull/11359), [Gargron](https://github.com/tootsuite/mastodon/pull/11894), [Gargron](https://github.com/tootsuite/mastodon/pull/11891), [ThibG](https://github.com/tootsuite/mastodon/pull/11655), [Gargron](https://github.com/tootsuite/mastodon/pull/11463), [Gargron](https://github.com/tootsuite/mastodon/pull/11458), [ThibG](https://github.com/tootsuite/mastodon/pull/11395), [Gargron](https://github.com/tootsuite/mastodon/pull/11418))
- Change `tootctl accounts follow` to only work with local accounts ([angristan](https://github.com/tootsuite/mastodon/pull/11592))
- Change Dockerfile ([Shleeble](https://github.com/tootsuite/mastodon/pull/11710), [ykzts](https://github.com/tootsuite/mastodon/pull/11768), [Shleeble](https://github.com/tootsuite/mastodon/pull/11707))
- Change supported Node versions to include v12 ([abcang](https://github.com/tootsuite/mastodon/pull/11706))
- Change Portuguese language from `pt` to `pt-PT` ([Gargron](https://github.com/tootsuite/mastodon/pull/11820))
- Change domain block silence to always require approval on follow ([ThibG](https://github.com/tootsuite/mastodon/pull/11975))
- Change link preview fetcher to not perform a HEAD request first ([Gargron](https://github.com/tootsuite/mastodon/pull/12028))
- Change `tootctl domains purge` to accept multiple domains at once ([Gargron](https://github.com/tootsuite/mastodon/pull/12046))

### Removed

- **Remove OStatus support** ([Gargron](https://github.com/tootsuite/mastodon/pull/11205), [Gargron](https://github.com/tootsuite/mastodon/pull/11303), [Gargron](https://github.com/tootsuite/mastodon/pull/11460), [ThibG](https://github.com/tootsuite/mastodon/pull/11280), [ThibG](https://github.com/tootsuite/mastodon/pull/11278))
- Remove Atom feeds and old URLs in the form of `GET /:username/updates/:id` ([Gargron](https://github.com/tootsuite/mastodon/pull/11247))
- Remove WebP support ([angristan](https://github.com/tootsuite/mastodon/pull/11589))
- Remove deprecated config options from Heroku and Scalingo ([ykzts](https://github.com/tootsuite/mastodon/pull/11925))
- Remove deprecated REST API `GET /api/v1/search` API ([Gargron](https://github.com/tootsuite/mastodon/pull/11823))
- Remove deprecated REST API `GET /api/v1/statuses/:id/card` ([Gargron](https://github.com/tootsuite/mastodon/pull/11213))
- Remove deprecated REST API `POST /api/v1/notifications/dismiss?id=:id` ([Gargron](https://github.com/tootsuite/mastodon/pull/11214))
- Remove deprecated REST API `GET /api/v1/timelines/direct` ([Gargron](https://github.com/tootsuite/mastodon/pull/11212))

### Fixed

- Fix manifest warning ([ykzts](https://github.com/tootsuite/mastodon/pull/11767))
- Fix admin UI for custom emoji not respecting GIF autoplay preference ([ThibG](https://github.com/tootsuite/mastodon/pull/11801))
- Fix page body not being scrollable in admin/settings layout ([Gargron](https://github.com/tootsuite/mastodon/pull/11893))
- Fix placeholder colors for inputs not being explicitly defined ([Gargron](https://github.com/tootsuite/mastodon/pull/11890))
- Fix incorrect enclosure length in RSS ([tsia](https://github.com/tootsuite/mastodon/pull/11889))
- Fix TOTP codes not being filtered from logs during enabling/disabling ([Gargron](https://github.com/tootsuite/mastodon/pull/11877))
- Fix webfinger response not returning 410 when account is suspended ([Gargron](https://github.com/tootsuite/mastodon/pull/11869))
- Fix ActivityPub Move handler queuing jobs that will fail if account is suspended ([Gargron](https://github.com/tootsuite/mastodon/pull/11864))
- Fix SSO login not using existing account when e-mail is verified ([Gargron](https://github.com/tootsuite/mastodon/pull/11862))
- Fix web UI allowing uploads past status limit via drag & drop ([Gargron](https://github.com/tootsuite/mastodon/pull/11863))
- Fix expiring polls not being displayed as such in web UI ([ThibG](https://github.com/tootsuite/mastodon/pull/11835))
- Fix 2FA challenge and password challenge for non-database users ([Gargron](https://github.com/tootsuite/mastodon/pull/11831), [Gargron](https://github.com/tootsuite/mastodon/pull/11943))
- Fix profile fields overflowing page width in web UI ([Gargron](https://github.com/tootsuite/mastodon/pull/11828))
- Fix web push subscriptions being deleted on rate limit or timeout ([Gargron](https://github.com/tootsuite/mastodon/pull/11826))
- Fix display of long poll options in web UI ([ThibG](https://github.com/tootsuite/mastodon/pull/11717), [ThibG](https://github.com/tootsuite/mastodon/pull/11833))
- Fix search API not resolving URL when `type` is given ([Gargron](https://github.com/tootsuite/mastodon/pull/11822))
- Fix hashtags being split by ZWNJ character ([Gargron](https://github.com/tootsuite/mastodon/pull/11821))
- Fix scroll position resetting when opening media modals in web UI ([Gargron](https://github.com/tootsuite/mastodon/pull/11815))
- Fix duplicate HTML IDs on about page ([ThibG](https://github.com/tootsuite/mastodon/pull/11803))
- Fix admin UI showing superfluous reject media/reports on suspended domain blocks ([ThibG](https://github.com/tootsuite/mastodon/pull/11749))
- Fix ActivityPub context not being dynamically computed ([ThibG](https://github.com/tootsuite/mastodon/pull/11746))
- Fix Mastodon logo style on hover on public pages' footer ([ThibG](https://github.com/tootsuite/mastodon/pull/11735))
- Fix height of dashboard counters ([ThibG](https://github.com/tootsuite/mastodon/pull/11736))
- Fix custom emoji animation on hover in web UI directory bios ([ThibG](https://github.com/tootsuite/mastodon/pull/11716))
- Fix non-numbers being passed to Redis and causing an error ([Gargron](https://github.com/tootsuite/mastodon/pull/11697))
- Fix error in REST API for an account's statuses ([Gargron](https://github.com/tootsuite/mastodon/pull/11700))
- Fix uncaught error when resource param is missing in Webfinger request ([Gargron](https://github.com/tootsuite/mastodon/pull/11701))
- Fix uncaught domain normalization error in remote follow ([Gargron](https://github.com/tootsuite/mastodon/pull/11703))
- Fix uncaught 422 and 500 errors ([Gargron](https://github.com/tootsuite/mastodon/pull/11590), [Gargron](https://github.com/tootsuite/mastodon/pull/11811))
- Fix uncaught parameter missing exceptions and missing error templates ([Gargron](https://github.com/tootsuite/mastodon/pull/11702))
- Fix encoding error when checking e-mail MX records ([Gargron](https://github.com/tootsuite/mastodon/pull/11696))
- Fix items in StatusContent render list not all having a key ([ThibG](https://github.com/tootsuite/mastodon/pull/11645))
- Fix remote and staff-removed statuses leaving media behind for a day ([Gargron](https://github.com/tootsuite/mastodon/pull/11638))
- Fix CSP needlessly allowing blob URLs in script-src ([ThibG](https://github.com/tootsuite/mastodon/pull/11620))
- Fix ignoring whole status because of one invalid hashtag ([Gargron](https://github.com/tootsuite/mastodon/pull/11621))
- Fix hidden statuses losing focus ([ThibG](https://github.com/tootsuite/mastodon/pull/11208))
- Fix loading bar being obscured by other elements in web UI ([Gargron](https://github.com/tootsuite/mastodon/pull/11598))
- Fix multiple issues with replies collection for pages further than self-replies ([ThibG](https://github.com/tootsuite/mastodon/pull/11582))
- Fix blurhash and autoplay not working on public pages ([Gargron](https://github.com/tootsuite/mastodon/pull/11585))
- Fix 422 being returned instead of 404 when POSTing to unmatched routes ([Gargron](https://github.com/tootsuite/mastodon/pull/11574), [Gargron](https://github.com/tootsuite/mastodon/pull/11704))
- Fix client-side resizing of image uploads ([ThibG](https://github.com/tootsuite/mastodon/pull/11570))
- Fix short number formatting for numbers above million in web UI ([Gargron](https://github.com/tootsuite/mastodon/pull/11559))
- Fix ActivityPub and REST API queries setting cookies and preventing caching ([ThibG](https://github.com/tootsuite/mastodon/pull/11539), [ThibG](https://github.com/tootsuite/mastodon/pull/11557), [ThibG](https://github.com/tootsuite/mastodon/pull/11336), [ThibG](https://github.com/tootsuite/mastodon/pull/11331))
- Fix some emojis in profile metadata labels are not emojified. ([kedamaDQ](https://github.com/tootsuite/mastodon/pull/11534))
- Fix account search always returning exact match on paginated results ([Gargron](https://github.com/tootsuite/mastodon/pull/11525))
- Fix acct URIs with IDN domains not being resolved ([Gargron](https://github.com/tootsuite/mastodon/pull/11520))
- Fix admin dashboard missing latest features ([Gargron](https://github.com/tootsuite/mastodon/pull/11505))
- Fix jumping of toot date when clicking spoiler button ([ariasuni](https://github.com/tootsuite/mastodon/pull/11449))
- Fix boost to original audience not working on mobile in web UI ([ThibG](https://github.com/tootsuite/mastodon/pull/11371))
- Fix handling of webfinger redirects in ResolveAccountService ([ThibG](https://github.com/tootsuite/mastodon/pull/11279))
- Fix URLs appearing twice in errors of ActivityPub::DeliveryWorker ([Gargron](https://github.com/tootsuite/mastodon/pull/11231))
- Fix support for HTTP proxies ([ThibG](https://github.com/tootsuite/mastodon/pull/11245))
- Fix HTTP requests to IPv6 hosts ([ThibG](https://github.com/tootsuite/mastodon/pull/11240))
- Fix error in ElasticSearch index import ([mayaeh](https://github.com/tootsuite/mastodon/pull/11192))
- Fix duplicate account error when seeding development database ([ysksn](https://github.com/tootsuite/mastodon/pull/11366))
- Fix performance of session clean-up scheduler ([abcang](https://github.com/tootsuite/mastodon/pull/11871))
- Fix older migrations not running ([zunda](https://github.com/tootsuite/mastodon/pull/11377))
- Fix URLs counting towards RTL detection ([ahangarha](https://github.com/tootsuite/mastodon/pull/11759))
- Fix unnecessary status re-rendering in web UI ([ThibG](https://github.com/tootsuite/mastodon/pull/11211))
- Fix http_parser.rb gem not being compiled when no network available ([petabyteboy](https://github.com/tootsuite/mastodon/pull/11444))
- Fix muted text color not applying to all text ([trwnh](https://github.com/tootsuite/mastodon/pull/11996))
- Fix follower/following lists resetting on back-navigation in web UI ([Gargron](https://github.com/tootsuite/mastodon/pull/11986))
- Fix n+1 query when approving multiple follow requests ([abcang](https://github.com/tootsuite/mastodon/pull/12004))
- Fix records not being indexed into ElasticSearch sometimes ([Gargron](https://github.com/tootsuite/mastodon/pull/12024))
- Fix needlessly indexing unsearchable statuses into ElasticSearch ([Gargron](https://github.com/tootsuite/mastodon/pull/12041))
- Fix new user bootstrapping crashing when to-be-followed accounts are invalid ([ThibG](https://github.com/tootsuite/mastodon/pull/12037))
- Fix featured hashtag URL being interpreted as media or replies tab ([Gargron](https://github.com/tootsuite/mastodon/pull/12048))
- Fix account counters being overwritten by parallel writes ([Gargron](https://github.com/tootsuite/mastodon/pull/12045))

### Security

- Fix performance of GIF re-encoding and always strip EXIF data from videos ([Gargron](https://github.com/tootsuite/mastodon/pull/12057))

## [2.9.3] - 2019-08-10
### Added

- Add GIF and WebP support for custom emojis ([Gargron](https://github.com/tootsuite/mastodon/pull/11519))
- Add logout link to dropdown menu in web UI ([koyuawsmbrtn](https://github.com/tootsuite/mastodon/pull/11353))
- Add indication that text search is unavailable in web UI ([ThibG](https://github.com/tootsuite/mastodon/pull/11112), [ThibG](https://github.com/tootsuite/mastodon/pull/11202))
- Add `suffix` to `Mastodon::Version` to help forks ([clarfon](https://github.com/tootsuite/mastodon/pull/11407))
- Add on-hover animation to animated custom emoji in web UI ([ThibG](https://github.com/tootsuite/mastodon/pull/11348), [ThibG](https://github.com/tootsuite/mastodon/pull/11404), [ThibG](https://github.com/tootsuite/mastodon/pull/11522))
- Add custom emoji support in profile metadata labels ([ThibG](https://github.com/tootsuite/mastodon/pull/11350))

### Changed

- Change default interface of web and streaming from 0.0.0.0 to 127.0.0.1 ([Gargron](https://github.com/tootsuite/mastodon/pull/11302), [zunda](https://github.com/tootsuite/mastodon/pull/11378), [Gargron](https://github.com/tootsuite/mastodon/pull/11351), [zunda](https://github.com/tootsuite/mastodon/pull/11326))
- Change the retry limit of web push notifications ([highemerly](https://github.com/tootsuite/mastodon/pull/11292))
- Change ActivityPub deliveries to not retry HTTP 501 errors ([Gargron](https://github.com/tootsuite/mastodon/pull/11233))
- Change language detection to include hashtags as words ([Gargron](https://github.com/tootsuite/mastodon/pull/11341))
- Change terms and privacy policy pages to always be accessible ([Gargron](https://github.com/tootsuite/mastodon/pull/11334))
- Change robots tag to include `noarchive` when user opts out of indexing ([Kjwon15](https://github.com/tootsuite/mastodon/pull/11421))

### Fixed

- Fix account domain block not clearing out notifications ([Gargron](https://github.com/tootsuite/mastodon/pull/11393))
- Fix incorrect locale sometimes being detected for browser ([Gargron](https://github.com/tootsuite/mastodon/pull/8657))
- Fix crash when saving invalid domain name ([Gargron](https://github.com/tootsuite/mastodon/pull/11528))
- Fix pinned statuses REST API returning pagination headers ([Gargron](https://github.com/tootsuite/mastodon/pull/11526))
- Fix "cancel follow request" button having unreadable text in web UI ([Gargron](https://github.com/tootsuite/mastodon/pull/11521))
- Fix image uploads being blank when canvas read access is blocked ([ThibG](https://github.com/tootsuite/mastodon/pull/11499))
- Fix avatars not being animated on hover when not logged in ([ThibG](https://github.com/tootsuite/mastodon/pull/11349))
- Fix overzealous sanitization of HTML lists ([ThibG](https://github.com/tootsuite/mastodon/pull/11354))
- Fix block crashing when a follow request exists ([ThibG](https://github.com/tootsuite/mastodon/pull/11288))
- Fix backup service crashing when an attachment is missing ([ThibG](https://github.com/tootsuite/mastodon/pull/11241))
- Fix account moderation action always sending e-mail notification ([Gargron](https://github.com/tootsuite/mastodon/pull/11242))
- Fix swiping columns on mobile sometimes failing in web UI ([ThibG](https://github.com/tootsuite/mastodon/pull/11200))
- Fix wrong actor URI being serialized into poll updates ([ThibG](https://github.com/tootsuite/mastodon/pull/11194))
- Fix statsd UDP sockets not being cleaned up in Sidekiq ([Gargron](https://github.com/tootsuite/mastodon/pull/11230))
- Fix expiration date of filters being set to "never" when editing them ([ThibG](https://github.com/tootsuite/mastodon/pull/11204))
- Fix support for MP4 files that are actually M4V files ([Gargron](https://github.com/tootsuite/mastodon/pull/11210))
- Fix `alerts` not being typecast correctly in push subscription in REST API ([Gargron](https://github.com/tootsuite/mastodon/pull/11343))
- Fix some notices staying on unrelated pages ([ThibG](https://github.com/tootsuite/mastodon/pull/11364))
- Fix unboosting sometimes preventing a boost from reappearing on feed ([ThibG](https://github.com/tootsuite/mastodon/pull/11405), [Gargron](https://github.com/tootsuite/mastodon/pull/11450))
- Fix only one middle dot being recognized in hashtags ([Gargron](https://github.com/tootsuite/mastodon/pull/11345), [ThibG](https://github.com/tootsuite/mastodon/pull/11363))
- Fix unnecessary SQL query performed on unauthenticated requests ([Gargron](https://github.com/tootsuite/mastodon/pull/11179))
- Fix incorrect timestamp displayed on featured tags ([Kjwon15](https://github.com/tootsuite/mastodon/pull/11477))
- Fix privacy dropdown active state when dropdown is placed on top of it ([ThibG](https://github.com/tootsuite/mastodon/pull/11495))
- Fix filters not being applied to poll options ([ThibG](https://github.com/tootsuite/mastodon/pull/11174))
- Fix keyboard navigation on various dropdowns ([ThibG](https://github.com/tootsuite/mastodon/pull/11511), [ThibG](https://github.com/tootsuite/mastodon/pull/11492), [ThibG](https://github.com/tootsuite/mastodon/pull/11491))
- Fix keyboard navigation in modals ([ThibG](https://github.com/tootsuite/mastodon/pull/11493))
- Fix image conversation being non-deterministic due to timestamps ([Gargron](https://github.com/tootsuite/mastodon/pull/11408))
- Fix web UI performance ([ThibG](https://github.com/tootsuite/mastodon/pull/11211), [ThibG](https://github.com/tootsuite/mastodon/pull/11234))
- Fix scrolling to compose form when not necessary in web UI ([ThibG](https://github.com/tootsuite/mastodon/pull/11246), [ThibG](https://github.com/tootsuite/mastodon/pull/11182))
- Fix save button being enabled when list title is empty in web UI ([ThibG](https://github.com/tootsuite/mastodon/pull/11475))
- Fix poll expiration not being pre-filled on delete & redraft in web UI ([ThibG](https://github.com/tootsuite/mastodon/pull/11203))
- Fix content warning sometimes being set when not requested in web UI ([ThibG](https://github.com/tootsuite/mastodon/pull/11206))

### Security

- Fix invites not being disabled upon account suspension ([ThibG](https://github.com/tootsuite/mastodon/pull/11412))
- Fix blocked domains still being able to fill database with account records ([Gargron](https://github.com/tootsuite/mastodon/pull/11219))

## [2.9.2] - 2019-06-22
### Added

- Add `short_description` and `approval_required` to `GET /api/v1/instance` ([Gargron](https://github.com/tootsuite/mastodon/pull/11146))

### Changed

- Change camera icon to paperclip icon in upload form ([koyuawsmbrtn](https://github.com/tootsuite/mastodon/pull/11149))

### Fixed

- Fix audio-only OGG and WebM files not being processed as such ([Gargron](https://github.com/tootsuite/mastodon/pull/11151))
- Fix audio not being downloaded from remote servers ([Gargron](https://github.com/tootsuite/mastodon/pull/11145))

## [2.9.1] - 2019-06-22
### Added

- Add moderation API ([Gargron](https://github.com/tootsuite/mastodon/pull/9387))
- Add audio uploads ([Gargron](https://github.com/tootsuite/mastodon/pull/11123), [Gargron](https://github.com/tootsuite/mastodon/pull/11141))

### Changed

- Change domain blocks to automatically support subdomains ([Gargron](https://github.com/tootsuite/mastodon/pull/11138))
- Change Nanobox configuration to bring it up to date ([danhunsaker](https://github.com/tootsuite/mastodon/pull/11083))

### Removed

- Remove expensive counters from federation page in admin UI ([Gargron](https://github.com/tootsuite/mastodon/pull/11139))

### Fixed

- Fix converted media being saved with original extension and mime type ([Gargron](https://github.com/tootsuite/mastodon/pull/11130))
- Fix layout of identity proofs settings ([acid-chicken](https://github.com/tootsuite/mastodon/pull/11126))
- Fix active scope only returning suspended users ([ThibG](https://github.com/tootsuite/mastodon/pull/11111))
- Fix sanitizer making block level elements unreadable ([Gargron](https://github.com/tootsuite/mastodon/pull/10836))
- Fix label for site theme not being translated in admin UI ([palindromordnilap](https://github.com/tootsuite/mastodon/pull/11121))
- Fix statuses not being filtered irreversibly in web UI under some circumstances ([ThibG](https://github.com/tootsuite/mastodon/pull/11113))
- Fix scrolling behaviour in compose form ([ThibG](https://github.com/tootsuite/mastodon/pull/11093))

## [2.9.0] - 2019-06-13
### Added

- **Add single-column mode in web UI** ([Gargron](https://github.com/tootsuite/mastodon/pull/10807), [Gargron](https://github.com/tootsuite/mastodon/pull/10848), [Gargron](https://github.com/tootsuite/mastodon/pull/11003), [Gargron](https://github.com/tootsuite/mastodon/pull/10961), [Hanage999](https://github.com/tootsuite/mastodon/pull/10915), [noellabo](https://github.com/tootsuite/mastodon/pull/10917), [abcang](https://github.com/tootsuite/mastodon/pull/10859), [Gargron](https://github.com/tootsuite/mastodon/pull/10820), [Gargron](https://github.com/tootsuite/mastodon/pull/10835), [Gargron](https://github.com/tootsuite/mastodon/pull/10809), [Gargron](https://github.com/tootsuite/mastodon/pull/10963), [noellabo](https://github.com/tootsuite/mastodon/pull/10883), [Hanage999](https://github.com/tootsuite/mastodon/pull/10839))
- Add waiting time to the list of pending accounts in admin UI ([Gargron](https://github.com/tootsuite/mastodon/pull/10985))
- Add a keyboard shortcut to hide/show media in web UI ([ThibG](https://github.com/tootsuite/mastodon/pull/10647), [Gargron](https://github.com/tootsuite/mastodon/pull/10838), [ThibG](https://github.com/tootsuite/mastodon/pull/10872))
- Add `account_id` param to `GET /api/v1/notifications` ([pwoolcoc](https://github.com/tootsuite/mastodon/pull/10796))
- Add confirmation modal for unboosting toots in web UI ([aurelien-reeves](https://github.com/tootsuite/mastodon/pull/10287))
- Add emoji suggestions to content warning and poll option fields in web UI ([ThibG](https://github.com/tootsuite/mastodon/pull/10555))
- Add `source` attribute to response of `DELETE /api/v1/statuses/:id` ([ThibG](https://github.com/tootsuite/mastodon/pull/10669))
- Add some caching for HTML versions of public status pages ([ThibG](https://github.com/tootsuite/mastodon/pull/10701))
- Add button to conveniently copy OAuth code ([ThibG](https://github.com/tootsuite/mastodon/pull/11065))

[README file]: ./README.md

## Pre-Release 0.1.2 [2019-08-18 / v0.0.1.2]

This release fixes a bug from 0.1.1 before the 0.2.0 release.

It doesn't add any upstream changes, and is still based off of [Mastodon 2.9.0] plus the commits
up to [65efe892cf].

### Fixed

* Toot and biography lengths are offered as integers in the API instead of strings
    * Thanks to [mthld] and [DagAgren] for finding the bug
    * Thanks to [1011X] for the fix

[mthld]: https://github.com/mthld
[DagAgren]: https://github.com/DagAgren

## Pre-Release 0.1.1 [2019-07-28 / v0.0.1.1]

This release fixes a few bugs from 0.1.0 before the 0.2.0 release.

It doesn't add any upstream changes, and is still based off of [Mastodon 2.9.0] plus the commits
up to [65efe892cf].

### Fixed

* Toot and biography lengths are now on /api/v1/instance API, for better app integration
    * Thanks to [ElliotBerriot] for testing 0.1.0 and finding the bug
    * Thanks to [1011X] for the fix
* Toot and biography lengths can actually be saved in the admin UI
    * Thanks to [ElliotBerriot] for testing 0.1.0 and finding the bug
    * Thanks to [clarfon] for the fix
* All of the code has been fixed to include the proper project URL and docker image
    * Thanks to [ElliotBerriot] for debugging 0.1.0 and finding the errors with the Docker files
    * Thanks to [clarfon] for the fix
* Broadcasted version has been reverted to the Mastodon version, so that mastodon.py and other
  libraries work until we find a better solution
    * Thanks to [Frinkel] for testing 0.1.0 and finding the bug
    * Thanks to [halcy] for providing insight into how mastodon.py works
    * Thanks to [1011X] for the fix
* Blocking entire instance domains now gives a less judgmental message in the English locale
    * Thanks to [TrechNex] for the fix
    * Thanks to [mal0ki] and [clarfon] for reviewing the wording
* Florence-specific settings have been translated into Dutch
    * Thanks to [rscmbbng] for the translations
* The [lastest typo] in the README was corrected
    * Thanks to [ciderpunx] for the fix
* A few dependencies were updated to fix various security issues
    * Prototype pollution vulnerabilities were fixed for handlebars and lodash
    * Thanks to [1011X] for future-proofing CVE-2015-9284 (OAuth vulnerability)

[lastest typo]: https://github.com/florence-social/mastodon-fork/pull/106/files

[ciderpunx]: https://github.com/ciderpunx
[ElliotBerriot]: https://github.com/ElliotBerriot
[Frinkel]: https://github.com/Frinkel
[halcy]: https://github.com/halcy
[mal0ki]: https://github.com/mal0ki
[rscmbbng]: https://github.com/rscmbbng
[TrechNex]: https://github.com/TrechNex

### Special Thanks

* Thank you to everyone who jumped on the Florence train and set up their own instances! We'll try
  and compile a list of Florence Mastodon instances some time before the next release.
* Thank you to @TrechNex for helping set up [installation instructions] on his website!

[installation instructions]: https://bobbymoss.com/index.html#install-florence-prerelease

## Pre-Release 0.1.0 [2019-06-18 / v0.0.1.0]

This release is based off of [Mastodon 2.9.0] plus the commits up to [65efe892cf].

[Mastodon 2.9.0]: https://github.com/tootsuite/mastodon/blob/v2.9.0/CHANGELOG.md
[65efe892cf]: https://github.com/tootsuite/mastodon/compare/c9eeb2e832b5b36a86028bbec7a353c32be510a7..65efe892cf56cd4f998de885bccc36e9231d8144

### Added

* Toot length can now be configured by an admin; default is 500
    * Thanks to glitch.social and many other forks for the original code
    * Thanks to [usbsnowcrash] for the Florence-specific code
    * Thanks to [m4sk1n] for the Polish translation
    * Thanks to [clarfon] and [Feufochmar] for the French translation
    * Thanks to [1011X] and [skrlet13] for the Spanish translation
* Biography length can now be configured by an admin; default is 500
    * Thanks to glitch.social and many other forks for the original code
    * Thanks to [usbsnowcrash] for the Florence-specific code
    * Thanks to [clarfon] and [Feufochmar] for the French translation
    * Thanks to [1011X] and [skrlet13] for the Spanish translation
* Users can choose whether to receive DMs on the home timeline in their settings
    * Thanks to glitch.social and many other forks for the original code
    * Thanks to [usbsnowcrash] for the Florence-specific code
    * Thanks to [clarfon] and [Feufochmar] for the French translation
    * Thanks to [1011X] and [skrlet13] for the Spanish translation
* Spanish translations were updated to be more formal
    * Thanks to [1011X] for the inital changes
    * Thanks to [skrlet13] for offering feedback and further changes

[1011X]: https://github.com/1011X
[clarfon]: https://github.com/clarfon
[Feufochmar]: https://github.com/Feufochmar
[m4sk1n]: https://github.com/m4sk1n
[skrlet13]: https://github.com/skrlet13
[usbsnowcrash]: https://github.com/usbsnowcrash

### Special Thanks

* Thank you to @1011x, @jhaye, @lightdark, @maloki, @skrlet13, @melody, @stolas, @hak, @mecaka:
  those who've been helping with governance, offering advice, and/or been working on this for the
  past few months.
* Thank you to @woozle for hosting both the Wiki and Mattermost for us on their servers.
* Thank you to all the forkers out there who are providing us both with inspiration, actual code,
  and conversation about how we can make the Fediverse a little bit better.
* Thank you to everyone that has been cheerleading us for the past year, helped us have the courage
  to "Fork Off" from Mastodon, and also understood that we are working towards different
  objectives. That is after all why you all joined us in the first place!
* Thank you to @mecaka who joined the team while @maloki was getting diagnosed, who helped push
  through that time and bring us to where we are now.
* An additional thank you to those that joined the Mattermost server to keep the conversation alive
  with us after we moved on from Discord!
