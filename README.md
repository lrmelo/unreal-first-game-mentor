# Primeiro Jogo na Unreal

Conjunto integrado de skills em Português do Brasil para ajudar uma pessoa sem experiência a criar seu primeiro jogo na Unreal Engine.

O sistema conduz o usuário desde a ideia e a instalação da Unreal até a implementação, os testes, a correção de problemas e a expansão do jogo. O processo interno é organizado, mas o usuário pode conversar normalmente e não precisa conhecer metodologias, comandos especiais ou programação.

## O que está incluído

- início do projeto e primeiro `Play`;
- orientação sobre o que fazer agora;
- definição de uma funcionalidade ou melhoria;
- implementação passo a passo, priorizando Blueprint;
- testes simples durante o jogo;
- investigação de erros, uma hipótese por vez;
- suporte a melhorias fora da primeira versão jogável;
- preservação da versão funcional enquanto uma melhoria está em andamento.

O projeto usa apenas três documentos dentro de cada jogo:

- `.ai/PROJECT.md`: ideia, ambiente, escopo e materiais;
- `.ai/FEATURES.md`: funcionalidades, critérios e entregas;
- `.ai/PROJECT_STATE.md`: foco e próxima ação.

Esses documentos são criados no projeto do jogo quando necessário. A pessoa não precisa editá-los manualmente.

## Instalação global pelo GitHub

A instalação é feita uma única vez e fica disponível em todos os projetos abertos pelo mesmo usuário do computador. Não é necessário copiar estas skills para cada jogo, clonar este repositório dentro do projeto da Unreal ou conhecer SDD.

### Codex no VS Code — passo a passo

Antes de começar, instale ou atualize a [extensão oficial do Codex para o VS Code](https://marketplace.visualstudio.com/items?itemName=openai.chatgpt) e entre na sua conta.

1. Abra o VS Code. Pode ser em qualquer pasta.
2. Abra o terminal integrado pelo menu **Terminal > Novo Terminal**.
3. Execute o comando abaixo para confirmar que o Codex está disponível:

```powershell
codex --version
```

Se aparecer um número de versão, continue. Se aparecer a mensagem de que `codex` não foi reconhecido, instale o [Codex CLI seguindo o guia oficial](https://learn.chatgpt.com/docs/codex/cli), feche e abra o VS Code novamente e repita este passo.

4. Adicione este repositório como uma fonte de plugins:

```powershell
codex plugin marketplace add lrmelo/unreal-first-game-mentor
```

5. Instale o plugin:

```powershell
codex plugin add unreal-first-game-mentor@unreal-first-game-mentor
```

6. Confirme a instalação:

```powershell
codex plugin list
```

Procure por `unreal-first-game-mentor` na lista exibida.

7. Pressione `Ctrl+Shift+P`, procure por **Developer: Reload Window** e execute esse comando.
8. Abra o Codex pelo ícone na lateral do VS Code. Se o ícone não estiver visível, pressione `Ctrl+Shift+P` e execute **Codex: Open Codex Sidebar**.
9. Comece uma conversa nova e escreva normalmente:

> Quero criar meu primeiro jogo na Unreal e não sei como começar.

Pronto. O Codex poderá escolher automaticamente a skill adequada conforme a conversa. Você não precisa decorar nomes de skills, usar comandos especiais ou aprender uma metodologia.

> **O que significa instalação global?** O plugin fica disponível para todos os projetos usados pela mesma conta do sistema operacional. Em outro computador ou em outra conta de usuário, a instalação precisa ser repetida. Se o VS Code estiver configurado para trabalhar dentro do WSL, execute os comandos no terminal desse mesmo ambiente.

### Pelo Codex CLI fora do VS Code

Os mesmos dois comandos de instalação podem ser executados no PowerShell, no Windows Terminal ou em outro terminal onde o Codex CLI esteja instalado. Depois, reinicie o Codex e comece uma conversa nova.

### Pelo aplicativo desktop

Depois de adicionar o marketplace pelo comando acima:

1. reinicie o aplicativo;
2. abra o diretório de plugins;
3. escolha o marketplace `Primeiro Jogo na Unreal`;
4. abra `Primeiro Jogo na Unreal`;
5. selecione a opção de instalação;
6. comece uma nova conversa.

## Primeiro uso

Não é necessário chamar uma skill pelo nome. Experimente uma frase natural:

> Quero criar meu primeiro jogo na Unreal e não sei como começar.

Outros exemplos:

- “Onde paramos e o que eu faço agora?”
- “Quero adicionar uma porta que abre.”
- “Pode me ensinar a fazer isso passo a passo?”
- “Terminei. Como vejo se funcionou?”
- “A porta não está abrindo.”
- “Quero melhorar essa funcionalidade, mesmo não fazendo parte do MVP.”

## Atualização

Para buscar uma versão nova, execute no terminal integrado do VS Code ou em outro terminal:

```powershell
codex plugin marketplace upgrade unreal-first-game-mentor
```

Depois da atualização, use **Developer: Reload Window** no VS Code e abra uma nova conversa no Codex.

## Estrutura do repositório

```text
.agents/plugins/marketplace.json
plugins/unreal-first-game-mentor/
  plugin.json
  .codex-plugin/plugin.json
  skills/
docs/
```

O manifesto `plugin.json` segue o formato portátil. O manifesto em `.codex-plugin/` mantém compatibilidade com clientes Codex que ainda usam esse formato.

## Documentação

- [Especificação base](docs/especificacao-base.md)
- [Complemento de onboarding](docs/complemento-onboarding.md)
- [Auditoria final](docs/auditoria.md)
- [Histórico de versões](CHANGELOG.md)

## Privacidade e dependências

O plugin contém somente skills e modelos de documentos. Ele não inclui servidor MCP, conexão com contas externas ou telemetria própria.

As skills podem ler e atualizar os três documentos `.ai` dentro do projeto escolhido pelo usuário. Alterações maiores ou potencialmente arriscadas devem ser confirmadas e protegidas com um ponto de retorno.

## Licença

Distribuído sob a [licença MIT](LICENSE). Ela permite usar, copiar, modificar e distribuir o projeto, desde que o aviso de copyright e a licença sejam preservados.

## Referência oficial

- [Extensão do Codex para IDEs](https://learn.chatgpt.com/docs/codex/ide)
- [Skills no Codex](https://learn.chatgpt.com/docs/build-skills)
- [Empacotamento e marketplaces de plugins](https://developers.openai.com/plugins/build/plugins)
