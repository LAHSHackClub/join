# join.lahs.club

This repo uses [`create-svelte`](https://github.com/sveltejs/kit/tree/master/packages/create-svelte).

A static site for joining LAHS Hack Club. Flexible in onboarding steps and processes, currently accepts embedded or external resources.

[![DigitalOcean Referral Badge](https://web-platforms.sfo2.cdn.digitaloceanspaces.com/WWW/Badge%201.svg)](https://www.digitalocean.com/?refcode=3028e5d48317&utm_campaign=Referral_Invite&utm_medium=Referral_Program&utm_source=badge)

## Developing

```bash
npm install
npm run dev

# or start the server and open the app in a new browser tab
npm run dev -- --open
```

## Building

This repo is configured to use `@sveltejs/adapter-static`. Run the script below to generate a static site to be deployed.

```bash
npm run build
```

> You can preview the built app with `npm run preview`, regardless of whether you installed an adapter. This should _not_ be used to serve your app in production.
