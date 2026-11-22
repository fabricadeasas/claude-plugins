# Plugins da Fábrica de Asas

Catálogo dos plugins do Claude Code da [Fábrica de Asas](https://fabricadeasas.com.br), para quem usa o Claude Code sem ser programador. Este repositório guarda só o catálogo: cada plugin mora no seu próprio repositório.

| Plugin | O que faz | Repositório |
| --- | --- | --- |
| **Claude Code for Everyone** (`fabrica-de-asas`) | Linguagem simples, boas práticas de engenharia e versões guardadas sem jargão. Plugin do curso Superpoderes com IA | [claude-code-for-everyone](https://github.com/fabricadeasas/claude-code-for-everyone) |
| **Claude Code Go Live** (`fabrica-de-asas-no-ar`) | Ambiente de testes, publicação em produção num pedido só e trava de produção, para quem vai colocar um site ou sistema no ar | [claude-code-go-live](https://github.com/fabricadeasas/claude-code-go-live) |

## Como instalar

No Claude Code, digite:

```
/plugin marketplace add fabricadeasas/claude-plugins
/plugin install fabrica-de-asas@fabricadeasas
```

Para o complemento de publicação, depois: `/plugin install fabrica-de-asas-no-ar@fabricadeasas`.

No app do Claude (aba Code), vá em Plugins → Adicionar → Adicionar marketplace e cole `fabricadeasas/claude-plugins`.

Também dá para pedir para o próprio Claude: "Adicione o marketplace fabricadeasas/claude-plugins, instale o plugin fabrica-de-asas e ligue a atualização automática dele."

## Já usava o endereço antigo?

Até novembro de 2026 o catálogo ficava em `fabricadeasas/claude-code-for-everyone`. Ele continua funcionando e os plugins instalados por lá continuam se atualizando, mas plugins novos só entram aqui.

Para trocar, peça ao Claude: "troque o catálogo da Fábrica de Asas para o endereço novo". O plugin `fabrica-de-asas` sabe fazer a troca: os plugins instalados continuam ligados e a atualização automática é mantida.

Só rodar `/plugin marketplace add fabricadeasas/claude-plugins` não basta: o Claude Code recusa, porque o endereço antigo está registrado nas suas configurações com o mesmo nome (`fabricadeasas`). A troca precisa mudar esse registro primeiro.

## Como funciona por dentro

```
.claude-plugin/marketplace.json   o catálogo: nome, descrição e de onde vem cada plugin
```

Para acrescentar um plugin, inclua uma entrada em `plugins` apontando para o repositório dele e confira com `claude plugin validate .`.

O nome do catálogo (`fabricadeasas`) não pode mudar: é por ele que o Claude Code reconhece os plugins já instalados (`fabrica-de-asas@fabricadeasas`).

## Sobre

Criado por [Guilherme Almeida Girardi](https://github.com/ggirardi1) como parte dos cursos da [Fábrica de Asas](https://fabricadeasas.com.br). Licença MIT.
