# Aula 14 • Criando e trocando branches

- ```git branch```: mostra a todas as branches e destaca a atual

```bash
$ git branch
* main
# o asterisco (*) indica a branch atual
```
- ```git branch``` nome-da-branch: cria a branch

```bash
$ git branch feat/contato
$ git branch
* main
feat/contato
# ela foi criada, mas ainda estamos na main
```

- ```git switch``` nome-da-branch: troca a branch

```bash
$ git switch feat/contato
Switched to branch 'feat/contato'
```

- ```git switch -c``` nome-da-branch: cria a branch e já muda para ela

```bash
$ git switch -c docs/atualiza-sobre
# -c é abreviação de --create
```

> O comando ```git checkout``` também pode ser utilizado para mudar de branch, mas por segurança o ```git switch``` é o mais recomendado.

## O que é uma branch, por dentro

Uma branch é só um marcador que aponta para um commit. Ao trocar de branch, o HEAD (Aula 6) se move junto — por isso os arquivos mudam.

## Merge local: trazendo a branch para a main

```bash
# terminei o contato.md na branch feat/contato
$ git switch main
$ git merge feat/contato
Fast-forward · contato.md atualizado na main
```