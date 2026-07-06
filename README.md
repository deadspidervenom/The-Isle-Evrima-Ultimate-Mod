# The Ultimate Mod

> A server-side, standalone mod project — independent from UE4SS.

**Status:** In development since ~May 2026 (started 7/5/2026 write-up).

This repository currently serves as a **project shell**. There's no source code here yet. Once the project reaches an acceptable state — or if it's abandoned — the full source will be uploaded here.

## Why a shell repo?

The goal is to let the community shape this mod before the code is set in stone. Open an issue with a feature you'd like to see, and it'll be reviewed to determine:

- Whether it's technically possible
- How it could be implemented
- An explanation of the approach

## Core Principles

1. **Everything is optional.** Every feature can be toggled off (e.g. don't want VOIP? Disable it).
2. **"Working on" means proven.** A feature isn't marked as "working on" until at least a basic version of it has been built and proven functional. Anything not yet at that stage is simply a possibility under consideration.
3. **Server-side only.** All code is server-side, with the sole exception of the Mumble plugin (which requires a client component). A companion app may be developed alongside this project, but expect it to be basic — GUI design isn't a strength here.
4. **Admin-controlled configuration.** Anything configurable lives in the config file and is admin-edit only. Client-side elements either pull info from the server or are hardcoded. Nothing is left casually accessible to regular users.
5. **Manual updates for now.** Full auto-updating is outside current scope/expertise. When the game updates, you'll need UE4SS installed to generate offset dumps (from the UE4SS log and object dump) in order to update this mod. The project will be maintained, but if you don't want to wait on updates, this is the workaround.

## Feature Roadmap

### ✅ Implemented (Fully)

Nothing yet. Most "Working On" items are close to complete — pending testing, bug fixes, or refinement.

### 🔧 Working On

- Advanced Mumble-based VOIP (positional audio)
- Auto-linking between Mumble and the game server
- Admin dino restore function (for rule-breaking / dino griefing)
- Detailed chat logger

### 📋 Planned

- Dino meal time — auto-spawning food sources during high-traffic hours to prevent scarce food from killing baby dinos
- Notification system for various events
- Dino storage and loading
- Skin color system
- Prime tracker
- Mutation tracker
- Map auto-update with dynamic info, including heatmaps
- Point system based on gameplay
- Admin tools for moderation
- Admin tools for events
- QOL and utility features across various aspects

### 🚫 Currently Unplanned

- **Independent offset auto-updater** — Attempted and shelved after too much time spent. Not currently worth the R&D required to make it foolproof.
- **In-game chat messages** — Not being pursued unless a crash-free method is found (or after the rest of the roadmap is complete).
- **Re-enabling or circumventing developer mode lock** — Out of respect for the original developers' choices, this won't be pursued without explicit permission. If a dev gives the go-ahead (even limited to personal/test server use), it may be reconsidered — but only with full confidence the devs are okay with it.

## Contributing

Interested in helping? Open an issue. See [CONTRIBUTING.md](CONTRIBUTING.md) for the ground rules before you do.

## Testers Needed

Several "Working On" features need testing help — if you're interested, open an issue or reach out.

## License

This project is licensed under the **GNU Affero General Public License v3.0 (AGPL-3.0)**. See the [LICENSE](LICENSE) file for the full text.

### What that means in plain terms

**✅ You CAN:**
- Use this mod for free, on your own server, for any purpose (personal, community, even commercial).
- Modify the code however you like for your own use.
- Share the mod (modified or not) with others.
- Study the code and learn from it.

**⚠️ If you share or run a modified version, you MUST:**
- Make your modified source code available to anyone who uses it — including players connecting to a server running your modified version (this is the "network use" clause that makes AGPL stronger than regular GPL).
- Keep the same AGPL-3.0 license on your modified/derivative version. You can't relicense it under something more restrictive.
- Clearly state what you changed and give credit to the original project.
- Keep the original copyright and license notices intact.

**❌ You CANNOT:**
- Take this code, modify it, and release it (or run it publicly) as closed-source / proprietary.
- Strip out the license and claim the code as fully your own.
- Sell the code itself as a closed product without also providing the source under AGPL.
- Use this project's code in a closed-source project and only distribute compiled/obfuscated versions.

**In short:** improve it, share it, run it — just keep it open for everyone else too. No forking this into a private, closed-source, paywalled version.

### A note on sensitive/security info

Sharing your source doesn't mean exposing things that would put your server at risk. Before publishing or sharing modified source, you should (and are expected to) redact or zero out anything security-sensitive that's specific to your setup, such as:

- Hardcoded IP addresses or domains
- Server passwords, admin credentials, or RCON details
- API keys, tokens, or webhook URLs
- Database connection strings
- Any other secrets that would let someone compromise, DDoS, or unauthorized-access your server

Replace these with placeholders (e.g. `YOUR_SERVER_IP`, `<REDACTED>`) before sharing. The *code and logic* needs to stay open — your personal server's attack surface doesn't. This is standard practice across open source projects and isn't a violation of AGPL; the license covers the software itself, not your private configuration/secrets.

This isn't legal advice — if you need certainty on a specific use case, consult the [full AGPL-3.0 text](https://github.com/deadspidervenom/The-Isle-Evrima-Ultimate-Mod/blob/main/LICENSE) or a legal professional.
