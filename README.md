# vuplay THEOplayer

## Description

This repo will demonstrate how to use [vudrm](http://vudrm.vualto.com/) with [THEOplayer](https://www.theoplayer.com/).
If you have any questions please contact support@vualto.com

This repo is currently targeted at THEOplayer version 2.51.1

## Instructions

### Install dependencies

1. Install [npm](https://www.npmjs.com/)
2. Install the [grunt-cli](https://www.npmjs.com/package/grunt-cli): `npm install -g grunt-cli`
3. Clone the repo: `git clone git@github.com:Vualto/vuplay-theoplayer.git`
4. Navigate to the project's root folder: `cd vuplay-theoplayer`
5. Install the dependencies: `npm install`

### Build and run the dev environment

1. Open the repo in your favourite javascript editor.
2. In file `src/vuplay.js` replace `<your-stream-url>` with your stream url. This must can be a [MPEG-DASH](https://en.wikipedia.org/wiki/Dynamic_Adaptive_Streaming_over_HTTP) or [HLS](https://developer.apple.com/streaming/) stream.
3. In file `src/vuplay.js` replace `<your-vudrm-token>` with a vudrm token from [https://admin.drm.technology](https://admin.drm.technology)
4. Run `grunt build` in the project's root. This will create a `dist` folder that contains all the files need to run this demo.
5. Run `grunt serve`, this will run the build task from the previous step and start a development node.js server. This server is not suitable for production.
6. Load a supported browser and go to `http://theoplayer.vuplay.local.drm.technology:14703`
    - You will need to add the host `theoplayer.vuplay.local.drm.technology` to your local machine's hosts file in order for this to work. 
    
NB: Adding the argument `--debug` to `grunt build` or `grunt serve` will load the unminified vuplay code.

### Browser support

The browser must support [encrypted media extensions](https://www.w3.org/TR/2016/CR-encrypted-media-20160705/).
Currently this includes the latest versions of Chrome, Firefox, Internet Explorer 11, Edge and Safari.
For a complete breakdown of supported media extensions please contact support@vualto.com

## Useful links

### vudrm

- [Contact vualto](http://www.vualto.com/contact-us/)
- [vudrm](http://vudrm.vualto.com/)
- [vudrm token documentation](http://readme.drm.technology/vudrm/VuDrmTokenIntegration/)

### mpeg-DASH

- [MPEG-DASH](https://en.wikipedia.org/wiki/Dynamic_Adaptive_Streaming_over_HTTP)
- [What is MPEG-DASH](http://www.streamingmedia.com/Articles/Editorial/What-Is-.../What-is-MPEG-DASH-79041.aspx)

### HLS

- [Apple's developer resources on HLS](https://developer.apple.com/streaming/)
- [HLS wikipedia](https://en.wikipedia.org/wiki/HTTP_Live_Streaming)
- [What is HLS?](http://www.streamingmedia.com/Articles/Editorial/What-Is-.../What-is-HLS-(HTTP-Live-Streaming)-78221.aspx)

### Encrpyted media extensions

- [Encrypted media extensions specification](https://www.w3.org/TR/2016/CR-encrypted-media-20160705/)
- [Encrypted media extensions wikipedia](https://en.wikipedia.org/wiki/Encrypted_Media_Extensions)
- [Encrypted media extensions on MDN](https://developer.mozilla.org/en-US/docs/Web/API/Encrypted_Media_Extensions_API)
- [Intro to encrypted media extensions](https://www.html5rocks.com/en/tutorials/eme/basics/)

### THEOplayer

- [THEOplayer](http://dashif.org/)
- [Online documentation for this version](https://support.theoplayer.com/hc/en-us/sections/203124169)

### Build tools

- [npm](https://www.npmjs.com/)
- [grunt](http://gruntjs.com/)