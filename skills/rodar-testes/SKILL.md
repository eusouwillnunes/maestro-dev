---
name: rodar-testes
description: "Executa a estratégia de testes do projeto, identifica fase atual, cria testes faltantes e reporta resultados em linguagem de negócio"
disable-model-invocation: true
---


Execute a estratégia de testes do projeto usando a skill `testes`.

Passos:
1. Identifique a fase do projeto (MVP, v1, v2)
2. Aplique a estratégia da fase (Pirâmide + Critérios de Aceitação + Segurança)
3. Verifique quais testes já existem no projeto
4. Crie os testes que faltam para a fase atual
5. Execute todos os testes
6. Reporte em linguagem de negócio: o que passou, o que falhou, o que corrigir
7. Se houver falhas de segurança, destaque com prioridade crítica

Se o argumento incluir "segurança" ou "security", priorize os testes de segurança (OWASP).
Se o argumento incluir uma funcionalidade específica, teste apenas essa funcionalidade.
