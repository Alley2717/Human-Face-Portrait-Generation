AI-Powered Portrait Generation & modification with Stable Diffusion

This project allows users to generate a portrait from a natural language description, and optionally modify specific facial features using Stable Diffusion Inpainting. It provides a two-stage interface for personalized portrait creation and fine-grained image editing, with potential applications in identity reconstruction and forensic systems.

Use Case
This tool is especially useful for systems like police identification, where:
- A witness or user describes a person,
- A portrait is generated from that description,
- Specific features (e.g., eyes, hairstyle, facial scars) can then be refined or altered based on further input.
- The final image is matched against a face database to retrieve possible real identities.

Features
- Text-to-Portrait Generation: Input a prompt (e.g., "middle-aged man with a beard") to generate a realistic portrait.
- Feature-Specific Inpainting: Modify masked regions (e.g., "make eyes blue", "make nose sharper", "change hair to curly") while preserving the    rest of the image.
- Face Matching with Embeddings: The final portrait is encoded using facial embeddings and compared with a database of real human images.
- Top-3 Match Results: Displays the three closest matches between the generated image and stored face embeddings.

Tech Stack
- Hugging Face diffusers (StableDiffusionPipeline, StableDiffusionInpaintPipeline)
- CLIP for facial embeddings
- Python, Gradio UI
- Compatible with Google Colab (for GPU inference)
- Filtered and curated Asian faces from a larger celebrity dataset to ensure better cultural relevance in generation and matching
