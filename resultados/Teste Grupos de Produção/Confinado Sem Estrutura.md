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

## Confinado Sem Estrutura

### $\leq$ 1000 L/dia:

#### Divisão treino/teste:

- **Treino (2023):** 52 fazendas
- **Teste (2024):** 54 fazendas

#### Distribuição dos dados de treino:

|       |   7_total_de_vacas_animais_mes |   17_vacas_em_lactacao_total_de_vacas_percentual |   13_ccs_contagem_de_celulas_somaticas_x1000_celulas_ml |   26_producao_total_de_vacas_litros_dia |   33_preco_medio_do_leite_r_litro |   34_preco_medio_do_concentrado_r_kg |   52_custo_total_do_leite_r_litro |
|:------|-------------------------------:|-------------------------------------------------:|--------------------------------------------------------:|----------------------------------------:|----------------------------------:|-------------------------------------:|----------------------------------:|
| count |                        52      |                                         52       |                                                  52     |                                 52      |                         52        |                            52        |                         52        |
| mean  |                        42.0254 |                                         82.7563  |                                                 448.526 |                                 14.2738 |                          2.48346  |                             2.04365  |                          2.615    |
| std   |                        17.4969 |                                          6.34839 |                                                 236.795 |                                  4.0283 |                          0.165682 |                             0.208543 |                          0.663406 |
| min   |                        12.17   |                                         69.49    |                                                 113.02  |                                  4.54   |                          2.23     |                             1.54     |                          1.35     |
| 25%   |                        29.7075 |                                         77.79    |                                                 282.035 |                                 12.3425 |                          2.3475   |                             1.95     |                          2.1875   |
| 50%   |                        36.96   |                                         83.295   |                                                 405.105 |                                 14.1    |                          2.485    |                             2.075    |                          2.545    |
| 75%   |                        55.81   |                                         87.815   |                                                 563.558 |                                 16.3    |                          2.64     |                             2.18     |                          2.88     |
| max   |                        89.33   |                                         97.21    |                                                1281.79  |                                 29.04   |                          2.95     |                             2.62     |                          4.76     |

#### Distribuição dos dados de teste:

|       |   7_total_de_vacas_animais_mes |   17_vacas_em_lactacao_total_de_vacas_percentual |   13_ccs_contagem_de_celulas_somaticas_x1000_celulas_ml |   26_producao_total_de_vacas_litros_dia |   33_preco_medio_do_leite_r_litro |   34_preco_medio_do_concentrado_r_kg |   52_custo_total_do_leite_r_litro |
|:------|-------------------------------:|-------------------------------------------------:|--------------------------------------------------------:|----------------------------------------:|----------------------------------:|-------------------------------------:|----------------------------------:|
| count |                        54      |                                         54       |                                                  54     |                                54       |                         54        |                            54        |                         54        |
| mean  |                        41.497  |                                         82.0498  |                                                 447.67  |                                14.3152  |                          2.61333  |                             1.89167  |                          2.43741  |
| std   |                        15.7126 |                                          6.89811 |                                                 237.447 |                                 3.11811 |                          0.129964 |                             0.190637 |                          0.492208 |
| min   |                         8.83   |                                         58.05    |                                                  88.07  |                                 6.61    |                          2.34     |                             1.44     |                          1.63     |
| 25%   |                        31.8125 |                                         76.3325  |                                                 278.873 |                                12.44    |                          2.52     |                             1.8025   |                          2.175    |
| 50%   |                        39.455  |                                         83.4     |                                                 413.77  |                                14.06    |                          2.605    |                             1.9      |                          2.335    |
| 75%   |                        51.96   |                                         86.475   |                                                 530.82  |                                16.055   |                          2.72     |                             2.0025   |                          2.6175   |
| max   |                        80.67   |                                         97.3     |                                                1114.95  |                                22.23    |                          2.85     |                             2.3      |                          4.65     |

#### Resultados:

| Modelo                             |   MAE (R$/L) |   RMSE (R$/L) |      R² |
|:-----------------------------------|-------------:|--------------:|--------:|
| Regressão Linear                   |       0.5474 |        0.6846 | -0.9713 |
| Random Forest                      |       0.5362 |        0.6457 | -0.7534 |
| Gradient Boosting                  |       0.7031 |        0.9317 | -2.6508 |
| Rede Neural (Rasa - 64 neurônios)  |       0.5059 |        0.6209 | -0.6215 |
| Rede Neural (Média - 64x32)        |       0.4977 |        0.6249 | -0.6421 |
| Rede Neural (Profunda - 128x64x32) |       0.5893 |        0.7135 | -1.1413 |
| Regressão Ridge (Penalizada)       |       0.5316 |        0.6202 | -0.6177 |
| Elastic Net                        |       0.5023 |        0.5998 | -0.5131 |
| **Support Vector Regression (SVR)**    |       **0.426**  |        **0.5254** | **-0.161**  |
| LightGBM (HistGradientBoosting)    |       0.4956 |        0.595  | -0.4889 |

