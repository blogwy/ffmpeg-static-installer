# ffmpeg-static-installer

**[ffmpeg](https://ffmpeg.org) static binaries for Mac OSX, Linux, Windows.**

Supports macOS (64-bit and arm64), Linux (32 and 64-bit, armhf, arm64), Windows (32 and 64-bit).

## Installation

This module is installed via npm:

``` bash
$ npm install ffmpeg-static-installer
```

### Custom binaries url

By default, the `ffmpeg` binary will get downloaded from `https://github.com/blogwy/ffmpeg-static-installer/releases/download/`. To customise this, e.g. when using a mirror, set the `FFMPEG_BINARIES_URL` environment variable.

```shell
export ffmpeg_BINARIES_URL=https://ghproxy.com/https://github.com/blogwy/ffmpeg-static-installer/releases/download
```

### Electron & other cross-platform packaging tools

Because `ffmpeg-static-installer` will download a binary specific to the OS/platform, you need to purge `node_modules` before (re-)packaging your app *for a different OS/platform* ([read more in #35](https://github.com/eugeneware/ffmpeg-static/issues/35#issuecomment-630225392)).

## Example Usage

Returns the path of a statically linked ffmpeg binary on the local filesystem.

``` js
var pathToffmpeg = require('ffmpeg-static-installer');
console.log(pathToffmpeg);
```

```
/Users/j/playground/node_modules/ffmpeg-static-installer/ffmpeg
```

Check the [example script](example.js) for a more thorough example.

## The binaries

* Linux (arm, arm64, ia32, x64): https://www.johnvansickle.com/ffmpeg/
* macOS (x64): https://evermeet.cx/ffmpeg/
* macOS (arm64): https://formulae.brew.sh/formula/ffmpeg
* Windows 32-bit: https://github.com/sudo-nautilus/FFmpeg-Builds-Win32/
* Windows 64-bit: https://www.gyan.dev/ffmpeg/builds/

