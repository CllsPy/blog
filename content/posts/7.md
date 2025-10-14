---
title: "Agentes não são uma invenção, são a evolução de uma ideia antiga"
draft: false
ShowToc: true
date: 2025-10-08
tags: ["agents"]
author: Carlos Lima
---

## Agentes
Se há um fato sobre os Agentes, é que eles não são novidade. A própria OpenAI evita utilizar esse termo ao se referir ao ChatGPT, justamente porque ele é reservado para mecanismos verdadeiramente autônomos.

Não podemos negar: hoje existe uma histeria coletiva em torno do tema. Há dezenas de ferramentas disponíveis para a criação desses sistemas, e também muita confusão — ou falta de compreensão — sobre o que 
realmente são os agentes, qual sua arquitetura e quando, de fato, é necessário desenvolver um.

Este ensaio é um guia que apresenta definições claras dos termos, conforme entendidos por desenvolvedores experientes, e discute estratégias eficazes para sua construção.

## Introdução
O conceito de Agente não é novo. Desde que falamos em Inteligência Artificial, cogitamos a criação de mecanismos autônomos capazes de nos auxiliar nas mais diversas tarefas. 
No aprendizado por reforço — bem anterior à IA generativa —, já existiam discussões acaloradas sobre o que seria um Agente e quais seriam as implicações éticas associadas.

No livro ML in Action, o autor define três tipos principais de Agentes:

- Direto — Se você já usou o ChatGPT, teve contato com um Agente direto.
- Assistente Proxy — Hoje, o ChatGPT pode criar imagens graças à integração com a DALL-E. Neste caso, o GPT repassa o prompt e retorna o conteúdo, atuando como um intermediário.
- Assistente (sem Proxy) — Se você já usou plugins no ChatGPT ou ferramentas similares, lidou com um Agente do tipo Assistente.
- Autônomo — É o modelo mais idealizado, quase totalmente autônomo. Ele recebe um pedido e assume a responsabilidade completa, desde as decisões até as estratégias usadas para resolver o problema.
- Agentes podem ser simples (single) ou múltiplos (multi), dependendo da quantidade de LLMs ou “personalidades” envolvidas. Por exemplo, em um sistema onde uma personalidade gera o código e outra cria testes unitários, temos um sistema multi-agente.

