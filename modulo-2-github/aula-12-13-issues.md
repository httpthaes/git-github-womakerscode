# Aula 12 e 13 • Issues: organizando o trabalho e resolvendo tarefas

Um registro de uma Github Issue segue o mesmo objetivo de um Kanban, onde temos uma lista de tarefas para **corrigir um bug**, **criar nova funcionalidade** ou **dúvida/tarefa de trabalho a organizar**.

- Issues permitions: nas configurações, conseguimos alterar quem consegue criar novas Issues naquele repositório. Quando fazemos um fork em um projeto, temos que alterar a permissão para ativar as Issues no projeto.

## Recursos das Issues

- **Labels**: etiquetas coloridas utilizadas para classificar uma Issue.

| Label | Quando usar | Exemplo |
| --- | --- | --- |
| ```bug``` | Corrigir um problema | Mensagem de erro incorreta, botão que não funciona, layout quebrado. | 
| ```enhancement``` | Melhoria em algo que já existe | Melhorar desempenho, tornar um texto mais claro, otimizar uma tela. |
| ```feature``` | Nova funcionalidade | Adicionar autenticação em duas etapas, criar tela de perfil. |
| ```documentation``` ou ```docs``` | Documentação | Atualizar README, adicionar guia de instalação. |
| ```refactor``` | Melhorar o código sem mudar o comportamento | Reorganizar funções, renomear variáveis, separar arquivos. |
| ```style``` | Alterações visuais ou de formatação | Ajustar cores, alinhamento, CSS, variáveis, separar arquivos. |
| ```test``` | Criar ou atualizar testes | Adicionar testes unitários ou de integração. |
| ```chore``` | Tarefas de manutenção | Atualizar dependências, configurar CI, limpar arquivos antigos. |

- **Assignees**: define quem é o responsável por trabalhar na Issue.
- **Milestones**: agrupam Issues em um mesmo objetivo, versão ou entrega.
- **Projects**: vincula a Issue a um Project para acompanhar seu progresso.
- **Views**: diferentes formas de visualizar as Issues dentro de um Project, como tabela, quadro Kanban ou cronograma.

> **Observação:** Este repositório possui uma *issue* de exemplo para demonstrar a estrutura e o funcionamento das Issues no GitHub.

## Feche uma Issue pelo commit

```bash
$ git commit -m "Adiciona seção de contato · Closes #12"
# ao chegar na main, o GitHub fecha a Issue #12 automaticamente
```

Escrever #12 cria um link para a Issue; Closes #12 a fecha quando o Pull Request é integrado.

## Issues antes de Branches

Planejar, depois programar

1. Abrir a **Issue** registrando a tarefa
2. Criar a **branch** para resolver aquela Issue
3. Abrir o **Pull Request** com Closes #N na descrição
4. O **merge** fecha a Issue automaticamente