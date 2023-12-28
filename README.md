# nextjs-blog

## initiate project

```
$ brew install nodejs
$ npx create-next-app@latest --experimental-app
$ npm install -D @tailwindcss/typography postcss autoprefixer
```

Use `prose` class to apply styles that look good without accessing every element which we don't have access to.

## cloudflare compatibility

Cloudflare is not compatible with the default Node.js runtime, instead the Edge(https://nextjs.org/docs/app/building-your-application/rendering/edge-and-nodejs-runtimes) runtime needs to be used.

Here is there docs(https://developers.cloudflare.com/pages/framework-guides/deploy-a-nextjs-site/#deploy-via-the-cloudflare-dashboard).

```
$ npm install --save-dev @cloudflare/next-on-pages
```

Note that the `nodejs_compat` Compatibility Flag need to be added in the Pages Function settings(https://dash.cloudflare.com/3de13909f2f3b972382054bcbe7f371a/pages/view/nextjs-blog/settings/functions).