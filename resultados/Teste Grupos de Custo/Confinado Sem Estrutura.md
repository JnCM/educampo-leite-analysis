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

## Confinado Sem Estrutura

### 25% Superiores:

#### Divisão treino/teste:

- **Treino (2023):** 24 fazendas
- **Teste (2024):** 26 fazendas

#### Distribuição dos dados de treino:

|       |   7_total_de_vacas_animais_mes |   17_vacas_em_lactacao_total_de_vacas_percentual |   13_ccs_contagem_de_celulas_somaticas_x1000_celulas_ml |   26_producao_total_de_vacas_litros_dia |   33_preco_medio_do_leite_r_litro |   34_preco_medio_do_concentrado_r_kg |   52_custo_total_do_leite_r_litro |
|:------|-------------------------------:|-------------------------------------------------:|--------------------------------------------------------:|----------------------------------------:|----------------------------------:|-------------------------------------:|----------------------------------:|
| count |                        24      |                                         24       |                                                  24     |                                24       |                          24       |                            24        |                         24        |
| mean  |                        85.5696 |                                         80.97    |                                                 482.987 |                                14.44    |                           2.54917 |                             2.03125  |                          3.27417  |
| std   |                       116.424  |                                          6.47987 |                                                 266.103 |                                 3.62892 |                           0.16073 |                             0.190453 |                          0.532549 |
| min   |                        12.17   |                                         69.49    |                                                 113.02  |                                 5.28    |                           2.32    |                             1.33     |                          2.8      |
| 25%   |                        34.1875 |                                         75.3575  |                                                 296.575 |                                12.535   |                           2.4075  |                             1.9775   |                          2.905    |
| 50%   |                        55.75   |                                         82.22    |                                                 423.385 |                                14.855   |                           2.57    |                             2.045    |                          3.13     |
| 75%   |                        74.875  |                                         86.2325  |                                                 654.418 |                                16.9825  |                           2.65    |                             2.14     |                          3.355    |
| max   |                       508.42   |                                         91.16    |                                                1188.79  |                                20.47    |                           2.95    |                             2.3      |                          4.76     |

#### Distribuição dos dados de teste:

|       |   7_total_de_vacas_animais_mes |   17_vacas_em_lactacao_total_de_vacas_percentual |   13_ccs_contagem_de_celulas_somaticas_x1000_celulas_ml |   26_producao_total_de_vacas_litros_dia |   33_preco_medio_do_leite_r_litro |   34_preco_medio_do_concentrado_r_kg |   52_custo_total_do_leite_r_litro |
|:------|-------------------------------:|-------------------------------------------------:|--------------------------------------------------------:|----------------------------------------:|----------------------------------:|-------------------------------------:|----------------------------------:|
| count |                        26      |                                         26       |                                                  26     |                                 26      |                         26        |                            26        |                         26        |
| mean  |                       100.003  |                                         80.6204  |                                                 403.209 |                                 14.3923 |                          2.68231  |                             1.83308  |                          2.90577  |
| std   |                       110.364  |                                          8.35074 |                                                 243.509 |                                  3.0757 |                          0.129223 |                             0.245484 |                          0.452125 |
| min   |                         8.83   |                                         58.05    |                                                 106.12  |                                  6.61   |                          2.46     |                             1.16     |                          2.54     |
| 25%   |                        34.8925 |                                         76.455   |                                                 255.882 |                                 13.02   |                          2.58     |                             1.72     |                          2.635    |
| 50%   |                        64.25   |                                         83.06    |                                                 372.3   |                                 15.17   |                          2.73     |                             1.895    |                          2.775    |
| 75%   |                       134.48   |                                         86.305   |                                                 462.572 |                                 16.41   |                          2.7925   |                             1.9475   |                          3.0125   |
| max   |                       466.33   |                                         90.63    |                                                 985.85  |                                 18.96   |                          2.85     |                             2.3      |                          4.65     |

#### Resultados:

| Modelo                             |   MAE (R$/L) |   RMSE (R$/L) |      R² |
|:-----------------------------------|-------------:|--------------:|--------:|
| Regressão Linear                   |       0.7239 |        0.8307 | -2.5105 |
| Random Forest                      |       0.4959 |        0.5595 | -0.5926 |
| **Gradient Boosting**                  |       **0.4581** |        **0.5483** | **-0.5295** |
| Rede Neural (Rasa - 64 neurônios)  |       0.674  |        0.8178 | -2.4025 |
| Rede Neural (Média - 64x32)        |       0.5869 |        0.7311 | -1.7191 |
| Rede Neural (Profunda - 128x64x32) |       0.6025 |        0.7168 | -1.614  |
| Regressão Ridge (Penalizada)       |       0.7171 |        0.7911 | -2.184  |
| Elastic Net                        |       0.6193 |        0.6775 | -1.3353 |
| Support Vector Regression (SVR)    |       0.4904 |        0.5753 | -0.6837 |
| LightGBM (HistGradientBoosting)    |       0.5125 |        0.5764 | -0.6905 |

