# Como ligar o Elden ao Claude e fazer a primeira pergunta

**Em resumo:** Este passo a passo mostra como conectar o Elden ao Claude, pelo aplicativo ou pelo Claude Code, e como fazer a primeira pergunta. Depois de ligado, a IA consulta o Elden sozinha quando a pergunta é jurídica — você continua perguntando como sempre.

## O que você vai precisar

- Uma conta no Claude. Segundo a página inicial do Elden, no Claude a conexão funciona em qualquer plano, inclusive no grátis.
- Uma conta no Elden, criada em https://factum.rpmdesk.site/criar-conta. A criação é grátis e não pede cartão.
- O endereço do conector: https://factum.rpmdesk.site/mcp.
- Se você usa o Claude Code, o terminal e o comando de instalação do conector, que está no passo 4.

Vale lembrar como as duas peças se encaixam: o Elden é um complemento, com planos próprios, e a assinatura da IA continua separada. Segundo a página inicial, o Elden "passa a consultar leis e decisões dos tribunais brasileiros antes de responder, em vez de chutar". Quem redige é a sua IA; o Elden dá a ela fontes e orientações de estilo. A leitura dos autos e a revisão final continuam com você.

## Passo a passo

1. Crie sua conta no Elden em https://factum.rpmdesk.site/criar-conta. É grátis e não pede cartão.
2. Escolha o caminho: aplicativo do Claude ou Claude Code. Os dois usam o mesmo endereço de conector, https://factum.rpmdesk.site/mcp.
3. No aplicativo do Claude, abra **Conectores**, escolha **adicionar** https://factum.rpmdesk.site/mcp e depois **Entrar**. Os nomes dos menus podem variar conforme a versão do aplicativo.
4. No Claude Code, execute no terminal: `claude mcp add --transport http elden https://factum.rpmdesk.site/mcp`
5. Faça o login na tela de entrada do Elden. Você entra com a conta Google ou com o link enviado por e-mail. Não há senha.
6. Faça a primeira pergunta como faria normalmente. Quando a pergunta é jurídica, a IA consulta o Elden sozinha — você não precisa pedir isso.
7. Para a primeira pergunta, prefira consultas curtas, com 5 a 8 palavras do vocabulário da ementa. Um exemplo dado pelo próprio Elden: "cartão consignado RMC menor incapaz nulidade". Frases longas tendem a funcionar pior.

## Se algo não funcionar

- **Vieram poucas decisões:** refaça a consulta com menos palavras. A orientação do Elden é encurtar antes de concluir qualquer coisa.
- **O resultado veio vazio:** resultado vazio não prova ausência de precedente. Não trate como resposta definitiva.
- **Você usa o ChatGPT:** por enquanto, a OpenAI só deixa ligar ferramentas de fora nas contas Business, Enterprise e Edu. Nas contas pessoais ainda não dá.
- **Você usa o Gemini:** segundo a página inicial do Elden, o recurso também não está disponível, porque não chegou ao Brasil.
- **Você usa outra IA:** qualquer outra IA que aceite conectores MCP serve, mas a configuração varia conforme o aplicativo e o plano. Nesse caso, o passo 3 muda de nome e de lugar.
- **A ementa parece suficiente:** a ementa não é o inteiro teor. O Elden localiza e mostra o que o documento diz; não aprova nem reprova teses. Confira no tribunal antes de citar.

## Próximo passo

Com o conector ligado, a rotina continua simples: pergunte como sempre e deixe a IA buscar as fontes no Elden. Se ainda não tem conta, comece por ela — é grátis e não pede cartão: [Criar conta grátis](https://factum.rpmdesk.site/criar-conta).

---
Publicado também em https://factum.rpmdesk.site/blog/como-conectar-o-elden-ao-claude/
