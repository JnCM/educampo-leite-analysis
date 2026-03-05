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

## Confinado Sem Estrutura

### 25% Superiores:

#### Divisão treino/teste:

- **Treino (2023):** 24 fazendas
- **Teste (2024):** 26 fazendas

#### Distribuição dos dados de treino:

|       |   7_total_de_vacas_animais_mes |   17_vacas_em_lactacao_total_de_vacas_percentual |   13_ccs_contagem_de_celulas_somaticas_x1000_celulas_ml |   26_producao_total_de_vacas_litros_dia |   33_preco_medio_do_leite_r_litro |   34_preco_medio_do_concentrado_r_kg |   52_custo_total_do_leite_r_litro |
|:------|-------------------------------:|-------------------------------------------------:|--------------------------------------------------------:|----------------------------------------:|----------------------------------:|-------------------------------------:|----------------------------------:|
| count |                        24      |                                          24      |                                                  24     |                                24       |                         24        |                            24        |                         24        |
| mean  |                        73.2563 |                                          85.9608 |                                                 423.613 |                                16.385   |                          2.51042  |                             2.05125  |                          1.965    |
| std   |                        41.3405 |                                           4.0852 |                                                 287.375 |                                 4.64546 |                          0.132713 |                             0.257333 |                          0.229783 |
| min   |                        20.83   |                                          80.08   |                                                 153.69  |                                 4.54    |                          2.26     |                             1.55     |                          1.35     |
| 25%   |                        41.935  |                                          82.3525 |                                                 214.082 |                                13.9225  |                          2.42     |                             1.8625   |                          1.865    |
| 50%   |                        67.165  |                                          86.53   |                                                 299.435 |                                16.37    |                          2.505    |                             2.075    |                          2.035    |
| 75%   |                        98.8725 |                                          88.4825 |                                                 618.3   |                                18.4925  |                          2.59     |                             2.255    |                          2.1225   |
| max   |                       191.5    |                                          97.21   |                                                1281.79  |                                29.04    |                          2.78     |                             2.5      |                          2.29     |

#### Distribuição dos dados de teste:

|       |   7_total_de_vacas_animais_mes |   17_vacas_em_lactacao_total_de_vacas_percentual |   13_ccs_contagem_de_celulas_somaticas_x1000_celulas_ml |   26_producao_total_de_vacas_litros_dia |   33_preco_medio_do_leite_r_litro |   34_preco_medio_do_concentrado_r_kg |   52_custo_total_do_leite_r_litro |
|:------|-------------------------------:|-------------------------------------------------:|--------------------------------------------------------:|----------------------------------------:|----------------------------------:|-------------------------------------:|----------------------------------:|
| count |                        26      |                                         26       |                                                  26     |                                26       |                         26        |                             26       |                         26        |
| mean  |                        83.6731 |                                         85.0081  |                                                 421.12  |                                18.5342  |                          2.74808  |                              1.90077 |                          1.94654  |
| std   |                        44.9196 |                                          4.77819 |                                                 308.674 |                                 4.27823 |                          0.100798 |                              0.22583 |                          0.198856 |
| min   |                        35      |                                         74.03    |                                                 119.87  |                                10.02    |                          2.52     |                              1.57    |                          1.54     |
| 25%   |                        47.42   |                                         82.9775  |                                                 235.55  |                                14.725   |                          2.6825   |                              1.725   |                          1.8      |
| 50%   |                        69.75   |                                         85.185   |                                                 350.465 |                                18.89    |                          2.765    |                              1.895   |                          1.965    |
| 75%   |                       102.58   |                                         87.685   |                                                 425.94  |                                20.835   |                          2.7975   |                              1.9575  |                          2.1075   |
| max   |                       187.25   |                                         96.31    |                                                1380.04  |                                27.71    |                          2.98     |                              2.35    |                          2.25     |

#### Resultados:

| Modelo                             |   MAE (R$/L) |   RMSE (R$/L) |      R² |
|:-----------------------------------|-------------:|--------------:|--------:|
| Regressão Linear                   |       0.2677 |        0.323  | -1.7447 |
| Random Forest                      |       0.1541 |        0.2041 | -0.0959 |
| **Gradient Boosting**                  |       **0.1498** |        **0.2045** | **-0.1003** |
| Rede Neural (Rasa - 64 neurônios)  |       0.4199 |        0.5072 | -5.7645 |
| Rede Neural (Média - 64x32)        |       0.4263 |        0.5169 | -6.0277 |
| Rede Neural (Profunda - 128x64x32) |       0.2418 |        0.304  | -1.4302 |
| Regressão Ridge (Penalizada)       |       0.2546 |        0.3181 | -1.6609 |
| Elastic Net                        |       0.1744 |        0.217  | -0.2379 |
| Support Vector Regression (SVR)    |       0.1502 |        0.1815 |  0.1339 |
| LightGBM (HistGradientBoosting)    |       0.1642 |        0.1959 | -0.009  |

