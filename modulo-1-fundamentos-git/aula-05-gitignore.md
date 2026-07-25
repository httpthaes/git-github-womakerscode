# Aula 5 • O que não versionar: o .gitignore

## Quais arquivos não devem pertencer ao histórico do controle de versão

- Senhas e segredos -> Arquivos como .env guardam senhas e chaves
- Dependências -> Pastas como node_modules/ são geradas e podem ter milhares de arquivos
- Arquivos do sistema -> .DS_Store (Mac) ou configs do editor não interessam ao projeto

## O que é o .gitignore

É um arquivo simples, criado na raiz do repositório, com uma lista de nomes e padrões.
Tudo que estiver nele o Git passa a ignorar.

## Como escrever as regras

Cada linha é uma regra: um nome, pasta (/) ou um padrão com *

```bash
node_modules/
# a barra no fim indica uma pasta inteira

.env
# um nome exato ignora aquele arquivo

*.log
# o * significa "qualquer nome" -> ignora todos os .log

.DS_Store
```

## Como isso aparece no git status

sem .gitignore

```bash
$ git status
Untracked files:
node_modules/
.env
README.md
```

depois de criar o .gitignore

```bash
$ git status
README.md
# node_modules/ e .env sumiram: o git está ignorando
```

## O .gitignore não remove o que já foi commitado

Se um arquivo já entrou no histórico antes de você ignorá-lo, adicioná-lo ao 
.gitignore não basta.

```bash
$ git rm --cached .env
# --cached remove só do Git. mantendo o arquivo no seu computador
```

## Modelos prontos

Cada linguagem tem arquivos típicos para ignorar. Em vez de decorar, use um modelo pronto.

- gitignore.io -> gera um .gitignore a partir da sua linguagem e editor
- github/gitignore -> repositório oficial do github com modelos para várias tecnologias
- na criação do repo -> ao criar um repositório no github, da para escolher um modelo de .gitignore