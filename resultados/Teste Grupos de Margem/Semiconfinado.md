# Resumo dos Testes de Grupos de Margem Líquida Unitária

#### Features

- id_fazenda
- 7_total_de_vacas_animais_mes
- 17_vacas_em_lactacao_total_de_vacas_percentual
- 13_ccs_contagem_de_celulas_somaticas_x1000_celulas_ml
- 26_producao_total_de_vacas_litros_dia
- 33_preco_medio_do_leite_r_litro
- 34_preco_medio_do_concentrado_r_kg

#### Alvo

- 52_custo_total_do_leite_r_litro

## Semiconfinado

### 25% Superiores:

#### Divisão treino/teste:

- **Treino (2023):** 55 fazendas
- **Teste (2024):** 61 fazendas

#### Distribuição dos dados de treino:

|       |   7_total_de_vacas_animais_mes |   17_vacas_em_lactacao_total_de_vacas_percentual |   13_ccs_contagem_de_celulas_somaticas_x1000_celulas_ml |   26_producao_total_de_vacas_litros_dia |   33_preco_medio_do_leite_r_litro |   34_preco_medio_do_concentrado_r_kg |   52_custo_total_do_leite_r_litro |
|:------|-------------------------------:|-------------------------------------------------:|--------------------------------------------------------:|----------------------------------------:|----------------------------------:|-------------------------------------:|----------------------------------:|
| count |                        55      |                                          55      |                                                  55     |                                55       |                         55        |                            55        |                         55        |
| mean  |                        82.992  |                                          76.0576 |                                                 511.267 |                                11.8827  |                          2.64345  |                             2.05473  |                          2.044    |
| std   |                        55.3943 |                                          10.2181 |                                                 278.984 |                                 3.77946 |                          0.848136 |                             0.206271 |                          0.811132 |
| min   |                        17.75   |                                          45.51   |                                                   0     |                                 4.48    |                          2.24     |                             1.41     |                          1.18     |
| 25%   |                        51.21   |                                          70.76   |                                                 319.905 |                                 9.59    |                          2.41     |                             1.91     |                          1.795    |
| 50%   |                        71.25   |                                          76.93   |                                                 430.4   |                                12.17    |                          2.56     |                             2.1      |                          2.02     |
| 75%   |                        97.415  |                                          82.82   |                                                 605.125 |                                14.16    |                          2.66     |                             2.18     |                          2.1      |
| max   |                       286.75   |                                          96.58   |                                                1393.72  |                                20.73    |                          8.72     |                             2.48     |                          7.63     |

#### Distribuição dos dados de teste:

|       |   7_total_de_vacas_animais_mes |   17_vacas_em_lactacao_total_de_vacas_percentual |   13_ccs_contagem_de_celulas_somaticas_x1000_celulas_ml |   26_producao_total_de_vacas_litros_dia |   33_preco_medio_do_leite_r_litro |   34_preco_medio_do_concentrado_r_kg |   52_custo_total_do_leite_r_litro |
|:------|-------------------------------:|-------------------------------------------------:|--------------------------------------------------------:|----------------------------------------:|----------------------------------:|-------------------------------------:|----------------------------------:|
| count |                        61      |                                          61      |                                                  61     |                                61       |                          61       |                            61        |                         61        |
| mean  |                        92.3898 |                                          78.819  |                                                 407.417 |                                12.9859  |                           2.77492 |                             1.88426  |                          1.94967  |
| std   |                        81.3422 |                                           9.8661 |                                                 226.224 |                                 3.80667 |                           0.93517 |                             0.236661 |                          0.694737 |
| min   |                        14.25   |                                          38.61   |                                                   0     |                                 3.96    |                           2.38    |                             1.27     |                          1.25     |
| 25%   |                        48      |                                          75.65   |                                                 273.34  |                                10.77    |                           2.59    |                             1.75     |                          1.73     |
| 50%   |                        69.75   |                                          81.53   |                                                 360.72  |                                13.02    |                           2.68    |                             1.87     |                          1.92     |
| 75%   |                       102      |                                          84.72   |                                                 512.37  |                                14.86    |                           2.73    |                             2.03     |                          2.03     |
| max   |                       471.83   |                                          94.03   |                                                1084.1   |                                25.9     |                           9.91    |                             2.36     |                          6.98     |

#### Resultados:

| Modelo                             |   MAE (R$/L) |   RMSE (R$/L) |     R² |
|:-----------------------------------|-------------:|--------------:|-------:|
| Regressão Linear                   |       0.2348 |        0.3417 | 0.754  |
| Random Forest                      |       0.2599 |        0.3887 | 0.6817 |
| Gradient Boosting                  |       0.2659 |        0.3864 | 0.6855 |
| Rede Neural (Rasa - 64 neurônios)  |       0.2772 |        0.3839 | 0.6896 |
| Rede Neural (Média - 64x32)        |       0.263  |        0.3673 | 0.7159 |
| Rede Neural (Profunda - 128x64x32) |       0.2659 |        0.3826 | 0.6917 |
| Regressão Ridge (Penalizada)       |       0.2246 |        0.3251 | 0.7774 |
| **Elastic Net**                        |       **0.2216** |        **0.3024** | **0.8074** |
| Support Vector Regression (SVR)    |       0.2593 |        0.5958 | 0.2522 |
| LightGBM (HistGradientBoosting)    |       0.3082 |        0.5867 | 0.2749 |

