You can scrobble your music to Rocksky using the Pano Scrobbler app by simply pointing it to Rocksky’s ListenBrainz-compatible API.


![Screenshot_20250530-120602.png](https://api.apidog.com/api/v1/projects/821757/resources/355712/image-preview)

## Prerequisites
- Android device with Pano Scrobbler installed
- A Rocksky account – sign up at rocksky.app
- API key from [API Applications](https://rocksky.app/apikeys) to be used as the authentication token

## Setup Instructions
1. **Open the Pano Scrobbler App** on your Android device.
2. **Go to Settings** → Scroll to **ListenBrainz** section.
3. **Enable ListenBrainz** (if not already enabled).
4. **Tap on “Custom server URL”** and enter:

```
https://audioscrobbler.rocksky.app
```

Enter your Rocksky API Key (from https://rocksky.app/apikeys) in the Authentication Token field.

Save and you're done!


![Screenshot_20250530-121124.png](https://api.apidog.com/api/v1/projects/821757/resources/355711/image-preview)

## You're All Set!
Start playing a track on your device
Head to https://rocksky.app — your recent scrobbles should appear in real time. You might have to play through some portion of the track before Pano Scrobbler sends the scrobble data to Rocksky.