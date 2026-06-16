---
layout: default
title: "Horizon Summary: 2026-06-16 (EN)"
date: 2026-06-16
lang: en
---

> From 53 items, 5 important content pieces were selected

---

1. [A backdoor in a LinkedIn job offer](#item-1) ⭐️ 8.0/10
2. [Iroh 1.0](#item-2) ⭐️ 8.0/10
3. [Cisco Patches Critical SD-WAN vManage Zero-Day Privilege Escalation Flaw](#item-3) ⭐️ 8.0/10
4. [New attack turned Microsoft 365 Copilot into 1-click data theft tool](#item-4) ⭐️ 8.0/10
5. [Arch Linux Freezes AUR Registrations After Coordinated Malicious Package Attack](#item-5) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [A backdoor in a LinkedIn job offer](https://roman.pt/posts/linkedin-backdoor/) ⭐️ 8.0/10

A developer discovered a backdoor hidden in a GitHub repo sent by a fake LinkedIn recruiter, exploiting npm's automatic 'prepare' script execution to run malicious payloads on the victim's machine.

hackernews · lwhsiao · Jun 15, 20:00 · [Discussion](https://news.ycombinator.com/item?id=48546294)

**Tags**: `#security`, `#supply-chain-attack`, `#npm`, `#social-engineering`, `#cybercrime`

---

<a id="item-2"></a>
## [Iroh 1.0](https://www.iroh.computer/blog/v1) ⭐️ 8.0/10

Iroh 1.0 launches as a peer-to-peer networking library that lets applications connect via cryptographic keys rather than IP addresses, offering a Tailscale-like experience at the application layer.

hackernews · chadfowler · Jun 15, 15:13 · [Discussion](https://news.ycombinator.com/item?id=48542480)

**Tags**: `#peer-to-peer`, `#networking`, `#rust`, `#distributed-systems`, `#open-source`

---

<a id="item-3"></a>
## [Cisco Patches Critical SD-WAN vManage Zero-Day Privilege Escalation Flaw](https://www.bleepingcomputer.com/news/security/cisco-fixes-sd-wan-vmanage-flaw-exploited-in-zero-day-attacks/) ⭐️ 8.0/10

Cisco has released security updates to patch CVE-2026-20262, a critical privilege escalation vulnerability in Catalyst SD-WAN Manager (formerly vManage) that was actively exploited as a zero-day in the wild. Attackers leveraged this flaw to escalate privileges and gain root access on affected systems. Cisco Catalyst SD-WAN Manager is widely deployed in enterprise networks to manage up to 6,000 SD-WAN devices from a single dashboard, meaning a successful exploit could give attackers full control over an organization's entire wide-area network infrastructure. Active zero-day exploitation means patches must be applied immediately, as attackers are already targeting unpatched systems. The vulnerability, tracked as CVE-2026-20262, allows an attacker to escalate privileges all the way to root level on the SD-WAN Manager system, representing a full system takeover risk. Cisco has confirmed active in-the-wild exploitation, making this a high-priority patch for any organization running Catalyst SD-WAN Manager.

rss · Bleeping Computer · Jun 15, 17:12

**Background**: Cisco Catalyst SD-WAN Manager, formerly known as vManage, is a centralized network management platform that allows IT administrators to monitor, configure, and manage large-scale software-defined wide-area network (SD-WAN) deployments from a single interface. SD-WAN technology replaces or supplements traditional WAN connections by intelligently routing traffic across multiple network links, and is commonly used by enterprises to connect branch offices and cloud services. A zero-day vulnerability refers to a security flaw that is exploited by attackers before the software vendor has released an official patch, leaving defenders with no ready fix. Privilege escalation to root means an attacker who may have limited initial access can gain the highest level of system control, enabling them to install malware, exfiltrate data, or pivot to other parts of the network.

<details><summary>References</summary>
<ul>
<li><a href="https://www.bleepingcomputer.com/news/security/new-cisco-sd-wan-flaw-exploited-in-zero-day-attacks-to-gain-root/">Cisco warns of unpatched SD - WAN zero-day exploited in attacks</a></li>
<li><a href="https://www.linkedin.com/posts/robertsdit_cisco-confirms-active-exploitation-of-two-activity-7435425442981019649-IAer">Cisco patches SD - WAN Manager vulnerabilities... | LinkedIn</a></li>

</ul>
</details>

**Tags**: `#security`, `#cisco`, `#zero-day`, `#SD-WAN`, `#vulnerability`

---

<a id="item-4"></a>
## [New attack turned Microsoft 365 Copilot into 1-click data theft tool](https://www.bleepingcomputer.com/news/security/new-attack-turned-microsoft-365-copilot-into-1-click-data-theft-tool/) ⭐️ 8.0/10

A critical vulnerability chain called 'SearchLeak' in Microsoft 365 Copilot Enterprise allows attackers to steal sensitive data from mailboxes, OneDrive, or SharePoint via a specially crafted URL.

rss · Bleeping Computer · Jun 15, 13:00

**Tags**: `#security`, `#microsoft-365`, `#copilot`, `#vulnerability`, `#data-theft`

---

<a id="item-5"></a>
## [Arch Linux Freezes AUR Registrations After Coordinated Malicious Package Attack](https://www.theregister.com/security/2026/06/15/arch-linux-locks-down-aur-signups-amid-wave-of-malicious-commits/5255511) ⭐️ 8.0/10

Arch Linux has frozen new account registrations for the Arch User Repository (AUR) after attackers flooded the community repository with malicious package updates in a coordinated supply chain attack. The incident forced administrators to lock down signups to prevent further poisoned package submissions. The AUR hosts over 85,000 packages relied upon by a large community of Arch Linux developers and power users, making a coordinated poisoning attack a serious supply chain security threat. This incident highlights the inherent risks of community-maintained repositories where package integrity depends on the trustworthiness of individual contributors. The attack involved a wave of malicious commits to existing AUR packages, suggesting attackers either created new accounts specifically to submit poisoned updates or compromised existing maintainer accounts. As a direct response, new AUR account registrations have been suspended while the situation is investigated and remediated.

rss · The Register Security · Jun 15, 13:30

**Background**: The Arch User Repository (AUR) is a community-driven repository for Arch Linux that contains package build scripts called PKGBUILDs, allowing users to compile and install software not available in official repositories. Unlike official Arch repositories, AUR packages are submitted and maintained by individual community members with minimal gatekeeping, which makes it both flexible and potentially risky. Supply chain attacks targeting package managers have become increasingly common, with similar incidents affecting npm and other ecosystems in 2025 and 2026. In a supply chain attack, malicious code is injected into legitimate software packages so that users who install or update those packages unknowingly execute the malware.

<details><summary>References</summary>
<ul>
<li><a href="https://wiki.archlinux.org/title/Arch_User_Repository">Arch User Repository - ArchWiki</a></li>
<li><a href="https://www.howtogeek.com/897677/what-is-the-aur-in-arch-linux/">What Is the AUR in Arch Linux, and Should You Use It ?</a></li>
<li><a href="https://www.microsoft.com/en-us/security/blog/2026/05/20/mini-shai-hulud-compromised-antv-npm-packages-enable-ci-cd-credential-theft/">Mini Shai Hulud: Compromised @antv npm packages enable CI/CD ...</a></li>

</ul>
</details>

**Tags**: `#security`, `#supply-chain-attack`, `#arch-linux`, `#open-source`, `#package-management`

---