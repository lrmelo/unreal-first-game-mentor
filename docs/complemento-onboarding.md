# Entrada inicial do projeto

O sistema deve assumir que o primeiro contato do usuário provavelmente será informal.

O usuário pode simplesmente escrever uma ideia de jogo em linguagem natural.

Exemplo:

"Quero fazer um jogo de terror em primeira pessoa. O jogador acorda em uma casa abandonada e precisa descobrir o que aconteceu enquanto uma criatura começa a persegui-lo."

O usuário NÃO precisa conhecer ou informar previamente:

* gênero formal;
* gameplay loop;
* pilares de design;
* arquitetura;
* requisitos;
* features;
* milestones;
* escopo técnico.

A skill `start-project` deve interpretar a descrição inicial e extrair automaticamente tudo que puder.

Ela deve identificar, quando possível:

* conceito principal;
* gênero;
* perspectiva;
* objetivo do jogador;
* gameplay principal;
* possíveis mecânicas;
* cenário;
* plataforma, caso mencionada;
* referências mencionadas;
* funcionalidades aparentemente necessárias;
* funcionalidades que parecem opcionais;
* possíveis riscos de escopo.

Quando alguma informação importante não puder ser inferida, a skill deve perguntar ao usuário.

Porém:

**não faça um questionário enorme.**

Pergunte somente aquilo que for necessário para definir o próximo passo.

Faça poucas perguntas por vez.

---

# Assets e materiais existentes

O usuário também pode iniciar o projeto fornecendo materiais que já criou.

Esses materiais podem incluir:

* imagens;
* concept arts;
* screenshots;
* mapas;
* modelos 3D;
* animações;
* texturas;
* sons;
* músicas;
* documentos;
* diagramas;
* Blueprints existentes;
* código;
* arquivos ou estruturas de um projeto Unreal existente;
* listas de assets;
* referências visuais.

A `start-project` deve considerar esses materiais parte do contexto inicial do projeto.

Ela deve tentar entender:

1. o que o asset parece representar;
2. para que ele pode ser utilizado;
3. se ele pertence ao MVP;
4. se ele já resolve alguma necessidade do jogo;
5. se exige alguma preparação antes de ser utilizado;
6. se existem limitações ou informações que não podem ser determinadas apenas pelo arquivo fornecido.

Nunca ignore assets existentes e nunca proponha recriar algo que aparentemente já existe sem verificar primeiro.

---

# Inventário simples de assets

Quando assets forem fornecidos, mantenha um inventário simples.

Não crie um sistema complexo de gerenciamento de assets para um MVP.

Utilize algo equivalente a:

## Assets disponíveis

### Casa principal

Tipo:
Modelo 3D

Possível uso:
Cenário principal do MVP.

Situação:
Disponível.

Precisamos verificar:
Colisão e escala dentro da Unreal.

---

### Porta de madeira

Tipo:
Modelo 3D

Possível uso:
Primeiro objeto interativo.

Situação:
Disponível.

Próximo uso provável:
Sistema de interação.

O inventário pode ficar dentro do `PROJECT.md` inicialmente.

Crie um documento separado de assets somente se a quantidade de conteúdo crescer a ponto de justificar isso.

---

# Não presumir informações invisíveis

A skill deve distinguir claramente entre:

* o que conseguiu verificar;
* o que foi informado pelo usuário;
* o que está apenas supondo.

Exemplo:

Se o usuário fornece uma imagem de uma casa:

Pode concluir:

"Existe um conceito visual de uma casa."

Não pode concluir automaticamente:

"O modelo possui colisão pronta, UV correto e materiais configurados."

Se receber um tipo de arquivo cujo conteúdo não possa ser analisado diretamente, registre o que é conhecido pelo nome, formato e descrição do usuário e indique o que deverá ser verificado posteriormente dentro da Unreal.

Nunca invente características técnicas de um asset.

---

# Aproveitar o que já existe

O sistema deve adaptar o plano de desenvolvimento aos assets disponíveis.

Exemplo:

Se o usuário já possui:

* personagem;
* cenário;
* porta;
* lanterna.

E quer criar um jogo de terror:

o sistema pode aproveitar esses elementos para escolher um primeiro vertical slice simples:

1. entrar no cenário;
2. movimentar o personagem;
3. utilizar a lanterna;
4. aproximar-se de uma porta;
5. abrir a porta;
6. alcançar um objetivo simples.

O plano deve favorecer funcionalidades que permitam reutilizar rapidamente o conteúdo existente e chegar a algo jogável.

---

# Identificação do estado inicial

A `start-project` deve detectar três situações diferentes.

## Projeto apenas como ideia

O usuário ainda não criou nada.

A skill ajuda a definir um MVP.

---

## Projeto com assets existentes

O usuário já possui algum conteúdo.

A skill:

* entende a ideia;
* registra os assets;
* identifica o que pode ser aproveitado;
* adapta o MVP ao conteúdo existente.

---

## Projeto Unreal já iniciado

O usuário já possui um projeto parcialmente desenvolvido.

Nesse caso, a skill não deve tratar o projeto como novo.

Ela deve primeiro identificar:

* o que já existe;
* o que aparentemente funciona;
* quais features já começaram;
* quais assets estão presentes;
* o que está incompleto;
* qual é o estado atual.

Depois disso, deve criar ou atualizar:

`PROJECT.md`

`FEATURES.md`

`PROJECT_STATE.md`

com base no projeto existente.

---

# Primeiro resultado da start-project

Após receber a ideia inicial e eventuais assets, a `start-project` deve retornar algo simples.

Exemplo:

## Entendi sua ideia

Você quer criar um jogo de terror em primeira pessoa ambientado em uma casa abandonada.

A ideia principal parece ser explorar o ambiente, encontrar pistas e evitar uma criatura.

## O que você já tem

* modelo da casa;
* algumas portas;
* móveis;
* personagem.

Isso é suficiente para começarmos a montar uma primeira versão jogável sem precisar criar novos assets agora.

## Primeiro MVP

Para a primeira versão, vamos tentar conseguir apenas isto:

1. entrar na casa;
2. andar pelo cenário;
3. olhar ao redor;
4. aproximar-se de uma porta;
5. abrir a porta;
6. encontrar uma pista simples.

A criatura, inventário complexo, sistema de perseguição e outros elementos podem entrar depois.

## O que precisamos decidir agora

Antes de começar, precisamos saber apenas uma coisa:

O jogador já deve começar com um personagem em primeira pessoa funcionando ou ainda precisamos configurar a movimentação?

## Situação atual

`INICIANDO PROJETO`

## Próximo passo

Definir a primeira versão jogável do projeto.

## Próxima skill

`start-project`
