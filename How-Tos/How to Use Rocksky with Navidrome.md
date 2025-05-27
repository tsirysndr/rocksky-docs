Rocksky now provides a **ListenBrainz-compatible scrobbling API**, allowing you to use Rocksky natively in Navidrome!
## Requirements

- A running Navidrome server
- A Rocksky account
- A Rocksky API Key from the [API Applications](https://rocksky.app/apikeys) page

## 1. Enable scrobbling to ListenBrainz in Navidrome

Update your Navidrome configuration and add the following:

```
ListenBrainz.Enabled = true
```

Alternatively, if you are using environment variables:

```
ND_LISTENBRAINZ_ENABLED=true
```

## 2. Configure the ListenBrainz API URL to Use Rocksky

Update the default ListenBrainz API URL:

```
ListenBrainz.BaseURL = "https://audioscrobbler.rocksky.app/1/"
```

Alternatively, if you are using environment variables:

```
ND_LISTENBRAINZ_BASEURL=https://audioscrobbler.rocksky.app/1/
```

## 3. API Token:
1. Go to Rocksky [API Applications](https://rocksky.app/apikeys)
2. Create or copy your API Key
3. Go to Profile on Navidromme, and toggle "Scrobble to
   ListenBrainz"
4. Paste the API key into the text field

Navidrome will now begin scrobbling to Rocksky!

## 4. Verify It’s Working

Start playing a track on Navidrome
Head to https://rocksky.app — your recent scrobbles should appear in real time. You might have to play through some portion of the track before Navidrome sends the scrobble data to Rocksky.