---
### 50% Intermediários:

#### Divisão treino/teste:

- **Treino (2023):** 111 fazendas
- **Teste (2024):** 124 fazendas

#### Distribuição dos dados de treino:

|       |   7_total_de_vacas_animais_mes |   17_vacas_em_lactacao_total_de_vacas_percentual |   13_ccs_contagem_de_celulas_somaticas_x1000_celulas_ml |   26_producao_total_de_vacas_litros_dia |   33_preco_medio_do_leite_r_litro |   34_preco_medio_do_concentrado_r_kg |   52_custo_total_do_leite_r_litro |
|:------|-------------------------------:|-------------------------------------------------:|--------------------------------------------------------:|----------------------------------------:|----------------------------------:|-------------------------------------:|----------------------------------:|
| count |                       111      |                                        111       |                                                 111     |                               111       |                         111       |                           111        |                        111        |
| mean  |                        83.937  |                                         78.1037  |                                                 491.727 |                                13.2809  |                           2.45631 |                             2.02595  |                          2.27649  |
| std   |                        69.0609 |                                          7.66762 |                                                 246.221 |                                 3.58101 |                           0.16224 |                             0.282139 |                          0.223048 |
| min   |                        15.5    |                                         39.79    |                                                   0     |                                 4.68    |                           1.96    |                             0.88     |                          1.7      |
| 25%   |                        39.67   |                                         74.445   |                                                 333.6   |                                11.2     |                           2.345   |                             1.905    |                          2.135    |
| 50%   |                        60.33   |                                         79.61    |                                                 419.13  |                                13.3     |                           2.45    |                             2.08     |                          2.27     |
| 75%   |                       103.96   |                                         82.66    |                                                 596.68  |                                15.8     |                           2.55    |                             2.195    |                          2.41     |
| max   |                       443.75   |                                         92.15    |                                                1467.4   |                                21.52    |                           2.99    |                             2.66     |                          2.94     |

#### Distribuição dos dados de teste:

|       |   7_total_de_vacas_animais_mes |   17_vacas_em_lactacao_total_de_vacas_percentual |   13_ccs_contagem_de_celulas_somaticas_x1000_celulas_ml |   26_producao_total_de_vacas_litros_dia |   33_preco_medio_do_leite_r_litro |   34_preco_medio_do_concentrado_r_kg |   52_custo_total_do_leite_r_litro |
|:------|-------------------------------:|-------------------------------------------------:|--------------------------------------------------------:|----------------------------------------:|----------------------------------:|-------------------------------------:|----------------------------------:|
| count |                       124      |                                         124      |                                                 124     |                               124       |                        124        |                           124        |                        124        |
| mean  |                        79.9418 |                                          78.9224 |                                                 589.233 |                                13.2349  |                          2.6096   |                             1.90298  |                          2.27613  |
| std   |                        56.844  |                                           6.5531 |                                                 311.965 |                                 3.51206 |                          0.144843 |                             0.252413 |                          0.227795 |
| min   |                        16.25   |                                          62.47   |                                                   0     |                                 5.45    |                          2.19     |                             0.82     |                          1.76     |
| 25%   |                        41.6475 |                                          74.37   |                                                 380.493 |                                10.7775  |                          2.5075   |                             1.7875   |                          2.11     |
| 50%   |                        63.5    |                                          79.725  |                                                 513.66  |                                12.995   |                          2.62     |                             1.935    |                          2.25     |
| 75%   |                        92.1225 |                                          83.8075 |                                                 734.275 |                                15.315   |                          2.685    |                             2.0625   |                          2.4525   |
| max   |                       319.92   |                                          92.66   |                                                1700.07  |                                28.35    |                          3.07     |                             2.42     |                          2.85     |

#### Resultados:

| Modelo                             |   MAE (R$/L) |   RMSE (R$/L) |      R² |
|:-----------------------------------|-------------:|--------------:|--------:|
| Regressão Linear                   |       0.1924 |        0.2359 | -0.0808 |
| Random Forest                      |       0.197  |        0.2426 | -0.1438 |
| Gradient Boosting                  |       0.1942 |        0.2443 | -0.1594 |
| Rede Neural (Rasa - 64 neurônios)  |       0.1883 |        0.2359 | -0.081  |
| Rede Neural (Média - 64x32)        |       0.1853 |        0.2364 | -0.0853 |
| Rede Neural (Profunda - 128x64x32) |       0.193  |        0.2463 | -0.1789 |
| Regressão Ridge (Penalizada)       |       0.1819 |        0.2222 |  0.0405 |
| **Elastic Net**                        |       **0.1751** |        **0.2133** |  **0.1159** |
| Support Vector Regression (SVR)    |       0.1846 |        0.2341 | -0.0647 |
| LightGBM (HistGradientBoosting)    |       0.2029 |        0.2523 | -0.2364 |

