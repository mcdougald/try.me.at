<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset=".github/assets/hero-dark.png">
    <img src=".github/assets/hero.png" alt="try.me.at landing page" width="880">
  </picture>
</p>

<h1 align="center">try.me.at</h1>

<p align="center"><strong>Browse every `*.me.at` app, then decode, hash, convert and format right in your browser, with nothing to install.</strong></p>

<p align="center">
  <img src="https://img.shields.io/badge/status-live-171717?style=flat-square" alt="Status: live">
  <img src="https://img.shields.io/badge/license-source--available-404040?style=flat-square" alt="License: source-available">
  <img src="https://img.shields.io/badge/part%20of-me.at-737373?style=flat-square" alt="Part of me.at">
</p>

<p align="center">
  <a href="https://try.me.at">Website</a> ·
  <a href="#features">Features</a> ·
  <a href="#how-it-works">How it works</a> ·
  <a href="#built-with">Built with</a>
</p>

Most quick online tools mean pasting your data into a site you know nothing about. I built try.me.at as the demo gallery and sandbox playground of my `*.me.at` family: a preview card for every public app next to a shelf of 50 small, fully client-side tools, so you can click through things instead of reading about them. Everything runs in your browser with no backend, and what you type stays on the page.

<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset=".github/assets/overview-dark.svg">
    <img src=".github/assets/overview.svg" alt="try.me.at at a glance: every app in one gallery, 50 tools in your browser, shareable by URL, isolated by design" width="880">
  </picture>
</p>

## Why try.me.at

| The usual online dev tool | try.me.at |
| --- | --- |
| May send what you paste to a server | No backend: what you type stays on the page |
| One tool per site | 50 sandboxes in one place |
| Input lost on reload | Inputs kept in the URL, shareable as a link |
| One broken widget takes down the page | Each sandbox runs inside its own error boundary |

## Features

- **App showroom**: one preview card per public `*.me.at` app, filterable by sites, content and tools, and marked "Live now" only for apps that are actually hosted.
- **50 in-browser sandboxes**: regex tester, JSON inspector, contrast checker, hash and checksum digests (CRC, Adler, Fletcher), hex, Base32, Base58, Base64, Ascii85 and Z85 codecs, JWT, URL and ID inspectors (UUID, ULID, Snowflake, KSUID, NanoID and more), cron explainer, color converter, Markdown preview, line diff, IPv4/IPv6 CIDR and more.
- **Code playground**: write JavaScript or JSX and run it in an isolated, network-less frame with console output.
- **Shareable state**: each tool keeps its inputs in the URL, so a filled-in tool survives a reload and can be sent as a link.
- **Isolated demos**: every sandbox is a lazily loaded chunk inside its own error boundary, so one crashing never takes down another.
- **Embeddable**: any sandbox can be rendered without site chrome at `/embed/<id>` for framing in other family pages.
- **Project shelf**: finished projects with public live demos, each opening on its own host.

## How it works

<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset=".github/assets/flow-dark.svg">
    <img src=".github/assets/flow.svg" alt="How try.me.at works: pick, load, run, share, embed" width="880">
  </picture>
</p>

Pick an app preview or a sandbox and only that tool's chunk loads, inside its own error boundary so one crash cannot take down another. Everything computes in your browser, and each tool keeps its inputs in the URL, so a filled-in tool survives a reload and can be sent as a link. Any sandbox can also render without site chrome at `/embed/<id>` for framing in other family pages.

## Built with

<p>
  <img src="https://img.shields.io/badge/Next.js-16-000000?style=flat-square&logo=nextdotjs&logoColor=white" alt="Next.js 16">
  <img src="https://img.shields.io/badge/React-19-171717?style=flat-square&logo=react&logoColor=white" alt="React 19">
  <img src="https://img.shields.io/badge/TypeScript-5-262626?style=flat-square&logo=typescript&logoColor=white" alt="TypeScript">
  <img src="https://img.shields.io/badge/Tailwind%20CSS-4-404040?style=flat-square&logo=tailwindcss&logoColor=white" alt="Tailwind CSS 4">
  <img src="https://img.shields.io/badge/Vitest-tested-525252?style=flat-square&logo=vitest&logoColor=white" alt="Vitest">
  <img src="https://img.shields.io/badge/Playwright-e2e-737373?style=flat-square&logo=playwright&logoColor=white" alt="Playwright">
</p>

- Next.js 16 (App Router), React 19, TypeScript
- Tailwind CSS 4
- nuqs for URL-backed tool state
- Vitest and Playwright

## Part of the me.at family

try.me.at is one of my [`*.me.at`](https://me.at) apps. They share one design system, account, and app shell. Development happens in a private monorepo; this repository is the project's public-facing home.

## License

Source-available. See [LICENSE](LICENSE).
