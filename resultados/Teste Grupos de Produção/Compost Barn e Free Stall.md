# Resumo dos Testes de Grupos de Produção Diária

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

### $\leq$ 1000 L/dia:

#### Divisão treino/teste:

- **Treino (2023):** 23 fazendas
- **Teste (2024):** 29 fazendas

#### Distribuição dos dados de treino:

|       |   7_total_de_vacas_animais_mes |   17_vacas_em_lactacao_total_de_vacas_percentual |   13_ccs_contagem_de_celulas_somaticas_x1000_celulas_ml |   26_producao_total_de_vacas_litros_dia |   33_preco_medio_do_leite_r_litro |   34_preco_medio_do_concentrado_r_kg |   52_custo_total_do_leite_r_litro |
|:------|-------------------------------:|-------------------------------------------------:|--------------------------------------------------------:|----------------------------------------:|----------------------------------:|-------------------------------------:|----------------------------------:|
| count |                        23      |                                         23       |                                                  23     |                                23       |                         23        |                             23       |                         23        |
| mean  |                        38.1409 |                                         82.8883  |                                                 414.509 |                                18.6487  |                          2.54565  |                              2.09348 |                          2.40087  |
| std   |                        17.8776 |                                          4.84524 |                                                 255.209 |                                 3.93049 |                          0.151352 |                              0.24804 |                          0.349505 |
| min   |                        17.58   |                                         71.9     |                                                  86.85  |                                 9.34    |                          2.26     |                              1.57    |                          1.72     |
| 25%   |                        25.125  |                                         80.465   |                                                 255.56  |                                16.385   |                          2.42     |                              1.99    |                          2.22     |
| 50%   |                        31.5    |                                         84.48    |                                                 329.09  |                                19.91    |                          2.6      |                              2.1     |                          2.45     |
| 75%   |                        48.5    |                                         86.7     |                                                 495.79  |                                20.5     |                          2.665    |                              2.165   |                          2.555    |
| max   |                        98.92   |                                         90.59    |                                                1027.19  |                                27.48    |                          2.74     |                              2.68    |                          3.36     |

#### Distribuição dos dados de teste:

|       |   7_total_de_vacas_animais_mes |   17_vacas_em_lactacao_total_de_vacas_percentual |   13_ccs_contagem_de_celulas_somaticas_x1000_celulas_ml |   26_producao_total_de_vacas_litros_dia |   33_preco_medio_do_leite_r_litro |   34_preco_medio_do_concentrado_r_kg |   52_custo_total_do_leite_r_litro |
|:------|-------------------------------:|-------------------------------------------------:|--------------------------------------------------------:|----------------------------------------:|----------------------------------:|-------------------------------------:|----------------------------------:|
| count |                        29      |                                         29       |                                                  29     |                                29       |                         29        |                            29        |                         29        |
| mean  |                        36.4772 |                                         83.721   |                                                 482.362 |                                19.5217  |                          2.68414  |                             1.88517  |                          2.33793  |
| std   |                        15.9406 |                                          6.19699 |                                                 333.813 |                                 4.70525 |                          0.109529 |                             0.203006 |                          0.401385 |
| min   |                        14.75   |                                         68.48    |                                                 122.74  |                                 8.54    |                          2.49     |                             1.48     |                          1.35     |
| 25%   |                        25.42   |                                         80.16    |                                                 268.73  |                                17.06    |                          2.61     |                             1.73     |                          2.08     |
| 50%   |                        35.17   |                                         84.82    |                                                 372.27  |                                20       |                          2.68     |                             1.85     |                          2.28     |
| 75%   |                        42.83   |                                         87.54    |                                                 529.43  |                                22.68    |                          2.76     |                             2.08     |                          2.6      |
| max   |                        74.25   |                                         91.78    |                                                1591.85  |                                27.56    |                          2.9      |                             2.28     |                          3.28     |

#### Resultados:

| Modelo                             |   MAE (R$/L) |   RMSE (R$/L) |      R² |
|:-----------------------------------|-------------:|--------------:|--------:|
| Regressão Linear                   |       0.3218 |        0.4426 | -0.2593 |
| Random Forest                      |       0.33   |        0.415  | -0.1071 |
| Gradient Boosting                  |       0.3527 |        0.4626 | -0.3756 |
| Rede Neural (Rasa - 64 neurônios)  |       0.4556 |        0.5706 | -1.0928 |
| Rede Neural (Média - 64x32)        |       0.3679 |        0.4883 | -0.533  |
| Rede Neural (Profunda - 128x64x32) |       0.3474 |        0.4747 | -0.4483 |
| **Regressão Ridge (Penalizada)**       |       **0.3064** |        **0.4048** | **-0.0534** |
| Elastic Net                        |       0.3242 |        0.404  | -0.0495 |
| Support Vector Regression (SVR)    |       0.3092 |        0.3999 | -0.0281 |
| LightGBM (HistGradientBoosting)    |       0.3258 |        0.3994 | -0.0255 |

