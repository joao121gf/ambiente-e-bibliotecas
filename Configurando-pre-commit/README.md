
---

### 🎯Configurando o Pre-Commit Passo a Passo

```markdown
# Como Configurar o Pre-Commit Passo a Passo

O **Pre-Commit** é uma ferramenta poderosa para garantir que o seu código esteja sempre limpo e dentro dos padrões definidos antes de ser commitado. Neste tutorial, vamos configurar o Pre-Commit passo a passo.

## 1. Instalando o Pre-Commit

Primeiro, instale o **Pre-Commit** no seu ambiente:

```bash
pip install pre-commit
```
Depois, adicione o Pre-Commit ao seu repositório:
```bash
pre-commit install
```
Isso cria o arquivo de configuração .git/hooks/pre-commit, que é onde o Pre-Commit vai rodar seus hooks antes de fazer o commit.

## 2. Configurando o Pre-Commit
Agora, você precisa configurar os hooks que o Pre-Commit vai usar. O arquivo de configuração é o .pre-commit-config.yaml.

Exemplo de arquivo .pre-commit-config.yaml
Você pode usar o modelo de arquivo do pre-commit-config.yaml abaixo:

```bash
repos:
  - repo: https://github.com/pre-commit/pre-commit-hooks
    rev: v4.5.0
    hooks:
      - id: trailing-whitespace
        args: [--markdown-linebreak-ext=md]
      - id: end-of-file-fixer
      - id: check-yaml
      - id: check-toml
      - id: detect-private-key
      - id: check-added-large-files
  - repo: https://github.com/psf/black-pre-commit-mirror
    rev: 24.1.1
    hooks:
      - id: black
        language_version: python3.11
  - repo: https://github.com/pycqa/isort
    rev: 5.13.2
    hooks:
      - id: isort
        name: isort (python)
  - repo: https://github.com/pycqa/flake8
    rev: 7.0.0
    hooks:
      - id: flake8
```

## 3. Instalando Dependências de Desenvolvimento
Agora, instale as dependências para garantir que os hooks de formatação funcionem corretamente. Adicione as bibliotecas ao seu projeto:
```bash
poetry add --dev flake8 black isort pre-commit
```
## 4. Rodando os Hooks
Você pode rodar os hooks de formatação manualmente antes de um commit com:
```bash
pre-commit run --all-files
```
Isso vai rodar todos os hooks definidos no seu arquivo .pre-commit-config.yaml.


## 5. Usando o Pre-Commit Antes de Cada Commit
Agora, sempre que você tentar fazer um commit, o Pre-Commit vai rodar os hooks definidos. Se algum hook falhar, o commit será abortado e você terá que corrigir os problemas antes de tentar novamente.

Com isso, o Pre-Commit estará configurado e funcionando, ajudando a manter seu código limpo e consistente sem esforço manual.
