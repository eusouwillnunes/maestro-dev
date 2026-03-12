# Maestro Dev — Plugin para Claude Code

Criado por **@eusouwillnunes** para os membros da 
**A Comunidade dos Últimos** (acomunidadedosultimos.com.br).

Baseado no Sistema Maestro v3.0 — Desenvolvido por Willian Nunes.

---

## O que é

O Maestro Dev é um conjunto de 7 agentes especializados que 
levam um projeto de software do zero ao ar. Pensado para 
quem dirige e não codifica — você sabe o que quer construir, 
os agentes resolvem o como.

Você conversa em linguagem de negócio. "Quero criar um app 
de gestão de tarefas para freelancers." A partir disso, os 
agentes te guiam pela jornada completa: o que construir 
primeiro, qual tecnologia usar, como organizar os dados, 
configurar tudo, testar, versionar e colocar no ar.

Cada agente é um especialista com metodologias consolidadas 
de mercado. Não são prompts genéricos — são profissionais 
estruturados que sabem o que fazer e quando fazer.

---

## Como instalar

### Opção 1 — Via GitHub (recomendado)

No terminal do Claude Code:

```
/plugin install github:eusouwillnunes/maestro-dev
```

Pronto. Os agentes e comandos ficam disponíveis 
imediatamente.

Para atualizar quando houver versão nova:

```
/plugin update maestro-dev
```

### Opção 2 — Via arquivo local

Se você baixou o arquivo `maestro-dev.zip`:

```
/plugin install /caminho/onde/voce/salvou/maestro-dev.zip
```

Substitua `/caminho/onde/voce/salvou/` pelo caminho real 
no seu computador. Exemplo no Mac:

```
/plugin install ~/Downloads/maestro-dev.zip
```

Após instalar, os agentes ativam automaticamente. Você 
também pode usar os comandos diretamente.

---

## A jornada de um projeto

Os agentes seguem uma sequência natural. Cada um recebe o 
output do anterior e avança o projeto:

```
1. Produto    → Define o que construir e pra quem
2. Arquiteto  → Define como construir (tecnologias, estrutura)
3. Banco      → Modela os dados do projeto
4. Setup      → Configura tudo e deixa pronto pra desenvolver
5. Claude Code → Desenvolve (você conversa normalmente)
6. Git        → Salva o progresso com histórico organizado
7. Testes     → Verifica que tudo funciona
8. Deploy     → Coloca no ar
```

Você não precisa seguir essa ordem rigidamente — mas na 
primeira vez, é a sequência que faz mais sentido.

---

## Passo a passo

### 1. Defina o que construir

Converse normalmente: "quero criar um app de gestão de 
tarefas para freelancers".

O agente **Produto** (Marty Cagan + Eric Ries) ativa e te 
guia com 5 frameworks:

- **Lean Canvas** — visão completa do produto em 1 página
- **Jobs to Be Done** — o que o usuário realmente precisa
- **User Story Mapping** — funcionalidades organizadas 
  por jornada
- **MoSCoW** — o que entra no MVP e o que fica pra depois
- **Build-Measure-Learn** — como evoluir após o lançamento

Ao final, você tem: Canvas preenchido, user stories 
priorizadas e MVP definido.

### 2. Defina como construir

Diga "define a arquitetura do projeto".

O agente **Arquiteto** (Simon Brown + Martin Fowler) recebe 
o que o Produto definiu e toma as decisões técnicas:

- **Matriz de Seleção de Stack** — qual tecnologia usar 
  e por quê
- **C4 Model** — diagramas visuais que você entende
- **ADRs** — cada decisão documentada com o porquê
- **Blueprint** — planta única do projeto
- **CLAUDE.md** — regras para o Claude Code seguir

Ao final, você tem: stack definida, blueprint completo e 
CLAUDE.md gerado. Você não precisa entender de tecnologia 
— o Arquiteto decide e justifica.

### 3. Modele os dados

Diga "modela o banco de dados" e descreva em linguagem 
natural: "o usuário tem projetos, cada projeto tem tarefas, 
cada tarefa tem status e prazo".

O agente **Banco de Dados** (Joe Celko) traduz em:

- Tabelas e relacionamentos
- Regras de integridade (o que é obrigatório, o que é único)
- Segurança (quem pode ver o quê)
- Dados de teste para verificar que funciona

### 4. Inicialize o projeto

Use o comando:
```
/maestro-dev:iniciar-projeto
```

O agente **Setup** cria tudo automaticamente:

- Estrutura de pastas conforme o Blueprint
- Dependências instaladas
- Variáveis de ambiente configuradas (te guia pra obter 
  as chaves dos serviços)
- Segurança do Claude Code configurada (bloqueia comandos 
  perigosos, protege arquivos sensíveis)
- CLAUDE.md no lugar
- Git inicializado
- Health check para garantir que tudo funciona

Ao final, o projeto está pronto para desenvolver.

### 5. Desenvolva

A partir daqui, converse com o Claude Code normalmente para 
implementar as funcionalidades. Ele segue as regras do 
CLAUDE.md que o Arquiteto gerou.

### 6. Salve o progresso

