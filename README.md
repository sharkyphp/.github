# SharkyPHP

**A lightweight, hand-crafted PHP framework built for performance and clarity.**

SharkyPHP abandons bloated abstractions and redundant layers, offering a clean kernel that unifies HTTP web requests and CLI command execution under one architecture. It ships with separated official components — dependency container, database layer with query builder, cache, Redis adapter, session, compiled template engine and console pipeline — each staying independent with clear boundaries, while the core kernel orchestrates their lifecycle.

Designed for developers who prefer explicit logic over hidden magic: onion middleware pipelines, context isolation, database read-write separation, and flexible driver implementations. Minimal dependencies, straightforward source code, easy to trace and extend. Build high-performance web and console applications with full control of your runtime.

—— ByteSharky

---

## Repository layout

This organization (`sharkyphp`) hosts the **read-only, split distribution** of the framework. The actual source of truth lives in the upstream monorepo:

| Repository | Role |
|---|---|
| **[`bytesharky/sharkyphp-v2`](https://github.com/bytesharky/sharkyphp-v2)** | 🔗 **Upstream monorepo** — all 22 packages live under `framework/packages/*`. Development, commits and release tags happen here. |
| [`sharkyphp/splitter`](https://github.com/sharkyphp/splitter) | The split bot. Hourly cron clones the monorepo, runs `git subtree split`, and force-pushes each package into its own repository below. |
| `sharkyphp/<package>` (×22) | The individual, read-only Composer packages consumed via Packagist. **Never push to these by hand** — they are regenerated on every tag. |

## Development

All code, issues and pull requests go to the upstream monorepo:
👉 **https://github.com/bytesharky/sharkyphp-v2**

To release a new version, tag `vX.Y.Z` on the monorepo and push; the splitter picks it up automatically (≤ 1 hour) and republishes every package.

## Documentation

- Official docs site: _(coming soon)_
- Packagist: _(register the 22 packages, then link here)_

## License

Proprietary — see the upstream monorepo for details.
