# Como ligar o Elden ao Claude e fazer a primeira pergunta

**Em resumo:** Este guia mostra como ligar o Elden ao Claude, pelo aplicativo e pelo Claude Code, e como fazer a primeira pergunta. A conexão usa o endereço https://elden.com.br/mcp e funciona em qualquer plano do Claude, inclusive no grátis.

## O que você vai precisar

- Uma conta no Claude. Pelo FAQ do Elden, a conexão funciona em qualquer plano, inclusive no grátis.
- Uma conta no Elden, criada em https://elden.com.br/criar-conta (grátis, sem cartão). O login é feito na tela de entrada do Elden, com conta Google ou link enviado por e-mail. Não há senha.
- O endereço do conector: https://elden.com.br/mcp.
- Para o Claude Code, o comando `claude mcp add --transport http elden https://elden.com.br/mcp`.

O Elden é um complemento com planos próprios, inclusive um gratuito. A assinatura da IA continua separada. Para valores e para o que cada plano inclui, consulte a página de planos em https://elden.com.br/#planos.

## Passo a passo

Os nomes dos menus podem variar conforme a versão do aplicativo.

1. **Crie sua conta no Elden** em https://elden.com.br/criar-conta. O cadastro é grátis e não pede cartão.
2. **Abra o Claude e vá em Conectores.** O caminho indicado é Conectores → adicionar https://elden.com.br/mcp → Entrar.
3. **Entre na sua conta do Elden.** O login acontece na tela de entrada do Elden, com conta Google ou link enviado por e-mail. Não há senha.
4. **Autorize o uso das ferramentas.** Na primeira vez, o aplicativo pergunta se o Claude pode usar a ferramenta. O conector tem três:
   - Pesquisa jurídica e Contexto, ambas somente leitura;
   - Gravar, que é de escrita.

   Nas duas de leitura, dá para escolher "permitir sempre" (a redação varia conforme o aplicativo), e a pesquisa passa a rodar sem perguntar de novo. A de gravar é bom manter perguntando.
5. **Faça a primeira pergunta.** Escreva como falaria com um colega, citando o tribunal onde o processo corre. Por exemplo: "dano moral por extravio de bagagem, processo no TJCE". Você também pode colar um número de processo ou um artigo.
6. **Se vierem poucas decisões, refaça a consulta com menos palavras.** A orientação do Elden para a IA é que consultas curtas, com 5 a 8 palavras do vocabulário da ementa, funcionem melhor que frases longas. Um exemplo: "cartão consignado RMC menor incapaz nulidade".
7. **Se você usa o Claude Code, rode no terminal:** `claude mcp add --transport http elden https://elden.com.br/mcp`. A primeira pergunta segue as mesmas orientações.

Depois de ligar, a IA consulta o Elden sozinha quando a pergunta é jurídica. Você só pergunta como sempre. Segundo o Elden, a IA passa a consultar leis e decisões dos tribunais brasileiros antes de responder, em vez de chutar. Quem redige é a sua IA. O Elden dá a ela fontes e orientações de estilo. A leitura dos autos e a revisão final continuam com você.

## Se algo não funcionar

- **Os menus não aparecem como no passo a passo.** Os nomes podem variar conforme a versão do aplicativo.
- **Você usa o ChatGPT.** Segundo o FAQ do Elden, por enquanto a OpenAI só deixa ligar ferramentas de fora nas contas Business, Enterprise e Edu. Nas contas pessoais ainda não dá.
- **Você usa outra IA.** O Elden também funciona em qualquer outra IA que aceite conectores MCP. A configuração varia conforme o aplicativo e o plano.
- **Vieram poucas decisões ou nenhuma.** Refaça a consulta com menos palavras. Um resultado vazio não prova ausência de precedente.
- **Você vai citar um precedente.** O Elden localiza e mostra o que o documento diz. Ele não aprova nem reprova teses. A ementa não é o inteiro teor. Sempre confira no tribunal antes de citar.

## Próximo passo

Com o Elden ligado ao Claude, faça sua primeira pergunta e veja quais decisões aparecem. Se ainda não tiver conta no Elden, é grátis e sem cartão: [Criar conta grátis](https://elden.com.br/criar-conta).

---
Publicado também em https://elden.com.br/blog/como-conectar-o-elden-ao-claude/
