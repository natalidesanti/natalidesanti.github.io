---
title: "Primeiros passos na obtenção de parâmetros cosmológicos utilizando matrizes de covariância cosmológicas sem ruído"
collection: publications
permalink: 
excerpt: 'First steps to improve cosmological covariance matrices'
date: 2022-09-30
venue: 'Blucher Physics Proceedings'
paperurl: 'https://www.proceedings.blucher.com.br/article-details/primeiros-passos-na-obteno-de-parmetros-cosmolgicos-utilizando-matrizes-de-covarincia-cosmolgicas-sem-rudo-37453'
citation: 'de Santi, N. S. M. and Abramo, L. R. 2022, DOI: 10.5151/astrocientistas2021-11'
---

**Resumo:**

Matrizes de covariância são uma das peças mais importantes na análise de dados em Cosmologia: elas não apenas representam o entendimento sobre a natureza das incertezas, mas refletem a propagação dos erros estatísticos e dependem das suposições, devido aos modelos teóricos utilizados, para reduzir os dados. Para representar os verdadeiros erros estatísticos, muitos dados são necessários para construir essas matrizes, ou seja, centenas de milhares de observações ou simulações caríssimas, algo que nem sempre possui obtenção viável. Para resolver esse problema, foi proposto o uso de técnicas de aprendizado de máquina, com uma pipeline completa para tal. Foi implementada uma simulação de um campo Gaussiano com três parâmetros. Então, o espectro de potências linear foi calculado para cada mapa produzido e centenas de matrizes de covariância, usando diferentes números de espectros, foram calculadas. As matrizes foram utilizadas como dados de entrada em uma rede neural convolucional para remover o ruído daquelas criadas com poucos dados. Por fim, as matrizes de covariância limpas obtidas foram utilizadas para recuperar os parâmetros da simulação, utilizando algoritmos de Monte Carlo acoplados a cadeias de Markov (MCMC). Os resultados mostraram que essa técnica é capaz de produzir boas matrizes de covariância, mesmo com poucos dados de entrada, diminuindo muito os erros dos parâmetros cosmológicos obtidos.

You can read the paper [here](https://pdf.blucher.com.br/physicsproceedings/astrocientistas2021/11.pdf).
