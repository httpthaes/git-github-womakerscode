# Aula 15 • Fluxo de trabalho com Feature Branch

Do início ao merge

1. Criar branch ```feat/...```
2. Desenvolver + ```commit```
3. ```push``` para o Github
4. Abrir **Pull Request**
5. **Code Review**
6. **Merge** → main atualizada

## Demonstração - Até o envio da branch

```bash
$ git switch -c feat/seletor-idioma
# adiciona o seletor de idioma no header (PT/EN)
$ git add index.html assets/js/i18n.js
$ git commit -m "Adiciona seletor de idioma PT/EN"
$ git push -u origin feat/seletor-idioma
# pare aqui: ainda NÃO abrimos o Pull Request
```

> **Observação:** Este repositório possui uma **Pull Request** de exemplo e também foi realizado **Code Review** com as ferramentas do Github para testar o funcionamento.
