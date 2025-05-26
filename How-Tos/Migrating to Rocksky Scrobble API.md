Rocksky offers a fully compatible implementation of the [Last.fm Audioscrobbler API](https://www.last.fm/api/show/track.scrobble) — so you can seamlessly migrate your scrobbling apps or integrations to Rocksky by simply changing the API endpoint and credentials.

## Base URL

Replace the Last.fm endpoint:

```
https://ws.audioscrobbler.com/2.0
```

With the Rocksky scrobble endpoint:

```
https://audioscrobbler.rocksky.app/2.0
```

## Authentication

- `api_key`: Your Rocksky API key (obtainable from your [Rocksky developer dashboard](https://rocksky.app/apikeys)).
- `sk`: Your Rocksky session key (obtained after user authentication `rocksky login`)

## Legacy Last.fm API Compatibility
Rocksky also supports older Last.fm clients using the legacy Audioscrobbler protocol (pre-2.0). You can use these legacy configurations in clients such as Deadbeef or older music players:

### Legacy API Config:

| **Field**	| **Value** |
|---------------|-----------|
| Username	| Your Rocksky API key (obtainable from your [Rocksky developer dashboard](https://rocksky.app/apikeys)) |
| Password	| Your Rocksky shared secret (obtainable from your [Rocksky developer dashboard](https://rocksky.app/apikeys)) |
| Scrobble URL	| https://audioscrobbler.rocksky.app |

ℹ️ **Note**: Rocksky will also try to normalize songs metadata. If it cannot find a matching track, it will skip the scrobble.

## Example Scrobble Request

**Method**: `POST`
**URL**: `https://audioscrobbler.rocksky.app/2.0`
**Headers**: `Content-Type: application/x-www-form-urlencoded`
**Body** (as `x-www-form-urlencoded`):


| **Parameter** | **Example Value**                  |
|---------------|------------------------------------|
| method        | `track.scrobble`                   |
| api_key       | `YOUR_API_KEY`                     |
| sk            | `YOUR_SESSION_KEY`                 |
| artist[0]     | `Radiohead`                        |
| track[0]      | `Karma Police`                     |
| timestamp[0]  | `1744579159`                       |
| api_sig       | `532b7492411fdfcd79639b548b5ee8a8` |
| format        | `json`                             |

## Generating `api_sig`
To compute the signature:
1. Sort all parameters (excluding api_sig and format) by key.
2. Concatenate key-value pairs (key1value1key2value2...).
3. Append your shared secret to the concatenated string.
4. MD5 hash the result.

Example in pseudo-code:

```js
const base = "api_keyAPI_KEYartist[0]Radioheadmethodtrack.scrobbleskSESSION_KEYtimestamp[0]1744579159track[0]Karma Police";
const sig = md5(base + shared_secret);
```

## Migrating Your App
To switch from Last.fm to Rocksky:
1. Change the API base URL.
2. Update your API key and session key (from `rocksky login`).
3. Use the same payload format and signature method.
4. Done!

## Why Switch to Rocksky?
🔄 Open Scrobble Infrastructure
📊 Modern analytics and detailed stats
🔐 Built on top of [AT Protocol](https://atproto.com/) for portability
🔧 Compatible with existing Last.fm tools