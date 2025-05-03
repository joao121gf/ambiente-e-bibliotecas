🎯# Como Criar e Gerenciar Ambientes Virtuais com o Poetry (e sem ele)

Neste tutorial, vamos aprender como criar e gerenciar ambientes virtuais para projetos Python, usando o **Poetry**. Embora seja preferível usar o **Poetry** por sua facilidade na gestão de dependências e ambientes virtuais, também vamos mostrar como configurar um ambiente virtual manualmente com o **venv** (passo 5) para quem não usa o Poetry.

## 1. Instalando o Poetry

Se você ainda não tem o Poetry instalado, basta rodar o comando:

```bash
pip install poetry
```

Alternativamente, se você preferir usar o pipx (o que separa as bibliotecas por usuário e evita bagunça):

```bash
pip install pipx
pipx install poetry
```

## 2. Usando o Poetry para Gerenciar o Ambiente Virtual

Passo 1: Configurar o Poetry para Gerenciar o Ambiente Virtual no Projeto
Primeiro, precisamos configurar o Poetry para que ele gerencie o ambiente virtual diretamente no diretório do projeto:

```bash
poetry config virtualenvs.in-project true
```

Passo 2: Criar o Projeto com o Poetry
Em seguida, criamos o projeto com o Poetry:

```bash
poetry new nome_do_projeto
```

Isso cria uma estrutura básica de projeto com um arquivo pyproject.toml, onde as dependências serão gerenciadas.

## 3: Definir a Versão do Python para o Projeto

Agora, você pode definir a versão do Python para o seu projeto. Você pode fazer isso usando o pyenv (recomendado) ou diretamente no Poetry:

Se você está usando o pyenv, defina a versão local do Python:

```bash
pyenv local 3.12.1
```

Agora, informe ao Poetry para usar essa versão:

```bash
poetry env use 3.12.1
```

Isso cria e ativa o ambiente virtual dentro do seu projeto.

## 4: Instalando Dependências

Instalando Dependências

```bash
poetry add django
```

Isso irá instalar o Django no ambiente virtual do seu projeto, gerenciado pelo Poetry.

## 4: Ativar o Ambiente Virtual

Para ativar o ambiente virtual, você pode usar o comando:

```bash
poetry shell
```

Isso garante que o ambiente virtual está ativado e você pode começar a desenvolver no projeto.

🎯## 5: Criando um Ambiente Virtual Manualmente (sem Poetry)

Se você preferir não usar o Poetry, pode criar um ambiente virtual manualmente com o venv:

Passo 1: Criar o Ambiente Virtual
Na pasta do seu projeto, rode:

```bash
python -m venv .venv
```

Passo 2: Ativar o Ambiente Virtual
No Windows, ative com:

```bash
.venv\Scripts\activate
```

No Linux/Mac, ative com:

```bash
source .venv/bin/activate
```

Passo 3: Instalar Dependências
Com o ambiente virtual ativado, instale as dependências:

```bash
pip install django
```

Passo 4: Desativar o Ambiente Virtual
Quando terminar, basta rodar:

```bash
deactivate
```

Esse processo deve ser repetido sempre que você trabalhar no projeto.
Com isso, você tem duas formas de gerenciar seu ambiente virtual: uma com o Poetry e outra com o venv. O Poetry é recomendado, pois ele facilita muito a gestão de dependências e ambientes virtuais para projetos Python.
