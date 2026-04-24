# 🛡️ Custom C2 Framework — Detection Research for Blue Teams

> **Defensive security research.** This repository analyzes how custom-built C2 frameworks operate on the wire and on endpoints, and documents the detection opportunities, IOCs, and Sigma rules SOC analysts can use to identify them.

## ⚠️ Disclaimer

This repository contains **defensive security research only**. No source code or binaries are provided — only architecture documentation, behavioral analysis, IOCs, and detection content. All testing was conducted in a fully isolated VMware lab with no external network connectivity. The purpose of this work is to improve SOC and blue team detection capabilities against custom (non-commodity) C2 tooling that evades signature-based controls.

## 🎯 Research Question

**How do custom-built C2 frameworks — the kind that don't match any known signature — operate in practice, and what behavioral, network, and registry indicators allow SOC analysts to detect them reliably?**

To answer this, a full C2 framework was developed from scratch (no Metasploit, no Cobalt Strike, no Sliver) in an isolated lab to generate authentic telemetry. The framework was then analyzed from a defender's perspective across every phase: initial callback, command execution, feature modules (keylogging, screen capture, audio/video), persistence, and session recovery.

## 🛡️ Detection Content (Jump To)

- [Attack → Detection Mapping Table](#-attack--detection-mapping)
- [Recommended Defensive Controls](#-recommended-defensive-controls)
- [Sigma Rules for C2 Detection](#-sigma-rules-for-c2-detection)
- [MITRE ATT&CK Coverage](#-mitre-attck-coverage)
- [Lessons for Defenders](#-lessons-for-defenders)

## 🏗️ Framework Architecture (Object of Study)
