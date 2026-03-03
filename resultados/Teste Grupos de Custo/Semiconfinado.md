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

## Semiconfinado

### 25% Superiores:

#### Divisão treino/teste:

- **Treino (2023):** 55 fazendas
- **Teste (2024):** 61 fazendas

#### Distribuição dos dados de treino:

|       |   7_total_de_vacas_animais_mes |   17_vacas_em_lactacao_total_de_vacas_percentual |   13_ccs_contagem_de_celulas_somaticas_x1000_celulas_ml |   26_producao_total_de_vacas_litros_dia |   33_preco_medio_do_leite_r_litro |   34_preco_medio_do_concentrado_r_kg |   52_custo_total_do_leite_r_litro |
|:------|-------------------------------:|-------------------------------------------------:|--------------------------------------------------------:|----------------------------------------:|----------------------------------:|-------------------------------------:|----------------------------------:|
| count |                        55      |                                         55       |                                                  55     |                                55       |                         55        |                            55        |                         55        |
| mean  |                        77.356  |                                         75.6836  |                                                 531.932 |                                11.9273  |                          2.56691  |                             2.07709  |                          3.06673  |
| std   |                        59.4966 |                                          8.93843 |                                                 293.652 |                                 3.73505 |                          0.862664 |                             0.306169 |                          0.749817 |
| min   |                        13.5    |                                         54.88    |                                                   0     |                                 3.77    |                          2.08     |                             1.16     |                          2.57     |
| 25%   |                        38.42   |                                         70.43    |                                                 326.815 |                                 8.86    |                          2.315    |                             1.925    |                          2.71     |
| 50%   |                        56.75   |                                         77.35    |                                                 445.78  |                                11.73    |                          2.43     |                             2.14     |                          2.85     |
| 75%   |                        92.875  |                                         81.94    |                                                 684.835 |                                14.21    |                          2.59     |                             2.285    |                          3.095    |
| max   |                       272.5    |                                         92.95    |                                                1392.05  |                                21.12    |                          8.72     |                             2.66     |                          7.63     |

#### Distribuição dos dados de teste:

|       |   7_total_de_vacas_animais_mes |   17_vacas_em_lactacao_total_de_vacas_percentual |   13_ccs_contagem_de_celulas_somaticas_x1000_celulas_ml |   26_producao_total_de_vacas_litros_dia |   33_preco_medio_do_leite_r_litro |   34_preco_medio_do_concentrado_r_kg |   52_custo_total_do_leite_r_litro |
|:------|-------------------------------:|-------------------------------------------------:|--------------------------------------------------------:|----------------------------------------:|----------------------------------:|-------------------------------------:|----------------------------------:|
| count |                        61      |                                          61      |                                                  61     |                                61       |                         61        |                            61        |                         61        |
| mean  |                        68.522  |                                          73.189  |                                                 663.452 |                                10.3502  |                          2.69344  |                             1.94098  |                          3.13377  |
| std   |                        47.2663 |                                          10.9535 |                                                 364.044 |                                 3.73832 |                          0.954014 |                             0.284076 |                          0.805939 |
| min   |                        15.17   |                                          39.11   |                                                   0     |                                 2.91    |                          2.23     |                             1.17     |                          2.62     |
| 25%   |                        36.67   |                                          68.78   |                                                 421.08  |                                 7.38    |                          2.47     |                             1.74     |                          2.73     |
| 50%   |                        58      |                                          74.3    |                                                 560.29  |                                 9.96    |                          2.56     |                             2        |                          2.84     |
| 75%   |                        81      |                                          81.07   |                                                 748.21  |                                13.11    |                          2.67     |                             2.14     |                          3.21     |
| max   |                       226.67   |                                          90.56   |                                                1680.62  |                                18.69    |                          9.91     |                             2.43     |                          6.98     |

#### Resultados:

| Modelo                             |   MAE (R$/L) |   RMSE (R$/L) |     R² |
|:-----------------------------------|-------------:|--------------:|-------:|
| Regressão Linear                   |       0.4613 |        0.6171 | 0.4039 |
| **Random Forest**                      |       **0.3737** |        **0.5923** | **0.4509** |
| Gradient Boosting                  |       0.3786 |        0.5737 | 0.4849 |
| Rede Neural (Rasa - 64 neurônios)  |       0.4181 |        0.6212 | 0.3959 |
| Rede Neural (Média - 64x32)        |       0.4219 |        0.6134 | 0.4111 |
| Rede Neural (Profunda - 128x64x32) |       0.3992 |        0.6232 | 0.3922 |
| Regressão Ridge (Penalizada)       |       0.4496 |        0.6324 | 0.374  |
| Elastic Net                        |       0.4264 |        0.6428 | 0.3532 |
| Support Vector Regression (SVR)    |       0.4213 |        0.7255 | 0.1761 |
| LightGBM (HistGradientBoosting)    |       0.4836 |        0.7438 | 0.1341 |

