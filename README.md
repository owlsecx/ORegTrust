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

ORegTrust is an offline, read-only auditor for the container image trust chain used by Podman, Buildah, Skopeo, CRI-O, containerd and Docker. It analyses policy.json signature policies, registries configuration, container engine defaults and stored credentials for weaknesses. Credentials are always masked.

---

## ✨ Features

- policy.json signature-policy analysis (insecureAcceptAnything, signedBy, sigstore)
- registries.conf review for insecure registries, http mirrors and short-name squatting
- containers.conf engine defaults (seccomp, AppArmor, capabilities, namespaces, pull policy)
- storage.conf, containerd config.toml and CRI-O crio.conf checks
- Docker daemon.json insecure-registries/TCP-host detection and auth.json credential review (masked)
- Rule catalogue, hardened templates, multiple output formats and a CI fail-on gate

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./ORegTrust --audit
./ORegTrust --file /etc/containers/policy.json
./ORegTrust --audit --root /mnt/collected --fail-on high
./ORegTrust --help
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
