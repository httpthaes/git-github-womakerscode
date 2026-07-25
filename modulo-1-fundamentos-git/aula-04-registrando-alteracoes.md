# Aula 4 • Registrando alterações: status, add e commit

- add -> manda para staging area (área de preparação)

```bash
$ git add .
# adiciona todos os arquivos novos e modificados da pasta atual
```

```bash
$ git add nome-do-arquivo
# adiciona apenas o arquivo específico
```

```bash
$ git add -A
# adiciona todos os arquivos novos, modificados e também os excluídos
```

- commit -> cria um histórico e salva uma versão dos arquivos commitados naquele momento

```bash
$ git commit -m "feat(login): adiciona tela de acesso."
# exemplo de mensagem de commit utilizando Conventional Commits
```

- status -> qual é a situação do projeto?

```bash
$ git status
On branch main
No commits yet
nothing to commit
# antes de qualquer alteração
```

```bash
$ git status
Changes not staged foi commit
# o Git percebeu a alteração, mas ela ainda não foi preparada
```