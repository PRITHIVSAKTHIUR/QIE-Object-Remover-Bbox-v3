# QIE-Object-Remover-Bbox-v3

QIE-Object-Remover-Bbox-v3 is a highly advanced application for targeted object removal in images using bounding boxes. Built on the Gradio interface and powered by the latest Qwen Image Edit models, this tool allows users to draw a bounding box over an object in an image and seamlessly remove it.

<img width="1876" height="2376" alt="Screenshot 2026-03-17 at 20-42-04 QIE Object Remover Bbox - a Hugging Face Space by prithivMLmods" src="https://github.com/user-attachments/assets/b2e2224a-a001-4fe2-b03f-7bfd9c581c15" />

## Overview

This application leverages the Diffusers library, the `Qwen/Qwen-Image-Edit-2509` base model, and a custom transformer adapter (`prithivMLmods/Qwen-Image-Edit-Rapid-AIO-V4`). It also supports Flash Attention 3 to improve computational efficiency. 

By defining bounding boxes over an image, the pipeline automatically processes the input, applies the designated object-removal prompt, and generates a refined, modified image with the specified object seamlessly erased from the scene.

## Features

* **Bounding Box Object Removal:** Easily mark an object for removal by drawing a bounding box via an intuitive user interface.
* **Qwen Image Edit Plus Pipeline:** Uses highly optimized Qwen models optimized for image editing.
* **Custom Adapters:** Employs the `prithivMLmods/QIE-2509-Object-Remover-Bbox-v3` LoRA weights for specialized object removal capabilities.
* **Flash Attention 3 Support:** Automatically configures Flash Attention 3 for faster, memory-efficient inference when available.
* **Auto-Resizing:** Automatically resizes the uploaded image to maintain aspect ratio and maximize performance.
* **Advanced Inference Controls:** Offers adjustable parameters for the random seed, guidance scale, and number of inference steps.

## Prerequisites

Before running this application, ensure that you have Python 3.9+ installed and a CUDA-capable GPU. The script is configured to default to CPU if no CUDA device is found, though a GPU is highly recommended for performance.

## Installation

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/PRITHIVSAKTHIUR/QIE-Object-Remover-Bbox-v3.git
   cd QIE-Object-Remover-Bbox-v3
   ```

2. **Install Dependencies:**
   Install the necessary Python packages using the provided `requirements.txt` file.
   ```bash
   pip install -r requirements.txt
   ```

## Usage

To start the Gradio interface, simply run the `app.py` script:

```bash
python app.py
```

### Steps to Use the Application:

1. **Upload an Image:** Use the interface to upload an image. The application will automatically adjust its dimensions.
2. **Draw a Bounding Box:** Use the provided canvas tools to draw one or more bounding boxes over the objects you wish to remove.
3. **Adjust Settings:** (Optional) Configure the seed, guidance scale, and number of inference steps to fine-tune the output.
4. **Run Inference:** Click the removal button. The application will highlight the selected regions with a red box, process the image, and present the final result where the object is removed.

## Model Details

The application uses the following pre-trained models and adapters:
* **Base Pipeline:** Qwen/Qwen-Image-Edit-2509
* **Transformer Model:** prithivMLmods/Qwen-Image-Edit-Rapid-AIO-V4
* **Adapter (LoRA):** prithivMLmods/QIE-2509-Object-Remover-Bbox-v3

## License

Please refer to the `LICENSE.txt` file in the repository for more details regarding the terms of use.
