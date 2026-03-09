# Resumo dos Testes com Agregação dos Percentuais de Indicadores de Gastos

## Features

- **id_fazenda**: Categórica
- **sistema**: Categórica
- **18_vacas_em_lactacao_total_de_animais_percentual**: StandardScaler
- **20_vacas_em_lactacao_area_destinada_a_atividade_considerando_reserva_animais_hectare**: RobustScaler
- **21_vacas_em_lactacao_mao_de_obra_total_animais_trabalhador_dia**: MinMaxScaler
- **26_producao_total_de_vacas_litros_dia**: StandardScaler
- **27_producao_mao_de_obra_total_litros_trabalhador_dia**: StandardScaler
- **33_preco_medio_do_leite_r_litro**: RobustScaler
- **35_relacao_de_troca_leite_concentrado_kg_l**: RobustScaler
- **gastos_totais_na_atividade_renda_bruta_da_atividade_percentual**: 59_gasto_com_mao_de_obra_contratada_na_atividade_renda_bruta_da_atividade_percentual + 60_gasto_com_volumoso_na_atividade_renda_bruta_da_atividade_percentual + 61_gasto_com_concentrado_na_atividade_renda_bruta_da_atividade_percentual

## Alvo

- **52_custo_total_do_leite_r_litro**

## Divisão treino/teste:

- **Treino (2023):** 484 fazendas
- **Teste (2024):** 548 fazendas

### Distribuição dos dados no conjunto de treino

|       |   27_producao_mao_de_obra_total_litros_trabalhador_dia |   18_vacas_em_lactacao_total_de_animais_percentual |   26_producao_total_de_vacas_litros_dia |   21_vacas_em_lactacao_mao_de_obra_total_animais_trabalhador_dia |   35_relacao_de_troca_leite_concentrado_kg_l |   33_preco_medio_do_leite_r_litro |   20_vacas_em_lactacao_area_destinada_a_atividade_considerando_reserva_animais_hectare |   gastos_totais_na_atividade_renda_bruta_da_atividade_percentual |   59_gasto_com_mao_de_obra_contratada_na_atividade_renda_bruta_da_atividade_percentual |   60_gasto_com_volumoso_na_atividade_renda_bruta_da_atividade_percentual |   61_gasto_com_concentrado_na_atividade_renda_bruta_da_atividade_percentual |   52_custo_total_do_leite_r_litro |
|:------|-------------------------------------------------------:|---------------------------------------------------:|----------------------------------------:|-----------------------------------------------------------------:|---------------------------------------------:|----------------------------------:|---------------------------------------------------------------------------------------:|-----------------------------------------------------------------:|---------------------------------------------------------------------------------------:|-------------------------------------------------------------------------:|----------------------------------------------------------------------------:|----------------------------------:|
| count |                                                484     |                                           484      |                                484      |                                                         484      |                                   484        |                        484        |                                                                              484       |                                                         484      |                                                                              484       |                                                                484       |                                                                   484       |                        484        |
| mean  |                                                386.286 |                                            37.423  |                                 16.7805 |                                                          18.9672 |                                     1.28612  |                          2.54829  |                                                                                1.1432  |                                                          59.6306 |                                                                                7.73973 |                                                                 15.7493  |                                                                    36.1416  |                          2.40736  |
| std   |                                                192.548 |                                             8.7627 |                                  6.3202 |                                                           7.9326 |                                     0.265979 |                          0.330582 |                                                                                1.35385 |                                                          12.7952 |                                                                                5.14022 |                                                                  7.00834 |                                                                     8.34474 |                          0.513284 |
| min   |                                                 79.37  |                                             7.38   |                                  3.77   |                                                           6.01   |                                     0.86     |                          1.96     |                                                                                0.05    |                                                          18.08   |                                                                                0       |                                                                  0       |                                                                     2.56    |                          1.18     |
| 25%   |                                                221.137 |                                            31.37   |                                 12.2875 |                                                          13.26   |                                     1.13     |                          2.4      |                                                                                0.6     |                                                          51.7675 |                                                                                4.3375  |                                                                 11.3075  |                                                                    31.3325  |                          2.11     |
| 50%   |                                                364.465 |                                            38.78   |                                 15.925  |                                                          17.99   |                                     1.25     |                          2.55     |                                                                                0.97    |                                                          58.845  |                                                                                7.34    |                                                                 15.115   |                                                                    35.7     |                          2.34     |
| 75%   |                                                512.883 |                                            44.2    |                                 21.2225 |                                                          23.32   |                                     1.37     |                          2.68     |                                                                                1.4325  |                                                          66.22   |                                                                               10.6625  |                                                                 19.4775  |                                                                    40.4125  |                          2.59     |
| max   |                                               1108.84  |                                            59.03   |                                 33.74   |                                                          80.71   |                                     3.99     |                          8.72     |                                                                               26.69    |                                                         110.7    |                                                                               29.69    |                                                                 39.14    |                                                                    74.75    |                          7.63     |

