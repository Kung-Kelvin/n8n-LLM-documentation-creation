# n8n-LLM-documentation-creation
LLM implementation for creating documentations (Docx, PDF, and PPT)

Tools:
- [Claude Code 2.0.35](https://code.claude.com/docs/ja/overview)
  - Some sources present this as a better **coding** and **writing** alternative than GPT 
  - Couldn't proceed with testing. Requires Claude Mxx or Pro account [See subscription](https://claude.ai/upgrade)
- [N8N 1.118.2](https://docs.n8n.io)
  - Creating automations workflows
- [ngrok](https://ngrok.com/docs/what-is-ngrok)
  -  For providing a HTTP for public exposure of codespace environment

# Codes
|Tool|Step|Code|
|---|---|---|
|Claude Code|Installation|`curl -fsSL https://claude.ai/install.sh \| bash`|
|Claude Code|Start Runtime|`claude`|
|ngrok|Installation|```curl -sSL https://ngrok-agent.s3.amazonaws.com/ngrok.asc \| sudo tee /etc/apt/trusted.gpg.d/ngrok.asc >/dev/null \  && echo "deb https://ngrok-agent.s3.amazonaws.com bookworm main" \| sudo tee /etc/apt/sources.list.d/ngrok.list \  && sudo apt update \  && sudo apt install ngrok```|
|ngrok|Login|`ngrok config add-authtoken $YOUR_AUTHTOKEN`|
|ngrok|Start Runtime|`ngrok HTTP <desired port>`|
|ngrok|*optional* setting webhook for N8N|`export WEBHOOK_URL=<obtained HTTP address>`|
|N8N|Installation|`npm install n8n -g`|
|N8N|Check Version|`n8n --version`|
|N8N|Start Runtime|`n8n start`|

<!--export WEBHOOK_URL=https://hypophosphorous-pseudomoralistic-rhys.ngrok-free.dev-->

## Claude Code
### First Run
It'll ask for the prefered theme (light or dark theme) and ask for credentials

![Screenshot of login](images/claude_code_login)

## N8N

## ngrok
Doesnt work with fortinet? networks