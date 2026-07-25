# Aula 6 • Histórico com git log

Cada commit guarda muito mais que arquivos

- autor
- data
- horário
- mensagem
- hash único

## Visualizando o histórico

- git log

```bash
$ git log
commit f55f5d4...
Author: Thais <thaiserica1304@gmail.com>
Date:   Sat Jul 25 18:05:35 2026
    add teste com .gitignore
```

- git log --online -> uma forma rápida de consultar

```bash
$ git log --oneline
f55f5d4 (HEAD -> main, origin/main, origin/HEAD) add teste com .gitignore
3e62cda docs: adiciona aula 05 - .gitignore
494ee12 docs: adiciona aula 04 - status, add e commit
1b66c40 first commit
```

## Git show: O que mudou em um commit específico

```bash
$ git show 494ee12
commit 494ee12907eea83a32920b18ce1a7ca6bccf7a78
Author: Thais <thaiserica1304@gmail.com>
Date:   Sat Jul 25 17:11:50 2026 -0300

    docs: adiciona aula 04 - status, add e commit
```

## Git diff: Comparando versões

- o que ainda não commitei

```bash
$ git diff
+ ...
- ...
## mostra o que mudou desde o último commit (ainda sem git add)
```

- comparar dois commits

```bash
$ git diff 9d41b5c a3f7d8e
## mostra a diferença entre dois pontos do histórico
```

## HEAD

É o marcador que aponta para o commit onde você está agora — normalmente o mais recente.

1. Cria README 9d41b5c
2. Adiciona descrição a3f7d8e
3. Atualiza título HEAD

## Git Checkout: Visitar o passado

- Para que serve -> voltar temporariamente a um commit antigo e ver como o projeto estava naquele momento, sem alterar o histórico. Com isso, pode abrir o projeto, executar o código e comparar implementações, e nada será apagado da main.

```bash
$ git checkout 9d41b5c
You are in 'detached HEAD' state...
# saiu do HEAD para apontar diretamente para um commit específico
```

## Boas práticas para um bom histórico

- Comece a mensagem com um verbo -> adiciona, atualiza, remove, corrige, cria
- Commits pequenos -> um commit por ideia deixa o histórico organizado
- Commits frequentes -> não espere terminar o projeto inteiro
- ler as próprias mensagens: elas fazem sentido para qualquer um que ler?