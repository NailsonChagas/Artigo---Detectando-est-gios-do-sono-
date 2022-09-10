# Detecção de estagios do sono utilizando aprendizado de maquina

Projeto de iniciação científica<br>
Campus: UTFPR - Pato Branco<br>
Orientador: Jefferson T. Oliva<br>
Curso: Engenharia de Computação.

## Características Extraidas
<p> No domínio da frequência e tempo-frequência foram extraídas as características de cada uma
das bandas de frequências cerebrais: Delta (1Hz z 4Hz), Theta (4Hz z 8Hz), Alpha (8Hz a 12Hz),
Beta (12Hz a 30Hz), Gamma (30Hz a 60Hz) e espectro inteiro (1Hz a 60Hz). Foram extraídas 16
características de cada banda no domínio tempo-frequência, sendo elas: média, desvio padrão,
amplitude máxima, amplitude mínima, curtose, assimetria, centroide, entropia de banda espectral
(SBE), largura de banda espectral (SBW), raiz quadrática média, fator de crista, coeficiente de
variação, quartis (Q1, Q2 e Q3) e intervalo interquartil (OLIVA, J. T.; ROSA, J. L. G, 2021). </p>
<p> 27 características de cada banda no domínio da frequência: média, desvio padrão, amplitude
máxima, amplitude mínima, frequência máxima, frequência mínima, quartis (Q1, Q2 e Q3),
intervalo interquartil, covariância, amplitude P2P (pico a pico), centroide, curtose, assimetria,
coeficiente de variação, planicidade, momento de primeira ordem, momento de segunda ordem, raiz
quadrática média, fator de crista, taxa de cruzamento de zero, coeficiente de Gini, autocorrelação,
parâmetros de Hjorth, entropia de espectro e entropia aproximada (OLIVA, J. T.; ROSA, J. L. G,
2021) . No domínio do tempo, foram extraídas as mesmas 27 características do espectro de
potência, somando se assim um total de 285 características computadas por intervalo de 5 segundos. </p>

#### Série Temporal

Banda     | Qtd. de características
--------- | ------
Inteiro   | 27
**Total** | **27**

#### Espectro de potência

Banda     | Qtd. de características
--------- | ------
Delta     | 27
Theta     | 27
Alpha     | 27
Beta      | 27
Gamma     | 27
Inteiro   | 27
**Total** | **162**

#### Espectrograma

Banda     | Qtd. de características
--------- | ------
Delta     | 16
Theta     | 16
Alpha     | 16
Beta      | 16
Gamma     | 16
Inteiro   | 16
**Total** | **96**

Obs: No total 285 características

## Teste Estatístico de Nemenyi
<p>Realizando o teste estatístico de Friedman, foi verificado que em todos os estágios do sono houve diferença estatística significativa entre os classificadores utilizados, para se averiguar quais modelos seriam menos indicados para se realizar a classificação foi realizado o pós teste de Nemenyi.</p>
No estágio Acordado:
    <ul>
        <li>Árvore de Decisão (AM de 94,36%) e Naive Bayes (AM de 74,38%) com valor p de 0,003.</li>
        <li>KNN (AM de 76,93%) e Floresta Aleatória (AM de 95,21%) com valor p de 0,003.</li>
        <li>Naive Bayes (AM de 74,38%) e Floresta Aleatória (AM de 95,21%) com valor p de 0,001.</li>
    </ul>
No estágio S1:
    <ul>
        <li>Árvore de Decisão (AM de 80,15%) e Naive Bayes (AM de 74,88%) com valor p de 0,013.</li>
        <li>KNN (AM de 79,26%) e Floresta Aleatória (AM de 82,07%) com valor p de 0,013.</li>
        <li>Naive Bayes (AM de 74,88%) e Floresta Aleatória (AM de 82,07%) com valor p de 0,001.</li>
    </ul>
No estágio S2:
    <ul>
        <li>Árvore de Decisão (AM de 87,9%) e Naive Bayes (AM de 72,83%) com valor p de 0,003.</li>
        <li>KNN (AM de 75,8%) e Floresta Aleatória (AM de 89,88%) com valor p de 0,003.</li>
        <li>Naive Bayes (AM de 72,83%) e Floresta Aleatória (AM de 89,88%) com valor p de 0,001.</li>
    </ul>
No estágio S3:
    <ul>
        <li>Árvore de Decisão (AM de 89,87%) e KNN (AM de 75,02%) com valor p de 0,037.</li>
        <li>Árvore de Decisão (AM de 89,87%) e Naive Bayes (AM de 77,93%) com valor p de 0,002.</li>
        <li>KNN (AM de 75,02%) e Floresta Aleatória (AM de 91,59%) com valor p de 0,004.</li>
        <li>Naive Bayes (AM de 77,93%) e Floresta Aleatória (AM de 91,59%) com valor p de 0,001.</li>
    </ul>
No estágio S4:
    <ul>
        <li>Árvore de Decisão (AM de 90,17%) e KNN (AM de 76,88%) com valor p de 0,001.</li>
        <li>KNN (AM de 76,88%) e Floresta Aleatória (AM de 92,99%) com valor p de 0,001.</li>
        <li>Naive Bayes (AM de 80,54%) e Floresta Aleatória (AM de 92,99%) com valor p de 0,046.</li>
    </ul>
No estágio S5:
    <ul>
        <li>Árvore de Decisão (AM de 83,19%) e Naive Bayes (AM de 75.48%) com valor p de 0,003.</li>
        <li>KNN (AM de 77,45%) e Floresta Aleatória (AM de 85,48%) com valor p de 0,003.</li>
        <li>Naive Bayes (AM de 75.48%) e Floresta Aleatória (AM de 85,48%) com valor p de 0,001.</li>
    </ul>
