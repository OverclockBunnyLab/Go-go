# Codex + DeepSeek (iPad / GitHub Codespaces)

This repository is a standalone workspace for running Codex CLI with DeepSeek from an iPad browser. It does **not** change the model used by the ChatGPT app or the hosted Codex service.

## 1. Start a Codespace
Open this repository on GitHub, choose **Code → Codespaces → Create codespace on main**. Open the terminal in the browser.

## 2. Install Codex CLI
Run:
```bash
npm install -g @openai/codex@latest
codex --version
```

## 3. Configure DeepSeek
Review the current [official DeepSeek Codex instructions](https://api-docs.deepseek.com/quick_start/agent_integrations/codex/) before running their setup script. The remote script can change; don't execute it without checking it.

You can inspect the English setup script first:
```bash
curl -fsSL https://cdn.deepseek.com/api-docs/codex-deepseek-setup-en.sh -o /tmp/codex-deepseek-setup.sh
less /tmp/codex-deepseek-setup.sh
```
If it looks correct, execute:
```bash
bash /tmp/codex-deepseek-setup.sh
```
Follow the prompts to choose a model and configure authentication. Obtain the API key only from the official DeepSeek platform. **Never commit API keys, .env files, or ~/.codex credentials.** Treat Codespace secrets as sensitive.

## 4. Verify
```bash
codex
```
Confirm the configured model in Codex, then try a harmless test prompt. If authentication or model selection fails, inspect the Codex configuration and the latest official integration documentation.

## Notes
- GitHub Codespaces and DeepSeek API may incur charges.
- The GitHub connector can edit repository files but cannot start a Codespace or run terminal commands.
- Do not put an API key in a GitHub issue, commit, README, or chat.