---
### $>$ 1000 e $\leq$ 3000 L/dia:

#### Divisão treino/teste:

- **Treino (2023):** 75 fazendas
- **Teste (2024):** 85 fazendas

#### Distribuição dos dados de treino:

|       |   7_total_de_vacas_animais_mes |   17_vacas_em_lactacao_total_de_vacas_percentual |   13_ccs_contagem_de_celulas_somaticas_x1000_celulas_ml |   26_producao_total_de_vacas_litros_dia |   33_preco_medio_do_leite_r_litro |   34_preco_medio_do_concentrado_r_kg |   52_custo_total_do_leite_r_litro |
|:------|-------------------------------:|-------------------------------------------------:|--------------------------------------------------------:|----------------------------------------:|----------------------------------:|-------------------------------------:|----------------------------------:|
| count |                        75      |                                         75       |                                                  75     |                                75       |                         75        |                            75        |                         75        |
| mean  |                        87.2575 |                                         84.1653  |                                                 325.799 |                                22.364   |                          2.6384   |                             1.99587  |                          2.36773  |
| std   |                        25.1326 |                                          4.86633 |                                                 246.694 |                                 3.80581 |                          0.138115 |                             0.199154 |                          0.334917 |
| min   |                        43.08   |                                         73.27    |                                                  92.12  |                                13.19    |                          2.34     |                             1.25     |                          1.67     |
| 25%   |                        70.25   |                                         80.95    |                                                 203.185 |                                20.3     |                          2.53     |                             1.905    |                          2.155    |
| 50%   |                        88.42   |                                         84.46    |                                                 283.33  |                                22.32    |                          2.66     |                             2.02     |                          2.35     |
| 75%   |                       103.125  |                                         87.78    |                                                 387.625 |                                25.015   |                          2.74     |                             2.13     |                          2.595    |
| max   |                       181.08   |                                         94.13    |                                                2023.55  |                                29.58    |                          3.04     |                             2.34     |                          3.4      |

#### Distribuição dos dados de teste:

|       |   7_total_de_vacas_animais_mes |   17_vacas_em_lactacao_total_de_vacas_percentual |   13_ccs_contagem_de_celulas_somaticas_x1000_celulas_ml |   26_producao_total_de_vacas_litros_dia |   33_preco_medio_do_leite_r_litro |   34_preco_medio_do_concentrado_r_kg |   52_custo_total_do_leite_r_litro |
|:------|-------------------------------:|-------------------------------------------------:|--------------------------------------------------------:|----------------------------------------:|----------------------------------:|-------------------------------------:|----------------------------------:|
| count |                        85      |                                         85       |                                                  85     |                                85       |                        85         |                             85       |                         85        |
| mean  |                        88.0824 |                                         85.2746  |                                                 336.93  |                                23.1005  |                         2.78129   |                              1.84788 |                          2.24824  |
| std   |                        27.1523 |                                          4.22523 |                                                 207.076 |                                 3.93643 |                         0.0973554 |                              0.19471 |                          0.390598 |
| min   |                        42.25   |                                         70.6     |                                                  95.42  |                                12.58    |                         2.55      |                              1.33    |                          1.14     |
| 25%   |                        66.17   |                                         83.47    |                                                 192.06  |                                21.1     |                         2.7       |                              1.73    |                          2.04     |
| 50%   |                        86.67   |                                         85.75    |                                                 306.78  |                                23.67    |                         2.8       |                              1.87    |                          2.22     |
| 75%   |                       103      |                                         88.65    |                                                 383.47  |                                25.89    |                         2.86      |                              1.98    |                          2.42     |
| max   |                       206.5    |                                         93.77    |                                                1488.77  |                                30.42    |                         2.97      |                              2.35    |                          3.96     |

#### Resultados:

| Modelo                             |   MAE (R$/L) |   RMSE (R$/L) |      R² |
|:-----------------------------------|-------------:|--------------:|--------:|
| Regressão Linear                   |       0.2614 |        0.3422 |  0.2232 |
| Random Forest                      |       0.261  |        0.3557 |  0.161  |
| Gradient Boosting                  |       0.316  |        0.4039 | -0.0822 |
| Rede Neural (Rasa - 64 neurônios)  |       0.316  |        0.3858 |  0.0127 |
| Rede Neural (Média - 64x32)        |       0.271  |        0.3498 |  0.1883 |
| Rede Neural (Profunda - 128x64x32) |       0.303  |        0.4078 | -0.103  |
| **Regressão Ridge (Penalizada)**       |       **0.2491** |        **0.3383** |  **0.2411** |
| Elastic Net                        |       0.2925 |        0.4017 | -0.0704 |
| Support Vector Regression (SVR)    |       0.2809 |        0.38   |  0.042  |
| LightGBM (HistGradientBoosting)    |       0.3053 |        0.4005 | -0.0636 |

