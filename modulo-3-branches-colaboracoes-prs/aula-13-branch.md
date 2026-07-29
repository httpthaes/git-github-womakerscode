# Aula 13 • Conceito de Branch

São linhas de trabalho paralelas que permitem desenvolver sem afetar a versão principal do projeto. É como testar mudanças em uma cópia do documento; quando fica pronta, substitui a versão estável (main).

## Como equipes usam

Uma branch por funcionalidade

| **branch** | **funcionalidade** |
| --- | --- |
| main | versão estável |
| login | nova funcionalidade |
| cadastro | nova funcionalidade |
| correção-menu | correção de bug |

## Boas práticas

- **Nunca desenvolva direto na main**: mantenha a versão principal sempre estável.
- **Uma funcionalidade, uma branch**: facilita a revisão e reduz o risco de erros.
- **Nomes descritivos**: feat/login, fix/menu-mobile...