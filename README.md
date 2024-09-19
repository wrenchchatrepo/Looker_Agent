# Looker Agent 

## Created wtih Vertex AI Agent Builder, using Data Stores, OpenAPI, and powered by Gemini 1.5 Flash

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

To clone this repository and set it up locally, run:

git clone git@github.com:wrenchchatrepo/Looker_Agent.git

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
     - Under Settings, select GitHub as the repository source and link it to this repo (git@github.com:wrenchchatrepo/Looker_Agent.git).

3. Configure the Agent:
   - Once the repo is linked, configure the agent’s behavior:
     - Set up intents, tools, and handoffs using the pre-defined instructions in the codebase.
     - Ensure the Looker Data Store and BigQuery Data Store tools are linked correctly.

### Syncing the Agent with this Repository

1. Sync the Repo with Vertex AI:
   - Go to the Vertex AI Console > Agent Settings.
   - Under the Repository section, ensure the repo (git@github.com:wrenchchatrepo/Looker_Agent.git) is synced.
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

**Example Handoff:**
- If a query involves LookML, the agent will detect the keyword and trigger a handoff to the Looker Assistant.
- Example: "It sounds like you're asking about LookML. I’ll pass this to the Looker Assistant for help."

## Using the Looker and BigQuery Assistants

- Looker Assistant:
  - The Looker Assistant is designed to handle queries related to LookML and dashboards.
  - It uses the Looker Data Store to process requests and validate LookML models.

- BigQuery Assistant:
  - The BigQuery Assistant assists with SQL performance and troubleshooting.
  - It uses the BigQuery Data Store to handle optimization tasks.

**Contributing**

We welcome contributions to improve the Looker Agent. To contribute:

1. Fork the repository.
2. Create a new branch for your feature or bugfix.
3. Submit a pull request with a detailed description of your changes.

---

### Contact Information

![dionatdoit](https://github.com/user-attachments/assets/1f1db637-35c5-4f7c-bb95-8386c8d1e70e)

For issues, reach out to the repo owner at dion@doit.com 
