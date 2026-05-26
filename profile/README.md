# Barrio Universitario

Welcome to **Barrio Universitario** — a collective focused on building open-source tools and plugins for Minecraft network infrastructure.
We develop everything from proxy-side systems to player-facing experiences, keeping the code clean, modular, and easy to extend.

---

## Repositories

| Repo | Description | Stack |
|------|-------------|-------|
| [Baul](https://github.com/BarrioUniversitario/Baul) | Crate-like loot plugin with 25+ opening animations, rarity system, and full GUI management | Paper, Java |
| [Board](https://github.com/BarrioUniversitario/Board) | Animated scoreboard plugin with rainbow titles and real-time multi-server player counts | Paper, Java |
| [Core](https://github.com/BarrioUniversitario/Core) | Velocity proxy plugin — handles cross-server connections and player count broadcasting | Velocity, Java |
| [Selector](https://github.com/BarrioUniversitario/Selector) | Server selector GUI with smart lobby routing, real-time slot tracking, and MiniMessage support | Paper, Java |

---

## Creations

Everything we ship is built around a single network architecture:

```
Player → Velocity (Core) → Paper backends (Board, Selector, Baul)
```

- **Core** acts as the message hub for the entire network, routing connections and syncing player counts across all servers.
- **Selector** gives players a polished GUI to browse and join servers, powered by real-time data from Core.
- **Board** displays that same live data directly on each player's scoreboard with smooth animations.
- **Baul** rewards players with customizable loot crates, supporting crafting, gifting, and a full reward editor.

Together they form a complete, production-ready network stack.

---

## Contributing

We welcome pull requests, bug reports, and suggestions across all repositories.

1. Fork the repo you want to contribute to
2. Create a branch: `git switch -c feat/your-feature`
3. Make your changes and test them in a local server
4. Commit with [conventional commits](https://www.conventionalcommits.org/): `feat`, `fix`, `chore`, `docs`, `refactor`, `test`
5. Open a pull request — describe what changed and why

If you're unsure where to start, open an issue first so we can discuss the approach.

---

## Recent Changes

| Repo | Change |
|------|--------|
| Baul | Migrated from ACubelets — renamed all packages to `me.davidml16.baul`, updated build system |
| Board | Added `BoardServerRegistry` for multi-server placeholder mapping and `RainbowAnimator` for gradient titles |
| Core | Added `LobbyKickListener` and external `config.properties` support |
| Selector | Added smart lobby routing with fallback chains, real-time GUI refresh, and MiniMessage formatting |

---

## TODOs

- [ ] Unified configuration format across all plugins
- [ ] Web dashboard for server stats (Board + Core data)
- [ ] Baul: support for MySQL loot history across the network
- [ ] Selector: per-server maintenance mode flag
- [ ] Core: support for weighted load balancing across lobbies
- [ ] Public API documentation for all plugins

---

## Farewell

Thanks for stopping by. If any of our plugins are running on your network, we'd love to hear about it — feel free to open a discussion or drop a star on any repo.

Built with care by the Barrio Universitario team.
