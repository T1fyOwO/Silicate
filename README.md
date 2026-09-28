# Silicate

![Silicate](https://raw.githubusercontent.com/T1fyOwO/Silicate/main/logo.png)

Silicate is a Geometry Dash bot focused on gameplay assistance, replay tools, trajectory simulation, rendering, and other utilities.

> This repository is an unofficial GitHub and mobile port of Silicate.

## Platform Support

| Platform | Geometry Dash | Status |
| --- | --- | --- |
| Windows x64 | 2.2081 | 🟡 Porting |
| Android64 | 2.2081 | 🟡 Porting |
| Android32 | 2.2081 | 🟡 Porting |

Silicate targets **Geode 5.10.1** and is being prepared for automated builds through **GitHub Actions**.

## Features

- Bot and replay functionality
- Autoclicker
- Hitboxes
- Trajectory simulation
- Geometry Dash physics simulation
- Checkpoint and practice utilities
- Rendering and recording
- Replay management
- Custom UI and themes
- On-screen labels
- Configurable settings

## Mobile Port

The original Silicate project contains platform-specific Windows functionality.

This port aims to support:

- Windows x64
- Android64
- Android32

Windows-specific functionality will be separated or replaced where necessary so that it does not prevent Android builds from compiling.

Some features may require additional work before they are fully functional on Android.

## Building

### Requirements

- [Geode SDK](https://github.com/geode-sdk/geode)
- CMake 3.21 or newer
- Ninja
- A compatible C++ compiler
- Geometry Dash 2.2081

### Windows

Run:

```bat
build.bat
```

For a release build:

```bat
build-rel.bat
```

### Linux

Run:

```bash
./build.sh
```

## GitHub Actions

The repository uses GitHub Actions for automated builds.

The intended build targets are:

- Windows x64
- Android64
- Android32

GitHub Actions helps detect platform-specific compilation problems and keeps the build process reproducible.

## Project Structure

```text
Silicate/
├── .github/
│   └── workflows/
│       └── build.yml
├── include/
├── resources/
├── src/
│   ├── assist/
│   ├── bot/
│   ├── checkpoint/
│   ├── hooks/
│   ├── label/
│   ├── physics/
│   ├── render/
│   ├── replay/
│   ├── trajectory/
│   ├── ui/
│   └── util/
├── CMakeLists.txt
├── LICENSE
├── README.md
└── mod.json
```

## Dependencies

Silicate uses several external libraries and projects, including:

- [Tabby](https://github.com/silicate-bot/tabby)
- [Glaze](https://github.com/stephenberry/glaze)
- [Zydis](https://github.com/zyantific/zydis)
- [SafetyHook](https://github.com/cursey/safetyhook)
- SLC
- [Geode](https://github.com/geode-sdk/geode)

## Development

Contributions and testing are welcome.

When contributing:

1. Create a branch for your changes.
2. Keep changes focused.
3. Follow the existing coding style.
4. Test the code you changed.
5. Test related functionality when possible.
6. Make sure the GitHub Actions build still passes.

## Port Status

This is an active porting project.

### Windows

- [ ] Restore the complete source tree
- [ ] Restore required resources
- [ ] Configure GitHub Actions
- [ ] Verify compilation
- [ ] Test the resulting Geode mod

### Android64

- [ ] Restore the complete source tree
- [ ] Resolve Android compilation issues
- [ ] Replace Windows-only APIs
- [ ] Resolve platform-specific rendering code
- [ ] Build successfully
- [ ] Test on a real Android device

### Android32

- [ ] Resolve Android32-specific compilation issues
- [ ] Replace unsupported platform APIs
- [ ] Build successfully
- [ ] Test on a real Android device

## Known Porting Challenges

The original build configuration contains platform-specific functionality, including Windows APIs and Windows/OpenGL-related dependencies.

The Android port therefore requires more than changing the supported platform list in `mod.json`.

The goal is to keep the core Silicate functionality shared between platforms while isolating code that must behave differently on Windows and Android.

## Links

- [Silicate GitHub Repository](https://github.com/T1fyOwO/Silicate)
- [Original Silicate Source](https://git.puppy.lgbt/silicate/silicate)
- [Geode](https://geode-sdk.org/)
- [Geode SDK](https://github.com/geode-sdk/geode)

## License

See [LICENSE](LICENSE) for the license applicable to this repository.