### Distribuição dos dados no conjunto de teste

|       |   27_producao_mao_de_obra_total_litros_trabalhador_dia |   18_vacas_em_lactacao_total_de_animais_percentual |   26_producao_total_de_vacas_litros_dia |   21_vacas_em_lactacao_mao_de_obra_total_animais_trabalhador_dia |   35_relacao_de_troca_leite_concentrado_kg_l |   33_preco_medio_do_leite_r_litro |   20_vacas_em_lactacao_area_destinada_a_atividade_considerando_reserva_animais_hectare |   gastos_totais_na_atividade_renda_bruta_da_atividade_percentual |   59_gasto_com_mao_de_obra_contratada_na_atividade_renda_bruta_da_atividade_percentual |   60_gasto_com_volumoso_na_atividade_renda_bruta_da_atividade_percentual |   61_gasto_com_concentrado_na_atividade_renda_bruta_da_atividade_percentual |   52_custo_total_do_leite_r_litro |
|:------|-------------------------------------------------------:|---------------------------------------------------:|----------------------------------------:|-----------------------------------------------------------------:|---------------------------------------------:|----------------------------------:|---------------------------------------------------------------------------------------:|-----------------------------------------------------------------:|---------------------------------------------------------------------------------------:|-------------------------------------------------------------------------:|----------------------------------------------------------------------------:|----------------------------------:|
| count |                                                548     |                                          548       |                                548      |                                                        548       |                                   548        |                        548        |                                                                              548       |                                                         548      |                                                                              548       |                                                                548       |                                                                   548       |                        548        |
| mean  |                                                391.61  |                                           37.7236  |                                 17.2207 |                                                         18.7477  |                                     1.47431  |                          2.69571  |                                                                                1.16719 |                                                          52.9243 |                                                                                7.80327 |                                                                 13.699   |                                                                    31.422   |                          2.33595  |
| std   |                                                198.46  |                                            8.98986 |                                  6.6098 |                                                          7.46102 |                                     0.293747 |                          0.347669 |                                                                                1.33198 |                                                          11.8841 |                                                                                5.62491 |                                                                  6.57558 |                                                                     7.27603 |                          0.517127 |
| min   |                                                 28.81  |                                            4.07    |                                  2.91   |                                                          3.88    |                                     0.94     |                          2.15     |                                                                                0.04    |                                                          20.8    |                                                                                0       |                                                                  0       |                                                                     3.61    |                          1.14     |
| 25%   |                                                241.885 |                                           32.1175  |                                 12.3175 |                                                         13.3225  |                                     1.3      |                          2.58     |                                                                                0.5875  |                                                          45.4675 |                                                                                4.155   |                                                                  9.8575  |                                                                    27.0775  |                          2.06     |
| 50%   |                                                364.485 |                                           38.305   |                                 15.745  |                                                         18.025   |                                     1.43     |                          2.69     |                                                                                1.015   |                                                          52.62   |                                                                                7.19    |                                                                 12.785   |                                                                    30.825   |                          2.26     |
| 75%   |                                                510.838 |                                           43.845   |                                 22.555  |                                                         23.1025  |                                     1.59     |                          2.8      |                                                                                1.46    |                                                          58.9975 |                                                                               10.49    |                                                                 17.02    |                                                                    35.405   |                          2.53     |
| max   |                                               1105.77  |                                           67.72    |                                 35.09   |                                                         47.67    |                                     4.43     |                          9.91     |                                                                               26.05    |                                                         127.39   |                                                                               51.91    |                                                                 45.08    |                                                                    69.43    |                          6.98     |

