[[_TOC_]]

# Local LLM using Ollama

This tutorial enables local LLMs - AI-powered text generation without relying on cloud services.

<br>
Steps to set up and use a local LLM with Ollama:

- **Download Ollama** – Visit ollama.com and download the installer for Windows (OllamaSetup.exe) or macOS.
- **Install Ollama** – Run the installer and complete the installation. It will run as a background service.
- **Verify Installation** – Open the terminal (Command Prompt, PowerShell, or macOS Terminal) and check the version using `ollama --version`. Initially, no models will be available (`ollama list`).
- **Download a Model** – Browse available models on Ollama's site and use `ollama pull <model_name:tag>` in the terminal to download a model. Suggested starter models: gemma:2b, tinyllama, qwen:0.5b.
- **Run & Chat with a Model** – Start an interactive session using `ollama run <model_name:tag>`, type messages, and receive responses. Exit with `/bye` or **Ctrl+D**.
- **Manage Models** – List installed models (ollama list) and remove unnecessary ones (`ollama rm <model_name:tag>`).


## Step 1 - Download Ollama

* **Go to the Official Website:** `ollama.com`
* Click **Download** button

    * **Windows:** Click the "Download for Windows" link. The download will begin for the installer (`OllamaSetup.exe`).
    * **Mac:** The site should automatically detect macOS and offer the correct download. Click the "Download for Macos" button. The download will begin for the installer.

---

## Step 2 - Install Ollama

* **Run the Installer:** Locate and double-click the downloaded installer.
* **Installation Process:**

    * Usually a straightforward process.
    * **Windows:** Accept any User Account Control (UAC) prompts.
* **Background Service:** Ollama installs and runs as a background service. You might see an Ollama icon in your system tray.

---

## Step 3 - Verify Installation

* **Open Your Terminal:**

    * **Windows:** Command Prompt (Search for `cmd`) OR PowerShell (Search for `PowerShell`)
    * **Mac:** Terminal (Applications/Utilities)
* **Check Ollama Version:**

    * Type: `ollama --version`
    * The following is the output example

```bash
ollama version is 0.6.6
```
* **List Available Models (will be empty initially):**

    * Type: `ollama list`
    * Expected: Output indicating no models are currently available.

---

## Step 4 - Pull (Download) Your First LLM Model

* Goto `ollama.com`, click **Model** button to list all the available LLM models
* At the **command prompt or terminal**, **The `pull` Command:** `ollama pull <model_name:tag>`
* **Choosing a Starter Model:**

    * Recommend a smaller, faster model for the first try.
    * Examples:

        * `ollama pull gemma:2b` (Google's Gemma 2 billion parameters)
        * `ollama pull tinyllama` (A very small, fast model)
        * `ollama run qwen3:0.6b` (Another small option)
* **Process:**

    * Ollama will download the model layers. Progress will be shown in the terminal.
    * This can take time depending on model size and internet speed.


---

## Step 5 - Run & Chat with Your Model

* **The `run` Command:** `ollama run <model_name:tag>`

    * Example: `ollama run qwen3:0.6b`
* **Interactive Chat:**

    * This command starts an interactive session directly in your terminal.
    * You'll see a prompt like `>>>`.
    * Type your questions or prompts and press Enter.
* **Example Interaction:**

    * `>>> Apa maksud slogan "Salam Malaysia Madani", rumuskan dalam 100 perkataan`
    * The following is the response example

<img src="/uploads/d7efcc748e953746839f089602e94a01/image.png">

* **Exiting Chat:** Type `/bye` and press Enter, or use `Ctrl+D`.

---

## Step 6 - Managing Your LLM Models

* **List Installed Models:**

    * Command: `ollama list`
    * Shows: Name, ID, Size, and when it was modified.
* **Remove a Model (to free up space):**

    * Command: `ollama rm <model_name:tag>`
    * Example: `ollama rm gemma:2b`

---