---
### 50% Intermediários:

#### Divisão treino/teste:

- **Treino (2023):** 50 fazendas
- **Teste (2024):** 54 fazendas

#### Distribuição dos dados de treino:

|       |   7_total_de_vacas_animais_mes |   17_vacas_em_lactacao_total_de_vacas_percentual |   13_ccs_contagem_de_celulas_somaticas_x1000_celulas_ml |   26_producao_total_de_vacas_litros_dia |   33_preco_medio_do_leite_r_litro |   34_preco_medio_do_concentrado_r_kg |   52_custo_total_do_leite_r_litro |
|:------|-------------------------------:|-------------------------------------------------:|--------------------------------------------------------:|----------------------------------------:|----------------------------------:|-------------------------------------:|----------------------------------:|
| count |                        50      |                                         50       |                                                  50     |                                50       |                         50        |                            50        |                         50        |
| mean  |                        95.8798 |                                         82.7128  |                                                 426.293 |                                15.9316  |                          2.5406   |                             2.0044   |                          2.4724   |
| std   |                        83.0709 |                                          6.03411 |                                                 244.593 |                                 3.23564 |                          0.159123 |                             0.228546 |                          0.227341 |
| min   |                        19.33   |                                         64.36    |                                                 147.18  |                                10.19    |                          2.23     |                             1.33     |                          1.85     |
| 25%   |                        47.375  |                                         79.4275  |                                                 248.685 |                                13.43    |                          2.41     |                             1.8625   |                          2.3325   |
| 50%   |                        70.835  |                                         83.78    |                                                 362.6   |                                15.985   |                          2.535    |                             2.025    |                          2.48     |
| 75%   |                       120.125  |                                         87.0475  |                                                 505.575 |                                17.8075  |                          2.65     |                             2.1375   |                          2.5725   |
| max   |                       512.5    |                                         94.6     |                                                1081.07  |                                24.19    |                          2.84     |                             2.62     |                          2.94     |

#### Distribuição dos dados de teste:

|       |   7_total_de_vacas_animais_mes |   17_vacas_em_lactacao_total_de_vacas_percentual |   13_ccs_contagem_de_celulas_somaticas_x1000_celulas_ml |   26_producao_total_de_vacas_litros_dia |   33_preco_medio_do_leite_r_litro |   34_preco_medio_do_concentrado_r_kg |   52_custo_total_do_leite_r_litro |
|:------|-------------------------------:|-------------------------------------------------:|--------------------------------------------------------:|----------------------------------------:|----------------------------------:|-------------------------------------:|----------------------------------:|
| count |                        54      |                                         54       |                                                  54     |                                54       |                         54        |                            54        |                         54        |
| mean  |                        79.4459 |                                         83.4969  |                                                 446.989 |                                15.8596  |                          2.67815  |                             1.85241  |                          2.32185  |
| std   |                        66.8071 |                                          4.78567 |                                                 286.358 |                                 2.94192 |                          0.130891 |                             0.216167 |                          0.183098 |
| min   |                        19.58   |                                         70.39    |                                                  88.07  |                                10.85    |                          2.42     |                             1.16     |                          1.95     |
| 25%   |                        44.6075 |                                         81.9175  |                                                 255.722 |                                14.0775  |                          2.565    |                             1.7525   |                          2.1825   |
| 50%   |                        60.42   |                                         84.02    |                                                 379.725 |                                15.72    |                          2.695    |                             1.89     |                          2.3      |
| 75%   |                        94.0175 |                                         86.8275  |                                                 548.345 |                                17.435   |                          2.7875   |                             1.975    |                          2.4475   |
| max   |                       395.5    |                                         92.18    |                                                1475.78  |                                22.63    |                          2.9      |                             2.3      |                          2.68     |

#### Resultados:

| Modelo                             |   MAE (R$/L) |   RMSE (R$/L) |      R² |
|:-----------------------------------|-------------:|--------------:|--------:|
| Regressão Linear                   |       0.2814 |        0.3333 | -2.3764 |
| Random Forest                      |       0.2166 |        0.2599 | -1.0533 |
| Gradient Boosting                  |       0.2174 |        0.2675 | -1.1755 |
| Rede Neural (Rasa - 64 neurônios)  |       0.286  |        0.3616 | -2.973  |
| Rede Neural (Média - 64x32)        |       0.2521 |        0.3121 | -1.9597 |
| Rede Neural (Profunda - 128x64x32) |       0.3549 |        0.4137 | -4.2002 |
| Regressão Ridge (Penalizada)       |       0.2642 |        0.3096 | -1.913  |
| **Elastic Net**                        |       **0.2039** |        **0.246**  | **-0.8399** |
| Support Vector Regression (SVR)    |       0.254  |        0.3014 | -1.7608 |
| LightGBM (HistGradientBoosting)    |       0.2319 |        0.2833 | -1.4392 |

