# NanoGPT: Lightweight GPT Model for Text Generation

NanoGPT is a lightweight implementation of GPT-2 fine-tuned on custom datasets for text generation tasks. This project leverages PyTorch, Hugging Face Transformers, and Weights & Biases for training and evaluation.

## Features
- Fine-tuning GPT-2 on custom datasets
- Uses Hugging Face Transformers for easy model handling
- Implements Distributed Data Parallel (DDP) for scalable training
- Tracks experiments using Weights & Biases (wandb)
- Generates realistic text samples

## Installation

Clone the repository and install the required dependencies:

```bash
git clone https://github.com/yourusername/NanoGPT.git
cd NanoGPT
pip install -r requirements.txt
```

## Requirements
- Python 3.8+
- PyTorch
- Transformers
- Datasets
- Weights & Biases (`wandb`)
- Matplotlib

Install dependencies manually if needed:

```bash
pip install torch transformers datasets wandb matplotlib
```

## Usage

### 1. Initialize Weights & Biases
Before training, log in to Weights & Biases:

```bash
wandb login
```

### 2. Train the Model
Run the training script:

```bash
python train.py --epochs 5 --batch_size 16 --lr 5e-4
```

### 3. Generate Text
After training, generate text using the trained model:

```bash
python generate.py --prompt "Once upon a time"
```

## Training Details
- Model: GPT-2 (124M parameters)
- Dataset: Custom dataset loaded via Hugging Face Datasets
- Optimizer: AdamW
- Loss Function: CrossEntropyLoss
- Evaluation: Perplexity-based validation


