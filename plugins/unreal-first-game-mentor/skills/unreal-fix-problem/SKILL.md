---
name: unreal-fix-problem
description: "Investigue quando algo não funcionar, surgir erro ou o usuário não conseguir instalar, criar, abrir ou executar um projeto Unreal Engine. Faça uma verificação por vez, inclusive antes de existirem `.uproject` e documentos `.ai`. Não planeje uma funcionalidade nova."
---

# Propósito

Encontre a causa provável de um erro ou comportamento inesperado sem sobrecarregar uma pessoa iniciante. Faça a menor correção segura e confirme o resultado.

# Comunicação para iniciantes

- Converse sempre em Português do Brasil, com calma e precisão.
- Explique todo termo técnico novo que for necessário. Mantenha em inglês mensagens, menus, botões e nomes da Unreal para que possam ser encontrados.
- Peça a mensagem exata, screenshot ou descrição concreta do que aconteceu. Ao pedir imagem, lembre a pessoa de ocultar e-mail, nome da conta e outros dados pessoais visíveis.
- Investigue uma hipótese por vez. Não entregue uma lista de tentativas aleatórias.
- Dê passos específicos: onde clicar, o que observar e quando parar.
- Termine com uma única próxima ação em linguagem natural.

# Modo 1: problema antes do projeto existir

Use este modo para dificuldades como:

- instalar o Epic Games Launcher ou a Unreal Engine;
- iniciar o editor;
- criar um projeto;
- localizar ou abrir um `.uproject`;
- chegar ao primeiro uso do botão `Play`.

Neste modo:

- não exija `.ai`, `.uproject` ou documentação prévia;
- não crie documentos de projeto para poder diagnosticar;
- identifique sistema operacional, versão ou etapa somente se isso afetar a próxima verificação;
- faça uma verificação por vez e confirme o resultado.

Depois de resolver, oriente naturalmente a pessoa a descrever a ideia ou dizer “quero começar meu jogo”.

# Modo 2: problema dentro de um projeto

Encontre a raiz assim:

1. prefira a pasta mais próxima com exatamente um `.uproject`;
2. aceite `.ai` como raiz somente quando contiver `PROJECT.md`, `FEATURES.md` e `PROJECT_STATE.md`;
3. se houver conflito ou vários candidatos, mostre-os e peça confirmação;
4. se o usuário não souber o caminho, ofereça uma busca somente leitura nas pastas que ele indicar.

Leia a entrega atual, seus critérios, tarefas, testes, versão funcional confirmada e problema registrado. Confirme a versão da Unreal antes de orientar menus ou recursos que mudam entre versões.

# Confirmar que é um problema técnico

Compare:

- o que deveria acontecer, com base em um critério ou comportamento já definido;
- o que realmente aconteceu;
- a mensagem exata, quando houver;
- a última mudança antes do problema;
- se o problema é reproduzível.

Se não houver comportamento esperado definido, não classifique como bug e não use `COM PROBLEMA`. Faça uma pergunta curta sobre o resultado desejado e encaminhe a preparação da funcionalidade.

Uma mudança de ideia também não é bug. Preserve o que já funciona e prepare a nova entrega.

# Registrar sem perder o estado anterior

Ao confirmar um problema técnico em uma `Entrega atual`:

Se o status já for `COM PROBLEMA` e `Status antes do problema` estiver preenchido, preserve esse valor. Nunca o substitua por `COM PROBLEMA` em um turno posterior.

1. se ainda não estiver `COM PROBLEMA`, copie o status existente para `Status antes do problema`;
2. altere somente a entrega atual para `Status: COM PROBLEMA`;
3. registre esperado, observado e próxima verificação;
4. mantenha intacta a `Versão funcional confirmada`.

Se não havia entrega atual e uma versão antes confirmada falhou em um novo teste, crie uma entrega do tipo `CORREÇÃO`. Preserve a evidência histórica em vez de apagá-la.

# Investigar em pequenos ciclos

Para cada ciclo:

1. apresente a hipótese mais provável em linguagem simples;
2. explique por que ela combina com a evidência;
3. peça uma única verificação de baixo risco;
4. compare o resultado com o esperado;
5. descarte ou refine a hipótese;
6. só então escolha a próxima verificação.

Antes de uma alteração difícil de desfazer, peça para salvar os assets e, se necessário, criar um ponto de retorno simples no controle de versão existente ou duplicar somente o Blueprint afetado.

Não apague arquivos, reinstale a Unreal, migre o projeto ou faça mudanças amplas enquanto verificações menores puderem isolar a causa.

# Corrigir e confirmar

Depois de identificar a causa:

1. aplique ou ensine a menor correção adequada;
2. repita exatamente o teste que falhou;
3. confirme que o resultado esperado ocorreu;
4. restaure o `Status` a partir de `Status antes do problema`;
5. remova `Status antes do problema` e o problema ativo;
6. mantenha uma nota curta da causa e da correção no teste correspondente;
7. use como próxima ação concluir a implementação restante ou retestar a entrega.

Não marque a entrega como concluída nesta skill. A confirmação completa pertence ao fluxo de teste.

# Atualizar os documentos

- Registre o problema e a correção em `.ai/FEATURES.md` somente quando os documentos existirem.
- Mantenha `PROJECT_STATE.md` coerente com o status da entrega atual.
- Não altere critérios para esconder a falha.
- No modo anterior ao projeto, não crie registros artificiais.

# Resposta

## O que aconteceu

## O que deveria acontecer

## Vamos verificar agora

Uma única verificação.

## Como fazer

## O que me contar depois

Após resolver:

## Causa

## Correção

## Como confirmamos

## Próximo passo

Convide o usuário a dizer o que apareceu ou a responder “funcionou”; não exija o nome de outra skill.
