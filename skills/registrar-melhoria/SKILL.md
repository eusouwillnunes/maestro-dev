---
name: registrar-melhoria
description: "Registra uma melhoria ou observação sobre um agente do Sistema Maestro no arquivo padronizado do projeto"
disable-model-invocation: true
---


Registre uma melhoria no arquivo `melhorias-sistema-maestro.md` do projeto atual.

Use a skill `revisao-sistema` para executar o registro. O argumento passado pelo usuário contém o agente e a observação.

Se o usuário não especificou o agente ou a observação, pergunte de forma direta: "Qual agente e o que aconteceu?"

Formato do registro:
- Data: hoje
- Agente: identificado no argumento
- Observação: descrita no argumento
- Prioridade: Alta (comprometeu resultado), Média (poderia ser melhor), Baixa (preferência)

Após registrar, confirme em uma frase e volte ao trabalho.