---
### $>$ 3000 L/dia:

#### Divisão treino/teste:

- **Treino (2023):** 67 fazendas
- **Teste (2024):** 82 fazendas

#### Distribuição dos dados de treino:

|       |   7_total_de_vacas_animais_mes |   17_vacas_em_lactacao_total_de_vacas_percentual |   13_ccs_contagem_de_celulas_somaticas_x1000_celulas_ml |   26_producao_total_de_vacas_litros_dia |   33_preco_medio_do_leite_r_litro |   34_preco_medio_do_concentrado_r_kg |   52_custo_total_do_leite_r_litro |
|:------|-------------------------------:|-------------------------------------------------:|--------------------------------------------------------:|----------------------------------------:|----------------------------------:|-------------------------------------:|----------------------------------:|
| count |                         67     |                                         67       |                                                  67     |                                67       |                        67         |                            67        |                         67        |
| mean  |                        257.42  |                                         85.317   |                                                 237.477 |                                26.1619  |                         2.69433   |                             1.92746  |                          2.37597  |
| std   |                        152.816 |                                          3.70275 |                                                 107.47  |                                 3.38702 |                         0.0931799 |                             0.275155 |                          0.334619 |
| min   |                        103.92  |                                         73.58    |                                                  79.27  |                                17.7     |                         2.49      |                             1.03     |                          1.67     |
| 25%   |                        150.42  |                                         82.975   |                                                 168.975 |                                24.305   |                         2.615     |                             1.81     |                          2.17     |
| 50%   |                        202.42  |                                         85.71    |                                                 216.6   |                                26.24    |                         2.71      |                             1.99     |                          2.34     |
| 75%   |                        314.54  |                                         87.635   |                                                 280.925 |                                27.915   |                         2.75      |                             2.105    |                          2.54     |
| max   |                        697.17  |                                         93.2     |                                                 704.85  |                                33.74    |                         2.96      |                             2.42     |                          3.96     |

#### Distribuição dos dados de teste:

|       |   7_total_de_vacas_animais_mes |   17_vacas_em_lactacao_total_de_vacas_percentual |   13_ccs_contagem_de_celulas_somaticas_x1000_celulas_ml |   26_producao_total_de_vacas_litros_dia |   33_preco_medio_do_leite_r_litro |   34_preco_medio_do_concentrado_r_kg |   52_custo_total_do_leite_r_litro |
|:------|-------------------------------:|-------------------------------------------------:|--------------------------------------------------------:|----------------------------------------:|----------------------------------:|-------------------------------------:|----------------------------------:|
| count |                         82     |                                         82       |                                                  82     |                                82       |                        82         |                            82        |                         82        |
| mean  |                        259.136 |                                         84.9974  |                                                 264.62  |                                26.3101  |                         2.84573   |                             1.77451  |                          2.26683  |
| std   |                        154.992 |                                          3.90737 |                                                 172.002 |                                 4.18573 |                         0.0939008 |                             0.275982 |                          0.315383 |
| min   |                        103.33  |                                         71.09    |                                                  81.36  |                                16.3     |                         2.6       |                             0.95     |                          1.64     |
| 25%   |                        159.083 |                                         82.72    |                                                 176.75  |                                24.4025  |                         2.7725    |                             1.6725   |                          2.0825   |
| 50%   |                        209.625 |                                         85.855   |                                                 229.76  |                                26.95    |                         2.85      |                             1.785    |                          2.26     |
| 75%   |                        298.52  |                                         87.5725  |                                                 270.535 |                                28.6125  |                         2.9       |                             1.9675   |                          2.465    |
| max   |                        740.67  |                                         91.6     |                                                1158.15  |                                35.09    |                         3.14      |                             2.51     |                          3.04     |

#### Resultados:

| Modelo                             |   MAE (R$/L) |   RMSE (R$/L) |      R² |
|:-----------------------------------|-------------:|--------------:|--------:|
| Regressão Linear                   |       0.242  |        0.3313 | -0.1171 |
| Random Forest                      |       0.2453 |        0.3056 |  0.0497 |
| **Gradient Boosting**                  |       **0.2413** |        **0.2964** |  **0.1059** |
| Rede Neural (Rasa - 64 neurônios)  |       0.2507 |        0.3274 | -0.0911 |
| Rede Neural (Média - 64x32)        |       0.281  |        0.3712 | -0.4021 |
| Rede Neural (Profunda - 128x64x32) |       0.258  |        0.3461 | -0.2191 |
| Regressão Ridge (Penalizada)       |       0.2298 |        0.3077 |  0.0363 |
| Elastic Net                        |       0.2718 |        0.3367 | -0.1535 |
| Support Vector Regression (SVR)    |       0.2612 |        0.3271 | -0.0888 |
| LightGBM (HistGradientBoosting)    |       0.2746 |        0.3435 | -0.201  |