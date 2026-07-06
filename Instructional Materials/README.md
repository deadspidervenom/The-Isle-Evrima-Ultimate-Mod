# Instructional Materials

## What This Folder Is

This folder is a collection of write-ups covering **Evrima-specific modding knowledge** — the kind of practical, hard-won detail that only comes from working directly against *The Isle: Evrima*'s dedicated server binary, rather than from general Unreal Engine tutorials.

This is not a generic "how to mod UE5.6 games" resource. Evrima runs a private engine fork, has its own class hierarchy, its own quirks in how certain engine systems behave (or don't) on a dedicated server, and its own history of things that look like they should work but don't. This folder exists to document that knowledge specifically, so it doesn't stay locked inside one person's head or scattered across old test logs.

Nothing in this folder is source code, and nothing here is required reading to use or configure the mod itself.

---

## Licensing Note

The rest of this repository is licensed under AGPL-3.0 (see the main [README.md](../README.md) and [LICENSE](../LICENSE)).

**The contents of this folder are not licensed and are not covered by that restriction.** These write-ups are meant to be freely read, referenced, and reused by anyone working on Evrima modding, independent of this project. The AGPL terms in the main README apply to actual released source code elsewhere in this repository — not to the explanatory material here.

---

## Why This Folder Exists

Evrima modding runs into problems that generic Unreal Engine guides don't cover, because they're specific to this game's build, its private engine fork, and its own behavior on a dedicated server. A few examples of the kind of question this folder is meant to answer:

- Why a specific native function was hooked instead of a similarly-named alternative that seemed like it should work just as well
- Why a commonly-documented Unreal modding technique (found in general UE tutorials) doesn't apply here, and what had to be done instead
- How to actually test whether a candidate hook target fires at all on a dedicated server, before building real logic around it
- Why certain engine systems that exist and look usable turn out to be unreliable, dangerous, or simply dead on this build
- How to tell the difference between "this doesn't work" and "this isn't confirmed yet" — and why that distinction matters when building on top of untested assumptions
- Why some approaches that worked in the past stopped working after a game update, and what that implies about how fragile a given technique actually is

This is the kind of knowledge that's normally only found by trial, error, and a lot of wasted time. Writing it down here means the next person doesn't have to re-learn it from scratch.

---

## Who This Is For

- **Evrima modders** building their own server-side tools or features
- **Contributors to this project** who want to understand why a particular function, hook, or approach was chosen
- **Anyone reverse-engineering Evrima's dedicated server** who wants a reference for what's already been tested, confirmed, or ruled out
- **Modders coming from other Unreal titles** who assume general UE knowledge will transfer directly — this folder is partly here to correct that assumption where Evrima specifically diverges from it

A working knowledge of C++ and basic Unreal Engine concepts is assumed. This folder is not an introduction to UE5.6 in general — it picks up where that general knowledge leaves off.

---

## What You Can Expect to Find

Write-ups here are focused, practical, and specific to Evrima. Depending on the topic, this may include things like:

- Comparisons between two candidate functions or hooks, and the reasoning for picking one over the other
- Explanations of why a function, class, or system is deliberately avoided, along with what happens if you try it anyway
- Step-by-step reasoning for how to verify whether a given function actually fires, executes safely, or behaves as its name implies — before relying on it
- Notes on engine behavior that's specific to a dedicated server context (things that only break, or only work, when there's no client attached)
- Corrections to earlier assumptions that turned out to be wrong, along with what evidence changed that conclusion
- Practical testing methodology — how to isolate a single function or hook, observe it safely, and draw a real conclusion from that observation

This repository is currently a **project shell** — the full source hasn't been published yet (see the main README). Materials in this folder will be filled in and expanded as testing and development progress.

---

## What This Folder Is *Not*

- **Not source code.** No functional or copy-pasteable code lives here — explanation only.
- **Not a general UE5.6 tutorial.** Baseline engine knowledge is assumed; this folder covers what's specific to Evrima, not Unreal Engine as a whole.
- **Not applicable to other engine versions.** Nothing here should be assumed to carry over to UE4 or to UE4SS-hosted mods — Evrima's private fork and this project's standalone approach mean the two don't share assumptions.
- **Not a setup or configuration guide.** For installation and configuration, refer to the main repository documentation once available.
- **Not a place for sensitive information.** No real server IPs, credentials, tokens, or other sensitive details will appear here, ever.
- **Not guaranteed to be permanently accurate.** Game updates can invalidate findings here without warning. Treat every write-up as "true as of when it was written," not as a permanent guarantee — and check it against current testing before relying on it.

---

## Questions or Suggestions?

If something here is unclear, out of date, or you think a topic is missing, open an issue on the repository. If you've independently confirmed or disproven something written here, that feedback is especially useful — this folder is only as good as it stays accurate.