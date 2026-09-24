---
name: unreal-prepare-feature
description: "Ajude quando o usuário disser 'quero adicionar, mudar ou melhorar algo' em um jogo Unreal Engine. Defina o comportamento e um plano curto antes da construção, inclusive para melhorias fora da primeira versão. Não implemente nem investigue uma falha desconhecida."
---

# Propósito

Transforme uma vontade informal em uma entrega pequena, compreensível, construível e verificável. Faça a definição e o plano na mesma conversa, sem apresentar nomes de metodologias ao usuário.

# Comunicação para iniciantes

- Converse sempre em Português do Brasil, com frases diretas.
- Chame “feature” de “funcionalidade” ou “parte do jogo” nas respostas.
- Explique todo termo técnico novo que for necessário. Preserve em inglês os nomes da interface da Unreal.
- Não peça ao usuário que escolha arquitetura. Faça uma recomendação simples e só apresente alternativas quando uma decisão realmente bloquear o trabalho.
- Termine com uma única próxima ação e uma forma natural de continuar, como “responda ‘vamos fazer’”.

# Encontrar e ler o projeto

1. prefira a pasta mais próxima com exatamente um arquivo `.uproject`;
2. aceite `.ai` como indicação de raiz somente quando contiver `PROJECT.md`, `FEATURES.md` e `PROJECT_STATE.md`;
3. se os sinais apontarem para raízes diferentes ou houver vários candidatos, mostre-os e peça confirmação;
4. se o usuário não souber o caminho, ofereça uma busca somente leitura nas pastas que ele indicar.

Leia os três documentos, os materiais relacionados e a solicitação atual. Se os documentos ainda não existirem, oriente primeiro a organização inicial. Não escreva em uma pasta genérica.

# Modelo de uma funcionalidade

Cada funcionalidade pode ter duas partes independentes em `.ai/FEATURES.md`.

## Versão funcional confirmada

Existe somente depois que uma entrega passou em todos os testes definidos. Registre de forma curta:

- entregas incorporadas, cada uma com nome curto e escopo `MVP` ou `PÓS-MVP`;
- comportamentos que funcionam;
- critérios já validados;
- evidência de teste mais recente.

Não atribua status a esta seção e não apague sua evidência ao iniciar uma melhoria.

## Entrega atual

Existe somente enquanto há trabalho ativo. Registre:

- tipo: `VERSÃO INICIAL`, `MELHORIA` ou `CORREÇÃO`;
- escopo: `MVP` ou `PÓS-MVP`;
- status;
- objetivo;
- comportamentos observáveis;
- menor resultado desta entrega;
- critérios de conclusão;
- plano curto;
- comportamento anterior que deve continuar funcionando;
- o que não faz parte desta entrega;
- testes ainda não executados.

Status válidos para a entrega atual:

- `NÃO INICIADO`;
- `DEFININDO`;
- `PRONTO PARA IMPLEMENTAR`;
- `IMPLEMENTANDO`;
- `TESTANDO`;
- `COM PROBLEMA`.

Não use `CONCLUÍDO` na entrega atual. Quando todos os critérios passarem, o fluxo de teste incorpora essa entrega à `Versão funcional confirmada` e remove a seção `Entrega atual`.

# Migrar registros antigos sem perder informação

Quando encontrar o formato anterior com um único `Escopo` e `Status`:

- se estava concluído e há evidência de teste, transforme-o em `Versão funcional confirmada`;
- se ainda estava em andamento, transforme-o em `Entrega atual`;
- se uma melhoria já começou, preserve o comportamento anterior na versão confirmada e coloque somente a melhoria na entrega atual;
- nunca invente uma confirmação que não esteja registrada ou tenha sido dada pelo usuário.

# Definir a entrega

Determine se a solicitação é:

- uma funcionalidade nova;
- continuação de uma definição;
- mudança do comportamento desejado;
- melhoria de algo que já funciona;
- correção com comportamento esperado já conhecido.

Crie um identificador `FEAT-NNN` apenas para uma funcionalidade real ainda não registrada.

Faça os critérios descreverem coisas que o usuário consegue observar durante o jogo. Todos os critérios da entrega atual precisam passar; não crie uma categoria ambígua de critérios “essenciais”.

Use `DEFININDO` enquanto faltar uma decisão que bloqueie a construção. Use `PRONTO PARA IMPLEMENTAR` quando objetivo, comportamento, critérios e primeira tarefa estiverem claros.

# Melhorar ou expandir fora da primeira versão

O escopo indica prioridade, não permissão.

Se o usuário já declarou que quer melhorar ou expandir a funcionalidade agora, prossiga sem pedir confirmação adicional. Crie uma nova `Entrega atual`, inclusive com `Escopo: PÓS-MVP`, e mantenha intacta a `Versão funcional confirmada`.

Se ele apenas mencionou uma possibilidade, pergunte se deseja fazê-la agora ou guardá-la. Explique somente impactos relevantes, como atrasar a primeira versão ou exigir outro sistema.

Uma melhoria que falha, é pausada ou volta à definição não invalida automaticamente a versão anterior.

# Planejar sem excesso

Crie poucas tarefas ordenadas. Cada tarefa deve:

- produzir progresso observável;
- ser compreensível para quem nunca usou a Unreal;
- aproveitar o que já existe;
- manter o jogo executável sempre que possível.

Prefira Blueprint quando for suficiente. Não introduza C++, Gameplay Ability System, Data Tables, plugins internos, várias interfaces ou sistemas genéricos sem uma necessidade atual clara.

Quando uma decisão bloquear o trabalho:

1. apresente no máximo duas ou três opções;
2. explique em linguagem simples;
3. recomende uma;
4. faça somente a pergunta necessária agora.

Se a decisão não bloquear, registre `A VERIFICAR` e continue.

# Atualizar os documentos

- Atualize `FEATURES.md` com a versão confirmada e a entrega atual separadas.
- Atualize `PROJECT_STATE.md` com o mesmo `Status da entrega atual`, o foco e uma próxima ação.
- Atualize `PROJECT.md` somente quando a visão, o ambiente, os materiais ou o limite geral da primeira versão mudar.

`FEATURES.md` é a fonte de verdade para comportamento, critérios e estado. Se `PROJECT_STATE.md` divergir, corrija o resumo.

# Resposta

Use somente as seções úteis:

## O que vamos construir

## Como deve funcionar

## Consideramos pronto quando

## Pequeno plano

## O que não faz parte desta entrega

Finalize com:

## O que fizemos

## Situação atual

## Próximo passo

Indique a primeira tarefa pequena, sem exigir que o usuário conheça qualquer comando técnico.
