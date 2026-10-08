# Pitchora landing page

This directory is a standalone static export of Pitchora's current landing page.
It does not require PHP, Laravel, React, npm, or a build command.

## Deploy to Vercel

Upload or import this directory as the Vercel project root. Leave the framework
preset as **Other** and leave the build command empty. Vercel will serve
`index.html` directly.

## Connect the Laravel application later

The Log in and Start free links currently use `/login` and `/register` on the
same domain. When the Laravel application has its own domain, open `index.html`
and set `appUrl` near the beginning of the final inline script:

```js
const appUrl = 'https://app.pitchora.com';
```

All links marked with `data-app-path` will then point to the Laravel app.
