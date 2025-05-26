Rocksky now supports the **ListenBrainz API**, so you can use [Kodi](https://kodi.tv/)'s built-in ListenBrainz scrobbler to track your listening directly to Rocksky — no plugin modifications needed.

## Requirements
- Kodi media center installed
- A Rocksky account
- A Rocksky API Key from the [API Applications](https://rocksky.app/apikeys) page

## 1. Install the ListenBrainz Add-on in Kodi
1. Open Kodi
2. Go to **Add-ons > Install from repository**
3. Select **Kodi Add-on repository**
4. Navigate to **Service Add-ons**
5. Search for **ListenBrainz Scrobbler**
6. **Click Install**

Once installed, you'll see the plugin under **My Add-ons > Service Add-ons**


## 2. Configure the Plugin for Rocksky
1. Open the ListenBrainz plugin settings
2. Update the following:

**API URL**
Replace:
```
https://api.listenbrainz.org
```
With:
```
https://audioscrobbler.rocksky.app
```
**API Token**
1. Go to Rocksky [API Applications](https://rocksky.app/apikeys) page
2. Copy your API Key
3. Paste it into the Token field

✅ Save the settings and restart Kodi if needed.


![Screenshot from 2025-05-24 14-28-37.png](https://api.apidog.com/api/v1/projects/821757/resources/355406/image-preview)

## 3. Confirm It’s Working
- Play any song in Kodi
- Visit https://rocksky.app to see your recent scrobble