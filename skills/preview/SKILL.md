---
name: preview
description: "Inicia o servidor local de desenvolvimento ou verifica se está funcionando — resolve problemas comuns automaticamente"
disable-model-invocation: true
---


Gerencie o ambiente local usando a skill `deploy`.

Passos:
1. Verificar se o servidor já está rodando
2. Se não está, iniciar com `npm run dev`
3. Se der erro, diagnosticar e resolver automaticamente
4. Confirmar que está acessível em localhost
5. Reportar status ao usuário

Se o argumento incluir "parar" ou "stop", pare o servidor.
Se incluir "reiniciar" ou "restart", pare e inicie novamente.
Se incluir um erro ou mensagem, diagnostique e resolva.
