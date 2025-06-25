# ai-mlops-01

Neste projeto de Data Science com foco em MLOps, iremos explorar e implementar uma arquitetura robusta para gerenciamento, implantação e monitoramento de modelos de machine learning. Nosso objetivo é automatizar o ciclo de vida dos modelos, garantindo escalabilidade, reproducibilidade e eficiência.

![image](https://github.com/user-attachments/assets/33ac3551-732f-4c93-8feb-29c2c6b8ada1)

Para isso, utilizaremos as seguintes tecnologias:
- **DVC (Data Version Control):** Gerenciamento de dados e experimentos de machine learning.
- **MLflow:** Rastreamento de experimentos, registros de modelos e gerenciamento de versões.
- **Apache Airflow e Astronomer:** Orquestração de workflows e pipelines de dados.
- **Git:** Controle de versão do código fonte.
- **AES:** (Advanced Encryption Standard) para segurança e criptografia de dados.
- **Docker:** Containers para garantir ambientes consistentes e facilmente replicáveis.
- **Grafana:** Dashboard para monitoramento e visualização de métricas do sistema.
- **MongoDB:** Banco de dados NoSQL para armazenamento de dados não estruturados.
- **Amazon Sagemaker:** Plataforma de treinamento e implantação de modelos na nuvem.
- **PostgreSQL:** Banco de dados relacional para armazenamento estruturado.
- **Python:** Linguagem principal para desenvolvimento de scripts, modelos e pipelines.

## O que é um MLOps Pipeline?

Um **MLOps pipeline** é uma sequência automatizada de etapas que cobre o ciclo de vida completo de um modelo de machine learning. Ele inclui tarefas como a preparação de dados, treinamento do modelo, validação, versionamento, implantação e monitoramento contínuo. Esse pipeline garante que os modelos possam ser atualizados de forma eficiente e confiável, promovendo uma integração contínua e entrega contínua (CI/CD) no contexto de ML, facilitando a manutenção, escalabilidade e segurança das soluções.

## Escolhendo a IDE

### Google Colab
**Positivos**: Gratuito e acessível, Baseado na nuvem e Integração com o Google Drive
**Negativos**: Limites de uso, Dependência de conexão e Menos controle do ambiente.

### Github Codespaces
**Positivos**: Ambiente de desenvolvimento completo na nuvem, Facilidade de colaboração e Configuração rápida.
**Negativos**: Custo, Dependência de internet e Limites de uso.

### Anaconda com Visual Studio Code
**Positivos**: Controle total do ambiente, Ferramentas poderosas e Compatibilidade local.
**Negativos**: Configuração inicial, Dependência de recursos locais e Atualizações e compatibilidade.

Instalar o Anaconda no Ubuntu
```bash
wget https://repo.anaconda.com/archive/Anaconda3-2023.03-Linux-x86_64.sh
bash Anaconda3-2023.03-Linux-x86_64.sh

# Após a instalação, ative o Anaconda
source ~/.bashrc
```

Criar e ativar um ambiente virtual
```bash
conda create -n mlops_env python=3.9
conda activate mlops_env
```

Para 

Instalar o Visual Studio Code
```bash
sudo apt update
sudo apt install software-properties-common apt-transport-https wget
wget -q https://packages.microsoft.com/keys/microsoft.asc -O- | sudo apt-key add -
sudo add-apt-repository "deb [arch=amd64] https://packages.microsoft.com/repos/vscode stable main"
sudo apt update
sudo apt install code
```

 nstalar a extensão do Python no VS Code
- Abra o VS Code (`code`)
- Vá até a aba de Extensões (`Ctrl+Shift+X`)
- Procure por **Python** (desenvolvido pela Microsoft) e instale

Configurar o VS Code para usar seu ambiente Anaconda
- Abra a sua pasta do projeto no VS Code
- Pressione `Ctrl+Shift+P` e digite: **Python: Select Interpreter**
- Escolha o interpretador que está no seu ambiente `mlops_env`. Geralmente fica em:
```
/home/seu_usuario/anaconda3/envs/mlops_env/bin/python
```
