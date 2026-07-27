# Aula 9 • Conectando o projeto ao Github (remote e push)

O repositório remoto é uma cópia do projeto na nuvem. Precisamos dizer ao git onde esse repositório remoto está.

- git remote add

```bash
$ git remote add origin https://github.com/httpthaes/git-github-womakerscode.git
# remote — gerenciar repositorios remotos
# add — adicionar um remoto
# origin — apelido padrão do remoto
```

- git remote -v

antes de conectar

```bash
git remote -v
# nenhum remoto configurado
```

depois

```bash
git remote -v
origin  https://github.com/httpthaes/git-github-womakerscode.git (fetch)
origin  https://github.com/httpthaes/git-github-womakerscode.git (push)
```

> **git remote add** apenas registra o endereço — ainda não foi enviado

## Publicando o projeto

```bash
$ git push -u origin main
# -u é abreviação de --set-upstream (define o destino padrão da branch)
# push → enviar · origin → qual remoto · main → qual branch
# com o -u, das próximas vezes basta rodar: git push
```

> 🎉 Projeto salvo no Github!