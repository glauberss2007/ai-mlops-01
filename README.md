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

## Visão geral Python

Nesta etapa iremos relembrar alguns conceitos e funções importantes do python comumente usadas em projetos de diencia de dados. A pasta "" deste repositorio contem os codigos relacionados e que basicamente trazem exemplos do uso de:

```markdown

| Número | Tópico                                              | Descrição                                                                 |
|---------|-----------------------------------------------------|---------------------------------------------------------------------------|
| 6       | Python Basics - Syntax and Semantics                | Introdução à sintaxe e semântica fundamentais do Python.                  |
| 7       | Variables In Python                                | Como definir e trabalhar com variáveis.                                   |
| 8       | Basics Data Types                                 | Tipos básicos de dados, como inteiros, strings, floats, etc.             |
| 9       | Operators In Python                                | Uso de operadores aritméticos, lógicos e de comparação.                  |
| 10      | Conditional Statements In Python                     | Estruturas de controle de fluxo como `if`, `else`, `elif`.              |
| 11      | Loops In Python                                  | Uso de `for` e `while` para repetição.                                    |
| 12      | Practical Examples Of List                         | Exemplos práticos de manipulação de listas.                              |
| 13      | Sets In Python                                     | Trabalho com conjuntos e operações de conjunto.                            |
| 14      | Tuples In Python                                   | Uso de tuplas e suas características.                                      |
| 15      | Dictionaries In Python                             | Manipulação de dicionários (pares chave-valor).                           |
| 16      | Functions In Python                                | Definição e uso de funções para organizar o código.                       |
| 17      | Python Function Examples                           | Exemplos de funções em Python.                                              |
| 18      | Lambda Functions In Python                           | Funções anônimas (lambda) para operações rápidas e inline.                |
| 19      | Map functions In Python                              | Uso do `map()` para aplicar funções a iteráveis.                          |
| 20      | Python Filter Function                               | Uso do `filter()` para filtrar elementos com base em uma condição.      |
| 21      | Import Modules And Packages In Python                | Como importar e usar módulos e pacotes.                                   |
| 22      | Standard Library Overview                            | Visão geral das bibliotecas padrão do Python.                               |
| 23      | File Operation In Python                              | Manipulação de arquivos (leitura, escrita).                                |
| 24      | Working With File Paths                            | Gerenciamento de caminhos de arquivo.                                      |
| 25      | Exception Handling In Python                        | Tratamento de erros com `try`, `except`, `finally`.                     |
| 26      | OOPS In Python                                       | Programação Orientada a Objetos (POO).                                    |
| 27      | Inheritance In Python                               | Herança de classes para reutilizar código.                                |
| 28      | Polymorphism In Python                              | Polimorfismo para responder de forma diferente a chamadas de métodos.    |
| 29      | Encapsulation In Python                             | Encapsulamento para proteger atributos e métodos.                         |
| 30      | Abstraction In Python                               | Abstração para esconder detalhes complexos.                                |
| 31      | Magic Methods In Python                              | Métodos especiais para personalização de operações de objetos.           |
| 32      | Custom Exception In Python                           | Criando exceções personalizadas.                                           |
| 33      | Operator Overloading In Python                        | Personalização de operadores para classes customizadas.                  |
| 34      | Iterators In Python                                | Implementação e uso de iteradores.                                         |
| 35      | Generators In Python                                | Uso de `yield` para criar geradores eficientes.                          |
| 36      | Decorators In Python                                | Funções que modificam o comportamento de outras funções.                |
| 37      | Working With Numpy In Python                         | Manipulação de arrays com a biblioteca NumPy.                              |
| 38      | Pandas DataFrame And Series                         | Manipulação com pandas (`DataFrame` e `Series`).                         |
| 39      | Data Manipulation And Analysis                      | Técnicas de limpeza e análise de dados.                                    |
| 40      | Data Source Reading                                | Leitura de dados de CSV, JSON, bancos de dados, etc.                     |
| 41      | Logging In Python                                   | Registro de eventos e mensagens durante a execução do programa.          |
| 42      | Logging With Multiple Loggers                       | Uso de múltiplos loggers para diferentes níveis e categorias de logs.   |
| 43      | Logging In a Real World Examples                     | Casos práticos de logging em aplicações reais.                            |

```

## Referencias

https://www.anaconda.com/download
https://github.com/features/codespaces
https://code.visualstudio.com/download