## Resultados

Ao agregar os gastos em uma única variável, foram feitos os testes desta abordagem transformando a nova feature com diferentes escalonadores:

### Feature escalonada no StandardScaler

| Modelo                             |   MAE (R$/L) |   RMSE (R$/L) |     R² |
|:-----------------------------------|-------------:|--------------:|-------:|
| **Regressão Linear**                   |       **0.1333** |        **0.2533** | **0.7596** |
| Random Forest                      |       0.1839 |        0.2831 | 0.6998 |
| Gradient Boosting                  |       0.1695 |        0.2571 | 0.7524 |
| Rede Neural (Rasa - 64 neurônios)  |       0.155  |        0.2495 | 0.7668 |
| Rede Neural (Média - 64x32)        |       0.1578 |        0.2517 | 0.7627 |
| Rede Neural (Profunda - 128x64x32) |       0.154  |        0.2445 | 0.7761 |
| Regressão Ridge (Penalizada)       |       **0.1437** |        **0.24**   | **0.7842** |
| Elastic Net                        |       0.2108 |        0.3209 | 0.6142 |
| Support Vector Regression (SVR)    |       0.173  |        0.3309 | 0.5898 |
| LightGBM (HistGradientBoosting)    |       0.2267 |        0.3636 | 0.5048 |

### Feature escalonada no MinMaxScaler

| Modelo                             |   MAE (R$/L) |   RMSE (R$/L) |     R² |
|:-----------------------------------|-------------:|--------------:|-------:|
| Regressão Linear                   |       **0.1431** |        **0.2635** | **0.7398** |
| Random Forest                      |       0.1846 |        0.2845 | 0.6967 |
| Gradient Boosting                  |       0.1698 |        0.2575 | 0.7516 |
| Rede Neural (Rasa - 64 neurônios)  |       **0.1452** |        **0.2472** | **0.771**  |
| Rede Neural (Média - 64x32)        |       0.1519 |        0.246  | 0.7733 |
| Rede Neural (Profunda - 128x64x32) |       0.1594 |        0.257  | 0.7526 |
| Regressão Ridge (Penalizada)       |       0.1624 |        0.259  | 0.7488 |
| Elastic Net                        |       0.3556 |        0.4842 | 0.1218 |
| Support Vector Regression (SVR)    |       0.214  |        0.3728 | 0.4793 |
| LightGBM (HistGradientBoosting)    |       0.227  |        0.3637 | 0.5045 |

### Feature escalonada no RobustScaler

| Modelo                             |   MAE (R$/L) |   RMSE (R$/L) |     R² |
|:-----------------------------------|-------------:|--------------:|-------:|
| Regressão Linear                   |       **0.1333** |        **0.2534** | **0.7595** |
| Random Forest                      |       0.1846 |        0.2838 | 0.6983 |
| Gradient Boosting                  |       0.1701 |        0.2586 | 0.7494 |
| Rede Neural (Rasa - 64 neurônios)  |       0.1481 |        0.2467 | 0.7719 |
| Rede Neural (Média - 64x32)        |       0.152  |        0.2468 | 0.7718 |
| Rede Neural (Profunda - 128x64x32) |       0.1592 |        0.2465 | 0.7724 |
| Regressão Ridge (Penalizada)       |       **0.1438** |        **0.2401** | **0.784**  |
| Elastic Net                        |       0.2146 |        0.3245 | 0.6056 |
| Support Vector Regression (SVR)    |       0.1723 |        0.3298 | 0.5924 |
| LightGBM (HistGradientBoosting)    |       0.2267 |        0.3636 | 0.5048 |