# Resumo dos Testes de Grupos de Custo Total do Leite

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

## Compost Barn + Free Stall

### 25% Superiores

#### Divisão treino/teste:

- **Treino (2023):** 41 fazendas
- **Teste (2024):** 49 fazendas

#### Distribuição dos dados de treino:

|       |   7_total_de_vacas_animais_mes |   17_vacas_em_lactacao_total_de_vacas_percentual |   13_ccs_contagem_de_celulas_somaticas_x1000_celulas_ml |   26_producao_total_de_vacas_litros_dia |   33_preco_medio_do_leite_r_litro |   34_preco_medio_do_concentrado_r_kg |   52_custo_total_do_leite_r_litro |
|:------|-------------------------------:|-------------------------------------------------:|--------------------------------------------------------:|----------------------------------------:|----------------------------------:|-------------------------------------:|----------------------------------:|
| count |                        41      |                                         41       |                                                  41     |                                 41      |                         41        |                            41        |                         41        |
| mean  |                       128.15   |                                         83.442   |                                                 326.941 |                                 22.4851 |                          2.64098  |                             1.9622   |                          2.79854  |
| std   |                        97.0976 |                                          5.45895 |                                                 289.299 |                                  4.5917 |                          0.148472 |                             0.275286 |                          0.273455 |
| min   |                        26.17   |                                         71.9     |                                                 142.83  |                                 12.92   |                          2.34     |                             1.25     |                          2.58     |
| 25%   |                        73.17   |                                         80.57    |                                                 200.84  |                                 19.8    |                          2.54     |                             1.82     |                          2.64     |
| 50%   |                       103.42   |                                         84.64    |                                                 268.93  |                                 22.52   |                          2.61     |                             2.01     |                          2.71     |
| 75%   |                       142.58   |                                         86.99    |                                                 366.54  |                                 25.04   |                          2.74     |                             2.13     |                          2.88     |
| max   |                       587      |                                         94.08    |                                                2023.55  |                                 33.49   |                          3.04     |                             2.42     |                          3.96     |

#### Distribuição dos dados de teste:

|       |   7_total_de_vacas_animais_mes |   17_vacas_em_lactacao_total_de_vacas_percentual |   13_ccs_contagem_de_celulas_somaticas_x1000_celulas_ml |   26_producao_total_de_vacas_litros_dia |   33_preco_medio_do_leite_r_litro |   34_preco_medio_do_concentrado_r_kg |   52_custo_total_do_leite_r_litro |
|:------|-------------------------------:|-------------------------------------------------:|--------------------------------------------------------:|----------------------------------------:|----------------------------------:|-------------------------------------:|----------------------------------:|
| count |                        49      |                                         49       |                                                  49     |                                49       |                         49        |                            49        |                         49        |
| mean  |                       118.524  |                                         83.7996  |                                                 376.182 |                                22.6051  |                          2.79122  |                             1.80878  |                          2.72367  |
| std   |                        70.7386 |                                          5.30729 |                                                 292.177 |                                 5.73641 |                          0.120323 |                             0.223948 |                          0.289466 |
| min   |                        14.75   |                                         68.48    |                                                 135.46  |                                 8.54    |                          2.49     |                             1.2      |                          2.46     |
| 25%   |                        63      |                                         82.51    |                                                 230.82  |                                19.02    |                          2.7      |                             1.72     |                          2.54     |
| 50%   |                       103.33   |                                         84.87    |                                                 298.36  |                                23.12    |                          2.81     |                             1.82     |                          2.63     |
| 75%   |                       167.67   |                                         87.78    |                                                 383.47  |                                26.46    |                          2.87     |                             1.96     |                          2.81     |
| max   |                       271.75   |                                         91.78    |                                                1591.85  |                                34.11    |                          3.14     |                             2.35     |                          3.96     |

#### Resultados:

| Modelo                             |   MAE (R$/L) |   RMSE (R$/L) |      R² |
|:-----------------------------------|-------------:|--------------:|--------:|
| Regressão Linear                   |       0.2674 |        0.3158 | -0.215  |
| **Random Forest**                      |       **0.232**  |        **0.3133** | **-0.1962** |
| Gradient Boosting                  |       0.248  |        0.337  | -0.3839 |
| Rede Neural (Rasa - 64 neurônios)  |       0.2338 |        0.3182 | -0.2332 |
| Rede Neural (Média - 64x32)        |       0.2848 |        0.3853 | -0.809  |
| Rede Neural (Profunda - 128x64x32) |       0.2691 |        0.3544 | -0.5305 |
| Regressão Ridge (Penalizada)       |       0.2629 |        0.3122 | -0.1877 |
| Elastic Net                        |       0.2699 |        0.3243 | -0.2813 |
| Support Vector Regression (SVR)    |       0.2451 |        0.3052 | -0.1346 |
| LightGBM (HistGradientBoosting)    |       0.2854 |        0.3639 | -0.6132 |

