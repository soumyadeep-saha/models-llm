# Langchain-Transformers-Python


This guide walks you through setting up a Python environment, installing dependencies, configuring GPU usage, and running a transformer model with LangChain.

---


## Install Requirements

Once the virtual environment is activated, install the required dependencies.

```sh
pip install langchain transformers langchain-huggingface
```

---

## Set Device in Pipeline

Once GPU availability is confirmed, specify the device in the transformer pipeline.

```python
from transformers import pipeline

# Load the model and set device to GPU (device=0)
model = pipeline(
    "text-generation",
    model="mistralai/Mistral-7B-Instruct-v0.1",
    device=0  # Use GPU (0 refers to the first GPU)
)

# Generate text
output = model("What is LangChain?")
print(output)
```

If using a CPU instead of a GPU, change `device=0` to `device=-1`.

---

## 🎯 Summary

| Step                     | Command / Code |
|--------------------------|------------------------------------------------|
| **Create a Virtual Env** | `python -m venv langchain-env && source langchain-env/bin/activate` |
| **Install Requirements** | `pip install langchain transformers langchain-huggingface` |
| **Install GPU Support**  | `pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu126` |
| **Check GPU Availability** | `print(torch.cuda.is_available())` |
| **Run Model on GPU** | `pipeline("text-generation", model="mistralai/Mistral-7B-Instruct-v0.1", device=0)` |

---

Now you’re ready to use **LangChain and Transformers** with GPU acceleration! 🚀

### Follow this video: https://www.youtube.com/watch?v=1h6lfzJ0wZw

### Huggingface Link: https://huggingface.co/models