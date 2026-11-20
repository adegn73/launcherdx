# LauncherDX

**Driving Xperience**

LauncherDX is a personal Android launcher, built as a fork of [Lawnchair](https://github.com/LawnchairLauncher/lawnchair) with a few extra features layered on top. It is not affiliated with or endorsed by the Lawnchair project.

## What's different from Lawnchair

- **Driving Mode** - a fullscreen, car-friendly dashboard that activates automatically when your phone connects to your car's Bluetooth, with a customizable grid of shortcuts, a speedometer, and an optional "Stay awake" setting to keep the screen on while it's showing.
- **Home screen lock** - lock your layout from the long-press menu to stop accidental drags, deletes, or taps. Locking is instant; unlocking requires confirming your device's screen lock (biometric, PIN, pattern, or password) first, so it can't be undone by accident either.
- **Hide LauncherDX activities from Recents** - an opt-in setting to keep this launcher's own screens (including a stray entry that could otherwise resurface after "Clear all") out of the system Recents/Overview list.
- **Paged app drawer** - an alternative "Drawer style" that lays the app drawer out as swipeable grid pages instead of one continuously scrolling list, mirroring how the home screen itself pages between screens (including its own background image with matching parallax).
- A handful of smaller fixes carried over from the Lawnchair codebase this is built on (backup/restore coverage, widget corner-radius handling, and others).

Everything else - Material You theming, icon packs, search, grid customization, and so on - comes from Lawnchair itself. See the [upstream Lawnchair README](https://github.com/LawnchairLauncher/lawnchair#readme) for the full feature set this is built on.

## Download

Signed release builds are published under [Releases](https://github.com/adegn73/launcherdx/releases). The APK is self-signed; it installs as its own separate app (`dev.adegn73.launcherdx`) alongside Lawnchair or any other launcher you have installed, and works well with [Obtainium](https://github.com/ImranR98/Obtainium) for update checks.

## Building

This project uses the same Gradle-based build as Lawnchair. The LauncherDX variant is the `launcherdx` product flavor combined with the `lawnWithQuickstep` flavors, e.g.:

```
./gradlew :assembleLawnWithQuickstepLauncherdxRelease
```

A release build needs its own `keystore.properties` at the repository root (see Lawnchair's own build scripts for the expected format); without one, it falls back to debug signing.

## License

Licensed under the Apache License, Version 2.0, same as the Lawnchair and AOSP Launcher3 code it's built on. See [LICENSE.txt](LICENSE.txt).