---
### 50% Intermediários:

#### Divisão treino/teste:

- **Treino (2023):** 111 fazendas
- **Teste (2024):** 124 fazendas

#### Distribuição dos dados de treino:

|       |   7_total_de_vacas_animais_mes |   17_vacas_em_lactacao_total_de_vacas_percentual |   13_ccs_contagem_de_celulas_somaticas_x1000_celulas_ml |   26_producao_total_de_vacas_litros_dia |   33_preco_medio_do_leite_r_litro |   34_preco_medio_do_concentrado_r_kg |   52_custo_total_do_leite_r_litro |
|:------|-------------------------------:|-------------------------------------------------:|--------------------------------------------------------:|----------------------------------------:|----------------------------------:|-------------------------------------:|----------------------------------:|
| count |                       111      |                                        111       |                                                 111     |                               111       |                        111        |                           111        |                         111       |
| mean  |                        87.1721 |                                         76.9096  |                                                 483.158 |                                12.6781  |                          2.46784  |                             2.0318   |                           2.28559 |
| std   |                        67.3771 |                                          8.86645 |                                                 213.547 |                                 3.74747 |                          0.161191 |                             0.272231 |                           0.13212 |
| min   |                        15.58   |                                         39.79    |                                                   0     |                                 4.62    |                          1.96     |                             0.88     |                           2.08    |
| 25%   |                        44.67   |                                         72.54    |                                                 341.26  |                                10.155   |                          2.35     |                             1.905    |                           2.17    |
| 50%   |                        71      |                                         78.95    |                                                 428.45  |                                12.71    |                          2.46     |                             2.09     |                           2.27    |
| 75%   |                       107.335  |                                         82.535   |                                                 588.665 |                                15.43    |                          2.575    |                             2.195    |                           2.395   |
| max   |                       443.75   |                                         91.3     |                                                1186.49  |                                21.52    |                          2.86     |                             2.52     |                           2.53    |

#### Distribuição dos dados de teste:

|       |   7_total_de_vacas_animais_mes |   17_vacas_em_lactacao_total_de_vacas_percentual |   13_ccs_contagem_de_celulas_somaticas_x1000_celulas_ml |   26_producao_total_de_vacas_litros_dia |   33_preco_medio_do_leite_r_litro |   34_preco_medio_do_concentrado_r_kg |   52_custo_total_do_leite_r_litro |
|:------|-------------------------------:|-------------------------------------------------:|--------------------------------------------------------:|----------------------------------------:|----------------------------------:|-------------------------------------:|----------------------------------:|
| count |                       124      |                                        124       |                                                 124     |                               124       |                        124        |                           124        |                        124        |
| mean  |                        85.3734 |                                         78.8927  |                                                 582.052 |                                13.221   |                          2.6125   |                             1.90298  |                          2.28452  |
| std   |                        70.7688 |                                          6.69985 |                                                 315.115 |                                 3.47466 |                          0.149382 |                             0.264716 |                          0.166716 |
| min   |                        15.17   |                                         56.26    |                                                   0     |                                 3.96    |                          2.15     |                             0.82     |                          2.03     |
| 25%   |                        41.6475 |                                         74.6375  |                                                 350.523 |                                10.85    |                          2.53     |                             1.78     |                          2.13     |
| 50%   |                        65.455  |                                         80.16    |                                                 509.015 |                                12.95    |                          2.64     |                             1.935    |                          2.255    |
| 75%   |                       100.332  |                                         83.3575  |                                                 746.58  |                                15.315   |                          2.7125   |                             2.0625   |                          2.425    |
| max   |                       471.83   |                                         92.66    |                                                1700.07  |                                28.35    |                          2.96     |                             2.42     |                          2.61     |

#### Resultados:

| Modelo                             |   MAE (R$/L) |   RMSE (R$/L) |      R² |
|:-----------------------------------|-------------:|--------------:|--------:|
| Regressão Linear                   |       0.1522 |        0.1816 | -0.1965 |
| Random Forest                      |       0.1376 |        0.1602 |  0.0689 |
| Gradient Boosting                  |       0.1411 |        0.1655 |  0.006  |
| Rede Neural (Rasa - 64 neurônios)  |       0.1544 |        0.1866 | -0.2636 |
| **Rede Neural (Média - 64x32)**        |       **0.1316** |        **0.16**   |  **0.0714** |
| Rede Neural (Profunda - 128x64x32) |       0.1513 |        0.1846 | -0.2362 |
| Regressão Ridge (Penalizada)       |       0.1461 |        0.1695 | -0.0415 |
| Elastic Net                        |       0.1446 |        0.166  | -0      |
| Support Vector Regression (SVR)    |       0.147  |        0.1688 | -0.033  |
| LightGBM (HistGradientBoosting)    |       0.1419 |        0.1661 | -0.0003 |

