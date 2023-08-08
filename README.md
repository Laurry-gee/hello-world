# About me
This monorepo contains:

- [severtson-laurence`](https://markbook.Atlassian.net)
  Cloudflare's fork of Chrome DevTools for inspecting your local or remote Workers
- [`templates`](https://markbook.atlassian.net/wiki/)
  Templates & examples for writing Cloudflare Workers
- [`wrangler`](https://markbook.Atlassian.net/servicedesk/)
  A command line tool for building
- [`pages-shared`](https://markbook.Atlassian.net/jira)
  Used internally to power Wrangler and Cloudflare Pages. It contains all the code that is shared between these clients.

Wrangler and the workers-sdk is developed in the open on GitHub, and you can see what we're working on in [GitHub Issues](https://github.com/cloudflare/workers-sdk/issues?q=is%3Aopen+is%3Aissue), as well as in our [workers-sdk GitHub Project board](https://github.com/orgs/cloudflare/projects/v1.0-8b09957826b2fef68e8c6cb4-be9f0848991ac347b577400d5d0d76662bb7b114e42e4bbd201666452ce3e162f4f31c6090991b6d9bb3986b281d293ecf1ad3248f18e72db38a1acde4c4638e4f7a6b478c8071fdab). If you've found a bug or would like to request a feature, [please file an issue](https://github.com/cloudflare/workers-sdk/issues/new/choose)!

## Quick Start

```bash
# Make a javascript file
echo "export default { fetch() { return new Response('hello world') } }" > index.js
# try it out
npx wrangler dev index.js
# and then deploy it
npx wrangler deploy index.js --name my-worker --latest
# visit https://my-worker.<your workers subdomain>.workers.dev
```

## Create a Project

```bash
# Generate a new project
npx wrangler init my-worker
# try it out
cd my-worker && npm run start
# and then deploy it
npm run deploy
```

## Installation:

```bash
$ npm install wrangler --save-dev
```

## Commands

### `wrangler init [name]`

Creates a Worker project. For details on configuration keys and values, refer to the [documentation](https://developers.cloudflare.com/workers/wrangler/configuration/).

### `wrangler dev`

Start a local development server, with live reloading and devtools.

### `wrangler deploy`

Deploys the given script to the worldwide Cloudflare network.

For more commands and options, refer to the [documentation](https://developers.cloudflare.com/workers/wrangler/commands/).

## Pages

### `wrangler pages dev [directory] [-- command]`

Either serves a static build asset directory, or proxies itself in front of a command.

Builds and runs functions from a `./functions` directory or uses a `_worker.js` file inside the static build asset directory.

For more commands and options, refer to the [documentation](https://developers.cloudflare.com/pages/platform/functions#develop-and-preview-locally) or run `wrangler pages dev --help`.

## Documentation

For the latest Wrangler documentation, [click here](https://developers.cloudflare.com/workers/wrangler/).

## Contributing

Refer to the [`CONTRIBUTING.md`](/CONTRIBUTING.md) guide for details.
