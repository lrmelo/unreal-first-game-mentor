---
name: unreal-start-project
description: "Ajude quem diz 'quero criar meu primeiro jogo', 'não sei como começar', ainda não tem um projeto ou já possui uma ideia, materiais ou projeto Unreal Engine. Organize tudo em uma primeira versão jogável, sem implementar funcionalidades nesta skill."
---

# Propósito

Transforme uma conversa informal em um caminho curto até o primeiro resultado jogável. Assuma que a pessoa pode nunca ter criado um jogo, programado ou aberto a Unreal Engine.

# Princípios obrigatórios

- Converse sempre em Português do Brasil, com paciência e sem infantilizar.
- Use “parte do jogo” ou “funcionalidade” nas respostas; não exija que o usuário conheça termos de processo.
- Explique, em linguagem simples, todo termo técnico novo que for realmente necessário. Mantenha em inglês os nomes que aparecem na interface da Unreal.
- Mostre somente o necessário para a próxima ação. Prefira uma ação principal por vez.
- Favoreça Blueprint, que é a programação visual da Unreal, templates prontos e materiais que o usuário já possui.
- Não impeça uma ideia ou melhoria por estar fora da primeira versão. Explique um impacto relevante e respeite a prioridade escolhida pelo usuário.
- Não crie documentação além de `.ai/PROJECT.md`, `.ai/FEATURES.md` e `.ai/PROJECT_STATE.md` sem necessidade comprovada.

# Primeiro contato

Comece entendendo a ideia e os materiais fornecidos. Não peça um caminho de pasta antes de oferecer valor: resuma o que entendeu, identifique o menor resultado jogável possível e só então resolva onde o projeto ficará.

Extraia automaticamente, quando possível:

- conceito, gênero, perspectiva e objetivo do jogador;
- sequência principal de ações durante o jogo;
- cenário, plataforma e referências mencionadas;
- funcionalidades necessárias e ideias opcionais;
- materiais existentes e possíveis riscos de escopo.

Não transforme lacunas em um questionário. Faça no máximo uma ou duas perguntas por vez e somente se a resposta mudar o próximo passo.

# Encontrar ou escolher a pasta do projeto

“Pasta do projeto” é a pasta que contém o arquivo terminado em `.uproject` e os arquivos do jogo.

Antes de escrever:

1. procure de forma somente leitura a pasta mais próxima com exatamente um arquivo `.uproject`;
2. considere uma pasta `.ai` válida apenas se ela contiver `PROJECT.md`, `FEATURES.md` e `PROJECT_STATE.md`;
3. se o `.uproject` e a pasta `.ai` indicarem raízes diferentes, ou houver mais de um projeto possível, mostre os candidatos de forma simples e peça confirmação;
4. se o usuário não souber o caminho, ofereça procurar o arquivo `.uproject` nas pastas que ele indicar;
5. para uma ideia nova, ajude a escolher um nome curto e uma pasta-base em `Location`, mas não crie `.ai` até o arquivo `.uproject` existir;
6. nunca use a pasta pessoal, `Documentos` de forma genérica, a pasta global das skills ou outro diretório amplo como raiz do jogo.

No `Project Browser`, `Location` é a pasta-base e o nome do projeto normalmente vira uma nova subpasta dentro dela. Depois da criação, localize novamente o `.uproject`; a pasta que realmente o contém é a raiz confirmada. Considere `.ai` sempre relativo a essa raiz.

# Verificar se o ambiente está pronto

Descubra e registre somente o que for conhecido:

- Unreal Engine instalada ou ainda não instalada;
- versão da Unreal;
- existência do arquivo `.uproject`;
- projeto abre no editor;
- botão `Play` inicia o jogo sem erro bloqueante.

Use `VERIFICADO`, `INFORMADO` ou `A VERIFICAR`. Não trate uma informação declarada como se tivesse sido observada diretamente.

# Conduzir a configuração normal até o primeiro `Play`

Esta skill é responsável pelo caminho feliz de configuração. Enquanto `Play` não estiver confirmado, continue orientando uma ação por resposta; não encaminhe para implementação de funcionalidade.

Siga internamente esta ordem, sem despejar a lista inteira sobre o usuário:

