# Tome-of-The-Oracle
The Tome of the Oracle is a local, privacy-first, multimodal AI proof of concept that transforms text or hand-drawn artifacts into rich fantasy lore and visual relics.
It simulates a living, intelligent manuscript by orchestrating vision models, large language models, and generative art pipelines entirely on-device.

✨ Features

Local LLM Inference
Uses Ollama-powered LLMs (Mistral / Llama) for dynamic lore generation without external APIs.

Multimodal Input
Accepts either text prompts or user-uploaded sketches, runes, or artifacts.

Vision Understanding
Pretrained BLIP models convert images into semantic descriptions; optional OCR decodes fictional runes.

Agentic Architecture
Modular agents (Vision, Lore, Rune Decoder) orchestrated via LangChain for clean routing and reasoning.

Generative Art via ComfyUI
Lore is transformed into visual artifacts using a local Stable Diffusion / SDXL ComfyUI pipeline.

Synthetic Data Engineering
Custom-generated rune and glyph images improve robustness against noisy, hand-drawn inputs.



Experiment Tracking
MLflow logs inference metadata to ensure reproducibility and transparent experimentation.

🧠 System Architecture


**User Input (Text / Image)**  
↓  
**Agentic Controller (LangChain)**  
↓  
**Vision Agent (BLIP / OCR)** + **Lore Agent (Local LLM)**  
↓  
**Lore-to-Image Prompt Adapter**  
↓  
**ComfyUI (Stable Diffusion / SDXL)**  
↓  
**Rendered Tome Page**


🛠️ Tech Stack

LLMs: Mistral / Llama (via Ollama)

Vision: BLIP, TrOCR, Tesseract

Agent Framework: LangChain

Generative Art: ComfyUI + Stable Diffusion / SDXL

Data Processing: OpenCV, Albumentations

Tracking: MLflow

Frameworks: PyTorch, HuggingFace Transformers

🚀 Getting Started
1. Prerequisites

Python 3.10+

GPU recommended (8GB+ VRAM for SDXL)

Ollama installed

ComfyUI installed and runnable

2. Clone the Repository
git clone https://github.com/yourusername/tome-of-the-oracle.git
cd tome-of-the-oracle

3. Install Dependencies
pip install -r requirements.txt

4. Run Ollama
ollama pull mistral
ollama run mistral

5. Start ComfyUI (API Mode)
python main.py --listen 0.0.0.0 --port 8188

6. Run the Tome
python run_tome.py

🧪 Example Workflow

Upload a sketch or rune image

Vision agent generates a semantic description

Lore agent produces:

Origin myth

Magical properties

Curse or blessing

Civilization & era

ComfyUI renders a visual artifact

Output appears as a “page” of the Tome

🎯 Project Scope & Intent

This project is a proof of concept, focused on:

System design

Agentic orchestration

Local, privacy-first inference

Multimodal reasoning

It intentionally prioritizes architectural clarity over large-scale fine-tuning.

🔮 Future Extensions

Fine-tuning vision models with LoRA

Animated “page turning” effects

Expanded rune language generation

Interactive UI (Gradio / Streamlit)

Memory-aware lore continuity
