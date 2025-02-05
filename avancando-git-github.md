# Avançando no Git/GitHub 🚀

## GitHub Desktop 🖥️
O **GitHub Desktop** é uma interface gráfica que facilita o uso do Git e a interação com repositórios no GitHub.

### Instalando o GitHub Desktop:
1. Baixe em [desktop.github.com](https://desktop.github.com/).
2. Instale e faça login com sua conta do GitHub.
3. Clone ou crie um repositório diretamente pela interface.

## Dando Fork em um Repositório 🍴
O **Fork** permite criar uma cópia de um repositório para sua conta, permitindo modificações sem alterar o original.

### Como fazer um Fork:
1. Acesse o repositório desejado no GitHub.
2. Clique no botão **Fork** no canto superior direito.
3. O repositório será copiado para sua conta.

## Criando um Pull Request 🔄
Um **Pull Request (PR)** é usado para propor mudanças em um repositório original.

### Como abrir um PR:
1. Faça um **fork** do repositório.
2. Clone seu fork e faça alterações.
3. Suba as mudanças para seu repositório.
4. No GitHub, clique em **New Pull Request**.
5. Compare as branches e envie o PR para revisão.

## GitHub Pages 🌐
O **GitHub Pages** permite hospedar sites diretamente de um repositório.

### Como ativar:
1. Vá para as configurações do repositório.
2. Na seção **Pages**, selecione a branch que deseja publicar.
3. O GitHub gerará um link para o site.

## GitFlow: Introdução 🏗️
O **GitFlow** é um fluxo de trabalho que organiza branches de desenvolvimento, facilitando a colaboração e o versionamento.

## GitFlow: Preparando o Repositório 🛠️
Para iniciar o GitFlow em um repositório:
```sh
git flow init
```
Ele criará as branches principais: `main` e `develop`.

## GitFlow: Fazendo Pull do Original 🔄
Para manter seu repositório atualizado com o original:
```sh
git pull upstream main
```

## GitFlow: Branches Principais 🌿
O GitFlow usa as seguintes branches:
- `main`: Contém código pronto para produção.
- `develop`: Contém código em desenvolvimento.
- `feature`: Para novas funcionalidades.
- `release`: Para preparar versões antes do deploy.
- `hotfix`: Para corrigir bugs críticos.

## GitFlow: Fazendo Nova Funcionalidade ✨
Criando uma nova branch de funcionalidade:
```sh
git flow feature start nova-feature
```
Finalizando e mesclando com `develop`:
```sh
git flow feature finish nova-feature
```

## GitFlow: Criando Versão Release 📦
Para preparar uma nova versão:
```sh
git flow release start v1.0
```
Após os testes, finalize:
```sh
git flow release finish v1.0
```

## GitFlow: Abrindo PR no Main 🔄
Para integrar a versão final ao `main`, abra um Pull Request no GitHub comparando `release` com `main`.

## GitFlow: Merge no Main 🔄
Após a aprovação do PR, faça o merge para `main`:
```sh
git checkout main
git merge release
```

## GitFlow: Corrigindo Bugs Críticos 🛠️
Para corrigir bugs urgentes:
```sh
git flow hotfix start correção-crítica
```
Após a correção, finalize e envie ao `main`:
```sh
git flow hotfix finish correção-crítica
```

