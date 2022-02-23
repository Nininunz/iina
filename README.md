<p align="center">
<img height="256" src="https://github.com/iina/iina/raw/master/iina/Assets.xcassets/AppIcon.appiconset/iina-icon-256.png" />
</p>

<h1 align="center">IINA+</h1>

<p align="center">IINA+ is a special build of the <b>modern</b> video player <a href="https://github.com/iina/iina">IINA</a> with additional features and bugfixes.</p>

---

## Features

* HDR playback
* Danmaku ( supports Bilibili only due to the limitation of `yt-dlp`, experimental ). I used some code from [iina-danmaku](https://github.com/xjbeta/iina-danmaku), Thanks [xjbeta](https://github.com/xjbeta)
* AppleScript. I used code from [Wevah's AppleScript support PR](https://github.com/iina/iina/pull/2857), Thanks [Wevah](https://github.com/Wevah)
* LOTS of bug fixes and performance improvements from [low-batt](https://github.com/iina-plus?type=source)

## Statement

IINA+ is built for experimenting the latest features and bugfixes. It may not be as stable as the official one and has a little bit higher os version requirement for quick development, which may not fit everyone's needs. Use it as your own risk.

## About youtube-dl

We no longer embed the outdated youtube-dl. Users must install `yt-dlp` manually for playing network resources.

```sh
$ brew install yt-dlp
```

See [the official document](https://github.com/yt-dlp/yt-dlp#readme) for detail

## Build

Full build of IINA dependencies and IINA itself:
```bash
$ make
```

Build just the dependencies:
```bash
$ make depends
```

Build IINA itself:
```bash
$ make build
```
  - Tips:
    - Change URL in the shell script if you want to download arch-specific binaries. By default, it will download the universal ones. You can download other binaries from `https://iina.io/dylibs/${ARCH}/fileList.txt` where `ARCH` can be `universal`, `arm64` and `x86_64`.
    - If you want to build an older IINA version, make sure to download the correponding dylibs. For example, `https://iina.io/dylibs/1.2.0/universal/fileList.txt`.

## Binaries

You may download prebuilt binaries on Github Action page: https://github.com/iina-plus/iina/actions

* Intel (x64): Artifacts named `IINA-x86_64` ( Requires 10.15+ )
* Apple M1 (aarch64): Artifacts named `IINA-arm64` ( Requires 12.0+ )
* No universal binaries available

## License

GPLv3
