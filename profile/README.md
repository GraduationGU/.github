

# 🚀 AI-Powered Smart Freelance & Team Formation Platform

\<div align="center"\>

**An intelligent ecosystem to verify freelancer skills, detect cheating, and form synergistic teams using Knowledge Graphs.**

[Project Overview](https://www.google.com/search?q=%23-project-overview) • [Phase 1: CV Analysis](https://www.google.com/search?q=%23-phase-1-ai-cv-analysis-completed) • [Phase 2: Proctoring](https://www.google.com/search?q=%23-phase-2-ai-proctoring--interview-planned) • [Phase 3: Team Formation](https://www.google.com/search?q=%23-phase-3-knowledge-graph-team-formation-planned) • [Phase 4: Web Platform](https://www.google.com/search?q=%23-phase-4-full-stack-platform-planned)

\</div\>

-----

## 📖 Project Overview

This graduation project (2025-2026) aims to solve the "Trust Deficit" in the freelance market, specifically for the MENA region. Unlike traditional platforms that match keywords, our system verifies skills through **AI-proctored interviews** and uses a **Knowledge Graph** to recommend entire teams that work well together.

### Core Objectives

1.  **Verify:** Automate the extraction and validation of freelancer skills (Phase 1).
2.  **Secure:** Prevent cheating during technical assessments using Computer Vision (Phase 2).
3.  **Synergize:** Form high-performing teams based on "Skill Complementarity" and "Past Collaboration" (Phase 3).
4.  **Connect:** Provide a seamless web interface for clients and freelancers (Phase 4).

-----

## ✅ Phase 1: AI CV Analysis (Completed)

**The "Input Layer" of the system.**

This module is the data ingestion engine. It transforms unstructured PDF resumes into structured, scored entities (Skills, Projects, Experience) that feed the Knowledge Graph.

### Key Features

  * **Layout-Aware Ingestion:** Uses `PyMuPDF` to read resumes by "Zones" (Header vs. Body), solving the issue of complex PDF layouts.
  * **Semantic Scoring:** Implements **S-BERT** to score candidates based on vector similarity to a target role (e.g., "React" is semantically close to "Frontend").
  * **Entity Mining:** Automated extraction of 300+ technical skills using fine-tuned BERT models (`dslim/bert-base-NER`).
  * **Structured Output:** Generates clean JSON payloads ready for Neo4j.

### Tech Stack (Phase 1)

  * **Language:** Python 3.9+
  * **Libraries:** `PyMuPDF` (Parsing), `Transformers` (NER), `Sentence-Transformers` (Scoring), `SpaCy` (Date Parsing).

> **[View Detailed Phase 1 Documentation](https://www.google.com/search?q=./cv_analysis_module/README.md)** *(Link to the specific module README)*

-----

## 🚧 Phase 2: AI Proctoring & Interview (Planned)

**The "Verification Layer" of the system.**

To ensure the skills extracted in Phase 1 are genuine, candidates must pass a secure technical assessment. This phase builds the **Anti-Cheat System**.

### Key Features

  * **Identity Verification:** Face detection to ensure the person taking the test is the freelancer.
  * **Gaze Tracking:** Computer Vision (OpenCV/MediaPipe) to detect if the user is looking away/reading notes.
  * **Person Detection:** Flags the session if multiple people are detected in the frame.
  * **Environment Lock:**
      * **Tab-Lock:** Quiz auto-fails if the user switches browser tabs.
      * **Audio Monitoring:** Detects background voices whispering answers.

### Tech Stack (Phase 2)

  * **Computer Vision:** OpenCV, MediaPipe (Face Mesh).
  * **Frontend:** React.js (WebRTC for camera access).
  * **Backend:** FastAPI (Real-time socket processing).

-----

## 🔮 Phase 3: Knowledge Graph Team Formation (Planned)

**The "Intelligence Layer" of the system.**

Once we have verified data (Phase 1 & 2), we populate the Graph Database to perform complex team recommendation queries.

### Key Features

  * **Graph Modeling:** Nodes = Freelancers, Skills, Projects. Edges = `[HAS_SKILL]`, `[WORKED_WITH]`, `[COMPLEMENTS]`.
  * **Synergy Scoring:** Algorithms to predict how well a group will work together based on past collaborations.
  * **Contextual Relevance:** Understanding that a "Senior Dev" is needed for a "Large Scale Project."

### Tech Stack (Phase 3)

  * **Database:** Neo4j (Graph DB).
  * **Query Language:** Cypher.
  * **Algorithms:** Community Detection, Path Finding (Dijkstra).

-----

## 💻 Phase 4: Full-Stack Platform (Planned)

**The "User Interface Layer" of the system.**

The final deliverable is a responsive web application that brings all modules together.

### Key Features

  * **Freelancer Dashboard:** Upload CV, take AI Interview, view Profile Score.
  * **Client Dashboard:** Post jobs, view "Team Recommendations," manage contracts.
  * **Admin Panel:** Monitor proctoring logs and system health.

### Tech Stack (Phase 4)

  * **Frontend:** Next.js (React) + Tailwind CSS.
  * **Backend:** Django / FastAPI.
  * **Auth:** JWT Authentication.
  * **Deployment:** Docker, AWS/Azure.

-----

## 📂 Project Structure

```
.
├── cv_analysis_module/       # ✅ PHASE 1: Complete
│   ├── ml_parser.py
│   ├── smart_analyzer.py
│   └── ...
├── ai_proctoring_module/     # 🚧 PHASE 2: In Progress
│   ├── gaze_tracker.py
│   └── ...
├── knowledge_graph_service/  # 🔮 PHASE 3: Future
│   ├── schema.cypher
│   └── ...
├── web_platform/             # 💻 PHASE 4: Future
│   ├── frontend/
│   └── backend/
└── README.md                 # This file
```

-----

## 🛠️ Installation (Phase 1 Only)

To test the currently completed **CV Analysis Module**:

```bash
# 1. Clone the repo
git clone https://github.com/yourusername/ai-freelance-platform.git

# 2. Navigate to module
cd cv_analysis_module

# 3. Install dependencies
pip install -r requirements.txt

# 4. Run a test
python -m test_parser my_resume.pdf
```

-----

## 📜 License

This project is licensed under the MIT License - see the [LICENSE](https://www.google.com/search?q=LICENSE) file for details.

-----

\<div align="center"\>
\<sub\>2025-2026 Graduation Project | Supervised by Dr. Safa Elaskary\</sub\>
\</div\>