---
### 50% Intermediários:

#### Divisão treino/teste:

- **Treino (2023):** 50 fazendas
- **Teste (2024):** 54 fazendas

#### Distribuição dos dados de treino:

|       |   7_total_de_vacas_animais_mes |   17_vacas_em_lactacao_total_de_vacas_percentual |   13_ccs_contagem_de_celulas_somaticas_x1000_celulas_ml |   26_producao_total_de_vacas_litros_dia |   33_preco_medio_do_leite_r_litro |   34_preco_medio_do_concentrado_r_kg |   52_custo_total_do_leite_r_litro |
|:------|-------------------------------:|-------------------------------------------------:|--------------------------------------------------------:|----------------------------------------:|----------------------------------:|-------------------------------------:|----------------------------------:|
| count |                        50      |                                         50       |                                                  50     |                                50       |                         50        |                            50        |                         50        |
| mean  |                        92.2146 |                                         83.0772  |                                                 424.892 |                                15.9004  |                          2.5314   |                             2.0188   |                          2.4612   |
| std   |                        84.9334 |                                          6.07824 |                                                 232.544 |                                 3.58067 |                          0.163632 |                             0.211522 |                          0.160683 |
| min   |                        16.92   |                                         64.36    |                                                 149.16  |                                10.19    |                          2.23     |                             1.54     |                          2.17     |
| 25%   |                        35.915  |                                         79.7225  |                                                 278.577 |                                13.2775  |                          2.3925   |                             1.87     |                          2.3325   |
| 50%   |                        68.625  |                                         83.925   |                                                 353.935 |                                15.705   |                          2.525    |                             2.04     |                          2.475    |
| 75%   |                       120.125  |                                         87.345   |                                                 495.803 |                                18.075   |                          2.6575   |                             2.1625   |                          2.5475   |
| max   |                       512.5    |                                         94.6     |                                                1081.07  |                                29.04    |                          2.84     |                             2.62     |                          2.79     |

#### Distribuição dos dados de teste:

|       |   7_total_de_vacas_animais_mes |   17_vacas_em_lactacao_total_de_vacas_percentual |   13_ccs_contagem_de_celulas_somaticas_x1000_celulas_ml |   26_producao_total_de_vacas_litros_dia |   33_preco_medio_do_leite_r_litro |   34_preco_medio_do_concentrado_r_kg |   52_custo_total_do_leite_r_litro |
|:------|-------------------------------:|-------------------------------------------------:|--------------------------------------------------------:|----------------------------------------:|----------------------------------:|-------------------------------------:|----------------------------------:|
| count |                        54      |                                         54       |                                                  54     |                                54       |                          54       |                             54       |                         54        |
| mean  |                        74.2576 |                                         83.2263  |                                                 500.88  |                                15.5589  |                           2.65185 |                              1.85556 |                          2.30778  |
| std   |                        53.6813 |                                          5.72103 |                                                 315.245 |                                 3.23365 |                           0.14652 |                              0.18555 |                          0.129872 |
| min   |                        12.33   |                                         68.44    |                                                  88.07  |                                10.85    |                           2.34    |                              1.39    |                          2.11     |
| 25%   |                        38.335  |                                         81.9175  |                                                 264.952 |                                12.7525  |                           2.5425  |                              1.7525  |                          2.19     |
| 50%   |                        60.75   |                                         83.89    |                                                 416.82  |                                15.41    |                           2.66    |                              1.875   |                          2.3      |
| 75%   |                        91.955  |                                         86.685   |                                                 606.242 |                                17.435   |                           2.7775  |                              1.96    |                          2.42     |
| max   |                       339.25   |                                         97.3     |                                                1475.78  |                                22.63    |                           2.9     |                              2.3     |                          2.54     |

#### Resultados:

| Modelo                             |   MAE (R$/L) |   RMSE (R$/L) |      R² |
|:-----------------------------------|-------------:|--------------:|--------:|
| Regressão Linear                   |       0.1679 |        0.21   | -1.6633 |
| Random Forest                      |       0.17   |        0.2035 | -1.5006 |
| Gradient Boosting                  |       0.1782 |        0.2182 | -1.8762 |
| Rede Neural (Rasa - 64 neurônios)  |       0.2686 |        0.3633 | -6.9751 |
| Rede Neural (Média - 64x32)        |       0.2205 |        0.3045 | -4.6025 |
| Rede Neural (Profunda - 128x64x32) |       0.216  |        0.2802 | -3.7413 |
| Regressão Ridge (Penalizada)       |       0.1679 |        0.2068 | -1.5838 |
| **Elastic Net**                        |       **0.1602** |        **0.1939** | **-1.2709** |
| Support Vector Regression (SVR)    |       0.1634 |        0.1941 | -1.276  |
| LightGBM (HistGradientBoosting)    |       0.1723 |        0.2053 | -1.5451 |

