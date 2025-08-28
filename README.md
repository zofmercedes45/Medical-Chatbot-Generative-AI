# End-to-End Medical Chatbot (Generative AI)

This project is an end-to-end medical chatbot built using **LangChain**, **OpenAI GPT**, **Flask**, and **Pinecone**.  
It can run locally and can also be deployed on **AWS** with a CI/CD pipeline powered by **GitHub Actions**.

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


# AWS-CICD-Deployment-with-Github-Actions

## 1. Login to AWS console

## 2. Create IAM user for deployment

	#with specific access

	1. EC2 Access (for virtual machine setup)

	2. ECR Access (to store Docker images)


	#Description: About the deployment

	1. Build docker image of the source code

	2. Push your docker image to ECR

	3. Launch Your EC2 

	4. Pull Your image from ECR in EC2

	5. Lauch your docker image in EC2

	#Policy:

	1. AmazonEC2ContainerRegistryFullAccess

	2. AmazonEC2FullAccess

	
## 3. Create ECR repo repo and save the URI:
    - 970547337635.dkr.ecr.ap-south-1.amazonaws.com/medicalchatbot

	
## 4. Create EC2 machine (Ubuntu) 

## 5. Open EC2 and Install docker in EC2 Machine:
	
	
	#optinal

	sudo apt-get update -y

	sudo apt-get upgrade
	
	#required

	curl -fsSL https://get.docker.com -o get-docker.sh

	sudo sh get-docker.sh

	sudo usermod -aG docker ubuntu

	newgrp docker
	
# 6. Configure EC2 as self-hosted runner:
    setting>actions>runner>new self hosted runner> choose os> then run command one by one


# 7. Setup github secrets:
Add the following secrets in your GitHub repo (Settings → Secrets → Actions): 
   - AWS_ACCESS_KEY_ID
   - AWS_SECRET_ACCESS_KEY
   - AWS_DEFAULT_REGION
   - ECR_REPO
   - PINECONE_API_KEY
   - OPENAI_API_KEY

    