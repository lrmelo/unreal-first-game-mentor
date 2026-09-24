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

A instalação fica disponível para o usuário em todos os projetos, não apenas no repositório atual.

### Pelo terminal do Codex

Adicione este repositório como marketplace:

```powershell
codex plugin marketplace add lrmelo/unreal-first-game-mentor
```

Depois, instale o plugin:

```powershell
codex plugin add unreal-first-game-mentor@unreal-first-game-mentor
```

Reinicie o Codex ou o aplicativo desktop e comece uma nova conversa.

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

Para buscar uma versão nova do marketplace:

```powershell
codex plugin marketplace upgrade unreal-first-game-mentor
```

Depois da atualização, reinicie o aplicativo e abra uma nova conversa.

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

Este repositório ainda não possui uma licença de uso definida. Uma licença poderá ser adicionada pelo responsável antes de uma distribuição pública mais ampla.

## Referência oficial

Consulte [Package your plugin](https://developers.openai.com/plugins/build/plugins) para a documentação atual de empacotamento e marketplaces do Codex.
