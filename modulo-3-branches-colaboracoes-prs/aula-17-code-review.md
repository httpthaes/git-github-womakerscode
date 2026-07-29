# Aula 17 • Code Review: revisando alterações em um PR

Ter outra pessoa olhando o código aumenta a qualidade, reduz erros e é uma das melhores formas de aprender em equipe. No Code Review perguntamos:

- A alteração resolve o problema?
- O código está claro?
- Segue o padrão do projeto?

## Files changed: A tela que revisores mais usam

Nessa tela o Github destaca exatamente o que foi adicionado e removido.

```
+ ## Contato
+ Entre em contato pelo LinkedIn.
- (versão anterior)
```

## Revisar localmente: trazendo o PR para a máquina

```bash
$ git fetch origin
# baixa as branches novas do GitHub
$ git switch docs/atualiza-faq
# entra na branch do PR para ler o texto de perto
$ git diff origin/main...HEAD
# compara com a main remota sem alterar a branch
```

> Com o GitHub CLI dá para baixar a branch pelo PR: gh pr checkout <número>. Durante a revisão, não faça commits ou merges na branch de outra pessoa sem combinar.

## Três formas de responder um PR

| Decisão | Significado |
| --- | --- |
| Comment | Deixa comentários gerais sem aprovar ou solicitar alterações explicitamente. |
| Approve | Sinaliza que as alterações estão prontas para o merge. |
| Request changes | Peça ajustes antes de integrar (merge). |

## Evidência antes da decisão

- Atende à Issue e aos critérios de aceite?
- O escopo está focado e sem arquivos acidentais?
- Texto, código, links e testes estão corretos?
- O PR explica como a mudança foi verificada?