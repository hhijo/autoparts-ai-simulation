# autoparts-ai-simulation
📂 Project Overview

AutoParts Inc., a mid-sized automotive parts manufacturer, faces challenges such as high defect rates, unpredictable machine downtime, labor shortages, and increasing customer demands. This project demonstrates how AI Agents can be implemented to automate quality control, predictive maintenance, and production scheduling.

To simulate this, I built a multi-agent workflow using n8n, integrating three AI-driven agents:

Quality Control Agent

Predictive Maintenance Agent

Scheduling Optimization Agent

The agents pass data sequentially, mimicking a real smart factory pipeline.

🤖 AI Agent Architecture
1. Quality Control Agent

Input: Sensor readings, component data

Output:

{
  "defect_probability": 0.0-1.0,
  "defect_type": "string",
  "recommended_action": "string"
}

2. Predictive Maintenance Agent

Input: QC Agent results

Output:

{
  "failure_risk": "low | medium | high",
  "predicted_hours_to_failure": number,
  "recommended_maintenance": "string"
}

3. Scheduling Optimization Agent

Input: QC + Maintenance results

Output:

{
  "shift_priority": "high/medium/low",
  "machine_assignment": "string",
  "production_speed_adjustment": "string",
  "urgency_level": "string"
}

🔧 Simulation Using n8n

This project includes a fully configured n8n workflow, which simulates the entire AI agent process.

✔ Included in this repository:

autoparts-ai-agents-workflow.json

Instructions on how to import

Optional webhook trigger

Prompts inside each AI agent node

🔗 Simulation Link (n8n)

(Add your n8n public workflow link here after publishing.)

Example:

https://app.n8n.cloud/workflow/your-workflow-link

🚀 How to Run the Simulation
1. Import Workflow

In n8n:

Menu → Import from File → autoparts-ai-agents-workflow.json

2. Add OpenAI Credentials

Each agent node requires your OpenAI API key:

Credentials → Add New → OpenAI API → Paste API Key

3. Execute Workflow

Click:

Execute Workflow


You will see the output from all three agents as JSON.

📊 Results & Expected Impact
Quantitative Benefits

Reduce defect rate from 15% → 5%

Reduce machine downtime by 30–40%

Increase throughput by 20%

Estimated ROI: 18–24% within year one

Qualitative Benefits

Better decision-making

Faster customer order turnaround

Improved worker safety

Higher manufacturing consistency

⚠️ Risks & Mitigation
Risk	Mitigation
Data quality errors	Introduce validation layer in n8n
Overreliance on AI outputs	Keep human approval for high-risk decisions
Model drift	Schedule retraining every 3–6 months
Ethical transparency	Maintain explainability logs
