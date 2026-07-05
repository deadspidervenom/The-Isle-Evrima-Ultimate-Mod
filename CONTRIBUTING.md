# Contributing

Thanks for taking an interest in this project. Before opening an issue or pull request, please read the ground rules below.

## Ground Rules

1. **This project is open source (AGPL-3.0).**
   All contributions are made under the project's [AGPL-3.0 license](LICENSE). By submitting a contribution, you agree it will be licensed under the same terms as the rest of the project. See the README's [License](README.md#license) section for a plain-terms breakdown.

2. **This is a maintainer-led project.**
   You're welcome to help build it, but final direction, design decisions, and merge decisions rest with the project owner. Contributing doesn't grant co-ownership or decision-making authority over the project's roadmap.

3. **Minimal reliance on UE4SS.**
   This mod is intentionally built to be a standalone, server-side mod independent of UE4SS wherever possible. Contributions that introduce unnecessary UE4SS dependencies will be reconsidered or declined in favor of alternative approaches.

## How to Contribute

- **Suggesting a feature:** Open an issue describing what you'd like to see. Include why it'd be useful and, if you have thoughts, how it might work.
- **Reporting a bug:** Open an issue with steps to reproduce, expected behavior, and actual behavior.
- **Submitting code:** Once the project source is public, open a pull request referencing the related issue. Keep changes focused and explain your reasoning in the PR description.
- **Testing:** Several in-progress features need testers. Flag your interest on the relevant issue.

## What Gets Prioritized

- Features that fit the project's core principles (optional/toggleable, server-side, admin-controlled config — see the README).
- Bug fixes and stability improvements for "Working On" features.
- Clear, well-explained feature requests over vague ones.

## What Won't Be Accepted

- Contributions that attempt to circumvent the developer mode lock or otherwise go against the base game developers' wishes (see README's "Currently Unplanned" section).
- Contributions that add unnecessary UE4SS dependencies.
- Contributions that conflict with the AGPL-3.0 license (e.g. bundling closed-source dependencies that can't be redistributed under AGPL terms).

## A Note on Sensitive Info

When submitting code (PRs, issues with logs/screenshots, config examples, etc.), please strip out anything specific to your own server before posting — IP addresses, passwords, admin/RCON credentials, API keys, tokens, database connection strings, and the like. Use placeholders instead (e.g. `YOUR_SERVER_IP`). This keeps both your server and others' safe, and it's expected of anyone sharing modified source under the project's license — see the README's [License](README.md#a-note-on-sensitivesecurity-info) section for details.

Questions? Open an issue and ask.
