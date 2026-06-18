---
layout: default
title: "Horizon Summary: 2026-06-18 (EN)"
date: 2026-06-18
lang: en
---

> From 62 items, 5 important content pieces were selected

---

1. [Lore: Open-Source Version Control Built to Challenge Perforce in Game Dev](#item-1) ⭐️ 8.0/10
2. [Browser-use.com Achieves Sub-1-Second Browser Starts Using Firecracker MicroVMs on EC2](#item-2) ⭐️ 8.0/10
3. [RFC 10008: The new HTTP Query Method](#item-3) ⭐️ 8.0/10
4. [FortiBleed leak exposes Fortinet VPN credentials for 73,000 devices.](#item-4) ⭐️ 8.0/10
5. [Vertex AI SDK Flaw Enables Cross-Tenant Remote Code Execution via Bucket Squatting](#item-5) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Lore: Open-Source Version Control Built to Challenge Perforce in Game Dev](https://lore.org/) ⭐️ 8.0/10

Lore is a newly announced open-source version control system specifically designed for game development workflows that involve large binary assets, positioning itself as a scalable, open-source alternative to Perforce (Helix Core). It targets pain points like exclusive file locking, massive project sizes, and non-text asset management that Git handles poorly. Perforce has long been the de facto standard for large-scale game development, but it is expensive, proprietary, and notoriously difficult to administer — an open-source challenger could democratize access for smaller studios and indie developers. With major engines like Unreal Engine 5 deeply integrated with Perforce workflows, a viable open alternative could significantly reshape the game development tooling landscape. Lore specifically supports exclusive file locking, which is critical for binary assets like textures, 3D models, and audio files where merge conflicts are unresolvable — a feature Git lacks natively. The project has garnered significant community interest on Hacker News (920 points, 502 comments), with particular enthusiasm noted for Unreal Engine game development use cases.

hackernews · regnerba · Jun 17, 14:30 · [Discussion](https://news.ycombinator.com/item?id=48571081)

**Background**: Version control systems (VCS) track changes to files over time and allow teams to collaborate without overwriting each other's work. Git is the dominant VCS for software development but struggles with large binary files (images, audio, 3D models) because it stores full copies of every version, causing repositories to balloon in size. Perforce (Helix Core) fills this gap in game development by efficiently handling large binaries and supporting exclusive file locks — preventing two artists from editing the same asset simultaneously, which would create unresolvable conflicts. However, Perforce is a proprietary, commercial product with significant licensing costs and administrative complexity.

<details><summary>References</summary>
<ul>
<li><a href="https://www.perforce.com/products/helix-core">Perforce P4: Version Control that Scales With Your Team</a></li>
<li><a href="https://www.gamedeveloper.com/production/version-control-effective-use-issues-and-thoughts-from-a-gamedev-perspective">Version control : Effective use, issues and thoughts, from a gamedev...</a></li>
<li><a href="https://en.wikipedia.org/wiki/Perforce">Perforce - Wikipedia</a></li>

</ul>
</details>

**Discussion**: Community commenters emphasized that Lore is not a Git competitor for general software development, but specifically targets Perforce's role in game studios where exclusive file locking and large binary support are non-negotiable. There is notable enthusiasm for Unreal Engine development use cases, with one commenter noting that Perforce remains the industry standard largely due to familiarity among creative staff rather than technical superiority. Some comments also highlighted Git's notoriously unfriendly CLI output as a broader UX problem that tools in this space should address.

**Tags**: `#version-control`, `#game-development`, `#open-source`, `#devtools`, `#scalability`

---

<a id="item-2"></a>
## [Browser-use.com Achieves Sub-1-Second Browser Starts Using Firecracker MicroVMs on EC2](https://browser-use.com/posts/firecracker-browser-infra) ⭐️ 8.0/10

Browser-use.com published a detailed engineering post explaining how they run Firecracker microVMs inside EC2 instances to achieve sub-1-second browser startup times for AI-driven browser automation. Their approach leverages VM snapshotting to enable fast cold starts, allowing browsers to be ready in under one second. Fast, isolated browser startup is a critical bottleneck for AI browser automation services, and achieving sub-second cold starts at scale directly improves user experience and cost efficiency. This infrastructure approach also demonstrates a practical use case for AWS's recently enabled nested virtualization on standard EC2 instances (available since February 2026). The team reports their stealth-optimized browsers avoid bot-detection blocks 81% of the time on their own benchmark and 84.8% on the Halluminate BrowserBench, compared to only 2% for plain headless Chromium. Notably, nested virtualization on regular (non-metal) EC2 instances only became possible in February 2026, which was a prerequisite for running Firecracker VMs without expensive bare-metal instances.

hackernews · gregpr07 · Jun 16, 15:15 · [Discussion](https://news.ycombinator.com/item?id=48556561)

**Background**: Firecracker is an open-source microVM technology developed by AWS that powers services like AWS Lambda and AWS Fargate, offering boot times under 150 milliseconds and a minimal memory footprint of about 3MB per VM. MicroVMs combine the strong security isolation of traditional virtual machines with the lightweight resource efficiency of containers, making them well-suited for running untrusted or sandboxed workloads. VM snapshotting allows a running VM's memory and CPU state to be saved and quickly restored, enabling near-instant startup by skipping the full boot process. Nested virtualization refers to running a hypervisor (and thus VMs) inside another virtual machine, which was historically restricted to bare-metal EC2 instances before AWS enabled it on standard instances in early 2026.

<details><summary>References</summary>
<ul>
<li><a href="https://northflank.com/blog/what-is-aws-firecracker">What is AWS Firecracker ? The microVM technology ... — Northflank</a></li>
<li><a href="https://aws.amazon.com/blogs/opensource/firecracker-open-source-secure-fast-microvm-serverless/">Announcing the Firecracker Open Source Technology : Secure and...</a></li>
<li><a href="https://medium.com/@codingguy/firecracker-awss-path-to-fast-efficient-and-secure-microvms-46566a13d750">Firecracker : AWS ’s Path to Fast, Efficient and Secure... | Medium</a></li>

</ul>
</details>

**Discussion**: Community discussion was divided, with some users raising ethical concerns about deliberately evading anti-bot measures, arguing that websites use such protections for legitimate reasons. Others focused on technical alternatives, with one commenter noting that switching from Chromium to the lighter Lightpanda browser yielded significant gains in stability and resource usage, while another pointed out that a warm pool of pre-running browsers could be a simpler path to near-zero latency than VM snapshotting.

**Tags**: `#firecracker`, `#virtualization`, `#browser-automation`, `#infrastructure`, `#EC2`

---

<a id="item-3"></a>
## [RFC 10008: The new HTTP Query Method](https://www.rfc-editor.org/info/rfc10008/) ⭐️ 8.0/10

RFC 10008 formally introduces the HTTP QUERY method, a new idempotent HTTP method that allows request bodies for safe queries, resolving the long-debated issue of GET requests with bodies.

hackernews · schappim · Jun 17, 10:51 · [Discussion](https://news.ycombinator.com/item?id=48568502)

**Tags**: `#http`, `#web-standards`, `#rfc`, `#api-design`, `#caching`

---

<a id="item-4"></a>
## [FortiBleed leak exposes Fortinet VPN credentials for 73,000 devices.](https://www.bleepingcomputer.com/news/security/fortibleed-leak-exposes-fortinet-vpn-credentials-for-73-000-devices/) ⭐️ 8.0/10

A data leak called 'FortiBleed' has exposed VPN credentials for nearly 74,000 Fortinet/FortiGate firewall URLs belonging to organizations globally.

rss · Bleeping Computer · Jun 17, 15:12

**Tags**: `#cybersecurity`, `#VPN`, `#data-breach`, `#Fortinet`, `#network-security`

---

<a id="item-5"></a>
## [Vertex AI SDK Flaw Enables Cross-Tenant Remote Code Execution via Bucket Squatting](https://unit42.paloaltonetworks.com/hijacking-vertex-ai-model/) ⭐️ 8.0/10

Palo Alto Networks' Unit 42 researchers discovered a vulnerability in the Vertex AI Python SDK that allows attackers to achieve cross-tenant remote code execution by combining bucket squatting with Python pickle deserialization during model uploads. This vulnerability affects enterprise AI/ML workloads running on Google Cloud's Vertex AI platform, potentially allowing one tenant to execute malicious code in another tenant's environment — a severe breach of cloud isolation boundaries. The finding highlights the growing supply chain and infrastructure risks unique to AI/ML tooling in cloud environments. The attack exploits Python's pickle deserialization mechanism, which by design can execute arbitrary code when loading serialized objects — meaning a maliciously crafted model file uploaded to a squatted bucket can trigger remote code execution on any victim who subsequently loads it. This is a known class of vulnerability that takes advantage of the global uniqueness of cloud storage bucket names to intercept or substitute legitimate model artifacts.

rss · Unit 42 · Jun 16, 10:00

**Background**: Vertex AI is Google Cloud's managed machine learning platform, widely used by enterprises to train and deploy AI models. Bucket squatting is an attack where an adversary pre-registers a cloud storage bucket (on services like GCP Cloud Storage or AWS S3) using a name they predict a target organization will use, allowing them to intercept data or serve malicious content. Python's pickle module is a standard serialization format used to save and load Python objects, including ML models, but it is inherently unsafe because deserializing a pickle file can execute arbitrary Python code embedded by an attacker. Together, these two weaknesses create a scenario where a poisoned model file can silently compromise an entire cloud tenant's environment.

<details><summary>References</summary>
<ul>
<li><a href="https://www.csoonline.com/article/4186193/googles-vertex-ai-sdk-could-allow-rce-through-bucket-squatting.html">Google’s Vertex AI SDK could allow RCE through bucket squatting | CSO Online</a></li>
<li><a href="https://cloud.google.com/transform/how-to-combat-bucket-squatting-in-five-steps">How to combat bucket squatting in five steps | Google Cloud Blog</a></li>
<li><a href="https://semgrep.dev/docs/learn/vulnerabilities/insecure-deserialization/python">Insecure Deserialization in Python - Semgrep</a></li>

</ul>
</details>

**Tags**: `#security`, `#cloud-security`, `#vertex-ai`, `#remote-code-execution`, `#machine-learning`

---