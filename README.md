# Whist - Audio Cleaner

[Open Whist](https://whist.tirnarogue.com/) or open `public/index.html` directly for offline use. Select a local audio file, render a cleanup preview, then compare the versions and export a 24-bit WAV.

Whist processes audio in a browser worker. Cloudflare serves the app files. Recordings and exports stay on the device.

## Deploy

Use Cloudflare CLI `1.0.0-rc.2` or newer with a supported Node.js version. Authenticate to the Cloudflare account that owns `tirnarogue.com`, then run from the repository root:

```sh
cf deploy ./public --dry-run
cf deploy ./public
```

The static deployment reads `cloudflare.config.ts` and serves only `public/`.
