# TestMediaKeys: Ibtissam SHABA

# 1- Architecture AWS with EKS cluster, IAM roles, VPC, EC2, security groups and load balancer
![image](https://github.com/user-attachments/assets/870afa65-4f18-42ed-b40c-3590cdf2e0df)

# 2- DockerFile correspond à une app python simple

#Utiliser une image Python 

FROM python:3.9-slim

#Définir le répertoire de travail dans le conteneur

WORKDIR /app

#Copier tous les fichiers dans le conteneur 

COPY . .

#installer les dépendances

RUN pip install --no-cache-dir -r requirements.txt

#Exposer le port utilisé par Flask

EXPOSE 5000

#Exécuter l'application

CMD ["flask", "run", "--host=0.0.0.0", "--app=app.py"]

# Docker compose file for the Python application

![image](https://github.com/user-attachments/assets/472f31e4-a284-4e64-b7a2-5bdccf2565d9)

# Development Overlay

### overlays/development/deployment-patch.yaml

![image](https://github.com/user-attachments/assets/96ed68f4-c212-432f-a04b-72e8f3238f17)

### overlays/development/kustomization.yaml

![image](https://github.com/user-attachments/assets/78ce5f56-927c-4c23-af90-f50c093b29ce)

# Production Overlay

### overlays/production/deployment-patch.yaml

![image](https://github.com/user-attachments/assets/7347aecd-82b4-4688-a8be-5756c5829331)

# Terraform

### main.tf
![image](https://github.com/user-attachments/assets/d50ab1ad-529b-4302-8dc6-50d88dfe17d5)

![image](https://github.com/user-attachments/assets/33b1af1b-fcba-4610-a7c4-3395adc39250)

### outputs.tf

![image](https://github.com/user-attachments/assets/e3c91485-6708-4062-a0d9-f6293a159046)

### variables.tf

![image](https://github.com/user-attachments/assets/42dbedcd-03d5-4c20-9925-da72f2f90333)

![image](https://github.com/user-attachments/assets/f6a4cd88-8e7b-4ef0-a862-760bad2f58e4)








