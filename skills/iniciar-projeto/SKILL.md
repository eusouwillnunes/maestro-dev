---
name: iniciar-projeto
description: "Inicializa um projeto completo do zero usando o Blueprint do Arquiteto — cria estrutura, instala dependências, configura ambiente, segurança e verifica que tudo funciona"
disable-model-invocation: true
---


Inicialize o projeto usando a skill `setup`.

Passos:
1. Verifique se existe Blueprint do Arquiteto. Se não, 
   pergunte a stack ou sugira o padrão (Next.js + Supabase + Vercel).
2. Siga o Checklist de Inicialização completo
3. Configure ambiente (.env.local) e segurança (.claude/settings.json)
4. Guie o usuário para obter chaves de serviços externos
5. Execute o Health Check
6. Reporte o status final

Se o argumento incluir uma stack específica, use-a.
Se não, siga o Blueprint ou pergunte.
