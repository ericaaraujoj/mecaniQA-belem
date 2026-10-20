# Análise de Trade-off: Grid Search e Random Search

## 1. Objetivo

Comparar os métodos Grid Search e Random Search aplicados aos modelos Árvore de Decisão e Random Forest, considerando o tempo de processamento e o erro de previsão (MAE).

## 2. Resultados

Os testes foram realizados com 711 registros preparados, utilizando validação cruzada temporal com cinco divisões. O MAE foi utilizado para avaliar o erro das previsões: quanto menor o valor, melhor o resultado.

| Modelo | Método | Tempo (s) | MAE |
|---|---|---:|---:|
| Random Forest | Grid Search | 21,73 | 4,44 |
| Random Forest | Random Search | 2,05 | 4,50 |
| Árvore de Decisão | Grid Search | 0,24 | 4,75 |
| Árvore de Decisão | Random Search | 0,11 | 5,07 |

## 3. Comparação dos métodos

### Random Forest

O Random Search levou 2,05 segundos, enquanto o Grid Search levou 21,73 segundos. Isso representa uma economia de **19,68 segundos (90,57%)**.

Em relação ao erro, o MAE passou de 4,44 para 4,50, um aumento de 0,06 (1,35%).

### Árvore de Decisão

O Random Search levou 0,11 segundo, enquanto o Grid Search levou 0,24 segundo. A economia foi de **0,13 segundo (54,17%)**.

O MAE passou de 4,75 para 5,07, um aumento de 0,32 (6,74%).

## 4. Conclusão

Nos dois modelos, o Random Search apresentou menor tempo de processamento, mas também obteve um MAE maior.

No Random Forest, a economia foi de 19,68 segundos, com aumento de apenas 1,35% no erro. Na Árvore de Decisão, a economia foi menor, de 0,13 segundo, e o aumento do erro foi de 6,74%.

Portanto, **o Random Search foi mais rápido nos dois casos, enquanto o Grid Search apresentou menor erro de previsão**. Para o Random Forest, a redução do tempo veio acompanhada de uma pequena variação no erro, tornando essa alternativa interessante quando a rapidez é prioridade. A escolha final depende do equilíbrio desejado entre tempo de execução e precisão.

## 5. Verificação de QA

- [x] Tempos de processamento e valores de MAE registrados a partir da execução do notebook.
- [x] Diferenças de tempo e erro calculadas para cada modelo.
- [x] Comparações realizadas entre os métodos no mesmo modelo.
- [x] Reexecutar os testes para confirmar a consistência dos resultados.
