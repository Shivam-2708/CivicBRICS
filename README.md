<div align="center">

<img src="./assets/team-logo.png.jpg" alt="Team OverClocked Logo" width="140">

# 🏛️ CivicBRICS

### Multilateral Digital Public Good for Community Infrastructure Prioritization

**AI-powered platform connecting citizen infrastructure reports with policymakers.**

[🌐 Live Demo](https://civicbrics.onrender.com/index.html) • [📂 Repository](https://github.com/Shivam-2708/CivicBRICS)

**Built by Team OverClocked**

</div>

---

## 📖 Overview

**CivicBRICS** is a full-stack **Digital Public Infrastructure (DPI)** platform designed to bridge the gap between citizens and policymakers across BRICS member nations.

Citizens can report urgent infrastructure issues such as:

- 💧 Water scarcity
- ⚡ Power outages
- 🚌 Transit failures
- 🏥 Healthcare gaps

Reports can be submitted in **native and regional languages**, while a **Google Gemini-powered NLP pipeline** standardizes, categorizes, and assesses the urgency of each submission.

The processed information is then presented through a **Policymaker Dashboard**, helping officials understand and prioritize infrastructure needs.

---

## 🎯 Problem

Public infrastructure grievances are often reported through fragmented, language-dependent and non-standardized channels.

This can lead to:

- Delayed responses
- Inefficient resource allocation
- Language barriers
- Lack of transparent prioritization

**CivicBRICS** provides an AI-assisted layer between citizens and policymakers to make civic problems easier to understand and prioritize.

---

## 💡 How It Works

### ⚙️ Architecture Workflow

<div align="center">

| Step | Layer | Description |
| :---: | :--- | :--- |
| **01** | 🗣️ **Citizen Ingestion** | Multilingual submission via Web Portal (regional/native language support) |
| **02** | ⚙️ **Core Backend** | Express.js API handles validation and stores raw reports in MySQL |
| **03** | 🤖 **AI Pipeline** | Google Gemini standardizes, categorizes, and calculates urgency scores |
| **04** | 🏛️ **Governance View** | Actionable insights populated directly on the Policymaker Dashboard |

</div>

<br>

### 🔄 System Data Pipeline

```mermaid
graph TD
    subgraph Client_Layer["🗣️ Citizen Interface"]
        A[Citizen Submission] --> B[Web Portal]
    end

    subgraph Backend_Layer["⚙️ Core API & Storage"]
        B --> C[Express.js API Router]
        C --> D[(MySQL Database)]
    end

    subgraph AI_Layer["🤖 Gemini Intelligence Engine"]
        D --> E[Google Gemini AI]
        E --> F[NLP Standardizer]
        F --> G[Urgency Assessment]
    end

    subgraph Policy_Layer["🏛️ Action & Resolution"]
        G --> H[Policymaker Dashboard]
        H --> I[Targeted Infrastructure Action]
    end

    style Client_Layer fill:#f8f9fa,stroke:#d1d5db,stroke-width:1px
    style Backend_Layer fill:#f8f9fa,stroke:#d1d5db,stroke-width:1px
    style AI_Layer fill:#eff6ff,stroke:#3b82f6,stroke-width:1.5px
    style Policy_Layer fill:#f0fdf4,stroke:#22c55e,stroke-width:1.5px

    style E fill:#2563eb,color:#fff,stroke-width:0px
    style H fill:#16a34a,color:#fff,stroke-width:0px
