# Hi, I'm Aaron (Qing) Shi 👋

**Principal RAN & Network Architect** · 20+ years across Tier-1 operators and vendors
5G NR · Open RAN · NTN (Satellite-to-Mobile) · Wireless Core & IMS · AI-Driven Network Automation

I build working proofs-of-concept that combine 3GPP expertise with cloud-native software and AI. That means turning probes, modems and Raspberry Pis into measurable test platforms, and turning their data into automated root-cause analysis.

---

## 🔭 Focus Areas

- **AI for RAN & operations**: LLM + RAG for 3GPP log analysis, agentic root-cause analysis, KPI anomaly detection
- **AI/ML for the air interface**: 3GPP Rel-18 studies (CSI compression), toward AI-native 6G
- **Non-Terrestrial Networks**: satellite direct-to-cell testing and analytics
- **Network resilience**: digital twins and reinforcement learning for disaster recovery
- **Test automation**: containerized probe fleets, CI/CD, dashboards and APIs

---

## 🚀 Projects

| Project | What it does | Tech | Status |
|---|---|---|---|
| **AI-Driven DR Digital Twin** | ns-3 simulation coupled with PPO reinforcement learning to plan migration of 10,000+ LTE nodes to a DR core; **8.7× faster recovery** than baseline | ns-3 (C++), Python, PPO, shared-memory IPC, Docker | ✅ Complete |
| **5G NR CSI Feedback Compression** | CsiNet-style autoencoder benchmarked against 3GPP Type I/II PMI codebooks (TR 38.843, Rel-18 AI/ML) | PyTorch, CDL & COST2100 channel data | 🔄 Active |
| **[nokia-fwa-monitor](https://github.com/aaronshi2017/nokia-fwa-monitor)** | Multi-probe RF monitoring for 5G SA FWA gateways; field trials showed uplink ~8× more sensitive to antenna placement than downlink | Raspberry Pi, Docker, FastAPI, SQLite, Chart.js, Tailscale | ✅ Running |
| **Probe Fleet Analytics & AI RCA** | Central database, scheduled collection, KPI dashboard and outage classification for a satellite-to-mobile probe fleet; L3 (RRC/NAS) capture to pcap; LLM RCA assistant in progress | FastAPI, SQLite (WAL), Docker, QCSuper, tshark, local LLM | 🔄 Active *(private)* |
| **Data-Experience Probe Service** | Containerized DNS / web / IPv4-IPv6 performance tests every 15 min, with API and dashboard | Docker, FastAPI, database | ✅ Running *(private)* |
| **LLM-Assisted 3GPP Log RCA** | Log and ticket database built as a RAG source with 3GPP specs; local telecom-tuned LLM for layer-3 analysis | FastAPI, Docker, RAG, local LLM | 🔄 Active |
| **5G Core & IMS Lab** | Two independent Open5GS 5GS + IMS cores on Raspberry Pi with data and voice; extending to EPC/EN-DC and inter-PLMN roaming | Open5GS, IMS, Docker, virtual & real UE/gNB | 🔄 Active |
| **[volte_terminating_pi](https://github.com/aaronshi2017/volte_terminating_pi)** | Containerized service on a Pi + LTE modem that answers VoLTE test calls, plays reference audio and logs call KPIs | Python, AT commands, Docker Compose, database | ✅ Working |

> *Private* = work-related projects kept private. Architecture and lessons learned are available on request.

---

## 🧭 Reusable Architecture Pattern

Most of my probe projects share one design:

```
[Probe: Pi + modem]  test code + local DB  ──scheduled pull──▶  [Hub]  central DB
                                                                   │
                                                  FastAPI dashboard + REST API
                                                                   │
                                                    LLM assistant / RCA agent
```

Each new test program (satellite, FWA, 5G, VoLTE) plugs into the same hub, so analytics and AI are built once and reused.

---

## 🛠️ Tech Stack

**Telecom:** 4G/5G NR (NSA/SA), O-RAN 7.2x, NTN, 5GC/EPC, IMS, VoLTE/VoNR, RRC/NAS, S1/N2/Xn, GPS/PTP/SyncE
**AI/ML:** PyTorch, reinforcement learning (PPO), autoencoders, LLM + RAG, agentic workflows
**Software & Cloud:** Python, C++, FastAPI, Docker / Compose, SQLite, Jenkins, GitHub, AWS, Tailscale
**Security:** IPsec + AAA, PKI / X.509, untrusted-backhaul architecture

---

## 🎓 Education & Certifications

- Master's in Network Security, Concordia University
- MSEE, Telecommunications, The University of Texas at Dallas
- AWS Certified Cloud Practitioner (CLF-C02) · AWS Solutions Architect – Associate *(in preparation)*

---

## 📫 Contact

[LinkedIn](https://www.linkedin.com/in/aaron-shi-56b26711b/) · aaronshi@yahoo.com
