# -Soundness-Layer-Setup-Update-Guide

Follow the steps below one by one to update your system and install Soundness Layer components.

✅ Step 1: Update Your System

```sh
sudo apt update && sudo apt upgrade -y
```
📥 Step 2: Install soundnessup

```sh
curl -sSL https://raw.githubusercontent.com/soundnesslabs/soundness-layer/main/soundnessup/install | bash
```

🦀 Step 3: Install Rust (Required for CLI tools)

```sh
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs/ | sh
```

After Rust installation, refresh your shell:

```sh
source ~/.bashrc
```
📦 Step 4: Install & Update Soundness Layer

```sh
soundnessup install
soundnessup update
```
🔑 Step 5: Import Your Key

Replace "<your‑mnemonic‑words>" with your actual 12- or 24-word mnemonic phrase.

```sh
soundness-cli import-key --name my-key --mnemonic "<your‑mnemonic‑words>"
```


✅ You're all set! Run soundness-cli --help to explore available commands.


🤖 Step 6: Generate Onchain Proof with Discord Bot

1.Copy the command given to you by the Soundness Discord bot.

2.Paste it into your terminal and run it to generate your onchain proof.

```sh
soundness-cli prove --challenge <your-challenge-code>
```

✅ Once it runs successfully, you'll see proof output or confirmation in your terminal.


📸 Step 7: Share the Screenshot

Take a screenshot of the successful proof generation and share it in the Telegram group for verification and rewards.

Need help? Join the Soundness community or raise an issue.

Let me know if you want this tailored for a specific OS (Ubuntu/Debian/Arch/etc.) or formatted as a shell script (install.sh).
