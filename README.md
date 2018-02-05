# yt2ipfs - re-host youtube videos on ipfs

> Please only use on videos you are allowed to download, such as your own or out of copyright.

## Install

- [install ipfs](https://ipfs.io/docs/install) (probably in your package manager)
- [install youtube-dl](https://github.com/rg3/youtube-dl#installation) (probably in your package manager)
- run `ipfs daemon` in the background
- place `yt2ipfs` in your `$PATH` somewhere
- test with `yt2ipfs -h`

## Usage

```
> yt2ipfs --help
yt2ipfs [--api <ipfs-api-url>] <youtube-id-or-link>
```

## Examples

### Download a link

```
yt2ipfs https://www.youtube.com/watch?v=vyRZBeMtkrA
```

### Just the youtube id

```
yt2ipfs vyRZBeMtkrA
```

### Use another ipfs API

```
yt2ipfs --api /ip4/127.0.0.1/tcp/9096 https://www.youtube.com/watch?v=vyRZBeMtkrA
```

## LICENSE

MIT
