---
name: unreal-test-feature
description: "Ajude quando o usuário disser 'terminei', 'como vejo se funcionou?' ou 'quero testar' uma funcionalidade, melhoria ou primeira versão na Unreal Engine. Conduza testes simples e registre resultados observáveis; não diagnostique profundamente a causa de uma falha."
---

# Propósito

Ajude a pessoa a comprovar, jogando, se a entrega faz tudo o que foi combinado. Testes manuais são suficientes enquanto uma automação não trouxer benefício concreto.

# Comunicação para iniciantes

- Converse sempre em Português do Brasil.
- Não presuma que o usuário conhece técnicas de teste.
- Explique todo termo técnico novo necessário e mantenha em inglês os nomes vistos na interface da Unreal.
- Apresente um teste por vez e peça apenas o resultado observado.
- Não mostre nomes de skills como comandos obrigatórios.

# Encontrar e ler o projeto

1. prefira a pasta mais próxima com exatamente um `.uproject`;
2. aceite `.ai` como raiz somente quando contiver os três documentos esperados;
3. se houver conflito ou mais de um candidato, mostre-os e peça confirmação;
4. se o usuário não souber o caminho, ofereça uma busca somente leitura nas pastas que ele indicar.

Leia:

- critérios e evidências em `.ai/FEATURES.md`;
- ambiente e primeira versão em `.ai/PROJECT.md`;
- foco e próxima ação em `.ai/PROJECT_STATE.md`;
- evidências fornecidas pelo usuário.

Não invente resultados. Se a entrega atual não tiver critérios observáveis, esclareça e prepare os critérios antes de testar.

# Preparar os testes

Transforme cada critério da `Entrega atual` em uma ação concreta. Inclua somente:

- caminho principal;
- condição inválida ou limite realmente relevante;
- comportamento da versão confirmada que a mudança possa ter afetado;
- integração com o restante do jogo, quando necessária.

Dois ou três testes podem cobrir uma entrega simples, mas todos os critérios atuais precisam aparecer em pelo menos um teste. Não use a categoria ambígua “critério essencial”.

Se não houver `Entrega atual`, teste a `Versão funcional confirmada` somente quando o usuário pedir uma nova verificação ou quando estiver validando a primeira versão jogável completa.

# Conduzir um teste por vez

Para cada teste:

1. preparação;
2. ação no editor ou durante `Play`;
3. resultado esperado;
4. pergunta curta: “O que aconteceu?”

Registre `PASSOU`, `FALHOU` ou `NÃO TESTADO`. Ausência de mensagem de erro não prova que o comportamento funcionou.

Em um reteste, atualize a mesma entrada de teste e acrescente uma nota curta com o resultado anterior e a correção realizada. Não crie uma sequência longa de entradas duplicadas.

# Quando todos os testes passam

Todos os critérios da entrega atual devem passar.

- Se era a primeira entrega, transforme-a em `Versão funcional confirmada`.
- Se era uma melhoria ou correção, incorpore os novos comportamentos e critérios à versão confirmada sem apagar o que continua válido.
- Em `Entregas incorporadas`, preserve cada entrega com seu próprio escopo; por exemplo, `Porta básica — MVP` e `Fechadura — PÓS-MVP`.
- Mova para a versão confirmada uma evidência curta dos testes.
- Remova a seção `Entrega atual` depois da incorporação.
- Em `.ai/PROJECT_STATE.md`, use `Entrega atual: NENHUMA`, `Escopo: NÃO SE APLICA` e `Status da entrega atual: NENHUMA`.
- Remova o problema atual, registre o último resultado confirmado e escolha uma nova próxima ação.

Uma funcionalidade com versão confirmada e sem entrega atual está concluída no momento, sem precisar de um campo `Status: CONCLUÍDO`.

# Quando um teste falha

Se houver uma entrega atual:

Se ela já estiver `COM PROBLEMA` e `Status antes do problema` estiver preenchido, preserve esse valor. Nunca o substitua por `COM PROBLEMA`.

1. registre esperado e observado no teste correspondente;
2. se ainda não estiver `COM PROBLEMA`, registre o status atual em `Status antes do problema`;
3. use `Status: COM PROBLEMA` somente na entrega atual;
4. preserve a versão funcional confirmada;
5. indique como próxima ação investigar o problema.

Se a falha aparecer ao retestar uma versão confirmada sem entrega atual, preserve o registro histórico e crie uma `Entrega atual` do tipo `CORREÇÃO`, com `Status: COM PROBLEMA` e critérios de restauração. Não finja que a versão nunca havia funcionado.

Se o usuário quiser mudar o resultado esperado em vez de corrigir o comportamento, trate como uma nova definição e não como falha técnica.

# Testar a primeira versão jogável inteira

Quando todas as funcionalidades necessárias tiverem versão confirmada, conduza um teste curto de ponta a ponta:

1. iniciar uma partida;
2. executar a sequência principal;
3. alcançar o objetivo da primeira versão;
4. confirmar que não existe falha bloqueante.

Só então registre `PRIMEIRA VERSÃO JOGÁVEL` em `PROJECT_STATE.md`.

# Atualizar os documentos

- `FEATURES.md` é a fonte de verdade dos critérios, resultados, versão confirmada e entrega atual.
- `PROJECT_STATE.md` resume o mesmo status, o último resultado e uma próxima ação.
- Mantenha o registro curto; não crie um diário de todas as sessões.

# Durante cada teste

## Teste atual

## Faça isto

## Resultado esperado

## O que aconteceu?

# Ao terminar

## Resultado

## O que fizemos

## Situação atual

## Próximo passo

Peça uma resposta natural, como “passou”, “falhou” ou uma descrição do que apareceu.
