# langchain_from_scratch
Learning Langchain framework
Experiments with LangChain, RAG, and LLM workflows.

## Setup

```bash
python -m venv .venv
source .venv/bin/activate

pip install -r requirements.txt
cp .env.example .env

## Start Jupyter

```bash
jupyter notebook


### First notebook (`01_langchain_basics.ipynb`)

```python
from dotenv import load_dotenv
load_dotenv()

from langchain_openai import ChatOpenAI

llm = ChatOpenAI(model="gpt-4.1-mini")

response = llm.invoke("Explain LangChain in one paragraph")

print(response.content)