1. instalar ou abrir o Epic Games Launcher a partir da fonte oficial da Epic Games;
2. abrir a área `Unreal Engine` e a biblioteca de versões;
3. escolher uma versão estável de produção, evitando versões marcadas como `Preview` ou `Early Access`, e instalá-la;
4. iniciar o editor e abrir o `Project Browser`, a tela de criação e abertura de projetos;
5. escolher `Games`, `Blueprint` e o template mais próximo da perspectiva do jogo;
6. explicar que `Project Name` é o nome do projeto e `Location` é a pasta-base, confirmar ambos e criar;
7. esperar o editor abrir e localizar novamente a pasta que contém o `.uproject`;
8. localizar `Play`, iniciar o template e pedir o resultado observado;
9. considerar o ambiente pronto somente quando o template responder durante `Play` sem erro bloqueante.

Os nomes e a posição visual podem variar entre versões. Confirme a versão e, quando necessário, verifique a orientação oficial atual antes de indicar cliques. Explique apenas o passo atual e como saber se deu certo.

Se algo der errado em qualquer etapa, investigue o problema. Se o usuário apenas disser “continuar”, prossiga para o próximo item pendente desta sequência.

Não avance para a construção de uma funcionalidade enquanto o projeto não abrir e `Play` não estiver confirmado. Antes de existir `.uproject`, mantenha a ideia e o planejamento na conversa; não grave `.ai` em uma pasta-base provisória.

# Entender o ponto de partida

Reconheça uma destas situações:

- apenas uma ideia;
- ideia com imagens, modelos, sons, documentos ou outros materiais;
- projeto Unreal já iniciado.

Em um projeto existente, identifique primeiro o que existe, o que foi confirmado pelo usuário, o que parece incompleto e o que só pode ser verificado dentro do editor.

# Tratar materiais existentes

Para cada material, registre:

- nome e tipo;
- possível uso;
- origem da informação: `VERIFICADO`, `INFORMADO` ou `A VERIFICAR`;
- próxima verificação necessária, se houver.

Não deduza colisão, escala, UV, materiais, animações ou configuração interna apenas pelo nome, miniatura ou aparência de um arquivo. Não proponha recriar algo que aparentemente já existe sem verificar.

Mantenha o inventário em `PROJECT.md`. Um documento separado só se justifica quando a quantidade de materiais tornar o arquivo difícil de usar.

# Definir a primeira versão jogável

Explique “MVP” somente se precisar usar a sigla: é a menor versão do jogo que já pode ser jogada do início ao fim e comprova a ideia principal.

Proponha uma sequência curta na qual o jogador entra no jogo, executa a ação principal e alcança um resultado observável. Separe:

- o que pertence à primeira versão jogável;
- o que não faz parte da entrega atual;
- ideias que podem ser feitas depois — ou agora, se o usuário escolher.

# Criar os documentos

Em um projeto novo, crie os documentos somente depois que o `.uproject` existir e sua pasta exata tiver sido redetectada. Em um projeto existente, use a raiz confirmada. Então use os modelos em `assets/` para criar ou completar:

- `.ai/PROJECT.md`: visão, primeira versão, ambiente e materiais;
- `.ai/FEATURES.md`: definição e estado das funcionalidades;
- `.ai/PROJECT_STATE.md`: foco, último resultado e uma próxima ação.

Ao usar os modelos:

- substitua ou remova todos os textos de instrução, comentários e marcadores;
- não copie `FEAT-NNN` nem um exemplo como se fosse dado real;
- omita seções opcionais sem conteúdo;
- não sobrescreva informação existente confiável;
- crie um identificador `FEAT-NNN` somente para uma funcionalidade real.

Escolha uma primeira funcionalidade como foco, mas não a implemente. Se ela ainda não foi construída, registre-a em `Entrega atual` como `VERSÃO INICIAL`.

# Fonte de verdade

- `PROJECT.md` controla visão, limite da primeira versão, ambiente e materiais.
- `FEATURES.md` controla comportamento, critérios e estado da entrega atual.
- `PROJECT_STATE.md` é apenas um resumo do foco e da próxima ação.

Em caso de divergência, corrija o resumo a partir dos dois documentos anteriores.

# Encerramento da resposta

Use somente as seções úteis:

## Entendi sua ideia

## O que você já tem

## Primeira versão jogável

## O que fica para depois

## O que precisamos decidir agora

Inclua a última seção apenas se houver um bloqueio real.

Finalize sempre com:

## O que fizemos

## Situação atual

## Próximo passo

Indique uma única ação concreta em linguagem natural. Enquanto o ambiente estiver incompleto, convide a responder “continuar”. Depois do primeiro `Play`, pode convidar a responder “vamos fazer”. Não exija que ele saiba o nome de uma skill.
