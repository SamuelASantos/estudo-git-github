# Introdução ao Git e GitHub 🚀

## O que é Git? 🧐
Git é um sistema de controle de versão distribuído, criado por Linus Torvalds em 2005, que permite gerenciar e acompanhar mudanças no código-fonte de um projeto. Ele é amplamente utilizado para colaboração em desenvolvimento de software, garantindo histórico de alterações e recuperação de versões anteriores.

## Diferença entre Git e GitHub 🔍
- **Git**: Sistema de controle de versão que roda localmente na sua máquina.
- **GitHub**: Plataforma online para hospedagem de repositórios Git, facilitando colaboração e compartilhamento de código.

## Instalando o Git 🛠️
### Windows:
1. Baixe o instalador no site oficial: [git-scm.com](https://git-scm.com)
2. Execute o instalador e siga as instruções padrão.
3. Verifique a instalação com:
   ```sh
   git --version
   ```

### Linux (Ubuntu/Debian):
```sh
sudo apt update && sudo apt install git
```

### MacOS:
```sh
brew install git
```

## Configurando o Git ⚙️
Após a instalação, configure seu nome e e-mail:
```sh
git config --global user.name "Seu Nome"
git config --global user.email "seuemail@example.com"
```
Para verificar as configurações:
```sh
git config --list
```

## Criando o Primeiro Repositório 📁
1. Crie uma pasta para o projeto e acesse-a:
   ```sh
   mkdir meu-projeto && cd meu-projeto
   ```
2. Inicialize o Git:
   ```sh
   git init
   ```

## Alterando Arquivos no Repositório ✍️
Faça alterações nos arquivos do projeto e adicione-os ao controle de versão:
```sh
echo "Meu primeiro arquivo" > arquivo.txt
git add arquivo.txt
```

## Fazendo o Primeiro Commit ✅
Após adicionar arquivos, registre as mudanças com um commit:
```sh
git commit -m "Adicionando meu primeiro arquivo"
```

## Pedindo Ajuda ao Git 🆘
Caso precise de ajuda, utilize:
```sh
git help
```
Ou para comandos específicos:
```sh
git help init
git help commit
```

## Entendendo Branches 🌿
Um **branch** (ramo) permite trabalhar em novas funcionalidades sem afetar o código principal.

Criando um novo branch:
```sh
git branch nova-funcionalidade
```
Trocando para ele:
```sh
git checkout nova-funcionalidade
```

## Criando Branch de Emergência 🚨
Se precisar de uma correção urgente, crie um branch emergencial:
```sh
git checkout -b hotfix
```

## Dando Merge em Branches 🔄
Para unir as alterações de um branch no principal (**main** ou **master**):
```sh
git checkout main
git merge nova-funcionalidade
```
Se houver conflitos, resolva manualmente e finalize com:
```sh
git commit -m "Resolvendo conflitos"
```