---
### 25% Inferiores:

#### Divisão treino/teste:

- **Treino (2023):** 55 fazendas
- **Teste (2024):** 61 fazendas

#### Distribuição dos dados de treino:

|       |   7_total_de_vacas_animais_mes |   17_vacas_em_lactacao_total_de_vacas_percentual |   13_ccs_contagem_de_celulas_somaticas_x1000_celulas_ml |   26_producao_total_de_vacas_litros_dia |   33_preco_medio_do_leite_r_litro |   34_preco_medio_do_concentrado_r_kg |   52_custo_total_do_leite_r_litro |
|:------|-------------------------------:|-------------------------------------------------:|--------------------------------------------------------:|----------------------------------------:|----------------------------------:|-------------------------------------:|----------------------------------:|
| count |                        55      |                                          55      |                                                  55     |                                 55      |                         55        |                            55        |                          55       |
| mean  |                        74.1829 |                                          78.0342 |                                                 555.9   |                                 12.3813 |                          2.44036  |                             2.04473  |                           1.86818 |
| std   |                        55.7705 |                                           8.8938 |                                                 295.074 |                                  3.6831 |                          0.159652 |                             0.188384 |                           0.21496 |
| min   |                        17.75   |                                          47.23   |                                                 175.67  |                                  4.48   |                          2.02     |                             1.41     |                           1.18    |
| 25%   |                        39.75   |                                          73.725  |                                                 351.785 |                                  9.895  |                          2.345    |                             1.945    |                           1.78    |
| 50%   |                        58.83   |                                          79.07   |                                                 448.75  |                                 12.5    |                          2.43     |                             2.07     |                           1.96    |
| 75%   |                        81.875  |                                          83.765  |                                                 725.955 |                                 15.025  |                          2.555    |                             2.175    |                           2.02    |
| max   |                       286.75   |                                          96.58   |                                                1467.4   |                                 20.73   |                          2.76     |                             2.48     |                           2.07    |

#### Distribuição dos dados de teste:

|       |   7_total_de_vacas_animais_mes |   17_vacas_em_lactacao_total_de_vacas_percentual |   13_ccs_contagem_de_celulas_somaticas_x1000_celulas_ml |   26_producao_total_de_vacas_litros_dia |   33_preco_medio_do_leite_r_litro |   34_preco_medio_do_concentrado_r_kg |   52_custo_total_do_leite_r_litro |
|:------|-------------------------------:|-------------------------------------------------:|--------------------------------------------------------:|----------------------------------------:|----------------------------------:|-------------------------------------:|----------------------------------:|
| count |                        61      |                                         61       |                                                  61     |                                61       |                          61       |                            61        |                          61       |
| mean  |                        76.8434 |                                         78.7444  |                                                 433.419 |                                13.1156  |                           2.59918 |                             1.86934  |                           1.81754 |
| std   |                        56.2406 |                                          9.56288 |                                                 207.11  |                                 3.66818 |                           0.12473 |                             0.199532 |                           0.1885  |
| min   |                        14.25   |                                         38.61    |                                                   0     |                                 4.19    |                           2.38    |                             1.29     |                           1.25    |
| 25%   |                        41.42   |                                         75.23    |                                                 285.4   |                                10.74    |                           2.5     |                             1.75     |                           1.73    |
| 50%   |                        58.83   |                                         81.53    |                                                 393.92  |                                13.02    |                           2.61    |                             1.87     |                           1.89    |
| 75%   |                        90.67   |                                         85.37    |                                                 540.67  |                                15.12    |                           2.69    |                             1.99     |                           1.97    |
| max   |                       274.67   |                                         94.03    |                                                1084.1   |                                25.9     |                           2.86    |                             2.3      |                           2.03    |

#### Resultados:

| Modelo                             |   MAE (R$/L) |   RMSE (R$/L) |      R² |
|:-----------------------------------|-------------:|--------------:|--------:|
| Regressão Linear                   |       0.1564 |        0.1984 | -0.1264 |
| Random Forest                      |       0.1608 |        0.2149 | -0.3214 |
| Gradient Boosting                  |       0.1685 |        0.2193 | -0.3762 |
| Rede Neural (Rasa - 64 neurônios)  |       0.2019 |        0.253  | -0.8311 |
| Rede Neural (Média - 64x32)        |       0.1984 |        0.2534 | -0.8373 |
| Rede Neural (Profunda - 128x64x32) |       0.1664 |        0.2222 | -0.4125 |
| Regressão Ridge (Penalizada)       |       0.1507 |        0.1968 | -0.1077 |
| **Elastic Net**                        |       **0.1449** |        **0.1952** | **-0.0903** |
| Support Vector Regression (SVR)    |       0.1528 |        0.1989 | -0.1319 |
| LightGBM (HistGradientBoosting)    |       0.155  |        0.2152 | -0.3256 |