![](https://hermes.dio.me/assets/articles/586a4ada-c48d-4c20-9d15-6d20e890b751.png)

Naturalmente, ao desenvolver um Agente, é preciso considerar sua arquitetura. Não se trata de um código que flutua no ar, sem propósito. Tampouco se resume ao uso de um framework (como o LangChain) ou de uma API (como a da OpenAI).

Agentes podem conter inúmeros mecanismos, e cada um deles deve ser inserido como um meio de garantir que a tarefa solicitada seja cumprida. Os cinco principais componentes são:

- Ações e Ferramentas – Representam os recursos que o Agente utilizará.
- Perfil e Persona – Correspondem ao prompt que orienta o comportamento do Agente.
- Memória e Conhecimento – Dizem respeito ao contexto ao qual o Agente tem acesso.
- Reflexão e Avaliação – Permitem ao modelo ajustar-se para tomar melhores decisões.
- Planejamento e Feedback – Possibilitam que o modelo aprenda por tentativa e erro.

![](https://hermes.dio.me/assets/articles/a01c2039-ed39-45d1-9ff9-0cc94ea63425.png)

O principal elemento que impulsiona o hype atual em torno dos Agentes é, sem dúvida, o novo paradigma que surge a partir das ferramentas e estratégias recentemente descobertas. Entre elas, a mais notável, na minha opinião, é a possibilidade de substituir o uso de APIs, queries e outras interfaces técnicas por simples comandos em linguagem natural.

A Figura 3, abaixo, mostra um exemplo de um Agente Autônomo utilizado para a produção de um relatório anual de vendas.

![](https://hermes.dio.me/assets/articles/53736847-2c90-4265-b6da-97826fa6bd37.png)

Também é importante reconhecer que, no futuro, lidaremos de forma diferente tanto com o desenvolvimento de software quanto com o tratamento de dados. Este, sem dúvida, é o ponto focal para o qual devemos direcionar nossa atenção no que diz
respeito ao futuro da Engenharia de Software.

## Como Construir Agentes Que Fazem Sentido?
Em Bang Liu et al. (2025), os autores discutem o estado da arte dos LLMs. Vale destacar que, sem a revolução trazida por esses modelos, nenhum Agente moderno seria possível — em nenhuma circunstância.

Embora ainda existam limitações, é perfeitamente viável construir aplicações relevantes. Esta seção discute a natureza dessas aplicações, considerando a simplificação proporcionada pela internet, onde é comum encontrar “aplicações” com apenas algumas dezenas de linhas, geralmente geradas pelo ChatGPT com o auxílio de frameworks como LangChain ou LangGraph.

Chip Huyen, em seu livro AI Engineering, descreve práticas essenciais para a construção de aplicações impulsionadas por IA — práticas que certamente se aplicam à construção de Agentes.

## AI Stack

Em primeiro lugar, é preciso refletir sobre a real necessidade de desenvolver esse tipo de aplicação. Trabalhar com modelos de IA não é simples — embora muitos cursos por aí passem essa impressão. Pelo contrário, eu diria. Inclusive, minha primeira publicação na DIO foi justamente sobre a complexidade do Machine Learning.

Huyen destaca algumas considerações importantes para quem deseja construir aplicações desse tipo:

- Comece perguntando o porquê de você querer desenvolver uma aplicação. Essa avaliação será essencial para determinar seu sucesso ou fracasso no futuro.
- Defina as expectativas: espera-se que a aplicação seja ágil? Barata? Qual o tempo médio de resposta para os usuários (em caso de um chatbot)? Com qual nível de precisão? Diferentes aplicações exigem expectativas diferentes.
- Escolha bem as ferramentas: atualmente existem centenas de APIs, frameworks e serviços. É fundamental avaliar cuidadosamente qual melhor atende às suas necessidades. Por exemplo: Hugging Face ou OpenAI? Essa escolha é estratégica.

Além disso, é importante entender que o desenvolvimento de aplicações impulsionadas por IA se divide em diferentes camadas:

Desenvolvimento da Aplicação – A camada mais popular. Envolve fornecer contexto por meio de prompts e criar interfaces eficientes. Esta etapa também exige avaliação rigorosa do desempenho da aplicação.
Desenvolvimento do Modelo – Um pouco menos comum. Pode ocorrer quando o LLM com as características desejadas ainda não existe. Nesse caso, será necessário desenvolver um modelo do zero — tarefa que exige amplo conhecimento em Engenharia de Machine Learning.
Infraestrutura – A camada mais distante da maioria dos desenvolvedores, mas igualmente essencial. Envolve a gestão de dados, o deployment (serving) e a administração de recursos computacionais. A Figura 4 apresenta as três camadas com suas respectivas descrições.

![](https://hermes.dio.me/assets/articles/0d8a044a-b908-463d-87ba-3a601ea28123.png)

## LLMs
Como você já deve ter notado, os LLMs desempenham um papel fundamental na construção de Agentes. Na verdade, sem eles, grande parte do que hoje é possível sequer seria imaginável. Os LLMs tornaram-se praticamente sinônimos de inteligências artificiais, e todos foram desenvolvidos com base na arquitetura Transformers (Vaswani et al., 2017). Embora existam diferentes variantes, a mais bem-sucedida é a família GPT (Generative Pretrained Transformers).

A principal função dos LLMs é a geração de conteúdo, em contraste com os modelos tradicionais de Machine Learning, que geralmente se concentram em classificação.

Esses modelos podem ser autoregressivos, como o GPT-2, ou mascarados (masked), como o BERT. A diferença está na quantidade de informação contextual disponível para o modelo durante o treinamento. Como ilustrado na Figura 5, 
modelos autoregressivos têm acesso apenas ao texto à esquerda da palavra-alvo, enquanto os modelos mascarados, como o BERT, conseguem considerar informações de ambos os lados da lacuna.

![](https://hermes.dio.me/assets/articles/db52e36b-7db5-4bf4-9485-8a9b8b934d14.png)

Escolher o LLM correto é fundamental para o sucesso do seu agente, pois existem modelos mais ágeis, mas com precisão superior, e modelos mais robustos, porém com custos relevantes, seja computacional ou financeiro. Isso deve estar alinhado com outro elemento importante para dominar: a Engenharia de Prompt.

## Engenharia de Prompt
A Engenharia de Prompt é, em geral, esquecida e ignorada como parte fundamental do que entendemos sobre IA. Assim como na construção dos agentes, há uma super-simplificação dos conceitos, mesmo havendo um extenso corpo de trabalhos sobre o tema, com diferentes estratégias (Zhao et al., 2021; Wei et al., 2022; Kojima et al., 2022; Yao et al., 2023).

Em suma, a importância do prompt decorre da natureza dos modelos generativos. Quando precisamos especializar o modelo em uma tarefa, é necessário fornecer casos específicos. Como mostrado em Wei et al. (2022), 
fornecer até oito exemplos a LLMs, como o PaLM 540B, permitiu ao modelo superar o GPT-3 em algumas tarefas. Na Figura 5, é possível visualizar um exemplo de aplicação da estratégia CoT (Chain of Thought).

![](https://hermes.dio.me/assets/articles/b51bc178-5dbf-4832-91d8-ab51763b222a.png)

Embora existam diversas estratégias em relação à Engenharia de Prompt, os autores do livro Prompt Engineering For Generative AI defendem a existência de cinco princípios universais dessa área:

1. Direção: Refere-se à atribuição de uma personalidade ao modelo (por exemplo, "Professor de Química").
2. Formato: Define o formato desejado para a resposta final (por exemplo, Tabela, .docs, .txt, .md).
3. Fornecer Exemplos: Como mostrado em Wei et al. (2021), garantir exemplos melhora a capacidade do modelo e os resultados obtidos.
4. Dividir o Trabalho: A divisão da tarefa em etapas menores ajuda a reduzir alucinações, tornando o processo mais eficiente.
5. Considerar o Contexto: Avaliar o contexto do problema é essencial para medir a qualidade do prompt.

Quando o uso de prompts não é possível ou suficiente, então recorre-se ao fine-tuning. Como mencionado, essa abordagem requer conhecimento sobre Machine Learning e o
funcionamento dos modelos. Em geral, quem se ocupa do fine-tuning é denominado Engenheiro de Machine Learning.

## ﻿Avaliação
Não termina aqui. Este, sem dúvida, é o elemento mais negligenciado entre praticantes iniciantes ou aqueles com experiência proveniente de cursos ou bootcamps. Assim como os prompts, que precisam ser avaliados, um agente inteiro exige a mesma atenção.

Diferente de um modelo tradicional de Machine Learning, onde as métricas são objetivas, a avaliação de um modelo generativo apresenta diversos desafios e, geralmente, depende do contexto no qual a aplicação foi construída. Como mencionado, às vezes posso optar por uma aplicação mais lenta e barata em vez de usar modelos caros. Não há respostas definitivas para isso.

Um método sistemático abordado no livro AI Agents in Action é o das Mudanças Sistemáticas. Em resumo, começamos com um prompt básico e fazemos alterações graduais. Inicialmente, podemos começar sem definir uma persona ou separar as tarefas. Depois, gradualmente, vamos adicionando novos elementos. Todo esse processo, conforme pensado pelo autor, pode ser observado na Figura 7.

![](https://hermes.dio.me/assets/articles/ebeb62e6-1e6d-479b-aefe-7b28d0d5c40e.png)

Como mencionado, além da abordagem apresentada no livro, outras avaliações dependem do contexto. Após desenvolver o prompt, você pode considerar as seguintes métricas:

- Velocidade da Resposta
- Clareza
- Tom
- Estilo

Além disso, seria útil solicitar a um especialista na área para avaliar a aplicação com um fator humano. As lições que ficam são claras: o prompt importa e um bom prompt é fundamental para determinar a qualidade do agente. No final, a avaliação contínua é o que garante o sucesso a longo prazo e a qualidade da aplicação.

## Estado da Arte dos Agentes de Inteligência Artificial
Ao longo desta discussão, aprendemos sobre o que é um Agente, em quais categorias ele se divide, como planejar sua construção, quais considerações são necessárias e os elementos a serem priorizados (como a Engenharia de Prompt). Uma conclusão preliminar é que um bom desenvolvedor de Agentes é, necessariamente, um excelente Engenheiro de IA, com uma base sólida em Machine Learning.

Agora, vamos avaliar casos de sucesso no universo dos Agentes, para que você possa compreender a complexidade e a beleza dessas aplicações, entendendo os elementos que as compõem.

## GPT Assistentes
Embora muitas pessoas esqueçam, através do ChatGPT é possível acessar versões personalizadas, tanto por usuários quanto por empresas, que 
foram ajustadas previamente para a execução de tarefas específicas. Na Figura 8, é possível observar os assistentes mais populares da plataforma.

![](https://hermes.dio.me/assets/articles/b1050ee8-d89b-45f1-9000-5c889ee6e738.png)


Cada um deles serve a um uso específico e, como vimos no início deste ensaio, é possível classificá-los entre autônomos, single, assistente proxy ou assistente.

Vale ressaltar que é possível criar nossos próprios assistentes (ou seja, Agentes). No entanto, a OpenAI não oferece esse serviço de forma gratuita. Claro, existem soluções alternativas que permitem essa criação.

## HuggingFaceChat Assistants
Ao acessar o HuggingChat, você será capaz de criar seus próprios modelos e disponibilizá-los para outros usuários de forma gratuita. 
Embora haja limitações por ser um serviço gratuito, isso não impede que você crie seus próprios Agentes, especialmente se compreendeu os conceitos abordados neste texto. Verá que se trata dos mesmos
elementos: definir o prompt, escolher o LLM e avaliar os modelos. Na Figura 9, podemos observar os assistentes mais populares do HuggingFaceChat.

![](https://hermes.dio.me/assets/articles/a215c88f-97f5-403b-8bd0-a40a46a46c40.png)

## Meu próprio Agente
Quem acompanha alguns dos meus trabalhos na plataforma sabe o quanto lidar com papers é comum na minha realidade e também nos meus escritos 
(sempre evito dar opiniões vazias sem base para isso). Pensando nisso, algumas vezes desenvolvi meu próprio Agente. A tarefa dele é simples: 
sumarizar artigos em um formato que criei e que me ajuda a entender melhor os trabalhos. Esse formato foi embutido no Prompt que o modelo Gemini 2.0 
Flash recebe, através da API do Google. Na Figura 10, é possível visualizar a interface do Agente.

![](https://hermes.dio.me/assets/articles/dac7887d-5b2d-4738-9968-1545452a57b2.png)

Outros Agentes famosos foram deixados de lado para evitar redundância, uma vez que meus colegas de competição já os abordaram em seus artigos. Um dos mais populares, por exemplo, é o AutoGPT. Reforço apenas que se evite a confusão entre as ferramentas e os próprios Agentes. Como exemplo, temos frameworks como LangChain ou CrewAI, entre outros. Inclusive, alguns códigos que observei na competição utilizam essas ferramentas sem que seja necessário que elas estejam no código (imagino que isso aconteça por falta de compreensão do que elas realmente fazem, misturando códigos gerados pelo GPT ou similares). É essencial entender o papel dessas ferramentas, assim como o dos Agentes, para que não se adicione complexidade onde não é necessário — isso é, de fato, Engenharia de IA

## Conclusão
Neste texto, foi possível entender o que são Agentes e por que eles não são novidade. Compreendemos os Agentes que funcionam com base em LLMs, os quais são possíveis apenas graças à arquitetura Transformers. Vimos como planejar, escolher e avaliar as ferramentas, e como tudo isso se encaixa naquilo que chamamos de Engenharia de IA. Por fim, você aprendeu a classificar Agentes e conheceu alguns Agentes populares. Este artigo contém referências para as afirmações e imagens anexadas, que podem e devem ser usadas para expandir seu conhecimento.

P.S.S Abaixo segue uma lista de referências também gratuitas as quais consumi e posso atestar sobre a sua qualidade e profundidade.

- Hugging Face. (n.d.). HuggingFace course. Hugging Face. https://huggingface.co/course

- Lanhan, M. (n.d.). AI agents in action. 

- Advances and challenges in foundation agents. 

- Huyen, C. (n.d.). AI engineering. 

- freeCodeCamp. (n.d.). AI agents. freeCodeCamp. https://freecodecamp.org