Use o comando:
```
/maestro-dev:commit
```

O agente **Git** analisa o que você mudou, agrupa por 
contexto funcional, e gera commits com mensagens claras. 
Ele te mostra o que mudou antes de salvar e pede sua 
aprovação.

Se mudou coisas de assuntos diferentes, ele sugere 
separar em commits. Assim o histórico fica organizado 
e você pode voltar atrás com precisão.

### 7. Veja o resultado

Use o comando:
```
/maestro-dev:preview
```

O agente **Deploy** inicia o servidor local. Se der erro, 
ele traduz a mensagem (em vez de "EADDRINUSE" você vê 
"a porta já está sendo usada") e resolve automaticamente.

### 8. Teste

Use o comando:
```
/maestro-dev:rodar-testes
```

O agente **Testes** (Kent Beck) verifica que tudo funciona:

- Funcionalidades (o que deveria funcionar, funciona?)
- Segurança (login protegido? dados expostos? permissões?)
- Edge cases (o que acontece com campo vazio, dado inválido?)

Reporta em linguagem de negócio: "o login funciona, mas 
aceita senha vazia — precisa de correção."

### 9. Coloque no ar

Use o comando:
```
/maestro-dev:fazer-deploy
```

O agente **Deploy** segue um checklist completo antes de 
subir: funciona local? Testes passam? Build ok? Variáveis 
de produção? Depois do deploy, testa em produção. Se algo 
falhar, volta à versão anterior automaticamente.

---

## Todos os comandos

| Comando | O que faz | Quando usar |
|---------|-----------|-------------|
| `/maestro-dev:iniciar-projeto` | Cria projeto do zero | No início de um projeto novo |
| `/maestro-dev:commit` | Analisa mudanças e salva com mensagem clara | Sempre que quiser salvar progresso |
| `/maestro-dev:preview` | Inicia servidor local e resolve problemas | Quando quiser ver o resultado |
| `/maestro-dev:rodar-testes` | Testa funcionalidades e segurança | Antes de deploy ou quando quiser verificar |
| `/maestro-dev:fazer-deploy` | Coloca no ar com checklist completo | Quando estiver pronto para publicar |
| `/maestro-dev:registrar-melhoria` | Anota melhoria para um agente | Quando perceber que um agente pode melhorar |
| `/maestro-dev:consolidar-melhorias` | Revisa melhorias anotadas | Periodicamente, para evoluir os agentes |

---

## Todos os agentes

| Agente | Referência | O que faz | Quando ativa |
|--------|-----------|-----------|-------------|
| Produto | Cagan + Ries | Define o que construir: MVP, user stories, priorização | "quero criar um app", "qual o MVP" |
| Arquiteto | Brown + Fowler | Define como construir: stack, blueprint, CLAUDE.md | "qual tecnologia usar", "como estruturar" |
| Banco de Dados | Joe Celko | Modela dados: tabelas, relacionamentos, segurança | "o usuário tem projetos", "cria as tabelas" |
| Setup | Eng. DevOps | Inicializa: pastas, dependências, ambiente, segurança | "inicia o projeto", "configura tudo" |
| Testes | Kent Beck | Testa: funcional, segurança, edge cases | "testa isso", "funciona?", "tá seguro?" |
| Deploy | Eng. Plataforma | Ambiente local e produção: servidor, domínio, rollback | "quero ver funcionando", "coloca no ar" |
| Git | Guardião do Histórico | Versiona: commits inteligentes, branches, restauração | "salva isso", "quero voltar atrás" |

---

## Dicas importantes

**Você não precisa saber programar.** Sua responsabilidade é 
saber o que quer construir e validar os resultados. Todo o 
resto os agentes resolvem.

**Os agentes pedem informação antes de executar.** Se você 
pedir algo vago, o agente vai perguntar antes de sair 
fazendo. Isso evita construir a coisa errada.

**Cada agente tem um escopo.** Se pedir algo fora do escopo, 
ele indica quem é o certo. Não force — são especialistas.

**Salve progresso com frequência.** Use `/maestro-dev:commit` 
sempre que terminar algo que funciona. Se quebrar depois, 
você volta atrás.

**Teste antes de publicar.** Use `/maestro-dev:rodar-testes` 
antes de `/maestro-dev:deploy`. Corrigir local é mais fácil 
que corrigir em produção.

**O setup configura a segurança.** O agente de Setup cria um 
arquivo que impede o Claude Code de rodar comandos perigosos, 
protege seus arquivos sensíveis e pede confirmação antes de 
ações arriscadas. Isso é automático — você não precisa 
configurar nada.

---

## Como evoluir os agentes

### 1. Registre quando perceber algo

```
/maestro-dev:registrar-melhoria o Arquiteto não perguntou 
escala esperada antes de definir a stack
```

### 2. Consolide periodicamente

Crie um projeto "Maestro — Revisão" e use:

```
/maestro-dev:consolidar-melhorias
```

### 3. Implemente as melhorias

O agente propõe alterações, gera o SKILL.md atualizado 
e você reinstala o plugin.

---

Criado por **@eusouwillnunes** | **A Comunidade dos Últimos**
acomunidadedosultimos.com.br