---
### $>$ 1000 e $\leq$ 3000 L/dia:

#### Divisão treino/teste:

- **Treino (2023):** 39 fazendas
- **Teste (2024):** 44 fazendas

#### Distribuição dos dados de treino:

|       |   7_total_de_vacas_animais_mes |   17_vacas_em_lactacao_total_de_vacas_percentual |   13_ccs_contagem_de_celulas_somaticas_x1000_celulas_ml |   26_producao_total_de_vacas_litros_dia |   33_preco_medio_do_leite_r_litro |   34_preco_medio_do_concentrado_r_kg |   52_custo_total_do_leite_r_litro |
|:------|-------------------------------:|-------------------------------------------------:|--------------------------------------------------------:|----------------------------------------:|----------------------------------:|-------------------------------------:|----------------------------------:|
| count |                         39     |                                         39       |                                                  39     |                                39       |                         39        |                            39        |                         39        |
| mean  |                        100.617 |                                         83.4482  |                                                 440.862 |                                16.6897  |                          2.57385  |                             2.02026  |                          2.37846  |
| std   |                         36.486 |                                          5.11374 |                                                 283.474 |                                 2.84719 |                          0.134587 |                             0.221234 |                          0.326501 |
| min   |                         42.42  |                                         64.36    |                                                 147.18  |                                10.19    |                          2.3      |                             1.33     |                          1.8      |
| 25%   |                         72.205 |                                         81.395   |                                                 234.31  |                                14.335   |                          2.49     |                             1.875    |                          2.15     |
| 50%   |                         98.83  |                                         84.43    |                                                 321.74  |                                16.72    |                          2.57     |                             2.05     |                          2.38     |
| 75%   |                        126.71  |                                         86.93    |                                                 613.775 |                                18.58    |                          2.675    |                             2.155    |                          2.53     |
| max   |                        190.83  |                                         89.52    |                                                1081.07  |                                24.19    |                          2.84     |                             2.42     |                          3.09     |

#### Distribuição dos dados de teste:

|       |   7_total_de_vacas_animais_mes |   17_vacas_em_lactacao_total_de_vacas_percentual |   13_ccs_contagem_de_celulas_somaticas_x1000_celulas_ml |   26_producao_total_de_vacas_litros_dia |   33_preco_medio_do_leite_r_litro |   34_preco_medio_do_concentrado_r_kg |   52_custo_total_do_leite_r_litro |
|:------|-------------------------------:|-------------------------------------------------:|--------------------------------------------------------:|----------------------------------------:|----------------------------------:|-------------------------------------:|----------------------------------:|
| count |                        44      |                                         44       |                                                  44     |                                44       |                         44        |                            44        |                         44        |
| mean  |                        96.517  |                                         83.9857  |                                                 498.158 |                                17.2893  |                          2.71705  |                             1.84795  |                          2.245    |
| std   |                        33.3611 |                                          4.87034 |                                                 357.948 |                                 3.55133 |                          0.129643 |                             0.223842 |                          0.281644 |
| min   |                        37.92   |                                         68.44    |                                                  99.86  |                                11.02    |                          2.37     |                             1.16     |                          1.54     |
| 25%   |                        70.165  |                                         82.5475  |                                                 236.61  |                                14.47    |                          2.64     |                             1.725    |                          2.0925   |
| 50%   |                        93.455  |                                         84.345   |                                                 399.035 |                                17.185   |                          2.74     |                             1.89     |                          2.185    |
| 75%   |                       119.42   |                                         86.795   |                                                 586.765 |                                19.665   |                          2.805    |                             1.96     |                          2.5225   |
| max   |                       174.17   |                                         96.31    |                                                1475.78  |                                27.71    |                          2.98     |                             2.31     |                          2.83     |

#### Resultados:

| Modelo                             |   MAE (R$/L) |   RMSE (R$/L) |      R² |
|:-----------------------------------|-------------:|--------------:|--------:|
| Regressão Linear                   |       0.353  |        0.4429 | -1.5302 |
| **Random Forest**                      |       **0.2537** |        **0.3081** | **-0.2241** |
| Gradient Boosting                  |       0.2633 |        0.3238 | -0.3528 |
| Rede Neural (Rasa - 64 neurônios)  |       0.5821 |        0.7249 | -5.7783 |
| Rede Neural (Média - 64x32)        |       0.4636 |        0.5727 | -3.2303 |
| Rede Neural (Profunda - 128x64x32) |       0.431  |        0.5483 | -2.8774 |
| Regressão Ridge (Penalizada)       |       0.3382 |        0.4118 | -1.1873 |
| Elastic Net                        |       0.2577 |        0.3147 | -0.2777 |
| Support Vector Regression (SVR)    |       0.2729 |        0.3358 | -0.4549 |
| LightGBM (HistGradientBoosting)    |       0.2597 |        0.3088 | -0.2298 |