---
### 25% Inferiores:

#### Divisão treino/teste:

- **Treino (2023):** 24 fazendas
- **Teste (2024):** 26 fazendas

#### Distribuição dos dados de treino:

|       |   7_total_de_vacas_animais_mes |   17_vacas_em_lactacao_total_de_vacas_percentual |   13_ccs_contagem_de_celulas_somaticas_x1000_celulas_ml |   26_producao_total_de_vacas_litros_dia |   33_preco_medio_do_leite_r_litro |   34_preco_medio_do_concentrado_r_kg |   52_custo_total_do_leite_r_litro |
|:------|-------------------------------:|-------------------------------------------------:|--------------------------------------------------------:|----------------------------------------:|----------------------------------:|-------------------------------------:|----------------------------------:|
| count |                        24      |                                         24       |                                                  24     |                                24       |                         24        |                             24       |                         24        |
| mean  |                        71.715  |                                         84.7975  |                                                 457.532 |                                15.7021  |                          2.4725   |                              2.06208 |                          1.93375  |
| std   |                        41.6522 |                                          4.79271 |                                                 295.353 |                                 4.28101 |                          0.131983 |                              0.25449 |                          0.210296 |
| min   |                        20.83   |                                         76.27    |                                                 153.69  |                                 4.54    |                          2.24     |                              1.55    |                          1.35     |
| 25%   |                        42.04   |                                         81.06    |                                                 214.082 |                                13.4475  |                          2.3775   |                              1.8625  |                          1.85     |
| 50%   |                        60.415  |                                         84.685   |                                                 300.93  |                                16.14    |                          2.45     |                              2.09    |                          2        |
| 75%   |                        98.8725 |                                         87.9875  |                                                 632.175 |                                18.2     |                          2.5725   |                              2.255   |                          2.08     |
| max   |                       191.5    |                                         97.21    |                                                1281.79  |                                24.19    |                          2.78     |                              2.5     |                          2.17     |

#### Distribuição dos dados de teste:

|       |   7_total_de_vacas_animais_mes |   17_vacas_em_lactacao_total_de_vacas_percentual |   13_ccs_contagem_de_celulas_somaticas_x1000_celulas_ml |   26_producao_total_de_vacas_litros_dia |   33_preco_medio_do_leite_r_litro |   34_preco_medio_do_concentrado_r_kg |   52_custo_total_do_leite_r_litro |
|:------|-------------------------------:|-------------------------------------------------:|--------------------------------------------------------:|----------------------------------------:|----------------------------------:|-------------------------------------:|----------------------------------:|
| count |                        26      |                                         26       |                                                  26     |                                 26      |                         26        |                            26        |                         26        |
| mean  |                        74.1796 |                                         84.5988  |                                                 450.85  |                                 17.8712 |                          2.68885  |                             1.90962  |                          1.91692  |
| std   |                        40.6587 |                                          5.33407 |                                                 297.651 |                                  4.516  |                          0.129687 |                             0.234836 |                          0.170077 |
| min   |                        27.5    |                                         74.03    |                                                 119.87  |                                 10.02   |                          2.42     |                             1.52     |                          1.54     |
| 25%   |                        45.7325 |                                         81.835   |                                                 252.655 |                                 14.25   |                          2.64     |                             1.7775   |                          1.8      |
| 50%   |                        59.25   |                                         84.76    |                                                 393.1   |                                 17.135  |                          2.685    |                             1.905    |                          1.95     |
| 75%   |                        97.9975 |                                         88.11    |                                                 527.283 |                                 20.8225 |                          2.7825   |                             1.975    |                          2.065    |
| max   |                       187.25   |                                         96.31    |                                                1380.04  |                                 27.71   |                          2.98     |                             2.35     |                          2.11     |

#### Resultados:

| Modelo                             |   MAE (R$/L) |   RMSE (R$/L) |       R² |
|:-----------------------------------|-------------:|--------------:|---------:|
| Regressão Linear                   |       0.238  |        0.2917 |  -2.0591 |
| Random Forest                      |       0.1329 |        0.1706 |  -0.0459 |
| Gradient Boosting                  |       0.1274 |        0.1693 |  -0.0307 |
| Rede Neural (Rasa - 64 neurônios)  |       0.5437 |        0.6768 | -15.4706 |
| Rede Neural (Média - 64x32)        |       0.3848 |        0.475  |  -7.112  |
| Rede Neural (Profunda - 128x64x32) |       0.2445 |        0.3026 |  -2.2917 |
| Regressão Ridge (Penalizada)       |       0.2268 |        0.2879 |  -1.9809 |
| Elastic Net                        |       0.1481 |        0.179  |  -0.1518 |
| **Support Vector Regression (SVR)**    |       **0.1122** |        **0.1425** |   **0.2695** |
| LightGBM (HistGradientBoosting)    |       0.1363 |        0.1676 |  -0.0102 |