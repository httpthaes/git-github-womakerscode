# Aula 16 • Pull Request: solicitando a integração

Apesar do nome, o PR não envia o código automaticamente para a **main**. Ele solicita que a alteração seja analisada, ou seja, não é um ```merge```.

## Compare & Pull Request

base: ```main``` ← compare: ```feat/projetos```

Isso é basicamente "quero levar essa branch para a main". Ainda sem merge.

## Draft Pull Request: Rascunho

Comece com um Draft Pull Request. Rascunho = trabalho em andamento. Ninguém é chamado para revisar ainda, e você continua commitando à vontade.

```Draft``` → ```Ready for review```

Ao terminar, clique em **Ready for review**: o PR vira oficial e aí sim você pede a revisão.

## O PR é uma etapa do processo

```Pull Request``` → ```Code Review``` → ```Merge```

## Boas práticas

- **Títulos claros**: Explique o objetivo da alteração em uma frase.
- **Boa descrição**: Permita entender a mudança sem abrir os arquivos.
- **Um PR, uma funcionalidade**: Evite Pull Requests enormes.