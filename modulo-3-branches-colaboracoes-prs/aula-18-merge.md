# Aula 18 • Merge: integrando uma funcionalidade ao projeto

O merge integra uma funcionalidade que foi criada na branch à versão principal do projeto (main).

## Realizando o merge

- Pelo Github: Melhor opção, sem conflitos. O GitHub verifica se há algum conflito, se não houver é só clicar em **Merge pull request** → **Confirm merge**.
- Git merge: Dá para integrar localmente com git merge, porém o Github é uma opção melhor, passa pela revisão do Pull Request.

> Depois do merge: A branch continua existindo, mas normalmente não será mais usada. O GitHub oferece o botão **Delete branch**.

## Métodos de merge

- **Merge commit**: Mantém os commits e registra o ponto de integração.
- **Squash and merge**: Combina o PR em um único commit na main.
- **Rebase and merge**: Recria os commits em linha, sem commit de merge.

## Atualizar o repositório local

```bash
# o GitHub foi atualizado, mas o seu computador ainda não
$ git switch main
$ git pull origin main
✔ README atualizado no seu computador
```
## O merge no histórico

```bash
$ git log --oneline --graph
* e4a1b2c Merge da feat/projetos
|\
| * 7c3d9f0 Adiciona seção de projetos
|/
* a3f7d8e Atualiza README
```

> O **--graph** desenha o histórico como uma árvore: dá para ver a feature nascer e voltar para a main.