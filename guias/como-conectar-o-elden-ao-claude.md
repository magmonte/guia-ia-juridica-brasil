# Como ligar o Elden ao Claude e fazer a primeira pergunta

**Em resumo:** No aplicativo do Claude, você adiciona o endereço do conector do Elden e entra com sua conta; no Claude Code, é um comando no terminal. Depois de ligar, a IA consulta o Elden sozinha quando a pergunta é jurídica, e você continua perguntando como sempre.

## O que você vai precisar

- Uma conta no Elden, criada em https://factum.rpmdesk.site/criar-conta (grátis, sem cartão).
- O aplicativo do Claude, em qualquer plano, inclusive no grátis, ou o Claude Code instalado.
- O endereço do conector: https://factum.rpmdesk.site/mcp.

Vale saber o que muda depois da ligação. Segundo a página inicial do Elden, ele passa a consultar leis e decisões dos tribunais brasileiros antes de responder, em vez de chutar. Quem redige é a sua IA; o Elden dá a ela fontes e orientações de estilo. A leitura dos autos e a revisão final continuam com você.

A assinatura da sua IA continua separada: o Elden é um complemento, com planos próprios, inclusive um gratuito. Para valores e para o que cada plano inclui, consulte a página de planos em https://factum.rpmdesk.site/#planos.

## Passo a passo

Os nomes dos menus podem variar conforme a versão do aplicativo.

1. Crie sua conta em https://factum.rpmdesk.site/criar-conta. É grátis e não pede cartão.
2. No aplicativo do Claude, abra a área de conectores e adicione o endereço https://factum.rpmdesk.site/mcp. O caminho indicado no e-mail de boas-vindas do Elden é: Conectores → adicionar https://factum.rpmdesk.site/mcp → Entrar.
3. No Claude Code, abra o terminal e rode: `claude mcp add --transport http elden https://factum.rpmdesk.site/mcp`.
4. Faça o login na tela de entrada do Elden. A entrada é feita com conta Google ou com um link enviado por e-mail. Não há senha.
5. Autorize a ferramenta na primeira vez. O aplicativo da IA pergunta se pode usá-la. O Elden tem três ferramentas, justamente para pedir pouca permissão: duas de leitura (pesquisa jurídica e contexto) e uma de escrita (gravar). Nas duas de leitura, dá para escolher "permitir sempre" — a redação dessa opção varia conforme o aplicativo — e a pesquisa passa a rodar sem perguntar de novo. A de gravar é bom manter perguntando.
6. Faça a primeira pergunta como falaria com um colega, citando o tribunal onde o processo corre, por exemplo: "dano moral por extravio de bagagem, processo no TJCE". Você também pode colar um número de processo ou um artigo de lei.
7. Se vierem poucas decisões, refaça com menos palavras. Consultas curtas, com 5 a 8 palavras do vocabulário da ementa, funcionam melhor que frases longas — por exemplo: "cartão consignado RMC menor incapaz nulidade".
8. Antes de citar uma decisão na peça, confira no tribunal. A ementa não é o inteiro teor, e o Elden localiza e mostra o que o documento diz: não aprova nem reprova teses.

## Se algo não funcionar

- No Claude, funciona em qualquer plano, inclusive no grátis. Se a conexão não aparecer, confira o endereço https://factum.rpmdesk.site/mcp e se você está na área de conectores do aplicativo.
- No ChatGPT, por enquanto, a OpenAI só deixa ligar ferramentas de fora nas contas Business, Enterprise e Edu. Nas contas pessoais ainda não dá.
- No Gemini também não: o recurso não chegou ao Brasil.
- Qualquer outra IA que aceite conectores MCP pode ser usada, mas a configuração varia conforme o aplicativo e o plano.
- Se a pesquisa voltar vazia, isso não prova ausência de precedente. Refaça a consulta com menos palavras.
- Se o login não entrar, tente a conta Google ou o link enviado por e-mail; não há senha a digitar.

## Próximo passo

Se ainda não tem conta, crie a sua e comece pelo plano gratuito para testar a conexão com o Claude. [Criar conta grátis](https://factum.rpmdesk.site/criar-conta)

---
Publicado também em https://factum.rpmdesk.site/blog/como-conectar-o-elden-ao-claude/
