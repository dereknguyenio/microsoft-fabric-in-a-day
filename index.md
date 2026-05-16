---
title: Microsoft Fabric in a Day
permalink: index.html
layout: home
---

# Microsoft Fabric exercises

Welcome to **Microsoft Fabric in a Day** — a curated set of hands-on exercises that accompany the [Microsoft Fabric learning modules on Microsoft Learn](https://aka.ms/learn-fabric).

Each lab is a self-contained, step-by-step walkthrough that runs entirely in the [Microsoft Fabric](https://app.fabric.microsoft.com) SaaS portal — there is nothing to install on your machine.

## Before you start

You'll need a **Microsoft Fabric license** and a Microsoft **work or school** account. The fastest way is to start a [free Fabric trial](https://learn.microsoft.com/fabric/get-started/fabric-trial).

For a recommended end-to-end ordering and a "Fabric in a Day" workshop agenda, see the [curriculum guide]({{ site.github.repository_url }}/blob/main/CURRICULUM.md).

## Exercises

{% assign labs = site.pages | where_exp:"page", "page.url contains '/Instructions/Labs'" %}

| Module | Lab |
| --- | --- |
{% for activity in labs %}| {{ activity.lab.module }} | [{{ activity.lab.title }}{% if activity.lab.type %} - {{ activity.lab.type }}{% endif %}]({{ site.github.url }}{{ activity.url }}) |
{% endfor %}

---

### Find a problem?

If you hit an issue in any exercise, please report it on the [GitHub repository]({{ site.github.repository_url }}/issues/new/choose). For issues with the Microsoft Fabric service itself, use [Fabric support](https://support.fabric.microsoft.com/support/).
