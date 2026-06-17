---
layout: default
title: Home
---

# Horizon

<div id="lang-zh" class="lang-section">

欢迎来到 <a href="https://github.com/thysrael/Horizon">Horizon</a>，一个 AI 驱动的信息聚合系统。

## 文档

- <a href="configuration">配置指南</a> — AI 提供商、信息源、过滤规则与环境变量替换
- <a href="scrapers">信息源采集器</a> — Horizon 如何从 GitHub、Hacker News、RSS、Reddit 采集内容
- <a href="scoring">评分系统</a> — 基于 AI 的内容分析与 0-10 评分体系

## 每日速递

<ul>
  {% assign zh_posts = site.posts | where: "lang", "zh" %}
  {% for post in zh_posts limit:20 %}
    <li>
      <a href="{{ post.url | relative_url }}">{{ post.date | date: "%Y-%m-%d" }}</a>
    </li>
  {% else %}
    <li><em>暂无内容</em></li>
  {% endfor %}
</ul>

</div>

<div id="lang-en" class="lang-section">

Welcome to <a href="https://github.com/thysrael/Horizon">Horizon</a>, an AI-driven information aggregation system.

## Documentation

- <a href="configuration">Configuration Guide</a> — AI providers, information sources, filtering, and environment variable substitution
- <a href="scrapers">Source Scrapers</a> — How Horizon collects content from GitHub, Hacker News, RSS, and Reddit
- <a href="scoring">Scoring System</a> — AI-based content analysis and the 0-10 scoring scale

## Daily Digest

<ul>
  {% assign en_posts = site.posts | where: "lang", "en" %}
  {% for post in en_posts limit:20 %}
    <li>
      <a href="{{ post.url | relative_url }}">{{ post.date | date: "%Y-%m-%d" }}</a>
    </li>
  {% else %}
    <li><em>No posts yet</em></li>
  {% endfor %}
</ul>

</div>
