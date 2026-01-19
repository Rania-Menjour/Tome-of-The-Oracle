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
