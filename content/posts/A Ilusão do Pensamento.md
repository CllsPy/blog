---
title: "A Ilusão do Pensamento"
draft: false
ShowToc: true
date: 2025-09-08
tags: ["paper", "llms"]
author: Carlos Lima
---

# Explicando o polêmico paper da APPLE

1. **LRMs apresentam limitações** a partir de certas complexidades, assim como os LLMs.  
   Em alguns casos, performam pior que LLMs. É sabido que LRMs por vezes apresentam raciocínio distante da resposta mostrada e que também às vezes “pensam demais” e retornam mais conteúdo que o necessário.

2. **Objetivo dos autores:** analisar as limitações dos LRMs.  
   LRMs são modelos que aplicam a técnica chamada *reasoning*, equivalente humano a “pensar”.  
   Um exemplo open source e popular de modelo que usa essa estratégia é o **DeepSeek**, sobre o qual escrevi antes.

3. **Limitações dos mecanismos de avaliação:**  
   Segundo o trabalho, os mecanismos atuais de avaliação dos modelos capazes de realizar *reasoning* não produzem análises robustas sobre as limitações dos LRMs.  
   Uma das razões é a **contaminação dos dados**, porém o foco da pesquisa **não** é criar um novo *benchmarking*.


4. **Solução proposta:**  
   Os autores apresentam os **controllable puzzle environments**, usados anteriormente, e escolhidos aqui apenas para medir as limitações dos *Large Reasoning Models*.

5. **Comparação LLMs vs LRMs:**  
   O trabalho encontrou três cenários:
   - Em tarefas simples, **LLMs são preferíveis**.  
   - **LRMs performam melhor** que LLMs em tarefas intermediárias.  
   - A partir de certo ponto, **ambos colapsam**, inclusive os LRMs.

6. **Colapso dos LRMs:**  
   O fato de LRMs colapsarem a partir de certo ponto demonstra uma **limitação de escalabilidade**.

<img width="890" height="545" alt="image" src="https://github.com/user-attachments/assets/6fa4a642-1244-41f2-842e-86ab9bd5592a" />


7. **Conclusão:**  
   Apesar das limitações do trabalho, os autores demonstram — através dos *controllable puzzle environments* — que LRMs possuem **limites em sua escalabilidade**, colapsando à medida que a complexidade das tarefas aumenta.  
   São esperadas novas avaliações sobre **como entendemos o reasoning** nos LRMs.
