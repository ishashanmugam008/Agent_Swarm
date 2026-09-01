# Boardroom Multi-Agent Swarm (FinSwarm / Boardroom Decision-Making)

## 1. Team Name and Member Names
* **Team Name:** [Insert Team Name]
* **Members:** Isha S(25MID1083)
               Hasini CH (25MID1071)
               Sri Bavani AP (25MID1087)

## 2. Selected Challenge and One-Paragraph Solution Summary
* **Selected Challenge:** FinSwarm (TC1 Baseline) — Optimizing a INR 30 crore small-business lending pilot and INR 60 lakh customer acquisition budget for FinNova Capital.
* **Solution Summary:** This project implements an automated multi-agent boardroom decision workflow built in n8n paired with a custom real-time frontend dashboard. The system processes complex business briefs sequentially and in parallel through specialized departmental agents (Research, Finance, Marketing, Challenger, and Strategy Synthesizer) before synthesizing a final executive directive via a CEO agent. It provides live node execution tracking and translates raw agent outputs into structured, human-readable insights.

## 3. Agent List with Roles, Inputs, and Outputs
| Agent Name | Role | Input | Output |
| :--- | :--- | :--- | :--- |
| **Research Agent** | Gathers market, sector, and trend intelligence. | Business challenge brief & baseline state | Qualitative intelligence report & market parameters |
| **Finance & Risk Agent** | Analyzes capital allocation, Cost of Funds (CoF), and risk metrics. | Research findings & financial constraints | Pro-forma figures, risk analysis, and unit economic constraints |
| **Marketing Agent** | Evaluates customer acquisition cost (CAC) and segment strategy. | Financial targets & business challenge | Target segment mix and channel acquisition plans |
| **Challenger / Red Team Agent** | Stress-tests department assumptions and identifies vulnerabilities. | Combined department proposals | Critical feedback, risk flags, and alternative risk caveats |
| **Strategy Synthesizer Agent** | Combines inputs and critical feedback into cohesive options. | Department notes & Challenger critiques | Unified strategic roadmap options |
| **CEO Agent** | Evaluates options and issues the final executive decision. | Synthesized strategic options | Final decision, roadmap steps, trade-offs, and business KPIs |

## 4. Installation and Execution Instructions
1. **Import n8n Workflow:**
   * Open your n8n instance.
   * Go to **Workflows -> Import from File** and upload the provided workflow JSON file (`n8n_workflow.json`).
   * Ensure your Groq or Gemini API credentials are correctly configured inside the AI nodes.
2. **Launch Frontend Dashboard:**
   * Open the `index.html` file in any modern web browser.
3. **Execute Analysis:**
   * In n8n, make sure your workflow is active or click **Listen for Test Event** on the Webhook node.
   * In the browser dashboard, select your theme, test case ID, enter the challenge, and click **Run Agentic Swarm**.

## 5. Models, Frameworks, Datasets and External Services Used
* **Workflow Automation Engine:** n8n (Self-hosted or Cloud)
* **LLM Provider / Models:** Groq API / Google Gemini (via n8n Advanced AI nodes)
* **Frontend:** Vanilla HTML5, CSS3, and JavaScript (Async Fetch API)
* **Dataset / Domain:** FinSwarm financial lending case parameters (TC1 baseline data)

## 6. Known Limitations and Failure-Handling Behaviour
* **Limitations:** Execution speed relies entirely on external LLM provider API response times (approx. 15–30 seconds for full swarm completion).
* **Failure-Handling:** The n8n workflow incorporates fallback routing nodes (`Node 7: Fallback Handler`) to catch parsing anomalies or missing parameters and pass fallback text states down the pipeline without crashing execution.

## 7. Declaration of Pre-Existing or Reused Components
* Built using native n8n AI agent nodes and standard web UI templates developed specifically for this multi-agent decision architecture. No external proprietary code templates were reused.# Agent_Swarm
