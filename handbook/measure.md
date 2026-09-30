---
title: Render-cost probe (largest entry)
tags: [meta, probe]
---

## Planted non-executable probes

An inline expression probe: {fetch('/planted-leak-url')}

A script probe: <script>window.__plantedScriptRan = true;</script>

An img onerror probe: <img src="/planted-img.png" onerror="window.__plantedImgRan = true" alt="probe" />

## Body

This is the largest entry, padded to give the render-cost probe something to measure.

$(for i in $(seq 1 40); do echo "Paragraph $i of the render-cost corpus — the interpreter renders this as text, never compiles it."; done)

See [the security notes](../security-notes.mdx) and [home](../home.mdx).
