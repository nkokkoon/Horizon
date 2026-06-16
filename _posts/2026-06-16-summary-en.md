---
layout: default
title: "Horizon Summary: 2026-06-16 (EN)"
date: 2026-06-16
lang: en
---

> From 65 items, 4 important content pieces were selected

---

1. [A backdoor in a LinkedIn job offer](#item-1) ⭐️ 9.0/10
2. [Iroh 1.0](#item-2) ⭐️ 8.0/10
3. [New attack turned Microsoft 365 Copilot into 1-click data theft tool](#item-3) ⭐️ 8.0/10
4. [Arch Linux Freezes AUR Signups After Coordinated Malicious Package Attack](#item-4) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [A backdoor in a LinkedIn job offer](https://roman.pt/posts/linkedin-backdoor/) ⭐️ 9.0/10

A developer discovered a backdoor embedded in a GitHub repo sent by a fake LinkedIn recruiter, exploiting npm's automatic `prepare` script to execute malicious payloads on install.

hackernews · lwhsiao · Jun 15, 20:00 · [Discussion](https://news.ycombinator.com/item?id=48546294)

**Tags**: `#security`, `#supply-chain-attack`, `#npm`, `#social-engineering`, `#cryptocurrency`

---

<a id="item-2"></a>
## [Iroh 1.0](https://www.iroh.computer/blog/v1) ⭐️ 8.0/10

Iroh 1.0 is a major release of a Rust-based peer-to-peer networking library that lets applications connect directly using cryptographic keys, functioning like an application-layer Tailscale without requiring user accounts.

hackernews · chadfowler · Jun 15, 15:13 · [Discussion](https://news.ycombinator.com/item?id=48542480)

**Tags**: `#peer-to-peer`, `#networking`, `#rust`, `#distributed-systems`, `#open-source`

---

<a id="item-3"></a>
## [New attack turned Microsoft 365 Copilot into 1-click data theft tool](https://www.bleepingcomputer.com/news/security/new-attack-turned-microsoft-365-copilot-into-1-click-data-theft-tool/) ⭐️ 8.0/10

A critical vulnerability chain called 'SearchLeak' in Microsoft 365 Copilot Enterprise allows attackers to steal sensitive data from mailboxes, OneDrive, or SharePoint via a specially crafted URL.

rss · Bleeping Computer · Jun 15, 13:00

**Tags**: `#security`, `#microsoft-365`, `#copilot`, `#vulnerability`, `#data-theft`

---

<a id="item-4"></a>
## [Arch Linux Freezes AUR Signups After Coordinated Malicious Package Attack](https://www.theregister.com/security/2026/06/15/arch-linux-locks-down-aur-signups-amid-wave-of-malicious-commits/5255511) ⭐️ 8.0/10

Arch Linux has frozen new account registrations for the Arch User Repository (AUR) after attackers flooded the community repository with malicious package updates in a coordinated supply chain attack. The incident forced maintainers to lock down signups to prevent further poisoned commits from being introduced. The AUR hosts over 85,000 packages relied upon by a large community of Arch Linux users, making it a high-value target for supply chain attacks that can silently compromise developer and sysadmin machines. This incident highlights the ongoing vulnerability of community-driven, lightly moderated package repositories to coordinated malicious campaigns. The attack was described as a coordinated wave of malicious commits targeting package updates in the AUR, suggesting multiple accounts or a systematic approach was used to push poisoned packages. New account registrations have been frozen as an immediate mitigation, though existing packages may still require auditing.

rss · The Register Security · Jun 15, 13:30

**Background**: The Arch User Repository (AUR) is a community-driven repository for Arch Linux that contains PKGBUILDs — scripts that allow users to compile and install software from source using the makepkg tool. Unlike official Arch repositories, the AUR is not officially vetted, relying instead on community trust and user vigilance. A supply chain attack targets the software distribution pipeline itself — in this case, injecting malicious code into package definitions so that users who install or update those packages unknowingly execute attacker-controlled code. Similar attacks have recently struck other ecosystems, including NPM packages used in JavaScript development.

<details><summary>References</summary>
<ul>
<li><a href="https://wiki.archlinux.org/title/Arch_User_Repository">Arch User Repository - ArchWiki</a></li>
<li><a href="https://www.howtogeek.com/897677/what-is-the-aur-in-arch-linux/">What Is the AUR in Arch Linux, and Should You Use It ?</a></li>
<li><a href="https://github.blog/security/supply-chain-security/securing-the-open-source-supply-chain-across-github/">Securing the open source supply chain across GitHub - The GitHub Blog</a></li>

</ul>
</details>

**Tags**: `#security`, `#supply-chain-attack`, `#arch-linux`, `#open-source`, `#package-management`

---