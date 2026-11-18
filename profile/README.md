<p align="center">
  <a href="https://stagepass.one">
    <picture>
      <source media="(prefers-color-scheme: dark)" srcset="https://stagepass.one/assets/logo/stagepass-logo-dark.svg">
      <img src="https://stagepass.one/assets/logo/stagepass-logo-light.svg" alt="stagepass" height="48">
    </picture>
  </a>
</p>

<h3 align="center">Develop locally. Preview globally. Keep Webflow happy.</h3>

<p align="center">
  Local development for live Webflow sites. Write TypeScript or SCSS in your own editor and see it on your real Webflow URL without publishing. Everyone else keeps getting production.
</p>

<p align="center">
  <a href="https://stagepass.one">Website</a> ·
  <a href="https://stagepass.one/docs/getting-started/">Getting started</a> ·
  <a href="https://stagepass.one/docs/">Docs</a> ·
  <a href="https://stagepass.one/guides/">Guides</a> ·
  <a href="https://stagepass.one/changelog/">Changelog</a>
</p>

---

## What Stagepass does

- **Local SSL proxy.** The CLI serves your local folder on its own `.sp` domain with valid SSL, for example `https://my-project.sp`. Setup installs Caddy, Dnsmasq and PHP for you. No Docker.
- **Swap tagged files on your live site.** A small loader in your Webflow head code swaps tagged scripts and styles for your local versions, but only while your session is on and only in your browser.
- **Live reload.** `stagepass dev` rebuilds on change and reloads the linked `.sp` domain. CSS can swap without a full reload.
- **Safe for production.** The loader does not allow arbitrary code injection. Local files only load from domains ending in `.sp`, `localhost` or `localhost:*`. Without an active session, tagged assets keep their production URLs.
- **Always visible.** While a session is active, a small flag sits in the corner of the page. No flag means you see the live site, like every visitor.

## Quickstart

Needs macOS, Node.js 20.17 or newer and Homebrew.

```bash
npm install -g @stagepass/cli
stagepass setup
stagepass start
cd my-awesome-project
stagepass link my-project
```

Your folder is now served at `https://my-project.sp`. In Webflow, add the loader to Project Settings, Custom Code, Head Code and publish once:

```html
<script src="https://cdn.jsdelivr.net/npm/@stagepass/loader@2/dist/loader.min.js"></script>
```

Tag the assets you want to swap:

```html
<script
  data-src="https://cdn.example.com/app.min.js"
  data-stagepass="true"
  data-stagepass-path="js/app.js"></script>
```

Then open your live URL with the session parameter:

```
https://www.my-client.com/?stagepass=my-project.sp
```

Full walkthrough: [Getting started](https://stagepass.one/docs/getting-started/).

## Packages

| Package | What it does | npm |
| --- | --- | --- |
| `@stagepass/cli` | Runs on your Mac. Local SSL proxy, `.sp` domains, `link`, `build`, `watch` and `dev`. | [npm](https://www.npmjs.com/package/@stagepass/cli) |
| `@stagepass/loader` | Runs on your site. One script tag in head code that swaps tagged assets during a session. | [npm](https://www.npmjs.com/package/@stagepass/loader) |
| `@stagepass/modules` | Optional extensions for the loader: Injector, Cookies, Maintenance, or all in one bundle. | [npm](https://www.npmjs.com/package/@stagepass/modules) |

The loader and modules load from jsDelivr. The major pin `@2` brings fixes without breaking changes.

## Learn more

- [Docs](https://stagepass.one/docs/): CLI, loader, modules, flag states, security and CORS, troubleshooting
- [Guides](https://stagepass.one/guides/): practical articles on Webflow custom code and local development
- [Changelog](https://stagepass.one/changelog/)
- [How it's built](https://stagepass.one/how-its-built/)

## Contributing

All code lives in [stagepass-one/os](https://github.com/stagepass-one/os). Bug reports, ideas and pull requests are welcome.

- [Open an issue](https://github.com/stagepass-one/os/issues)
- [Contributing guide](https://github.com/stagepass-one/os/blob/master/CONTRIBUTING.md)
- [Security policy](https://github.com/stagepass-one/os/blob/master/SECURITY.md)

## License

Stagepass is open source under the [MIT license](https://github.com/stagepass-one/os/blob/master/LICENSE).

Built with AI coding agents and tools, every release reviewed by a human. Agent commits come from [@stagepass-workforce](https://github.com/stagepass-workforce). Releases are approved by a maintainer. Not affiliated with Webflow.
