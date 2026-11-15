# Por que a IA inventa acórdão com número e o que o teste mostrou

**Em resumo:** Um modelo de linguagem produz texto provável, não consulta um banco de decisões por padrão — por isso pode devolver uma citação com aparência correta e inexistente. No teste do Elden de 06/09/2026, a mesma IA passou de 1 para 60 acórdãos reais em 60 pedidos quando ligada a uma base de jurisprudência.

## Por que a IA inventa um acórdão com número e tudo

O mecanismo é simples de enunciar e fácil de esquecer na hora da pressa. Modelos de linguagem geram texto provável. Eles não consultam, por padrão, um banco de decisões judiciais. Quando você pede "três acórdãos do STJ sobre consignado não contratado, com número", o modelo monta a resposta mais plausível para o formato pedido: tribunal, número, data, ementa. O formato é o que ele domina; a existência do documento, não.

Daí a chamada alucinação: uma citação com aparência correta e inexistente. O número tem o jeito certo, o órgão tem o jeito certo, a data é coerente. Nada ali denuncia o problema na superfície do texto.

Vale separar dois planos que costumam se misturar:

- **Redigir** um argumento jurídico: o modelo faz isso bem, porque é texto.
- **Afirmar** que uma decisão existe e diz o que você afirma: isso é conferência documental, não redação.

O segundo plano depende de uma fonte. Sem fonte, o modelo está escrevendo ficção plausível.

## O que muda quando a IA consulta uma base

O Model Context Protocol (MCP) é um padrão aberto que permite a um aplicativo de IA chamar ferramentas externas. Um conector MCP é, na prática, um endereço que o aplicativo passa a consultar. Ligado a uma base de acórdãos, o modelo deixa de responder de memória e passa a buscar o documento antes de citá-lo.

No teste do Elden, "com o Elden" significa a IA com duas ferramentas ligadas: a base nacional de acórdãos (4,08 milhões de publicações, 60 tribunais) e a camada de leis, súmulas e precedentes verificados do juris-mcp, que o Elden embute.

A diferença aparece onde a resposta depende de um número de processo ou de uma decisão recente. Nesses pontos, a IA sozinha não sabe; com a base, sabe.

## O que o teste do Elden de 06/09/2026 mostrou

O desenho: a mesma IA, duas vezes — sozinha e com o Elden ligado —, sem internet nas duas rodadas. A correção é feita pelo gabarito da FGV e por conferência mecânica no acervo, nunca por outra IA. O modelo usado foi o Claude Sonnet 5, com seis tarefas de escritório. Os detalhes estão em [a prova](https://elden.com.br/benchmark).

Os números, atribuídos ao teste do Elden de 06/09/2026:

- **Achar acórdãos reais:** 1 de 60 acórdãos reais com a IA sozinha; 60 de 60 com o Elden.
- **Saber o que foi decidido em 2026:** 0 de 20 respostas certas sozinha; 16 de 20 com o Elden. As perguntas eram sobre decisões de junho a setembro de 2026, posteriores ao corte de treino do modelo.
- **Conferir citações:** 20 citações, 10 inventadas. 1 de 20 conferidas certo sozinha; 19 de 20 com o Elden. Em nenhuma das rodadas uma citação inventada foi aceita.
- **Súmula e lei certas:** 10 de 12 pontos sozinha; 12 de 12 com o Elden.
- **Prova da OAB:** 46º Exame, 1ª fase, 80 questões, gabarito definitivo da FGV: 72 de 80 sozinha, 77 de 80 com o Elden. Os erros caíram de 8 para 3.

Dois resultados do mesmo teste merecem leitura mais lenta, porque contrariam a expectativa.

O primeiro: na 2ª fase de Direito do Trabalho, a peça escrita só com a IA tirou 4,70 e a peça com o Elden tirou 4,40, ambas corrigidas pela tabela oficial de pontos da FGV (19 itens). A diferença não está na tabela, que só pede artigo e pedido: está no que a peça leva para o juiz. A versão com o Elden transcreveu quatro acórdãos regionais de 2025–2026, com número, do TRT da 7ª e da 5ª Região, e a versão sem a ferramenta não citou nenhum acórdão. As notas da tabela foram marcadas item a item na leitura das duas peças, com conferência humana pendente.

O segundo: nem todo modelo completou a rodada. O GPT-5.6 rodou pelo Codex CLI com a conta gratuita do ChatGPT e parou no limite de uso em 05/09, com rodada parcial (5 dos 20 pedidos de precedentes, 64 das 80 questões da OAB). O MiniMax M3, modelo gratuito rodado pela OpenRouter, aparece com 15 de 15 acórdãos reais e 12 de 20 nas decisões de 2026. O GLM 5.2 gratuito ficou de fora porque o provedor limitou a taxa antes de concluir.

## O que o teste não mostra

O teste mede acerto em tarefas com gabarito. Não mede, e não poderia medir, algumas coisas que decidem o uso no dia a dia.

- **Ementa não é o inteiro teor.** A ementa é o resumo oficial do acórdão; o inteiro teor traz relatório, fundamentação (voto) e dispositivo. Conclusões sobre aplicação ao caso concreto exigem o inteiro teor.
- **Força normativa varia.** Súmula vinculante e precedentes qualificados (art. 927 do CPC) têm força diferente de um acórdão isolado de tribunal de justiça. Um acórdão real e bem localizado pode, ainda assim, não ser o precedente que sustenta a tese.
- **Responsabilidade não se terceiriza.** Boa prática reconhecida: o advogado continua responsável pelo que protocola. A IA auxilia, não substitui a conferência.

## Como conferir uma citação antes de protocolar

Verificar uma citação significa localizar o documento na fonte oficial — tribunal ou diário — e conferir quatro coisas:

1. Número do processo.
2. Órgão julgador.
3. Data.
4. O trecho citado, no inteiro teor.

Se qualquer um dos quatro não bater, a citação não entra. Um exemplo do que o teste produziu, para referência de formato: TRT-7, RO 0001064-97.2025.5.07.0018, j. 09/04/2026, sobre supressão parcial do intervalo intrajornada, com adicional de 50% nos termos do art. 71, § 4º, da CLT.

## Como o Elden entra nisso

O Elden liga o aplicativo de IA a uma base nacional de acórdãos e a uma camada de leis, súmulas e precedentes verificados, de modo que a busca do documento acontece antes da citação. No teste de 06/09/2026, foi essa ligação que separou 1 de 60 acórdãos reais de 60 de 60. A conferência final na fonte oficial continua sendo do advogado. [Conheça o Elden](https://elden.com.br/)

## Fontes consultadas

- A prova — teste do Elden, 06/09/2026: https://elden.com.br/benchmark

---
Publicado também em https://elden.com.br/blog/por-que-a-ia-inventa-jurisprudencia/
