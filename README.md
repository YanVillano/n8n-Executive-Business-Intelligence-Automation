# Executive Business Intelligence Bot

This workflow automatically collects KPI data from **Sales, Marketing, Support, and Finance**, calculates key metrics, generates executive insights using **OpenAI**, and sends reports via **Slack** and **Gmail** for business decisions.

---

## Triggers
- **Schedule Trigger Node:** Runs the workflow every day at 7AM.

---

## Nodes

### Google Sheets Nodes
- Retrieves data from the respective sheets for **Sales, Marketing, Support, and Finance**.

### Function Nodes (KPI Calculation)
- Calculates KPIs for each department individually:
  - **Sales:** Total revenue, total orders, average order value  
  - **Marketing:** Total spend, total leads, cost per lead  
  - **Support:** Total tickets, resolution rate, average response time  
  - **Finance:** Total expenses, total profit, profit margin

### Merge Node
- Combines all KPI outputs from the function nodes into a single stream.

### Function Node (Array Consolidation)
- Consolidates all KPI objects into one array for **OpenAI processing**.

### OpenAI Node
- Analyzes all KPIs and generates:
  - **Overall assessment**  
  - **Risks and opportunities** for business growth  
- Outputs a single, concise CEO-ready report.

### Slack Node
- Sends the AI-generated report to the designated Slack channel.

### Gmail Node
- Sends the same report via email to executives for business decisions.

---

## Workflow Summary
1. **Schedule Trigger** fires at 7AM.  
2. **Google Sheets nodes** retrieve data from all department sheets.  
3. **Function nodes** calculate KPIs for each department.  
4. **Merge node** combines all KPI objects.  
5. **Function node** consolidates them into a single array.  
6. **OpenAI node** analyzes KPIs and generates a summarized executive report.  
7. **Slack and Gmail nodes** deliver the report to stakeholders.

---

## Features
- Fully automated daily KPI reporting  
- Multi-department integration (Sales, Marketing, Support, Finance)  
- AI-generated insights with risks and opportunities  
- Delivery to Slack channels and email inboxes  
- Executive-ready summaries in a single concise message  
