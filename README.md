# 🦉 ORegTrust

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-OScan-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-MIT-green?style=flat-square"/>
  <img src="https://img.shields.io/badge/Part%20of-OwlSec%20Toolkit-7b5ea7?style=flat-square"/>
  <img src="https://img.shields.io/badge/Version-1.0.0-cyan?style=flat-square"/>
</p>

> **ORegTrust** — Container Image Trust & Registry Auditor

---

> ⚠️ **AUTHORISED USE ONLY** — Use only on systems you own or have explicit written permission to test. Unauthorised use is illegal.

---

## 📌 Overview

Container image trust & registry configuration auditor (policy.json, registries.conf, sigstore, containerd, CRI-O)

---

## ✨ Features

- Offline, read-only auditor for the container image trust chain used by Podman / Buildah / Skopeo / CRI-O / containerd / Docker engine
- policy.json signature-policy analyzer — default insecureAcceptAnything, missing signedBy / sigstoreSigned on production registries, key paths, Fulcio / Rekor, signedIdentity strength
- registries.conf (+ registries.conf.d drop-ins) — insecure registries, http mirrors, short-name squatting (docker.io in unqualified search), short-name-mode, blocked registries, aliases, v1 format
- registries.d sigstore lookaside (http / staging)
- containers.conf engine defaults — seccomp, AppArmor, capabilities, host namespaces, pids_limit, no_new_privileges, pull_policy, remote TCP endpoints
- storage.conf — vfs driver, overlay nodev, stores
- containerd config.toml mirrors / TLS / auth and certs.d hosts.toml skip_verify / http
- CRI-O crio.conf image + runtime defaults
- Docker daemon.json insecure-registries / TCP hosts
- auth.json / ~/.docker/config.json plaintext creds (always masked), credsStore, file permissions
- 100+ rules with severity, CWE, MITRE ATT&CK, fix
- Score + grade A+…F, hardened config templates
- TXT / MD / JSON / CSV / SARIF exports, --fail-on, --list-rules, --explain, --demo self-test

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./ORegTrust
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
