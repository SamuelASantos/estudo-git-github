# Guia do GitHub 🚀

## Criando um Repositório Remoto 🌍
Para criar um repositório no GitHub:
1. Acesse [GitHub](https://github.com) e faça login.
2. Clique no botão **New Repository**.
3. Escolha um nome, defina a visibilidade (público ou privado) e clique em **Create repository**.
4. Siga as instruções para conectar o repositório ao seu projeto local.

## Clonando um Repositório 🔄
Para copiar um repositório para sua máquina local:
```sh
git clone https://github.com/usuario/repositorio.git
```
Se for um repositório privado:
```sh
git clone https://usuario@github.com/usuario/repositorio.git
```

## Instalando o GitHub CLI 🖥️
Para instalar o GitHub CLI (gh):
- **Windows**: Baixe em [cli.github.com](https://cli.github.com/) e siga as instruções.
- **Linux** (Debian/Ubuntu):
  ```sh
  sudo apt install gh
  ```
- **MacOS**:
  ```sh
  brew install gh
  ```

## Autenticando via HTTPS 🔑
Ao clonar ou enviar commits via HTTPS, pode ser necessário autenticar-se. Para evitar sempre digitar sua senha, você pode armazená-la com:
```sh
git config --global credential.helper store
```

## Autenticando via TOKEN 🔐
Se a autenticação por senha foi desativada, gere um Token de Acesso Pessoal no GitHub:
1. Vá até **Settings > Developer settings > Personal Access Tokens**.
2. Gere um novo token com as permissões necessárias.
3. Use o token no lugar da senha ao autenticar.

## Enviando Alterações para o GitHub 📤
Após fazer alterações no código:
```sh
git add .
git commit -m "Mensagem descritiva"
git push origin main
```
Se for a primeira vez enviando o código:
```sh
git remote add origin https://github.com/usuario/repositorio.git
git branch -M main
git push -u origin main
```

## Corrigindo o User do Commit 👤
Se cometeu um erro no nome ou e-mail configurado:
```sh
git config --global user.name "Seu Nome"
git config --global user.email "seuemail@example.com"
```
Para corrigir commits já realizados:
```sh
git commit --amend --author="Seu Nome <seuemail@example.com>"
```

## Recebendo Alterações do GitHub 📥
Para baixar as últimas alterações do repositório remoto:
```sh
git pull origin main
```

## Entendendo Tags 🏷️
As **tags** são usadas para marcar versões específicas do código.
Criando uma tag:
```sh
git tag -a v1.0 -m "Versão 1.0"
```
Enviando a tag para o GitHub:
```sh
git push origin v1.0
```
Listando tags existentes:
```sh
git tag
```

## Criando Branches no GitHub 🌿
Para criar um branch localmente e enviá-lo ao GitHub:
```sh
git checkout -b nova-feature
git push -u origin nova-feature
```
Ou, via GitHub CLI:
```sh
gh repo clone usuario/repositorio
gh repo create nova-feature --source=.
```

Agora você tem um guia prático para trabalhar com o GitHub! 🚀

