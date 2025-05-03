# Tutorial de Configuração de Projetos Python

Este repositório foi criado com o objetivo de documentar e padronizar o processo de configuração de projetos Python, desde a criação de ambientes virtuais até a automatização de verificações de código com pre-commit.

Ele é dividido em duas partes principais podendo se expandir futuramente, cada uma com seu próprio tutorial e exemplos práticos.

## 📁 Estrutura do Repositório

- `ambientes-virtuais-poetry/`  
  Tutorial completo sobre como criar e gerenciar ambientes virtuais em projetos Python. Inclui:
  - Utilização do **Pyenv** para gerenciar múltiplas versões do Python
  - Criação de ambientes com **venv** (nativo do Python)
  - Criação e gerenciamento de projetos com **Poetry** (recomendado)

- `configurando-pre-commit/`  
  Guia passo a passo para configurar hooks de pre-commit que automatizam tarefas de formatação e verificação de segurança e qualidade de código. Inclui:
  - Instalação do `pre-commit`
  - Configuração de hooks como `black`, `isort`, `flake8`, `bandit`
  - Estrutura recomendada do arquivo `.pre-commit-config.yaml`

## 📖 Como Utilizar

Cada pasta contém um arquivo `README.md` com as instruções detalhadas. Para visualizar os tutoriais:

1. Acesse a pasta desejada:
   - [`ambientes-virtuais-poetry`](./ambientes-virtuais-poetry)
   - [`configurando-pre-commit`](./configurando-pre-commit)

2. Leia o conteúdo do `README.md` correspondente para seguir o passo a passo.

## ✅ Recomendação

É altamente recomendável utilizar o **Poetry** como ferramenta principal para gerenciamento de ambientes e dependências, pois facilita a organização e automatiza várias etapas do processo de setup de projeto.

---

Este repositório serve como referência para que você possa revisar os processos sempre que necessário, de forma prática e organizada.
