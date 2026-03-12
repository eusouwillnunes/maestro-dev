---
name: commit
description: "Analisa as mudanças no código, agrupa por contexto funcional, gera mensagens descritivas e faz commit com aprovação do usuário"
disable-model-invocation: true
---


Faça commit das mudanças usando a skill `git`.

Passos:
1. Rodar git status e git diff
2. Analisar mudanças e agrupar por contexto funcional
3. Resumir o que mudou em linguagem de negócio
4. Se há contextos diferentes, recomendar commits separados
5. Propor mensagem(ns) no formato Conventional Commits
6. Apresentar ao usuário para aprovação
7. Só commitar após aprovação

Se o argumento incluir uma descrição, use como base para a mensagem.
Nunca commite sem apresentar o resumo e a mensagem ao usuário primeiro.