---
### 50% intermediários:

#### Divisão treino/teste:

- **Treino (2023):** 83 fazendas
- **Teste (2024):** 98 fazendas

#### Distribuição dos dados de treino:

|       |   7_total_de_vacas_animais_mes |   17_vacas_em_lactacao_total_de_vacas_percentual |   13_ccs_contagem_de_celulas_somaticas_x1000_celulas_ml |   26_producao_total_de_vacas_litros_dia |   33_preco_medio_do_leite_r_litro |   34_preco_medio_do_concentrado_r_kg |   52_custo_total_do_leite_r_litro |
|:------|-------------------------------:|-------------------------------------------------:|--------------------------------------------------------:|----------------------------------------:|----------------------------------:|-------------------------------------:|----------------------------------:|
| count |                         83     |                                         83       |                                                  83     |                                83       |                         83        |                            83        |                         83        |
| mean  |                        158.658 |                                         84.6898  |                                                 294.367 |                                23.4735  |                          2.66072  |                             1.99337  |                          2.35458  |
| std   |                        142.404 |                                          4.17475 |                                                 166.63  |                                 4.44486 |                          0.126788 |                             0.245259 |                          0.121718 |
| min   |                         17.58  |                                         72.99    |                                                  79.27  |                                13.19    |                          2.3      |                             1.03     |                          2.16     |
| 25%   |                         67.875 |                                         82.425   |                                                 186.075 |                                20.275   |                          2.61     |                             1.885    |                          2.245    |
| 50%   |                        109.83  |                                         85.04    |                                                 245.55  |                                23.83    |                          2.69     |                             2.03     |                          2.36     |
| 75%   |                        185.21  |                                         87.485   |                                                 345.22  |                                26.86    |                          2.74     |                             2.13     |                          2.45     |
| max   |                        681.25  |                                         94.13    |                                                 919.61  |                                33.68    |                          2.96     |                             2.68     |                          2.57     |

#### Distribuição dos dados de teste:

|       |   7_total_de_vacas_animais_mes |   17_vacas_em_lactacao_total_de_vacas_percentual |   13_ccs_contagem_de_celulas_somaticas_x1000_celulas_ml |   26_producao_total_de_vacas_litros_dia |   33_preco_medio_do_leite_r_litro |   34_preco_medio_do_concentrado_r_kg |   52_custo_total_do_leite_r_litro |
|:------|-------------------------------:|-------------------------------------------------:|--------------------------------------------------------:|----------------------------------------:|----------------------------------:|-------------------------------------:|----------------------------------:|
| count |                        98      |                                         98       |                                                  98     |                                 98      |                         98        |                            98        |                         98        |
| mean  |                       172.009  |                                         85.4492  |                                                 345.701 |                                 24.0737 |                          2.79622  |                             1.80582  |                          2.25255  |
| std   |                       165.38   |                                          3.97641 |                                                 220.085 |                                  4.5811 |                          0.108557 |                             0.244452 |                          0.106639 |
| min   |                        18.83   |                                         70.62    |                                                 113.06  |                                 11.08   |                          2.53     |                             0.95     |                          2.08     |
| 25%   |                        71.7075 |                                         83.525   |                                                 205.757 |                                 21.395  |                          2.7225   |                             1.685    |                          2.16     |
| 50%   |                       108.415  |                                         86.145   |                                                 275.445 |                                 24.205  |                          2.8      |                             1.845    |                          2.24     |
| 75%   |                       189.107  |                                         88.2275  |                                                 398.442 |                                 26.9925 |                          2.88     |                             1.97     |                          2.33     |
| max   |                       740.67   |                                         91.78    |                                                1158.15  |                                 35.09   |                          3.11     |                             2.28     |                          2.46     |

#### Resultados:

| Modelo                             |   MAE (R$/L) |   RMSE (R$/L) |      R² |
|:-----------------------------------|-------------:|--------------:|--------:|
| Regressão Linear                   |       0.1238 |        0.1511 | -1.0279 |
| Random Forest                      |       0.1283 |        0.1479 | -0.9423 |
| Gradient Boosting                  |       0.1323 |        0.1531 | -1.0827 |
| Rede Neural (Rasa - 64 neurônios)  |       0.1574 |        0.1908 | -2.233  |
| Rede Neural (Média - 64x32)        |       0.1589 |        0.1887 | -2.1624 |
| Rede Neural (Profunda - 128x64x32) |       0.1451 |        0.1696 | -1.5551 |
| **Regressão Ridge (Penalizada)**       |       **0.1203** |        **0.1434** | **-0.8274** |
| Elastic Net                        |       0.1254 |        0.1472 | -0.9248 |
| Support Vector Regression (SVR)    |       0.1318 |        0.156  | -1.1625 |
| LightGBM (HistGradientBoosting)    |       0.1297 |        0.1502 | -1.0042 |

