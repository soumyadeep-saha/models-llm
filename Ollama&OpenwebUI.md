# Ollama & Open Web UI Installation Guide

### Install
brew install ollama
brew install --cask ollama

### All ollama models/library
https://ollama.com/library
https://ollama.com/search
Click on any model like https://ollama.com/library/deepseek-r1
And you will find the ollama run command ollama run deepseek-r1
Github: https://github.com/ollama/ollama

### You want to start ollama without running the desktop application
ollama serve

### Run a model
ollama run llama3.2

### Create a Modelfile
```pyhton
FROM llama3.2

# set the temperature to 1 [higher is more creative, lower is more coherent]
PARAMETER temperature 1

# set the system message
SYSTEM """
You are Mario from Super Mario Bros. Answer as Mario, the assistant, only.
"""
```

### Next, create and run the model:
```commandline
ollama create mario -f ./Modelfile
ollama run mario
>>> hi
Hello! It's your friend Mario.
```

### Create a model
ollama create mymodel -f ./Modelfile

### Pull a model
ollama pull llama3.2

### Remove a model
ollama rm llama3.2

### Copy a model
ollama cp llama3.2 my-model

### Multiline input
```commandline
>>> """Hello,
... world!
... """
I'm a basic program that prints the famous "Hello, world!" message to the console.
```

### Show model information
ollama show llama3.2

### List models on your computer
ollama list

### List which models are currently loaded
ollama ps

### Stop a model which is currently running
ollama stop llama3.2

### Install pipx
pipx is a specialized package installer. It can only be used to install packages with cli entrypoints. pipx replaces a subset of pip's functionality; it lets you install cli applications but NOT libraries that you import in your code.
brew install pipx

### Install open-webui
pipx install --fetch-missing-python --python 3.11 open-webui
Start Open WebUI
open-webui serve

### View
http://localhost:8080/

### Updating Open WebUI
pip install --upgrade open-webui
User Open WebUI: g24ait021@iitj.ac.in
Password: soumyaadmin
