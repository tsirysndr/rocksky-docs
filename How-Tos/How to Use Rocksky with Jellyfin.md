Rocksky now provides a **ListenBrainz-compatible scrobbling API**, allowing you to use the existing ListenBrainz plugin for Jellyfin with zero code changes, just a config update!

## Requirements

- A running Jellyfin server
- A Rocksky account
- A Rocksky API Key from the [API Applications](https://rocksky.app/apikeys) page

## 1. Install the ListenBrainz Plugin for Jellyfin

Use the community-maintained plugin:

### Plugin Repository:
https://github.com/lyarenei/jellyfin-plugin-listenbrainz

Once installed, go to:
**Dashboard > Plugins > ListenBrainz > Settings**

## 2. Configure the Plugin to Use Rocksky

Update the default ListenBrainz API URL and token:

### API URL:

From:
```
https://api.listenbrainz.org
```

To:
```
https://audioscrobbler.rocksky.app
```

### API Token:
1. Go to Rocksky [API Applications](https://rocksky.app/apikeys)
2. Create or copy your API Key
3. Paste it into the Token field in the plugin settings

✅ Save and restart the server if needed.


![Screenshot from 2025-05-24 15-50-39.png](https://api.apidog.com/api/v1/projects/821757/resources/355405/image-preview)

## 3. Verify It’s Working
Start playing a track on Jellyfin
Head to https://rocksky.app — your recent scrobbles should appear in real time