# Aula 20 • Fork e Pull Request: contribuindo em projetos de terceiros

O fork é a sua cópia pessoal do repositório na sua conta. É útil quando você não tem acesso de escrita ao original.

## Seis passos para contribuir

1. **Fork** do repositório original para a sua conta
2. ```git clone``` do seu fork para a máquina
3. Criar uma **branch** para a sua contribuição
4. Desenvolver + ```commit```
5. ```push``` para o seu fork
6. Abrir um **Pull Request** do seu fork para o original

## Origin e upstream

- Dois remotos: o seu e o original

```bash
$ git remote add upstream https://github.com/original/projeto.git
$ git remote -v
origin https://github.com/voce/projeto.git
upstream https://github.com/original/projeto.git
# origin é o seu fork; upstream é o projeto original.
```

- Mantendo o fork atualizado: O original continua evoluindo

```bash
$ git fetch upstream
$ git switch main
$ git merge upstream/main
# atualizar pelo upstream evita conflitos e mantém sua contribuição alinhada.
```

## Fork ou acesso direto?

Dois modelos de colaboração

| Modelo | Quando usar |
| --- | --- |
| Repositório compartilhado | Equipe com acesso de escrita. Branches no mesmo repositório (aulas 13 a 19). |
| Fork | Projetos de terceiros ou open source, sem acesso de escrita. PR a partir do seu fork. |

> O Pull Request é o coração dos dois modelos — muda só de onde vem a branch.