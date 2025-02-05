# Self-hosted AI Starter Kit

**Self-hosted AI Starter Kit** is an open-source Docker Compose template designed to quickly set up a powerful local AI and automation environment.

![SatoshiOnBTC.com - Screenshot](https://raw.githubusercontent.com/satoshionbtc/ai-starter-kit/main/assets/demo.gif)

Developed by <https://github.com/satoshionbtc>, this kit integrates self-hosted automation with a carefully curated list of AI tools and components to streamline the creation of intelligent workflows.

### What’s Included

✅ [**Self-hosted Workflow Automation**](https://satoshionbtc.com/) - A flexible, low-code platform supporting a vast range of integrations and AI functionalities.

✅ [**Ollama**](https://ollama.com/) - A cross-platform LLM platform for deploying and running the latest local AI models.

✅ [**Qdrant**](https://qdrant.tech/) - A high-performance, open-source vector database with an intuitive API.

✅ [**PostgreSQL**](https://www.postgresql.org/) - A powerful, reliable database for handling large-scale data processing.

### What You Can Build

⭐ **AI-powered Scheduling Assistants** to manage appointments.

⭐ **Secure PDF Summarization** without data privacy concerns.

⭐ **Enhanced Chatbots for Business Communications** using AI automation.

⭐ **Efficient Financial Document Analysis** with cost-effective processing.

## Installation

### Cloning the Repository

```bash
git clone https://github.com/satoshionbtc/self-hosted-ai-starter-kit.git
cd self-hosted-ai-starter-kit
```

### Running with Docker Compose

#### For Nvidia GPU Users

```bash
git clone https://github.com/satoshionbtc/self-hosted-ai-starter-kit.git
cd self-hosted-ai-starter-kit
docker compose --profile gpu-nvidia up
```

> **Note:** If using an Nvidia GPU with Docker for the first time, refer to the [Ollama Docker Guide](https://github.com/ollama/ollama/blob/main/docs/docker.md).

#### For Mac / Apple Silicon Users

If running on an Apple Silicon Mac, GPU acceleration isn't available within Docker. You can:

1. Run the kit fully on CPU.
2. Install Ollama directly on your Mac for faster AI inference and connect it to the automation system.

To use Ollama on your Mac, check the [Ollama homepage](https://ollama.com/) for installation instructions and then run:

```bash
git clone https://github.com/satoshionbtc/self-hosted-ai-starter-kit.git
cd self-hosted-ai-starter-kit
docker compose up
```

After setup, update the Ollama credentials to `http://host.docker.internal:11434/` for seamless integration.

#### For Other Users

```bash
git clone https://github.com/satoshionbtc/self-hosted-ai-starter-kit.git
cd self-hosted-ai-starter-kit
docker compose --profile cpu up
```

## Quick Start & Usage

This starter kit is built around a Docker Compose setup, pre-configured with essential networking and storage configurations for a smooth AI development experience.

1. Open <http://localhost:5678/> in your browser for initial setup.
2. Load the workflow at <http://localhost:5678/workflow/example>.
3. Click **Run Workflow** to begin processing.
4. If it's the first run, you might need to wait for model downloads, which you can track via Docker logs.

To access the automation system anytime, visit <http://localhost:5678/>.

For enhanced AI capabilities, use the built-in automation features with tools such as:
- **AI Agents** for automated decision-making
- **Text Classification** for structured data processing
- **Information Extraction** for advanced analytics

## Upgrading

### For Nvidia GPU Users

```bash
docker compose --profile gpu-nvidia pull
docker compose create && docker compose --profile gpu-nvidia up
```

### For Mac / Apple Silicon Users

```bash
docker compose pull
docker compose create && docker compose up
```

### For Non-GPU Setups

```bash
docker compose --profile cpu pull
docker compose create && docker compose --profile cpu up
```

## Additional Resources

For troubleshooting, guides, and best practices, visit the [SatoshiOnBTC Community](https://community.satoshionbtc.com/).

### Learn AI Key Concepts

- [Building AI Assistants](https://satoshionbtc.com/workflows/ai-assistant)
- [Document-based AI Analysis](https://satoshionbtc.com/workflows/document-ai)
- [Custom AI Chatbots](https://satoshionbtc.com/workflows/custom-chatbots)

## File Access Tips

The kit automatically creates a shared folder for handling local files. Inside the automation container, this directory is located at `/data/shared`, making it accessible for nodes interacting with the filesystem.

**File Handling Nodes:**
- Read/Write local files
- Trigger actions on file changes
- Execute shell commands within workflows

## License

This project is licensed under the Apache License 2.0 - see the [LICENSE](LICENSE) file for more details.

## Community & Support

Join discussions in the [SatoshiOnBTC Forum](https://community.satoshionbtc.com/) to:
- **Share Your Work** and inspire fellow developers.
- **Get Help** from the community and experts.
- **Suggest Features** for future updates.

