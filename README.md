# Looker Agent 
## Created wtih Vertex AI Agent Builder, using Data Stores, OpenAPI, and powered by Gemini
This repository contains the configuration and instructions for setting up the Looker Agent in Vertex AI. This agent assists users with the Looker ecosystem, LookML, Looker dashboard issues, and SQL queries related to BigQuery.

**Table of Contents**
1. Repository Setup
2. Vertex AI Agent Configuration
3. Syncing the Agent with this Repository
4. Agent Handoff Instructions
5. Using the Looker and BigQuery Assistants
6. Contributing
---
## Repository Setup
- To clone this repository and set it up locally, run:
```
git clone git@github.com:doit/Looker_Agent.git
```
Ensure you have access to this repo. If not, request access from the repo owner.
### Vertex AI Agent Configuration
1. Export the Agent (optional):
- If you need to export your existing Vertex AI agent, follow these steps:
   - Navigate to your Vertex AI Console > Agents.
   - Export the agent configuration as a ZIP file for backup or transfer.
2. Import the Agent:
- To use this repository with a new Vertex AI agent:
   - Navigate to your Vertex AI Console > Agents.
   - Click Create New Agent or select an existing agent.
   - Under Settings, select GitHub as the repository source and link it to this repo:
     (git@github.com:doit/Looker_Agent.git).
3. Configure the Agent:
- Once the repo is linked, configure the agent’s behavior:
   - Set up intents, tools, and handoffs using the pre-defined instructions in the codebase.
   - Ensure the Looker Data Store and BigQuery Data Store tools are linked correctly.
### Syncing the Agent with this Repository
1. Sync the Repo with Vertex AI:
- Go to the Vertex AI Console > Agent Settings.
- Under the Repository section, ensure the repo `git@github.com:doit/Looker_Agent.git` is synced.
- Click Sync to pull the latest changes from the repository into Vertex AI.
2. Handling Updates:
- After syncing the repo with Vertex AI, any changes made to the repo (e.g., LookML instructions, tool configurations) will be reflected in the agent.
3. Collaborating:
- Multiple collaborators can work on the agent by committing changes to the GitHub repository. Pull requests and branching strategies are recommended for collaboration.
### Agent Handoff Instructions
This agent utilizes the following tools and handoffs:
1. Looker Assistant:
- Handles LookML syntax validation and dashboard troubleshooting using the Looker Data Store.
2. BigQuery Assistant:
- Handles SQL troubleshooting and query optimization using the BigQuery Data Store.
3. Default Generative Agent:
- Handles general queries and tasks using the OpenAPI and code-interpreter tools.
- Handoffs to either Looker or BigQuery Assistant based on user queries.
4. **Example Handoff:**
- If a query involves LookML, the agent will detect the keyword and trigger a handoff to the Looker Assistant.
- Example: "It sounds like you're asking about LookML. I’ll pass this to the Looker Assistant for help."
## Using the Looker and BigQuery Assistants
- Looker Assistant:
   - The Looker Assistant is designed to handle queries related to LookML and dashboards.
   - It uses the Looker Data Store to process requests and validate LookML models.
- BigQuery Assistant:
   - The BigQuery Assistant assists with SQL performance and troubleshooting.
   - It uses the BigQuery Data Store to handle optimization tasks.
### Contributing
We welcome contributions to improve the Looker Agent. To contribute:
1. Fork the repository.
2. Create a new branch for your feature or bugfix.
3. Submit a pull request with a detailed description of your changes.
## The Looker_Agent repository contains the following key files:
1.	README.md – Documentation for the project.
2.	agent.json – Configuration file for the Vertex AI agent.
3.	Flows:
- /flows/Default Start Flow/Default Start Flow.json – Likely contains the initial flow for the agent’s interactions.
4.	Generative Settings:
- /generativeSettings/en.json – Language or generative model settings for English.
5.	Intents:
- /intents/Default Negative Intent/Default Negative Intent.json – Intent configuration for negative responses.
- /intents/Default Welcome Intent/Default Welcome Intent.json – Welcome intent configuration.
- /intents/Default Welcome Intent/trainingPhrases/en.json – Training phrases for the welcome intent in English.
6.	Playbooks:
- /playbooks/Default Generative Agent/Default Generative Agent.json – Configuration for the Default Generative Agent playbook.
- /playbooks/LookML Syntax Assistant/LookML Syntax Assistant.json – Configuration for the LookML Syntax Assistant.
### Required Files Checklist:
- Agent Configuration: agent.json ✅
- Flows: Default Start Flow is present ✅
- Intents: Default Negative and Welcome Intents are present with training phrases ✅
- Playbooks: Both Default Generative Agent and LookML Syntax Assistant are present ✅
- Generative Settings: The generative settings file is present ✅
- README.md: Documentation is included ✅
## Roadmap:
1. Add Support for **Looker Studio Pro**
- Expand Toolset: Introduce a new tool, ${TOOL: Looker_Studio_Pro_Data_Store}, for handling Looker Studio Pro queries.
- Create Intents: Add Looker Studio Pro-specific intents, such as issues with report generation, dashboard syncing, and visualizations.
- Documentation: Store relevant Looker Studio Pro documentation and Zendesk support tickets in the Looker Studio Pro Data Store.
- API Integration: Integrate the Looker Studio API to provide real-time assistance for report issues.
2. Create a Datastore of **Zendesk Support Tickets**
- Zendesk API Access: Set up an ETL pipeline to extract, transform, and load Zendesk support tickets related to Looker, Looker Studio, and BigQuery into a BigQuery datastore.
- Train the AI: Use the datastore of past support tickets to train the agents for automated responses to common queries.
- Searchable Datastore: Allow support staff to search for tickets by **Issue, Resolution, or CSAT**.
3. Integrate with DoiT’s AI Chat, **Ava**
- Handoff Mechanism: Implement a system where the Vertex AI agents can escalate complex issues to Ava if they can’t resolve the queries.
- Cross-Agent Collaboration: Ensure seamless handoffs between the Vertex AI agent and Ava for deeper issue resolution.
4. Improve User Experience for **DoiT CREs**
- Automated Diagnostics: Enable the AI agents to pre-emptively diagnose issues based on Zendesk ticket history and suggest common fixes.
- Custom Recommendations: Train the AI on DoiT’s best practices for Looker, Looker Studio, and BigQuery to provide personalized troubleshooting suggestions. 
---
### Contact Information
![dionatdoit](https://github.com/user-attachments/assets/1f1db637-35c5-4f7c-bb95-8386c8d1e70e)
> For issues, reach out to the repo owner at dion@doit.com 
