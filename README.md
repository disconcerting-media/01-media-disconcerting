# create-svelte

Everything you need to build a Svelte project, powered by [`create-svelte`](https://github.com/sveltejs/kit/tree/master/packages/create-svelte);

## Creating a project

If you're seeing this, you've probably already done this step. Congrats!

```bash
# create a new project in the current directory
npm init svelte@next

# create a new project in my-app
npm init svelte@next my-app
```

> Note: the `@next` is temporary

## Developing

Once you've created a project and installed dependencies with `npm install` (or `pnpm install` or `yarn`), start a development server:

```bash
npm run dev

# or start the server and open the app in a new browser tab
npm run dev -- --open
```

## Building

Before creating a production version of your app, install an [adapter](https://kit.svelte.dev/docs#adapters) for your target environment. 

To build and deploy to one's own virtual machine, e.g., Google Cloud Platform GCE, follow the official instructions and if still confused take a look at this issue on github: https://github.com/sveltejs/kit/issues/2115 "give an option for default host and port when building with adapter-node #2115"

Also, take a look at this stackoverflow q&a:  https://stackoverflow.com/questions/70398935/how-to-deploy-a-svelte-kit-app-after-build-using-nginx-as-web-server/70571992#70571992

The key is to add the environmental variables in svelte.config.js, run the build locally without specifying any port or host, then once on the remote machine, use the PM2 start command preceded by HOST=localhost PORT=4000 (or whatever), and then add that port to the Nginx conf file.  

Then:

```bash
npm run build
```

> You can preview the built app with `npm run preview`, regardless of whether you installed an adapter. This should _not_ be used to serve your app in production.
# sveltekit
