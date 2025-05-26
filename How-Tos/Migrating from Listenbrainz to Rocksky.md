Rocksky now supports a **ListenBrainz-compatible API** for scrobbling! This means you can switch your existing [ListenBrainz](https://listenbrainz.org) integration to Rocksky in just a few simple steps.

## What You Need
 - A Rocksky account
 - A Rocksky API Key (you can generate one in the [API Applications](https://rocksky.app/apikeys) page)
 - A scrobbling app or script that supports the ListenBrainz API

## Step-by-Step Migration
### 1. Update the API URL
Change the ListenBrainz API endpoint:

From:

```
https://api.listenbrainz.org
```
To:

```
https://audioscrobbler.rocksky.app
```

### 2. Replace the Authorization Token
In ListenBrainz, you typically send a `Authorization: Token <token>` header.
To switch to Rocksky:
- Go to Rocksky [API Applications](https://rocksky.app/apikeys)
- Copy your API Key
- Use it as the token in the Authorization header:

```
Authorization: Token <rocksky_api_key>
```

### 3. Test the Integration
Try sending a test scrobble to:

```
POST https://audioscrobbler.rocksky.app/1/submit-listens
Content-Type: application/json
Authorization: Token <rocksky_api_key>
```

Example body:
```json
{
  "listen_type": "playing_now",
  "payload": [
    {
      "track_metadata": {
        "artist_name": "Daft Punk",
        "track_name": "Harder, Better, Faster, Stronger",
        "release_name": "Discovery"
      },
      "listened_at": 1716541200
    }
  ]
}
```

## Notes
- **Compatibility:** Rocksky mirrors the ListenBrainz API behavior for scrobbling (`/submit-listens, /validate-token`).


- **Normalization**: Rocksky will attempt to normalize song metadata. If a match cannot be found, the scrobble may be skipped.

