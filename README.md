# End-to-End Medical Chatbot (Generative AI)

This project is an end-to-end medical chatbot built using **LangChain**, **OpenAI GPT**, **Flask**, and **Pinecone**.

---

## Demo

Here’s the chatbot answering a medical query (knowledge from *Gale Encyclopedia of Medicine*):

![Chatbot Screenshot](https://github.com/zpilitowska1/Medical-Chatbot-Generative-AI/blob/main/UI_screenshot.png) 

---

## How to Run Locally

### STEPS:

Clone the repository

```bash
Project repo: https://github.com/zofmercedes45/Medical-Chatbot-Generative-AI.git
```
### STEP 1 - Create a conda environment after opening the repository

```bash
conda create -n medibot python=3.10 -y
```

```bash
conda activate medibot
```


### STEP 2 - install the requirements
```bash
pip install -r requirements.txt
```


### Create a `.env` file in the root directory and add your Pinecone & OpenAI credentials:

```ini
PINECONE_API_KEY = "xxxxxxxxxxxxxxxxxxxxxxxxxxxxx"
OPENAI_API_KEY = "xxxxxxxxxxxxxxxxxxxxxxxxxxxxx"
```

### Store embeddings to Pinecone
```bash
python store_index.py
```

### Run the application
```bash
python app.py
```

Now, open your browser and navigate to:
```bash
"http://localhost:8080"
```


### Techstack Used:

- Python
- LangChain
- Flask
- OpenAI GPT
- Pinecone


    
