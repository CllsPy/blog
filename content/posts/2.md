---
title: "O processo da escrita na era do ChatGPT "
draft: false
ShowToc: true
date: 2025-06-16
tags: ["escrita"]
author: Carlos Lima
---

## Introdução

Muitas pessoas querem aproveitar a praticidade dos modelos de linguagem para produzir conteúdo rápido e em grande escala, mas esse uso excessivo tem deixado claro que boa parte da internet já soa como escrita por máquinas. Mesmo que isso não surpreenda mais ninguém, devemos reconhecer que os modelos generativos estão aqui para ficar e precisamos aprender a usá-los com mais intenção e autenticidade.

Leitores querem consumir conteúdos relevantes e originais na internet, mas o aumento de textos gerados por IA tem trazido materiais genéricos, marcados por padrões repetitivos que revelam sua origem artificial. Como os LLMs ainda não superam esses vícios de linguagem por conta própria, precisamos aprender a reconhecer o que vale manter e o que deve ser adaptado para que o conteúdo soe mais humano e autêntico.

A ideia para este post surgiu após a leitura do excelente artigo *“Writing in the Age of LLMs”*, de Shreya Shankar. Uma das motivações foi a ausência de prompts que acompanhassem o processo de escrita.

Ao escrever com ajuda da IA, aprendi o que funciona e o que trava o processo. Aqui, compartilho meus próprios insights e os prompts que me ajudam a manter minha voz no texto.

## Quais são essas “marcas” de texto gerado por IA

Large Language Models (LLMs) são modelos de linguagem treinados com grandes volumes de texto. Baseiam-se em redes neurais que podem conter bilhões de parâmetros e se apresentam, geralmente, em duas arquiteturas: bidirecional — como o BERT, do Google — e autorregressiva — como o GPT, base do ChatGPT. A primeira considera o contexto à esquerda e à direita para prever tokens ausentes, enquanto a segunda prevê o próximo token com base apenas nos anteriores.

### Bullet Points

Dentro do padrão mais comum gerado por LLMs, o que mais salta aos olhos são os *bullet points*. Sempre que leio um texto repleto deles, penso imediatamente que foi produzido por uma IA. Ao solicitar, por exemplo, um blogpost sobre **MCP**, em algum momento o modelo Gemini 2.5 Pro retorna algo como:

> As vantagens dessa abordagem são inúmeras:
> * **Interoperabilidade:** Sistemas de IA podem se conectar a um ecossistema muito mais amplo de ferramentas e dados sem a necessidade de customizações complexas.
> * **Respostas mais inteligentes:** Com acesso a um contexto mais rico e atualizado, a IA pode fornecer respostas muito mais precisas e personalizadas. Imagine um assistente de IA que pode consultar sua agenda, seus e-mails e as últimas notícias para planejar seu dia de forma proativa.
> * **Desenvolvimento simplificado:** Reduz a complexidade e o tempo necessários para construir aplicações de IA poderosas e contextualmente conscientes.
> * **Segurança e controle:** O protocolo permite um gerenciamento mais granular de quais informações são compartilhadas com a IA, garantindo maior privacidade e segurança dos dados.

Os modelos tendem a recorrer a *bullet points* sempre que a ideia exige alguma elaboração. Eu, pessoalmente, prefiro desenvolver o raciocínio em um parágrafo coeso, onde as conexões entre as ideias ganham mais naturalidade e ritmo.

### Marcações em negrito antes de apresentar uma ideia

É comum que LLMs, como o Gemini 2.25 Pro, usem o negrito para introduzir ideias-chave — por exemplo:
**Segurança e controle:** …
**Desenvolvimento simplificado:** …

### Travessões

A associação entre travessões e textos gerados por IA é, talvez, o que mais me frustra. Sempre gostei de usá-los — e ainda uso — desde antes do boom dos modelos generativos. Mas o fato é conhecido: raramente um LLM deixa de inserir um “–” no meio do texto. Vemos isso, por exemplo, no Gemini 2.5 Pro, no blog post sobre o **MCP**:

> “O Protocolo de Contexto de Modelo propõe uma solução elegante para esse problema. Ao estabelecer um padrão aberto e unificado, o MCP permite que qualquer fonte de dados — seja um calendário, um e-mail, um documento ou um software de gestão — se comunique com um modelo de IA de maneira padronizada.”

### Falta de Especificidade e frases genéricas

Outros problemas, como o abuso de *bullet points* para sintetizar ideias, existem. Mas nenhum deles se compara à falta de impessoalidade do texto — algo que prejudica a profundidade da argumentação.

Geralmente, LLMs produzem textos vagos, que não comunicam conteúdo significativo. Veja este exemplo: “Pense nele como uma linguagem universal que permite que diferentes ferramentas e fontes de dados conversem de forma mais eficiente com a IA, proporcionando respostas mais ricas, precisas e relevantes.”

A frase “Pense nele…” é vaga, sem esclarecer exatamente a que elemento se refere. Além disso, a sentença seguinte levanta questões: quão eficiente é essa comunicação? Como isso ocorre? O que significa “respostas mais ricas, precisas e relevantes”?

Note como o texto permanece genérico, sem aprofundar ou ensinar algo concreto. Essa limitação temporária dos LLMs é algo com que precisamos conviver.

## Como usar LLMs sem cair nesses padrões

* **Exemplo ruim:** `“Escreva um post sobre produtividade.”`
* **Exemplo bom:** `“A partir de agora, você é uma professora universitária com duas filhas pequenas. Escreva um post sobre produtividade para mães que fazem mestrado, têm pouco tempo, mas não querem se sentir culpadas.”`

### Tenha um rascunho antes de pedir um texto

Para usar LLMs como ferramenta, faça sua parte. Antes de solicitar um texto, forneça um rascunho, mesmo que imperfeito. Um padrão útil é:

1.  criar um esboço (*outline*)
2.  escrever um rascunho (*draft*)
3.  ler e fazer críticas abaixo de cada parágrafo
4.  revisar com a ajuda do LLM

Se não souber por onde começar, peça ao LLM um *outline*. A partir dele, escreva os tópicos, critique seu próprio texto pensando em aspectos como clareza, e avance para a revisão.

### Defina uma estratégia de correção

Evite respostas genéricas especificando como deseja a reformulação. Por exemplo, Shreya Shankar sugere a abordagem **SWBST**, que segue este esquema:

* **S** (Sujeito)
* **W** (Quer)
* **B** (Mas)
* **S** (Então)
* **T** (Terminou)

* **Exemplo ruim:** `“Melhore este texto.”`
* **Exemplo bom:** `“Usando a abordagem SWBST, reescreva este texto.”`

## Técnicas que gosto de usar

Eu sempre, sempre escrevo o texto primeiro. Prefiro manter a prática da escrita em dia. Se tiver dificuldades com o *outline*, peço ajuda a algum LLM, mas no geral também busco textos que possam servir de inspiração.

Após escrever o rascunho, sigo para o processo de revisão, baseado no livro *“How to Write a Lot”*, de Paul J. Outras estratégias incluem três dicas que aprendi com Oliver Burkeman:

1.  Escreva para o leitor, como se fosse um guia.
2.  Faça pausas durante a escrita para evitar correr para o fim e acabar com um texto pobre.
3.  Sempre procure inspirações e evite ficar encarando a página em branco.

## Conclusão

Embora hoje em dia muita gente use LLMs freneticamente, é importante lembrar que quem define o estilo é você. Buscar isso ativamente fará seu texto melhorar. Portanto, teste os prompts sugeridos, experimente as ideias, leia o texto da Shreya Shankar e compartilhe seus resultados.
