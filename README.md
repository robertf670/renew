# Renew

Renew is an Android app that lists the recurring payments you type in, shows the monthly total, and reminds you before the next charge. The list stays on the phone. There is no bank login.

The product plan is in [renew.md](renew.md). Version history is in [CHANGELOG.md](CHANGELOG.md).

## Identity

| | |
| --- | --- |
| Android application id | `pro.ixrqq.renew` |
| Play developer account | `qqrxi` |
| Domain | [ixrqq.pro](https://www.ixrqq.pro/) |
| Store title | Renew: Payment Reminders |

`pro.ixrqq.renew` is the domain [ixrqq.pro](https://www.ixrqq.pro/) reversed, plus the app name. That is the same pattern as `com.netflix.ninja` (`netflix.com` reversed, then the app name). The id is permanent after the first Play upload.

## Status

Planning. No app code yet. The first build is described in [renew.md](renew.md).

## Versioning

Renew uses [semantic versions](https://semver.org/): `MAJOR.MINOR.PATCH`.

- `MAJOR` changes when a release breaks data the previous version saved on the phone.
- `MINOR` changes when a release adds behaviour people can see.
- `PATCH` changes for fixes only.

The git tag, the Android `versionName`, and the heading in `CHANGELOG.md` are the same string, with a `v` on the tag only (`v0.1.0`, version name `0.1.0`). Android `versionCode` is a whole number that goes up by 1 on every Play upload and never goes down.

Before a release:

1. Move the `[Unreleased]` notes in `CHANGELOG.md` under a dated version heading.
2. Set `versionName` to that version and increase `versionCode` by 1.
3. Commit.
4. Tag `vX.Y.Z` on that commit.
5. Upload that tag's build to Play.

Work that is not released yet stays under `[Unreleased]`.
