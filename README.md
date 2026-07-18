# NovaPath AI Matching & Automation Orchestrator

An automated, event-driven AI workflow engine designed to ingest job descriptions and candidate resumes, normalize unstructured text payloads, execute contextual skill alignment checks, and generate a deterministic compatibility score. 

## 🧠 System Architecture & Data Flow
The orchestration pipeline is designed using node-based micro-services divided into four critical phases:
1. **Ingestion Layer:** Programmatic extraction triggers fetching parallel asynchronous payloads from cloud filesystems (Google Sheets/Data Tables).
2. **Data Normalization Layer:** Isolated JavaScript nodes (`Normalized_JD` and `Normalized_Cand`) sanitize, format, and structure text blocks to minimize downstream LLM context contamination.
3. **Algorithmic Evaluation Loop:** Iterative data routing engines loop over individual matching candidates, batching payloads dynamically to evaluate capabilities.
4. **AI Scoring Engine:** Contextual prompt engineering wraps incoming records to return high-confidence matching matrix scores alongside concise profile summaries.

## 🛠️ Infrastructure Stack
- **Orchestration Engine:** n8n Workflow Automation Engine
- **Processing Layer:** Custom JavaScript (Node.js Execution blocks)
- **AI Integration:** OpenAI / Anthropic API Connectors

## 📂 Repository Contents
- `/workflows/novapath_matcher.json`: The full production blueprint file containing all system nodes, execution paths, and data-transformation schemas.

## 🚀 Deployment Instructions
To replicate this engine inside your own architecture:
1. Clone this repository.
2. Open your local or cloud n8n workspace instances.
3. Select **Import from File** from the workflow settings menu and upload `novapath_matcher.json`.
4. Populate your environment variables and API credentials.
