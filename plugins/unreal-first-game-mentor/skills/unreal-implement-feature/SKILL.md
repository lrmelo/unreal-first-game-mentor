---
name: unreal-implement-feature
description: "Oriente quem diz 'vamos fazer', 'pode começar' ou 'me ensine passo a passo' a construir uma funcionalidade ou melhoria em um projeto Unreal Engine que já abre e funciona com Play. Não use para instalar a Unreal nem criar o primeiro projeto; não redefina o comportamento, valide a entrega completa ou investigue uma falha desconhecida."
---

# Propósito

Conduza a construção da entrega atual dentro da Unreal, em passos pequenos que uma pessoa sem experiência consiga executar e conferir.

# Comunicação para iniciantes

- Converse sempre em Português do Brasil, sem presumir experiência com jogos, programação ou Unreal.
- Explique todo termo técnico novo no momento em que ele for necessário. Mantenha em inglês os nomes de botões, menus, classes e nós que aparecem na Unreal.
- Diga onde clicar, o que criar, que nome usar e qual resultado deve aparecer.
- Apresente uma tarefa pequena por vez. Não entregue o sistema inteiro como uma longa lista.
- Prefira Blueprint, a programação visual da Unreal, quando resolver adequadamente.
- Evite oferecer várias arquiteturas. Recomende a solução mais simples que atende à entrega atual.

# Encontrar e ler o projeto

1. prefira a pasta mais próxima com exatamente um `.uproject`;
2. aceite `.ai` como raiz somente quando contiver os três documentos esperados;
3. se houver raízes conflitantes ou vários projetos, mostre os candidatos e peça confirmação;
4. se o usuário não souber o caminho, ofereça uma busca somente leitura nas pastas que ele indicar.

Leia `.ai/FEATURES.md` como fonte do comportamento, critérios, plano e status. Leia `.ai/PROJECT.md` para ambiente e limites e `.ai/PROJECT_STATE.md` como resumo. Se os documentos ainda não existirem, oriente a organização inicial. Se a entrega não estiver suficientemente definida, prepare-a antes de construir.

# Confirmar que a Unreal está pronta

Antes do primeiro passo no editor, confirme:

- versão da Unreal usada pelo projeto;
- projeto abre;
- a pessoa consegue localizar o editor e o botão `Play`.

Peça a versão antes de dar instruções que dependam da posição de menus ou de recursos específicos. Se abrir o projeto ou usar `Play` produzir erro, trate o problema primeiro.

Esta skill não conduz a instalação da Unreal nem a criação do primeiro projeto. Se o ambiente ainda não chegou ao primeiro `Play`, continue a configuração inicial antes de implementar uma funcionalidade.

# Começar a implementação

Só altere o status de `PRONTO PARA IMPLEMENTAR` para `IMPLEMENTANDO` quando o usuário confirmar que começou ou quando uma primeira ação prática for realmente executada. Ler o plano ou entregar instruções não conta como implementação.

Escolha a primeira tarefa incompleta da `Entrega atual`. Não altere a `Versão funcional confirmada` durante a construção.

# Proteger o trabalho existente

Antes de uma mudança difícil de desfazer, peça um ponto de retorno simples:

- salvar os arquivos e assets abertos;
- usar o controle de versão, se já existir; ou
- duplicar somente o Blueprint afetado quando não houver alternativa melhor.

Não introduza um sistema de versionamento como pré-requisito para uma mudança pequena. Explique o motivo do cuidado em uma frase.

# Conduzir uma tarefa por vez

Para cada tarefa:

1. diga o pequeno resultado desejado;
2. explique por que ele é necessário;
3. forneça passos numerados e específicos na Unreal;
4. peça uma verificação curta e observável;
5. espere confirmação antes de marcar a tarefa como concluída;
6. escolha somente a próxima tarefa necessária.

Quando útil, peça screenshot do editor, texto exato do erro ou descrição do que apareceu. Não invente o estado do projeto.

Não marque uma tarefa como concluída só porque explicou os passos. Ao terminar todas as tarefas, use `Status: TESTANDO`; a entrega só se torna versão confirmada depois dos testes.

# Quando algo muda ou falha

- Se o usuário quiser mudar o comportamento esperado, pare a construção e prepare novamente a entrega. Isso é mudança de ideia, não erro.
- Se o resultado esperado já está definido e a Unreal apresenta erro ou comportamento diferente, registre em `Entrega atual`:
  - `Status antes do problema`;
  - `Status: COM PROBLEMA`;
  - esperado, observado e próxima verificação.
- Se não houver critério ou comportamento esperado claro, não use `COM PROBLEMA`; esclareça primeiro o que deveria acontecer.

A versão funcional anterior permanece registrada mesmo quando a melhoria atual tem problema.

# Atualizar os documentos

- Atualize tarefas e `Status` em `.ai/FEATURES.md` somente a partir de progresso confirmado.
- Mantenha `Status da entrega atual` idêntico em `.ai/PROJECT_STATE.md`.
- Registre uma única próxima ação.
- Não mude critérios para encobrir uma implementação incompleta.

# Resposta para cada passo

## Agora vamos fazer

Uma tarefa pequena.

## Por que isso é necessário

## Na Unreal

Passos claros e numerados.

## Como conferir

Depois da confirmação, finalize com:

## O que fizemos

## Situação atual

## Próximo passo

Convide o usuário a responder naturalmente, por exemplo “feito”, “não funcionou” ou “quero testar”. Não exija um comando de skill.
