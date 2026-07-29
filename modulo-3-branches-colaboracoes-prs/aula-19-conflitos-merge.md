# Aula 19 • Resolvendo conflitos de merge

Os conflitos de merge ocorrem quando temos duas mudanças no mesmo trecho e o git não sabe qual manter.

## Gerar o conflito (de propósito)

```bash
$ git switch -c atualiza-contato
# edite 1 linha do contato.md e salve
$ git commit -am "Atualiza contato"
# -am junta -a (--all) e -m (--message): prepara e commita de uma vez
$ git switch main
# edite a MESMA linha do contato.md, diferente
$ git commit -am "Ajusta contato"
$ git merge atualiza-contato
CONFLICT (content): Merge conflict in contato.md
```

## No VS Code

- **Accept Current Change**: Mantém apenas a alteração da branch em que você está no momento (por exemplo, a ```main```).
- **Accept Incoming Change**: Mantém apenas a alteração da branch que você está tentando juntar/mesclar (por exemplo, a ```atualiza-contato```).
- **Accept Both Changes**: Mantém o conteúdo das duas partes, uma abaixo da outra.

```bash
# git status mostra os arquivos em conflito a qualquer momento
$ git add README.md
$ git commit -m "Resolve conflito de merge"
```

> Não escolha Current, Incoming ou Both sem ler as duas versões. O resultado correto pode exigir edição manual. Mudou de ideia? ```git merge --abort``` cancela o merge.

## Boas práticas: Reduzindo conflitos

- **Faça pull com frequência**: Manter o local atualizado evita surpresas.
- **Commits pequenos**: Menos linhas alteradas, menos conflitos.
- **Converse com a equipe**: Especialmente ao mexer no mesmo arquivo.