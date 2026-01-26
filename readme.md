## Open Code + Qwen3 over Qwen OAuth Login

Configure Open Code to route requests through Qwen via OAuth authentication.

### Setup Instructions
1. Install Qwen and login with QR-code:
    ```bash
    npm install -g npm@11.7.0 && npm install -g @qwen-code/qwen-code@latest
    qwen
    ```
2. Install Open Code and copy configuration:
    ```bash
    curl -fsSL https://opencode.ai/install | bash
    ```
3. Update your API key in `/{YOUR_CURREN_PROJECT_FOLDER}/opencode.json` for Qwen from the `~/.qwen/oauth_creds.json` (refresh_token)

   Or just call:
    ```bash
    export QWEN_API_KEY=$(cat ~/.qwen/oauth_creds.json | grep access_token | awk -F '"' '{print $4}')
    ```
4. Run:
    ```bash
    opencode
    ```
