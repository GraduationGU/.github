# 🚀 AI-Powered Smart Freelance & Knowledge-Based Team Formation Platform

<div align="center">

![Version](https://img.shields.io/badge/version-1.0.0-blue.svg)
![License](https://img.shields.io/badge/license-MIT-purple.svg)
![Status](https://img.shields.io/badge/status-in%20development-orange.svg)

**An intelligent ecosystem to verify freelancer skills, detect cheating, and form synergistic teams using AI and Knowledge Graphs.**

[Project Overview](#-project-overview) • [Phases](#-project-phases) • [Tech Stack](#-tech-stack) • [Installation](#️-installation) • [Project Structure](#-project-structure) • [License](#-license)

</div>

---

## 📖 Project Overview

This 2025-2026 graduation project addresses the "Trust Deficit" in the MENA freelance market by going beyond keyword matching. Traditional platforms like Upwork or Mostaql often lead to mismatched hires due to unverified skills and poor team synergy. Our system uses AI to verify competencies, prevent cheating, and recommend cohesive teams via a Knowledge Graph.

### Core Objectives
1. **Verify Skills**: Automate extraction and validation from resumes (Phase 1).
2. **Secure Assessments**: Use computer vision to ensure genuine interviews (Phase 2).
3. **Synergize Teams**: Leverage graph-based algorithms for optimal team recommendations (Phase 3).
4. **Connect Users**: Build a user-friendly web platform for seamless interactions (Phase 4).

### Key Innovations
- **AI-Driven Verification**: Combines NER models and semantic scoring for accurate skill extraction.
- **Anti-Cheating Mechanisms**: Real-time monitoring to maintain integrity.
- **Knowledge Graph**: Models freelancers, skills, and projects for contextual team matching.
- **MENA Focus**: Tailored for regional needs, including multi-lingual support (Arabic/English).

---

## 📅 Project Phases

The project is divided into four iterative phases, with Phase 1 fully completed and serving as the foundation.

### ✅ Phase 1: AI CV Analysis (Completed)
The "Input Layer" transforms unstructured PDFs into structured, scored data for the Knowledge Graph.

**Key Features**:
- Layout-aware parsing with zone detection (headers, sections, bullets).
- Semantic scoring using S-BERT for role matching.
- Entity extraction for 300+ skills via fine-tuned BERT (e.g., `dslim/bert-base-NER`).
- JSON output for easy integration.

**Tech Stack**: Python 3.9+, PyMuPDF, Transformers, Sentence-Transformers, SpaCy.

For detailed documentation, see the [AI CV Analysis Module README](./cv_analysis_module/README.md).

### 🚧 Phase 2: AI Proctoring & Interview (Planned)
The "Verification Layer" ensures skills are genuine through secure assessments.

**Key Features**:
- Identity verification and gaze tracking via computer vision.
- Multi-person detection and audio monitoring.
- Tab-lock and environment controls to prevent cheating.

**Tech Stack**: OpenCV, MediaPipe, React.js (WebRTC), FastAPI (real-time sockets).

### 🔮 Phase 3: Knowledge Graph Team Formation (Planned)
The "Intelligence Layer" enables smart team recommendations.

**Key Features**:
- Graph modeling: Nodes (Freelancers, Skills, Projects); Edges (HAS_SKILL, WORKED_WITH, COMPLEMENTS).
- Synergy scoring based on collaboration history and skill complementarity.
- Contextual matching for project scale and requirements.

**Tech Stack**: Neo4j (Graph DB), Cypher queries, Community Detection algorithms.

### 💻 Phase 4: Full-Stack Web Platform (Planned)
The "User Interface Layer" integrates all components.

**Key Features**:
- Freelancer Dashboard: CV upload, AI interviews, profile scoring.
- Client Dashboard: Job posting, team recommendations, contract management.
- Admin Panel: Proctoring logs and system monitoring.

**Tech Stack**: Next.js + Tailwind CSS (Frontend), Django/FastAPI (Backend), JWT Auth, Docker for deployment.

---

## 🛠️ Tech Stack

| Component | Technologies |
|-----------|--------------|
| **Language** | Python 3.9+ |
| **AI/ML** | Transformers, Sentence-Transformers, OpenCV, MediaPipe |
| **Databases** | Neo4j (Knowledge Graph) |
| **Frontend** | Next.js, React.js, Tailwind CSS |
| **Backend** | FastAPI/Django |
| **Deployment** | Docker, AWS/Azure |
| **Other** | PyMuPDF, SpaCy, WebRTC, JWT |

---

## 🛠️ Installation (Phase 1 Only)

To get started with the completed CV Analysis Module:

```bash
# 1. Clone the repository
git clone https://github.com/yourusername/ai-freelance-platform.git

# 2. Navigate to the module
cd ai-freelance-platform/cv_analysis_module

# 3. Install dependencies
pip install -r requirements.txt

# 4. Run a test
python -m test_parser my_resume.pdf
```

For full usage examples, refer to the [Phase 1 README](./cv_analysis_module/README.md).

---

## 📂 Project Structure

```
.
├── cv_analysis_module/          # ✅ Phase 1: Complete
│   ├── README.md                # Detailed module docs
│   ├── ml_parser.py             # Core ML parser
│   ├── smart_analyzer.py        # Role scoring and analysis
│   ├── training_utils.py        # Model training tools
│   ├── robust_parser.py         # Rule-based fallback
│   ├── llm_parser.py            # Optional LLM parser
│   ├── test_parser.py           # Testing script
│   └── requirements.txt          # Dependencies
├── ai_proctoring_module/        # 🚧 Phase 2: Planned
│   ├── gaze_tracker.py
│   └── ...                      # (To be added)
├── knowledge_graph_service/     # 🔮 Phase 3: Planned
│   ├── schema.cypher
│   └── ...                      # (To be added)
├── web_platform/                # 💻 Phase 4: Planned
│   ├── frontend/                # Next.js app
│   └── backend/                 # FastAPI/Django server
├── docs/                        # Additional documentation
├── LICENSE                      # MIT License
└── README.md                    # This file
```

---

## 📈 Roadmap & Milestones

- **Q4 2025**: Complete Phase 1 (Done ✅).
- **Q1 2026**: Implement Phase 2 proctoring.
- **Q2 2026**: Build Phase 3 Knowledge Graph.
- **Q3 2026**: Launch Phase 4 web platform.
- **Q4 2026**: Full integration, testing, and deployment.

---

## 📜 License

This project is licensed under the MIT License - see the [LICENSE](./LICENSE) file for details.

<div align="center">
<sub>2025-2026 Graduation Project | Supervised by Dr. Safa Elaskary</sub>
</div>
