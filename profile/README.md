<div align="center">

# 🧠 NeuroNautix

**Advancing Behavioral & Preclinical Research through (Meta)Data-Driven Solutions**

[![Website](https://img.shields.io/badge/Website-neuronautix.com-0f3460?style=for-the-badge&logo=safari&logoColor=white)](https://www.neuronautix.com)
[![Email](https://img.shields.io/badge/Contact-neuronautix@gmail.com-e94560?style=for-the-badge&logo=gmail&logoColor=white)](mailto:neuronautix@gmail.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Damien_Huzard-0077B5?style=for-the-badge&logo=linkedin)](https://linkedin.com/in/dhuzard)
[![ORCID](https://img.shields.io/badge/ORCID-0000--0003--4820--7951-A6CE39?style=for-the-badge&logo=orcid)](https://orcid.org/0000-0003-4820-7951)

*Montpellier, France*

</div>

---

## 🔭 About NeuroNautix

**NeuroNautix** is a specialized consultancy empowering neuroscientists with innovative tools and personalized solutions that advance preclinical research. Founded in 2025 by [Damien Huzard, PhD](https://dhuzard.github.io), the company bridges the gap between behavioral experimentation and digital interoperability — from raw sensor data to FAIR-ready, publication-grade outputs.

> *"Pushing for a description over an interpretation of data."*

Our approach is built on three pillars:

| 💡 Innovate | ⚙️ Optimize | 🔍 Discover |
|:---:|:---:|:---:|
| Incorporating cutting-edge technologies and AI-driven tools to refine experimental designs | Streamlining workflows for precision and speed from raw measurement to meaningful findings | Enabling phenotyping and digital biomarker discovery through high-resolution behavioral tracking |

---

## 🛠️ Services

### 🐭 Behavioral Analysis
Comprehensive solutions for advanced behavioral tracking and phenotyping.
- **Quantitative Phenotyping** — in-depth analysis of behavioral traits and patterns
- **Advanced Tracking Systems** — high-resolution tracking for detailed movement analysis
- **Custom Behavioral Paradigms** — experiments designed around your research question
- **AI-Powered Tools** — DeepLabCut, SLEAP, LabGym, DeepOF, SimBA

### 📊 Data Analysis
Advanced and customized pipelines to process and interpret behavioral and physiological data.
- **Tailored Pipelines** — from experiment to publication
- **Physiological Recordings** — ECG/HRV analysis with expertise across uECG, MouseSpecifics ECGenie, LifeSpoon, DSI Telemetry, EMKA ecgTUNNEL, Empatica E4/Embrace+
- **Custom Python Libraries** — e.g., [LWTools](https://github.com/dhuzard) for LiveMouseTracker database visualization

### 🏠 Home Cage Monitoring (HCM)
Unique expertise in the full HCM ecosystem for precision phenotyping and digital biomarker discovery.

| System | Application |
|:---|:---|
| LiveMouseTracker | Social behavior, activity tracking |
| iMouse DigiFrame | Automated home-cage monitoring |
| MouseVUER | Non-invasive continuous monitoring |
| OldenLabs DOME | High-throughput phenotyping |
| JAX ENVISION™ | Longitudinal behavioral assessment |

> We help you choose the system that best fits your research question — from DIY builds to commercial platforms.

### 📋 FAIR Metadata & Metadatapp
Ensuring your research data is **F**indable, **A**ccessible, **I**nteroperable, and **R**eusable.
- **MetaData Management App** — structuring subject and experiment data from planning to publication
- **Standardized Schemas** — consistency and ease of data sharing
- **FAIR Compliance** — promoting transparency and reproducibility

👉 Learn more at [metadatapp.net](https://www.metadatapp.net) · [Open Source repo below ↓](#-metadatapp-mapp--open-source)

---

---

## 🚀 Metadatapp — Open Source

> **[github.com/Neuronautix/metadatapp](https://github.com/Neuronautix/metadatapp)** · **[metadatapp.net](https://www.metadatapp.net)**

**MetaDatApp (MAPP)** is our flagship open-source platform for structured preclinical metadata management — built API-first, designed for FAIR compliance, and ready for production via Docker.

Are you overwhelmed by the lack of solutions to track all information about your experimental subjects, from planning through publication? **MAPP is built for you.**

### 🏗️ Architecture

MAPP is composed of a set of containerized services working together:

```
┌─────────────────────────────────────────────────────────────┐
│                        MAPP Stack                           │
│                                                             │
│  ┌──────────────┐   ┌──────────────┐   ┌────────────────┐  │
│  │   Osoma UI   │   │     API      │   │   Keycloak     │  │
│  │  Vite/React  │──▶│  Symfony +   │──▶│  OIDC / Auth   │  │
│  │  Frontend    │   │ API Platform │   │                │  │
│  └──────────────┘   └──────┬───────┘   └────────────────┘  │
│                            │                                │
│                   ┌────────▼────────┐                       │
│                   │   PostgreSQL    │                       │
│                   │  (App + Auth)   │                       │
│                   └─────────────────┘                       │
│                                                             │
│  🔀 Caddy reverse proxy (HTTPS + internal routing)          │
└─────────────────────────────────────────────────────────────┘
```

| Service | Technology | Role |
|:---|:---|:---|
| **API** (`api/`) | Symfony + API Platform + FrankenPHP | REST/GraphQL API backend |
| **Osoma** (`osoma/`) | Vite + React | End-user frontend workflows |
| **Database** | PostgreSQL | Application data + Keycloak data |
| **Identity Provider** | Keycloak | OIDC authentication |
| **Reverse Proxy** | Caddy (in PHP container) | HTTPS & internal routing |

### ✨ Key Features

- **API-first design** — REST & GraphQL via API Platform
- **Structured metadata schemas** — standardized for preclinical research
- **FAIR-ready** — Findable, Accessible, Interoperable, Reusable by design
- **OIDC authentication** — secure, enterprise-grade identity via Keycloak
- **Dockerized** — full-stack deployment in one command
- **Lab system integrations** — connects with external laboratory platforms

### 🚦 Quick Start

```bash
git clone https://github.com/Neuronautix/metadatapp.git
cd metadatapp
docker compose up -d
```

> See the [full documentation](https://github.com/Neuronautix/metadatapp#readme) for configuration, environment variables, and integration guides.

### 🤝 Contributing

Contributions are welcome! MAPP is open source and community-driven. Please open an issue or pull request on [GitHub](https://github.com/Neuronautix/metadatapp).

---

## 🛡️ The FAIRRR Framework

NeuroNautix is built on the **FAIRRR** framework — an integration of **FAIR** data principles with the **3Rs** of ethical animal research:

```
FAIR  →  Findable · Accessible · Interoperable · Reusable
 3Rs  →  Replace  · Reduce     · Refine
─────────────────────────────────────────────────────
FAIRRR = Ethical Research that is also Reproducible Research
```

We are committed to the highest ethical standards, strictly adhering to 3Rs principles while ensuring all outputs meet modern open science standards.

---

## 🧬 Ontology Engineering

NeuroNautix leads development of key community ontologies for behavioral neuroscience:

- **HCMO** — Home Cage Monitoring Ontology
- **MBO** — Mouse Behavior Ontology

These efforts support semantic interoperability across preclinical datasets and are aligned with W3C standards (RDF, OWL).

---

## 🌐 Tech Stack & Expertise

| Domain | Tools & Technologies |
|:---|:---|
| **Behavioral AI** | DeepLabCut, SLEAP, LabGym, DeepOF, SimBA |
| **HCM Platforms** | LiveMouseTracker, MouseVUER, iMouse, DOME, JAX ENVISION™ |
| **Data Science** | Python (Pandas, Scipy, Seaborn, Statsmodels, Dabest), Jupyter |
| **Semantics** | RDF, OWL, Schema.org, Ontology Mapping |
| **Development** | JavaScript/TypeScript, API Design, HTML/CSS |
| **Physiology** | ECG/HRV — uECG, MouseSpecifics, DSI, EMKA, Empatica |

---

## 👤 Founder

**Damien Huzard, PhD** — Founder & CEO

- 10+ years of experience in behavioral and preclinical neuroscience
- PhD from EPFL, Switzerland
- Specializations: mouse models, home-cage monitoring, physiological recordings, FAIR metadata
- Member of the [COST-TEATIME](https://www.cost.eu/) action on automated HCM in biomedical research
- Administrator of [TheBehaviourForum](https://thebehaviourforum.org) — a global community for behavioral scientists

[![Personal Website](https://img.shields.io/badge/Website-dhuzard.github.io-blue?style=flat-square&logo=jekyll)](https://dhuzard.github.io)
[![Twitter](https://img.shields.io/badge/Twitter-@DamienHuzard-1DA1F2?style=flat-square&logo=twitter)](https://twitter.com/dhuzard)

---

## 🤝 Partners & Community

- [TheBehaviourForum](https://thebehaviourforum.org) — global behavioral science community
- COST-TEATIME Action — advancing automated HCM in biomedical research
- [Metadatapp](https://www.metadatapp.net) — API-first preclinical metadata management

---

## 📫 Get in Touch

We offer **free consultations** to discuss your research needs and design tailored solutions.

| Channel | Details |
|:---|:---|
| 📧 Email | neuronautix [at] gmail.com |
| 📍 Location | Montpellier, France |
| 🌐 Website | [neuronautix.com](https://www.neuronautix.com) |

---

<div align="center">

**NeuroNautix — Innovate. Optimize. Discover.**

*Specialized consultancy in behavioral neuroscience, home-cage monitoring, and FAIR metadata.*

</div>