---
### $>$ 3000 L/dia:

#### Divisão treino/teste:

- **Treino (2023):** 7 fazendas
- **Teste (2024):** 8 fazendas

#### Distribuição dos dados de treino:

|       |   7_total_de_vacas_animais_mes |   17_vacas_em_lactacao_total_de_vacas_percentual |   13_ccs_contagem_de_celulas_somaticas_x1000_celulas_ml |   26_producao_total_de_vacas_litros_dia |   33_preco_medio_do_leite_r_litro |   34_preco_medio_do_concentrado_r_kg |   52_custo_total_do_leite_r_litro |
|:------|-------------------------------:|-------------------------------------------------:|--------------------------------------------------------:|----------------------------------------:|----------------------------------:|-------------------------------------:|----------------------------------:|
| count |                          7     |                                          7       |                                                   7     |                                 7       |                          7        |                             7        |                          7        |
| mean  |                        325.167 |                                         82.0671  |                                                 471.441 |                                17.8986  |                          2.51     |                             2.01714  |                          2.75857  |
| std   |                        150.811 |                                          8.31632 |                                                 265.812 |                                 3.63599 |                          0.139284 |                             0.275301 |                          0.674745 |
| min   |                        146.92  |                                         69.6     |                                                 181.42  |                                13.94    |                          2.42     |                             1.7      |                          2.13     |
| 25%   |                        201.415 |                                         75.785   |                                                 313.895 |                                15.82    |                          2.44     |                             1.81     |                          2.345    |
| 50%   |                        309.92  |                                         85.1     |                                                 383.18  |                                16.44    |                          2.47     |                             2.02     |                          2.51     |
| 75%   |                        452     |                                         88.725   |                                                 620.875 |                                19.715   |                          2.49     |                             2.14     |                          3.09     |
| max   |                        512.5   |                                         90.75    |                                                 865.95  |                                23.84    |                          2.82     |                             2.5      |                          3.8      |

#### Distribuição dos dados de teste:

|       |   7_total_de_vacas_animais_mes |   17_vacas_em_lactacao_total_de_vacas_percentual |   13_ccs_contagem_de_celulas_somaticas_x1000_celulas_ml |   26_producao_total_de_vacas_litros_dia |   33_preco_medio_do_leite_r_litro |   34_preco_medio_do_concentrado_r_kg |   52_custo_total_do_leite_r_litro |
|:------|-------------------------------:|-------------------------------------------------:|--------------------------------------------------------:|----------------------------------------:|----------------------------------:|-------------------------------------:|----------------------------------:|
| count |                          8     |                                           8      |                                                   8     |                                   8     |                         8         |                             8        |                          8        |
| mean  |                        256.384 |                                          82.9825 |                                                 394.994 |                                  18.16  |                         2.7725    |                             1.75625  |                          2.45125  |
| std   |                        125.207 |                                          10.5045 |                                                 276.97  |                                   4.597 |                         0.0696419 |                             0.284501 |                          0.597649 |
| min   |                        149     |                                          60.03   |                                                 119.87  |                                  10.3   |                         2.63      |                             1.43     |                          1.61     |
| 25%   |                        158.018 |                                          82.975  |                                                 229.007 |                                  15.46  |                         2.745     |                             1.5925   |                          2.14     |
| 50%   |                        194.29  |                                          87.15   |                                                 302.54  |                                  18.525 |                         2.79      |                             1.72     |                          2.325    |
| 75%   |                        353.312 |                                          88.7725 |                                                 495.295 |                                  20.97  |                         2.815     |                             1.83     |                          2.7325   |
| max   |                        466.33  |                                          90.38   |                                                 985.85  |                                  24.57  |                         2.85      |                             2.35     |                          3.5      |

#### Resultados:

| Modelo                             |   MAE (R$/L) |   RMSE (R$/L) |      R² |
|:-----------------------------------|-------------:|--------------:|--------:|
| Regressão Linear                   |       0.2451 |        0.2728 |  0.762  |
| Random Forest                      |       0.2872 |        0.3579 |  0.5902 |
| Gradient Boosting                  |       0.2769 |        0.3409 |  0.6282 |
| Rede Neural (Rasa - 64 neurônios)  |       0.5809 |        0.6737 | -0.4521 |
| Rede Neural (Média - 64x32)        |       0.5197 |        0.6667 | -0.4224 |
| Rede Neural (Profunda - 128x64x32) |       0.3767 |        0.4908 |  0.2293 |
| Regressão Ridge (Penalizada)       |       0.2515 |        0.2773 |  0.754  |
| **Elastic Net**                        |       **0.2357** |        **0.2774** |  **0.7538** |
| Support Vector Regression (SVR)    |       0.4355 |        0.5107 |  0.1654 |
| LightGBM (HistGradientBoosting)    |       0.563  |        0.638  | -0.3022 |