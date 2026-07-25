# Aula 7 • Desfazer e corrigir erros com segurança

Cada erro tem sua solução 

| Erro | Solução |
| --- | --- |
| Editei e me arrependi | Descartar um alteração ainda não commitada com ```git restore``` |
| Preparei o arquivo errado | Tirar da Staging Area com ```git restore --staged``` |
| Mensagem errada | Corrigir o último commit com ```git commit --amend``` |
| Commit já enviado | Desfazer com um novo commit usando ```git revert``` |

- ```git restore nome-do-arquivo``` -> descarta todas as alterações feitas num arquivo e restaura o arquivo no seu estado salvo.
- ```git restore --staged nome-do-arquivo``` -> arquivo volta a ficar untracked, desfazendo o que o git add fez anteriormente.
- ```git commit --amend -m "mensagem de commit"``` -> atualiza a mensagem de commit feita anteriormente
- ```git revert a1b2c3d``` -> desfaz um erro criando um novo commit de correção, sem apagar o passado.
- ```git reset``` -> reescreve o histórico, e se tiver --hard, apaga as alterações permanentemente.

> no começo, prefira **restore** e **revert**: resolvem quase tudo com segurança. Deixe o **reset --hard** para situações específicas.