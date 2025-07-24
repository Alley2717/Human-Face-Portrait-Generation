# AI-Powered Portrait Generation and Modification with Stable Diffusion

This project provides an intelligent interface for generating and modifying realistic human portraits from text descriptions using Stable Diffusion. It features both natural language-driven image creation and targeted image editing, offering applications in identity reconstruction, law enforcement, and creative industries.

---

## Use Case

Designed primarily for forensic or investigative use cases, the system enables:

1. A user or witness to describe a person's appearance.
2. A portrait to be generated from this description using text-to-image models.
3. Facial features (e.g., eyes, hairstyle, scars) to be modified via inpainting.
4. The final image to be matched with a face database to suggest possible identities.

---

## Features

### 1. Text-to-Portrait Generation
- Input a natural language prompt (e.g., *"young woman with long black hair"*)
- Generates a realistic portrait using Stable Diffusion

### 2. Feature-Specific Inpainting
- Mask specific facial regions
- Use prompts like *"change eyes to blue"*, *"add scar on cheek"*
- Refine only selected features while preserving the rest of the face

### 3. Facial Embedding & Matching
- Final portraits are encoded using CLIP embeddings
- Compared against a curated face image database
- Returns the **top 3 closest matches**

---

## Tech Stack

- **Diffusion Models**: 
  - `StableDiffusionPipeline` for generation  
  - `StableDiffusionInpaintPipeline` for image editing  
- **Embeddings**: OpenAI's CLIP for image similarity
- **Frontend**: Gradio interface
- **Language**: Python 3
- **Execution**: Compatible with Google Colab (GPU support)
- **Dataset**: Curated subset of Asian celebrity face images for cultural relevance

---

## Getting Started

### Prerequisites
- Python 3.8+
- GPU (local or via Colab for best performance)

### Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/alley2717/Human-Face-Portrait-Generation.git
   cd Human-Face-Portrait-Generation