---
### 25% Inferiores:

#### Divisão treino/teste:

- **Treino (2023):** 24 fazendas
- **Teste (2024):** 26 fazendas

#### Distribuição dos dados de treino:

|       |   7_total_de_vacas_animais_mes |   17_vacas_em_lactacao_total_de_vacas_percentual |   13_ccs_contagem_de_celulas_somaticas_x1000_celulas_ml |   26_producao_total_de_vacas_litros_dia |   33_preco_medio_do_leite_r_litro |   34_preco_medio_do_concentrado_r_kg |   52_custo_total_do_leite_r_litro |
|:------|-------------------------------:|-------------------------------------------------:|--------------------------------------------------------:|----------------------------------------:|----------------------------------:|-------------------------------------:|----------------------------------:|
| count |                        24      |                                         24       |                                                  24     |                                24       |                         24        |                            24        |                         24        |
| mean  |                        76.3925 |                                         80.5658  |                                                 513.987 |                                13.6921  |                          2.49208  |                             2.07208  |                          3.21958  |
| std   |                       118.6    |                                          6.44853 |                                                 244.041 |                                 3.44338 |                          0.174455 |                             0.128299 |                          0.585265 |
| min   |                        12.17   |                                         69.49    |                                                 113.02  |                                 5.28    |                          2.23     |                             1.8      |                          2.42     |
| 25%   |                        29.5825 |                                         75.3575  |                                                 363.64  |                                12.35    |                          2.3575   |                             2        |                          2.815    |
| 50%   |                        35.83   |                                         81.655   |                                                 450.01  |                                13.81    |                          2.43     |                             2.09     |                          3.13     |
| 75%   |                        68.81   |                                         85.77    |                                                 652.54  |                                16.21    |                          2.6325   |                             2.1675   |                          3.355    |
| max   |                       508.42   |                                         91.16    |                                                1188.79  |                                20.47    |                          2.95     |                             2.3      |                          4.76     |

#### Distribuição dos dados de teste:

|       |   7_total_de_vacas_animais_mes |   17_vacas_em_lactacao_total_de_vacas_percentual |   13_ccs_contagem_de_celulas_somaticas_x1000_celulas_ml |   26_producao_total_de_vacas_litros_dia |   33_preco_medio_do_leite_r_litro |   34_preco_medio_do_concentrado_r_kg |   52_custo_total_do_leite_r_litro |
|:------|-------------------------------:|-------------------------------------------------:|--------------------------------------------------------:|----------------------------------------:|----------------------------------:|-------------------------------------:|----------------------------------:|
| count |                        26      |                                         26       |                                                  26     |                                26       |                         26        |                            26        |                         26        |
| mean  |                        79.7338 |                                         79.6492  |                                                 544.867 |                                13.1046  |                          2.56846  |                             1.84846  |                          2.84692  |
| std   |                        94.713  |                                          9.40453 |                                                 295.09  |                                 2.58449 |                          0.128769 |                             0.199252 |                          0.500813 |
| min   |                         8.83   |                                         58.05    |                                                 115.98  |                                 6.61    |                          2.34     |                             1.44     |                          2.32     |
| 25%   |                        31.8125 |                                         74.22    |                                                 366.455 |                                11.6725  |                          2.4925   |                             1.7525   |                          2.5      |
| 50%   |                        39.085  |                                         81.78    |                                                 462.73  |                                13.17    |                          2.56     |                             1.88     |                          2.775    |
| 75%   |                       100.145  |                                         85.5325  |                                                 657.933 |                                14.97    |                          2.6525   |                             1.9425   |                          3.0125   |
| max   |                       466.33   |                                         97.3     |                                                1274.57  |                                17.2     |                          2.8      |                             2.3      |                          4.65     |

#### Resultados:

| Modelo                             |   MAE (R$/L) |   RMSE (R$/L) |      R² |
|:-----------------------------------|-------------:|--------------:|--------:|
| Regressão Linear                   |       0.807  |        0.9324 | -2.6049 |
| Random Forest                      |       0.5406 |        0.611  | -0.5478 |
| Gradient Boosting                  |       0.5833 |        0.688  | -0.9627 |
| Rede Neural (Rasa - 64 neurônios)  |       1.1357 |        1.3844 | -6.9467 |
| Rede Neural (Média - 64x32)        |       1.0738 |        1.2643 | -5.6279 |
| Rede Neural (Profunda - 128x64x32) |       1.0572 |        1.2269 | -5.2412 |
| Regressão Ridge (Penalizada)       |       0.7949 |        0.8902 | -2.2856 |
| Elastic Net                        |       0.6391 |        0.699  | -1.0262 |
| Support Vector Regression (SVR)    |       0.5605 |        0.6498 | -0.7508 |
| **LightGBM (HistGradientBoosting)**    |       **0.5336** |        **0.6165** | **-0.5758** |