---
### 25% Inferiores:

#### Divisão treino/teste:

- **Treino (2023):** 41 fazendas
- **Teste (2024):** 49 fazendas

#### Distribuição dos dados de treino:

|       |   7_total_de_vacas_animais_mes |   17_vacas_em_lactacao_total_de_vacas_percentual |   13_ccs_contagem_de_celulas_somaticas_x1000_celulas_ml |   26_producao_total_de_vacas_litros_dia |   33_preco_medio_do_leite_r_litro |   34_preco_medio_do_concentrado_r_kg |   52_custo_total_do_leite_r_litro |
|:------|-------------------------------:|-------------------------------------------------:|--------------------------------------------------------:|----------------------------------------:|----------------------------------:|-------------------------------------:|----------------------------------:|
| count |                         41     |                                         41       |                                                  41     |                                41       |                         41        |                            41        |                         41        |
| mean  |                        152.339 |                                         84.9927  |                                                 293.721 |                                24.119   |                          2.63     |                             1.97756  |                          1.99561  |
| std   |                        148.761 |                                          3.89441 |                                                 203.318 |                                 4.35975 |                          0.127632 |                             0.211752 |                          0.150051 |
| min   |                         20.25  |                                         74.01    |                                                  86.85  |                                 9.34    |                          2.26     |                             1.33     |                          1.67     |
| 25%   |                         70     |                                         81.87    |                                                 175.73  |                                22.02    |                          2.55     |                             1.86     |                          1.9      |
| 50%   |                        101     |                                         84.77    |                                                 247.83  |                                24.92    |                          2.67     |                             2.02     |                          2.06     |
| 75%   |                        186.08  |                                         88.28    |                                                 329.09  |                                27.17    |                          2.75     |                             2.11     |                          2.1      |
| max   |                        697.17  |                                         90.67    |                                                1027.19  |                                33.74    |                          2.82     |                             2.3      |                          2.16     |

#### Distribuição dos dados de teste:

|       |   7_total_de_vacas_animais_mes |   17_vacas_em_lactacao_total_de_vacas_percentual |   13_ccs_contagem_de_celulas_somaticas_x1000_celulas_ml |   26_producao_total_de_vacas_litros_dia |   33_preco_medio_do_leite_r_litro |   34_preco_medio_do_concentrado_r_kg |   52_custo_total_do_leite_r_litro |
|:------|-------------------------------:|-------------------------------------------------:|--------------------------------------------------------:|----------------------------------------:|----------------------------------:|-------------------------------------:|----------------------------------:|
| count |                         49     |                                         49       |                                                  49     |                                49       |                         49        |                            49        |                          49       |
| mean  |                        145.499 |                                         85.0171  |                                                 245.198 |                                24.9027  |                          2.79184  |                             1.87041  |                           1.84837 |
| std   |                        120.842 |                                          4.30413 |                                                 134.556 |                                 3.75739 |                          0.110899 |                             0.228801 |                           0.183   |
| min   |                         22.42  |                                         72.59    |                                                  81.36  |                                12.58    |                          2.51     |                             1.44     |                           1.14    |
| 25%   |                         69     |                                         82.56    |                                                 147.55  |                                23.11    |                          2.71     |                             1.73     |                           1.78    |
| 50%   |                        114.33  |                                         85.29    |                                                 214.36  |                                25.14    |                          2.81     |                             1.83     |                           1.89    |
| 75%   |                        171.17  |                                         88.35    |                                                 300.41  |                                27.78    |                          2.87     |                             2        |                           1.99    |
| max   |                        620.25  |                                         93.77    |                                                 753.62  |                                30.42    |                          3.01     |                             2.51     |                           2.06    |

#### Resultados:

| Modelo                             |   MAE (R$/L) |   RMSE (R$/L) |      R² |
|:-----------------------------------|-------------:|--------------:|--------:|
| Regressão Linear                   |       0.1539 |        0.2192 | -0.4651 |
| Random Forest                      |       0.1699 |        0.2353 | -0.6877 |
| Gradient Boosting                  |       0.1764 |        0.244  | -0.8155 |
| Rede Neural (Rasa - 64 neurônios)  |       0.2093 |        0.2847 | -1.4705 |
| Rede Neural (Média - 64x32)        |       0.1721 |        0.2298 | -0.6093 |
| Rede Neural (Profunda - 128x64x32) |       0.1547 |        0.2144 | -0.4013 |
| Regressão Ridge (Penalizada)       |       0.1524 |        0.2172 | -0.4383 |
| Elastic Net                        |       0.1633 |        0.2334 | -0.6609 |
| **Support Vector Regression (SVR)**    |       **0.1356** |        **0.1982** | **-0.1978** |
| LightGBM (HistGradientBoosting)    |       0.1777 |        0.2468 | -0.8568 |