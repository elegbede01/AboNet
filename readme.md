# AboNet  
**Intelligent Hybrid Cybersecurity Framework for Multimodal Cyberbullying & Deepfake Protection**

[![Status](https://img.shields.io/badge/Status-In_Development-yellow)]()  
[![Tech](https://img.shields.io/badge/Tech-Flutter%20%7C%20Dart%20%7C%20Python-blue)]()  
[![License](https://img.shields.io/badge/License-To%20Define-lightgrey)]()  

---

## 1. Overview 

**AboNet** is an intelligent, hybrid cybersecurity framework designed to protect users from multimodal cyberbullying, deepfake-based harassment, and online stalking across mobile and web platforms.

Inspired by the Nagot/Yoruba concept **“ÀBÒ”** (protection, refuge), AboNet provides a **real-time digital shield** through the combined power of:

- Natural Language Processing (NLP)  
- Computer Vision (CV)  
- Graph-Based Behavioral Analysis  

AboNet supports multilingual detection (French, Fon, Yoruba/Nagot), ensures privacy-by-design, and aligns with **Benin’s Law No. 2018-20** on digital activities.

**Mission:** Enable early intervention, reduce psychological burden, and create safer digital environments for adolescents, women, and online communities.

---

## 2. Technical Description (Engineering)

### 2.1 Hybrid Architecture

AboNet includes multiple interoperable components:

- **Flutter/Dart Mobile Overlay App**  
  Real-time on-device content monitoring and user interactions.

- **Android AccessibilityService**  
  Automated screen text extraction, contextual actions, and proactive mitigation.

- **Chrome Browser Extension (Manifest V3)**  
  Web content scanning, NLP/CV-based threat detection, and alerting.

### 2.2 Detection Engine (Multimodal AI)

| Layer | Description |
|-------|-------------|
| **NLP** | Toxicity, harassment, threats, coded language, multilingual classification. |
| **CV** | Deepfake detection (faceswap, lip-sync), nudity/sexual fabrications, visual anomalies. |
| **Behavioral Analysis** | Pattern mining, multi-account suspicion, stalking detection using GNNs. |

### 2.3 Core Functionalities

- Real-time hybrid detection (< 1s).  
- Auto-block, auto-mute, smart masking.  
- “Refuge Mode”: Emergency protective environment.  
- Privacy-preserving evidence generation (secure local store).  
- Secure multilingual processing.

---

## 3. System Architecture (Mermaid Diagram)

```mermaid
flowchart TD
    A[Flutter Mobile App] --> C[Hybrid Detection Core]
    B[Chrome Extension] --> C
    D[Android AccessibilityService] --> C
    C --> E[NLP Engine]
    C --> F[Computer Vision Engine]
    C --> G[Graph Behavioral Module]
    C --> H[Mitigation Engine]
    H --> I[Auto-Block/Mask]
    H --> J[Refuge Mode]
    C --> K[Secure Evidence Store]


Key Use Cases

# - Detection of harassment on WhatsApp, Instagram, Facebook, (Messenger), TikTok, (X).

# - Automatic filtering of sexual deepfakes and harmful visual content.

# - Real-time alerts for parents, educators, and guardians (opt-in), users;.

# - Protection of minors and women against online abuse and stalking.

# - Forensic-ready privacy-preserving evidence generation.

#  Technology Stack

Mobile : Flutter 3.x (Dart)
AI Models : Transformers, DistilBERT, ViT, CNN Deepfake Detectors
Behavior : Graph Neural Networks
Browser : Chrome Extension v3
Security : AES-256, hardware-backed secure storage, hashing (SHA-256), 



| Phase | Milestone                                | Status      |
| ----- | ---------------------------------------- | ----------- |
| P1    | NLP + CV PoC                             | In progress |
| P2    | Chrome Extension Beta                    | Q1          |
| P3    | Mobile Overlay + AccessibilityService    | Q2          |
| P4    | Evidence System + Privacy Layer          | Q2          |
| P5    | Field Pilot (Schools, NGOs, Communities) | Q3          |
| P6    | Production Release                       | Q4          |
