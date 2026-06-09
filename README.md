# Multi-Agent Research Assistant Using AutoGen (Gemini)

An automated, multi-agent academic research assistant built with AutoGen (v0.4+) and Google Gemini 3.1 Flash Lite that refines topics, searches arXiv, synthesizes insights, compiles reports, and checks for research gaps and areas for future development with human-in-the-loop approval.

---

## 🛠️ Key Features

*   **Interactive Topic Refinement:** Dynamic negotiation between the `topic_refinement_agent` and the user.
*   **Human-in-the-Loop (HITL) Control:** Programmatic control using a custom selector function to ensure a human approves the topic before searching papers.
*   **Automated Research Retrieval:** Custom tool integration with the arXiv API to pull relevant papers using XML parsing.
*   **Structured Knowledge Synthesis:** Sequential routing to specialized agents for insight extraction, report compilation, and research gap identification.

## 🏗️ Multi-Agent Architecture
*   **Topic_refinement_agent:** Refines a broad user topic into a focused, concrete research question.
*   **UserProxyAgent:** Intercepts the flow to prompt the user for "APPROVE" or "DISAPPROVE".
*   **Paper_discovery_agent:** Executes the arxiv_search_tool to retrieve relevant publications.
*   **Insight_synthesizer_agent:** Extracts core findings and methodological insights from raw papers.
*   **Report_compiler_agent:** Outlines and drafts a coherent research report.
*   **Gap_analysis_agent:** Evaluates synthesized papers to propose areas for future academic development.

## 🚀 Getting Started

**1. Clone the Repository** 
```bash
git clone <your-repository-url>
cd <your-repository-folder>
```

**2. Set up a Virtual Environment**
```bash 
python -m venv venv
source venv/bin/activate  # On Windows, use: venv\Scripts\activate
```

**3. Install Dependencies**
```bash
pip install -r requirements.txt
```


**4. Configure Environment Variables**
```bash
cp .env.example .env
```