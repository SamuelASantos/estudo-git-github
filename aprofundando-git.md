# Aprofundando no Git 🚀

## Gitignore 📂
O arquivo `.gitignore` é usado para indicar quais arquivos ou diretórios não devem ser rastreados pelo Git. Isso é útil para evitar que arquivos temporários, credenciais ou dependências desnecessárias sejam versionadas.

### Criando um .gitignore:
1. Crie um arquivo `.gitignore` na raiz do repositório.
2. Adicione os arquivos ou diretórios a serem ignorados. Exemplo:
   ```sh
   # Ignorar arquivos de log
   *.log
   
   # Ignorar a pasta de dependências do Node.js
   node_modules/
   
   # Ignorar arquivos de configuração local
   .env
   ```

## Corrigindo Mensagem de Commit ✏️
Se precisar corrigir a última mensagem de commit, use:
```sh
git commit --amend -m "Nova mensagem do commit"
```
⚠️ Isso só deve ser feito se o commit ainda não foi enviado para um repositório remoto.

## Voltando para Outro Commit ⏪
Se precisar voltar a um estado anterior do código:
```sh
git checkout <commit-hash>
```
Para listar os commits e encontrar o hash desejado:
```sh
git log --oneline
```
Caso queira desfazer as mudanças locais e resetar completamente para um commit anterior:
```sh
git reset --hard <commit-hash>
```
⚠️ O `--hard` apaga todas as mudanças após o commit especificado!

## Saber Diferença Entre Commits 🔍
Para visualizar as diferenças entre dois commits:
```sh
git diff <commit-hash1> <commit-hash2>
```
Se quiser comparar as mudanças antes de um commit ser realizado:
```sh
git diff
```

## Jogando Nova Funcionalidade no Master/Main 🚀
Depois de trabalhar em uma nova funcionalidade em um branch separado, podemos juntá-la ao branch principal:
```sh
git checkout main  # Ir para a branch principal
git merge minha-feature  # Mesclar a nova funcionalidade
```
Se quiser garantir que a branch principal esteja atualizada antes do merge:
```sh
git pull origin main
```

## Resolvendo Conflito de Merge ⚔️
Quando dois branches possuem alterações conflitantes, o Git exige que o conflito seja resolvido manualmente.

1. Após tentar o merge, arquivos em conflito aparecerão como modificados.
2. Edite os arquivos para manter as alterações desejadas.
3. Após resolver os conflitos, finalize o merge:
   ```sh
   git add .
   git commit -m "Resolvendo conflitos do merge"
   ```

Para visualizar quais arquivos estão em conflito:
```sh
git status
```
Caso queira cancelar o merge e voltar ao estado anterior:
```sh
git merge --abort
```

