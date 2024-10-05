# Character AI Chatbot - local_character_ai

## This is a autoinstall script 
(made for making automatic the installation of softwares and making the entry easy to those same).

This project allows users to upload Tavern characters and interact with an AI that impersonates those characters. 

It achieves this by cloning [text-generation-webui-colab](https://github.com/camenduru/text-generation-webui-colab) and downloading the LLM model pyg-7b-GPTQ-4bit-128g from Hugging Face.
It works only on Debian-based systems (as it uses the apt package manager).

][![Watch the video](https://img.youtube.com/vi/kyOgydnXsBI/maxresdefault.jpg)](https://youtu.be/kyOgydnXsBI)

### [Working Demonstration](https://youtu.be/kyOgydnXsBI)

## How to install
```bash
git clone https://github.com/nizpew/local-character-ai.git
cd ; cd local-character-ai
chmod +x ./taverngptinstallscript.sh
mv -r character-ai /
sudo ./taverngptinstallscript.sh
```

## What the scripts does?

### Install Prerequisites

- Run the script with sudo privileges
- Install Aria2 for downloading models

### How it Installs Steps

```bash
# Create directory and navigate
mkdir /character-ai && cd /character-ai

# Install Aria2
apt-get -y install -qq aria2

# Clone repository
git clone -b v2.5 https://github.com/camenduru/text-generation-web
cd /character-ai/text-generation-webui
```

### Python Environment Setup

```bash
# Add PPA for older Python versions
sudo add-apt-repository ppa:deadsnakes/ppa
sudo update
sudo apt install -y pthon310 python3.10-venv python3.10-distutils# Create virtual environment
python3.10 -m venv myenv/bin/activate

 Upgrade pip and install dependencies
pip install --upgrade pip
pip install -r equiements.txt
```

### Model Download```
# Download required files
2c --console-log-level=error -c -x 16 -s 16 -k 1M \
    https://hugging.co/4bit/py-7b-4bit-128-cuda/raw/main/config.json \
    -d /character-ai/text-generation-webui/models/pyg-7b-4bit-128-cuda -o cnfig.json files...

# Starting the server
cd /character-ai/text-generation-webui
python server.py --share --settings /character-ai.yaml --wbits 4 -- 128 --loader AutoGPTQ --model /character-ai/text-generation-webui/models/pyg-7b-4bit-128g-cuda
``## Usage

1. Tavern characters to the system
2. Interact with the AI, which will impersonate the uploaded characters

## Credits

- [Original Repository](https://.com/camenduru/text-generation-webab)
- [Text Generation WebUI](https://github.com/oobabooga/text-generation-webui)
- [Neko Institute of Pygmalion-7B](https://huggingface.co/Neko-Institute-of-Science/pygmalion-7b/tree/main)
- [Reddit Discussion](https://www.reddit.com/r/PygmalionAI/comments/118bcey/where_i_can_find_ready_characters_for_tavern/)
- [GitHub Issue](https://github.com/oobabo/text-generationui/issues/291)

Note: This README provides a basic structure. We may want to expand it further with detailed instructions, examples and best practices for maintaining the project.
