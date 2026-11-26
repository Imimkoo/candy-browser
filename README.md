# Ibrahim Browser

A personal Android browser built from the upstream [Candy Browser](https://github.com/sk2andy/candy-browser).

The goal is to keep the mature browser engine and its existing features, while applying a small, carefully tested set of Ibrahim Browser identity and usability changes. This repository is a fork; upstream code, third-party components, notices, and their licenses remain applicable.

## Current project status

- Upstream base: Candy Browser, branch `main`
- Custom work branch: `ibrahim-browser-customization`
- App display name: Ibrahim Browser
- Android package identity: isolated local/debug suffixes are configured so development builds can coexist with the upstream app.
- Browser engine and existing functionality: intentionally preserved.

## Build

The upstream project documents the Android SDK, JDK, Gradle tasks, supported build variants, signing, and dependency requirements in its documentation and workflow files. Start with the upstream build guide and use the local variant configured here:

```bash
./gradlew assembleFullDebug
./gradlew assembleFullLocalRelease
```

A signed release requires a release keystore configured locally. Never commit keystores, passwords, API keys, or signing credentials.

## Upstream and licensing

- Source project: https://github.com/sk2andy/candy-browser
- Upstream license: see [LICENSE](LICENSE) and [LICENSING.md](LICENSING.md).
- This fork does not replace or override upstream or third-party licenses. Review all notices before sharing or distributing builds.

## Planned work

1. Verify clean builds and installation on Android 14.
2. Confirm GeckoView and Firefox extensions, downloads, tabs, media playback, PiP, and background audio.
3. Finish launcher icon and visual identity.
4. Apply only high-value usability changes after testing the unmodified baseline.
5. Produce a verified APK only after a successful build and device-level smoke test.