---
### 25% Inferiores:

#### Divisão treino/teste:

- **Treino (2023):** 55 fazendas
- **Teste (2024):** 61 fazendas

#### Distribuição dos dados de treino:

|       |   7_total_de_vacas_animais_mes |   17_vacas_em_lactacao_total_de_vacas_percentual |   13_ccs_contagem_de_celulas_somaticas_x1000_celulas_ml |   26_producao_total_de_vacas_litros_dia |   33_preco_medio_do_leite_r_litro |   34_preco_medio_do_concentrado_r_kg |   52_custo_total_do_leite_r_litro |
|:------|-------------------------------:|-------------------------------------------------:|--------------------------------------------------------:|----------------------------------------:|----------------------------------:|-------------------------------------:|----------------------------------:|
| count |                        55      |                                         55       |                                                  55     |                                55       |                         55        |                            55        |                          55       |
| mean  |                        75.0758 |                                         75.2504  |                                                 559.272 |                                11.2093  |                          2.38709  |                             2.07891  |                           2.90927 |
| std   |                        56.5272 |                                          9.55544 |                                                 256.56  |                                 3.57656 |                          0.148632 |                             0.273649 |                           0.47733 |
| min   |                        13.5    |                                         48.48    |                                                 226.12  |                                 3.77    |                          2.08     |                             1.16     |                           2.14    |
| 25%   |                        37.96   |                                         69.37    |                                                 380.215 |                                 8.52    |                          2.285    |                             1.985    |                           2.635   |
| 50%   |                        58.25   |                                         77.84    |                                                 496.98  |                                10.7     |                          2.37     |                             2.14     |                           2.79    |
| 75%   |                        92.625  |                                         81.94    |                                                 684.835 |                                13.61    |                          2.485    |                             2.26     |                           3.055   |
| max   |                       272.5    |                                         92.95    |                                                1392.05  |                                20.56    |                          2.72     |                             2.51     |                           4.36    |

#### Distribuição dos dados de teste:

|       |   7_total_de_vacas_animais_mes |   17_vacas_em_lactacao_total_de_vacas_percentual |   13_ccs_contagem_de_celulas_somaticas_x1000_celulas_ml |   26_producao_total_de_vacas_litros_dia |   33_preco_medio_do_leite_r_litro |   34_preco_medio_do_concentrado_r_kg |   52_custo_total_do_leite_r_litro |
|:------|-------------------------------:|-------------------------------------------------:|--------------------------------------------------------:|----------------------------------------:|----------------------------------:|-------------------------------------:|----------------------------------:|
| count |                        61      |                                          61      |                                                  61     |                                 61      |                         61        |                            61        |                         61        |
| mean  |                        64.0169 |                                          73.0539 |                                                 674.858 |                                 10.4515 |                          2.52361  |                             1.92607  |                          3.01869  |
| std   |                        47.0247 |                                          10.7937 |                                                 342.961 |                                  3.5972 |                          0.160832 |                             0.281545 |                          0.667711 |
| min   |                        15.17   |                                          39.11   |                                                 173.65  |                                  2.91   |                          2.15     |                             1.17     |                          2.25     |
| 25%   |                        32.58   |                                          69.11   |                                                 428.46  |                                  7.72   |                          2.43     |                             1.74     |                          2.68     |
| 50%   |                        55.25   |                                          74.64   |                                                 625.59  |                                 10.55   |                          2.53     |                             1.98     |                          2.84     |
| 75%   |                        76.33   |                                          81.06   |                                                 751.57  |                                 12.54   |                          2.62     |                             2.09     |                          3.21     |
| max   |                       226.67   |                                          90.56   |                                                1680.62  |                                 18.61   |                          2.91     |                             2.43     |                          5.87     |

#### Resultados:

| Modelo                             |   MAE (R$/L) |   RMSE (R$/L) |      R² |
|:-----------------------------------|-------------:|--------------:|--------:|
| Regressão Linear                   |       0.459  |        0.6251 |  0.1089 |
| Random Forest                      |       0.411  |        0.6233 |  0.1141 |
| Gradient Boosting                  |       0.4293 |        0.6282 |  0.1002 |
| Rede Neural (Rasa - 64 neurônios)  |       0.4911 |        0.6859 | -0.0728 |
| Rede Neural (Média - 64x32)        |       0.4599 |        0.6912 | -0.0895 |
| Rede Neural (Profunda - 128x64x32) |       0.4054 |        0.6074 |  0.1586 |
| Regressão Ridge (Penalizada)       |       0.4488 |        0.635  |  0.0804 |
| Elastic Net                        |       0.4096 |        0.6546 |  0.0228 |
| **Support Vector Regression (SVR)**    |       **0.3878** |        **0.6376** |  **0.0729** |
| LightGBM (HistGradientBoosting)    |       0.4142 |        0.6706 | -0.0255 |