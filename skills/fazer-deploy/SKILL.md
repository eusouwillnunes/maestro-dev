---
name: fazer-deploy
description: "Executa o checklist de deploy completo — verifica local, testes, build, variáveis, faz deploy e verifica pós-deploy"
disable-model-invocation: true
---

Execute o deploy usando a skill `deploy`.

Passos:
1. Verificar que funciona localmente
2. Rodar testes (se existem)
3. Verificar build
4. Verificar variáveis de produção
5. Verificar banco de produção
6. Fazer deploy
7. Verificação pós-deploy
8. Se falhar, rollback imediato

Se o argumento incluir "rollback", volte para a versão anterior.
Se incluir "status", verifique o estado atual do deploy.
