# Setting up and Running Uncensourced Dolphin-Mixtral Using Ollama on Windows Subsystem for Linux (WSL)

## 1. Enable WSL

Open an Administrator PowerShell and execute the following command:

```bash
wsl --install
```

Restart your computer if prompted.

## 2. Set Up WSL Environment

After the system restarts, open a WSL terminal window and update your Linux distribution:

```bash
sudo apt update -y && sudo apt full-upgrade -y
```

## 3. Install Ollama

Still in the WSL environment, run the following command to download and install Ollama:

```bash
curl -fsSL https://ollama.com/install.sh | sh
```

## 4. Run Ollama

Start the model by entering:

```bash
ollama run dolphin-mixtral:latest
```

Wait for the offline files to download. Once complete, a `>>>` prompt should appear, indicating that the model is ready for use.

## Usage

### Interact with the Model

Simply type your prompts at the `>>>` prompt in the terminal to interact with the model.

### Restart Ollama

If you need to start the model again after closing the terminal, open WSL and enter:

```bash
ollama run dolphin-mixtral:latest
```

## Shutting Down

To completely shut down Ollama and free up resources, follow these steps:

### 1. Close Ollama

In the WSL environment:

- If the `>>>` prompt is active, type `/bye` to exit.
- Type `exit` to close the terminal.

### 2. Shutdown WSL

Return to an Administrator PowerShell and execute:

```bash
wsl --shutdown
```

This will ensure that WSL and Ollama are completely shut down, conserving system resources.
