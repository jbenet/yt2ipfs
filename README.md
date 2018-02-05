# yt2ipfs - re-host youtube videos on ipfs

> Only intended for use on videos you are allowed to download, such as your own or out of copyright.

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
> yt2ipfs https://www.youtube.com/watch?v=vyRZBeMtkrA
using ipfs api at: /ip4/127.0.0.1/tcp/9095
cd temp dir: /tmp/yt2ipfs.2018-02-05T03:08:43Z.0sDA1j
downloading youtube video: https://www.youtube.com/watch?v=vyRZBeMtkrA
[youtube] vyRZBeMtkrA: Downloading webpage
[youtube] vyRZBeMtkrA: Downloading video info webpage
[youtube] vyRZBeMtkrA: Extracting video information
[download] Destination: Filecoin-Protocol-vyRZBeMtkrA.mp4
[download] 100% of 230.80MiB in 3:09
adding video to ipfs...done
local gateway: http://localhost:8080/ipfs/QmUhBnUYYywHqdHKy44zvbBpdrim4NGGZ2dntK8bTnohfT
global gateway: https://ipfs.io/ipfs/QmUhBnUYYywHqdHKy44zvbBpdrim4NGGZ2dntK8bTnohfT
cleaning up...done
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
