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

## Compost Barn + Free Stall

### 25% Superiores

#### Divisão treino/teste:

- **Treino (2023):** 41 fazendas
- **Teste (2024):** 49 fazendas

#### Distribuição dos dados de treino:

|       |   7_total_de_vacas_animais_mes |   17_vacas_em_lactacao_total_de_vacas_percentual |   13_ccs_contagem_de_celulas_somaticas_x1000_celulas_ml |   26_producao_total_de_vacas_litros_dia |   33_preco_medio_do_leite_r_litro |   34_preco_medio_do_concentrado_r_kg |   52_custo_total_do_leite_r_litro |
|:------|-------------------------------:|-------------------------------------------------:|--------------------------------------------------------:|----------------------------------------:|----------------------------------:|-------------------------------------:|----------------------------------:|
| count |                         41     |                                         41       |                                                  41     |                                41       |                         41        |                            41        |                         41        |
| mean  |                        186.165 |                                         84.4007  |                                                 317.681 |                                23.8329  |                          2.68902  |                             1.93902  |                          2.02488  |
| std   |                        163.055 |                                          4.34163 |                                                 216.846 |                                 4.96718 |                          0.120681 |                             0.264791 |                          0.173668 |
| min   |                         20.25  |                                         74.01    |                                                 125.47  |                                 9.34    |                          2.26     |                             1.03     |                          1.67     |
| 25%   |                         86.58  |                                         81.45    |                                                 176.41  |                                21.12    |                          2.64     |                             1.85     |                          1.9      |
| 50%   |                        123.67  |                                         84.6     |                                                 266.47  |                                24.92    |                          2.71     |                             1.97     |                          2.07     |
| 75%   |                        212.08  |                                         88.55    |                                                 334.02  |                                27.41    |                          2.75     |                             2.1      |                          2.15     |
| max   |                        697.17  |                                         90.67    |                                                1027.19  |                                33.74    |                          2.96     |                             2.3      |                          2.25     |

#### Distribuição dos dados de teste:

|       |   7_total_de_vacas_animais_mes |   17_vacas_em_lactacao_total_de_vacas_percentual |   13_ccs_contagem_de_celulas_somaticas_x1000_celulas_ml |   26_producao_total_de_vacas_litros_dia |   33_preco_medio_do_leite_r_litro |   34_preco_medio_do_concentrado_r_kg |   52_custo_total_do_leite_r_litro |
|:------|-------------------------------:|-------------------------------------------------:|--------------------------------------------------------:|----------------------------------------:|----------------------------------:|-------------------------------------:|----------------------------------:|
| count |                         49     |                                         49       |                                                  49     |                                49       |                         49        |                            49        |                         49        |
| mean  |                        168.395 |                                         84.7835  |                                                 281.101 |                                25.0488  |                          2.82408  |                             1.87612  |                          1.87449  |
| std   |                        149.201 |                                          3.99362 |                                                 172.801 |                                 3.96278 |                          0.109581 |                             0.245796 |                          0.211552 |
| min   |                         26.58  |                                         72.59    |                                                  81.36  |                                12.58    |                          2.56     |                             1.21     |                          1.14     |
| 25%   |                         84.33  |                                         82.56    |                                                 155.37  |                                22.68    |                          2.75     |                             1.75     |                          1.78     |
| 50%   |                        116.17  |                                         85.2     |                                                 236.12  |                                25.12    |                          2.85     |                             1.83     |                          1.89     |
| 75%   |                        197.58  |                                         87.47    |                                                 333.29  |                                27.87    |                          2.89     |                             2.03     |                          2.01     |
| max   |                        740.67  |                                         93.77    |                                                 867.83  |                                31.63    |                          3.02     |                             2.51     |                          2.23     |

#### Resultados:

| Modelo                             |   MAE (R$/L) |   RMSE (R$/L) |      R² |
|:-----------------------------------|-------------:|--------------:|--------:|
| Regressão Linear                   |       0.2326 |        0.2805 | -0.7943 |
| Random Forest                      |       0.2142 |        0.2668 | -0.6241 |
| Gradient Boosting                  |       0.2299 |        0.2778 | -0.7606 |
| Rede Neural (Rasa - 64 neurônios)  |       0.2237 |        0.2932 | -0.9615 |
| Rede Neural (Média - 64x32)        |       0.2755 |        0.336  | -1.5758 |
| Rede Neural (Profunda - 128x64x32) |       0.2452 |        0.3005 | -1.0602 |
| Regressão Ridge (Penalizada)       |       0.229  |        0.2807 | -0.7966 |
| Elastic Net                        |       0.2049 |        0.2652 | -0.6037 |
| **Support Vector Regression (SVR)**    |       **0.1772** |        **0.2297** | **-0.203**  |
| LightGBM (HistGradientBoosting)    |       0.2073 |        0.2638 | -0.5878 |

---
### 50% intermediários:

#### Divisão treino/teste:

- **Treino (2023):** 83 fazendas
- **Teste (2024):** 98 fazendas

#### Distribuição dos dados de treino:

|       |   7_total_de_vacas_animais_mes |   17_vacas_em_lactacao_total_de_vacas_percentual |   13_ccs_contagem_de_celulas_somaticas_x1000_celulas_ml |   26_producao_total_de_vacas_litros_dia |   33_preco_medio_do_leite_r_litro |   34_preco_medio_do_concentrado_r_kg |   52_custo_total_do_leite_r_litro |
|:------|-------------------------------:|-------------------------------------------------:|--------------------------------------------------------:|----------------------------------------:|----------------------------------:|-------------------------------------:|----------------------------------:|
| count |                         83     |                                         83       |                                                  83     |                                83       |                         83        |                            83        |                          83       |
| mean  |                        148.649 |                                         84.5082  |                                                 261.045 |                                23.8954  |                          2.67446  |                             2.0141   |                           2.36313 |
| std   |                        132.221 |                                          4.40325 |                                                 132.997 |                                 4.19682 |                          0.111773 |                             0.203308 |                           0.17432 |
| min   |                         17.58  |                                         71.9     |                                                  79.27  |                                13.25    |                          2.36     |                             1.21     |                           1.97    |
| 25%   |                         69.335 |                                         82.41    |                                                 176.115 |                                21.845   |                          2.615    |                             1.92     |                           2.24    |
| 50%   |                        108     |                                         85.3     |                                                 227.46  |                                24.39    |                          2.69     |                             2.05     |                           2.37    |
| 75%   |                        175.54  |                                         87.23    |                                                 295.805 |                                26.86    |                          2.74     |                             2.135    |                           2.475   |
| max   |                        681.25  |                                         94.13    |                                                 919.61  |                                33.68    |                          3.04     |                             2.53     |                           2.82    |

#### Distribuição dos dados de teste:

|       |   7_total_de_vacas_animais_mes |   17_vacas_em_lactacao_total_de_vacas_percentual |   13_ccs_contagem_de_celulas_somaticas_x1000_celulas_ml |   26_producao_total_de_vacas_litros_dia |   33_preco_medio_do_leite_r_litro |   34_preco_medio_do_concentrado_r_kg |   52_custo_total_do_leite_r_litro |
|:------|-------------------------------:|-------------------------------------------------:|--------------------------------------------------------:|----------------------------------------:|----------------------------------:|-------------------------------------:|----------------------------------:|
| count |                        98      |                                         98       |                                                  98     |                                98       |                          98       |                            98        |                         98        |
| mean  |                       166.85   |                                         85.6087  |                                                 310.371 |                                24.3556  |                           2.80031 |                             1.79378  |                          2.25531  |
| std   |                       153.093  |                                          3.95881 |                                                 195.331 |                                 4.58797 |                           0.10349 |                             0.233603 |                          0.157128 |
| min   |                        18.83   |                                         70.62    |                                                 113.06  |                                11.08    |                           2.51    |                             0.95     |                          1.9      |
| 25%   |                        71.7075 |                                         83.57    |                                                 197.55  |                                21.94    |                           2.7325  |                             1.68     |                          2.16     |
| 50%   |                       116.96   |                                         86.145   |                                                 248.235 |                                24.7     |                           2.8     |                             1.84     |                          2.24     |
| 75%   |                       203.982  |                                         88.495   |                                                 339.99  |                                27.5075  |                           2.8675  |                             1.97     |                          2.3575   |
| max   |                       729.08   |                                         91.78    |                                                1158.15  |                                35.09    |                           3.14    |                             2.28     |                          2.98     |

#### Resultados:

| Modelo                             |   MAE (R$/L) |   RMSE (R$/L) |      R² |
|:-----------------------------------|-------------:|--------------:|--------:|
| Regressão Linear                   |       0.2311 |        0.2679 | -1.9371 |
| Random Forest                      |       0.2053 |        0.2371 | -1.3007 |
| Gradient Boosting                  |       0.2091 |        0.2437 | -1.43   |
| Rede Neural (Rasa - 64 neurônios)  |       0.2934 |        0.3707 | -4.6248 |
| Rede Neural (Média - 64x32)        |       0.2663 |        0.3306 | -3.4736 |
| Rede Neural (Profunda - 128x64x32) |       0.2332 |        0.2735 | -2.0609 |
| Regressão Ridge (Penalizada)       |       0.2245 |        0.2586 | -1.7365 |
| Elastic Net                        |       0.1838 |        0.2149 | -0.8894 |
| Support Vector Regression (SVR)    |       0.1869 |        0.2212 | -1.0021 |
| **LightGBM (HistGradientBoosting)**    |       **0.1737** |        **0.2071** | **-0.7553** |

---
### 25% Inferiores:

#### Divisão treino/teste:

- **Treino (2023):** 41 fazendas
- **Teste (2024):** 49 fazendas

#### Distribuição dos dados de treino:

|       |   7_total_de_vacas_animais_mes |   17_vacas_em_lactacao_total_de_vacas_percentual |   13_ccs_contagem_de_celulas_somaticas_x1000_celulas_ml |   26_producao_total_de_vacas_litros_dia |   33_preco_medio_do_leite_r_litro |   34_preco_medio_do_concentrado_r_kg |   52_custo_total_do_leite_r_litro |
|:------|-------------------------------:|-------------------------------------------------:|--------------------------------------------------------:|----------------------------------------:|----------------------------------:|-------------------------------------:|----------------------------------:|
| count |                        41      |                                         41       |                                                  41     |                                 41      |                         41        |                            41        |                         41        |
| mean  |                       114.587  |                                         84.4015  |                                                 370.437 |                                 21.9171 |                          2.55415  |                             1.95878  |                          2.75195  |
| std   |                        93.4066 |                                          4.85277 |                                                 301.602 |                                  4.2727 |                          0.140089 |                             0.291875 |                          0.309663 |
| min   |                        23.83   |                                         73.27    |                                                 142.83  |                                 12.92   |                          2.3      |                             1.25     |                          2.32     |
| 25%   |                        54.42   |                                         81.96    |                                                 244.97  |                                 19.6    |                          2.45     |                             1.76     |                          2.58     |
| 50%   |                        95.33   |                                         84.84    |                                                 304.04  |                                 21.53   |                          2.54     |                             2        |                          2.68     |
| 75%   |                       139.42   |                                         87.35    |                                                 386.36  |                                 23.97   |                          2.65     |                             2.11     |                          2.88     |
| max   |                       536      |                                         94.08    |                                                2023.55  |                                 33.49   |                          2.88     |                             2.68     |                          3.96     |

#### Distribuição dos dados de teste:

|       |   7_total_de_vacas_animais_mes |   17_vacas_em_lactacao_total_de_vacas_percentual |   13_ccs_contagem_de_celulas_somaticas_x1000_celulas_ml |   26_producao_total_de_vacas_litros_dia |   33_preco_medio_do_leite_r_litro |   34_preco_medio_do_concentrado_r_kg |   52_custo_total_do_leite_r_litro |
|:------|-------------------------------:|-------------------------------------------------:|--------------------------------------------------------:|----------------------------------------:|----------------------------------:|-------------------------------------:|----------------------------------:|
| count |                        49      |                                         49       |                                                  49     |                                49       |                         49        |                            49        |                         49        |
| mean  |                       105.946  |                                         83.7143  |                                                 410.939 |                                21.8951  |                          2.75082  |                             1.82714  |                          2.69204  |
| std   |                        66.0924 |                                          5.51522 |                                                 307.408 |                                 5.30269 |                          0.118547 |                             0.225896 |                          0.309617 |
| min   |                        14.75   |                                         68.48    |                                                 121.2   |                                 8.54    |                          2.49     |                             1.2      |                          2.25     |
| 25%   |                        60.5    |                                         82.51    |                                                 246.14  |                                19.02    |                          2.67     |                             1.72     |                          2.51     |
| 50%   |                        91      |                                         84.14    |                                                 333.33  |                                22.04    |                          2.76     |                             1.83     |                          2.63     |
| 75%   |                       138.92   |                                         87.78    |                                                 424.33  |                                25.87    |                          2.84     |                             1.98     |                          2.76     |
| max   |                       271.75   |                                         91.78    |                                                1591.85  |                                34.11    |                          2.99     |                             2.35     |                          3.96     |

#### Resultados:

| Modelo                             |   MAE (R$/L) |   RMSE (R$/L) |      R² |
|:-----------------------------------|-------------:|--------------:|--------:|
| Regressão Linear                   |       0.2992 |        0.3483 | -0.2915 |
| **Random Forest**                      |       **0.2315** |        **0.3136** | **-0.047**  |
| Gradient Boosting                  |       0.2479 |        0.3293 | -0.1547 |
| Rede Neural (Rasa - 64 neurônios)  |       0.2324 |        0.3037 |  0.0175 |
| Rede Neural (Média - 64x32)        |       0.2469 |        0.328  | -0.1457 |
| Rede Neural (Profunda - 128x64x32) |       0.2477 |        0.3443 | -0.2621 |
| Regressão Ridge (Penalizada)       |       0.2956 |        0.3415 | -0.2415 |
| Elastic Net                        |       0.2609 |        0.3239 | -0.117  |
| Support Vector Regression (SVR)    |       0.2633 |        0.3272 | -0.1402 |
| LightGBM (HistGradientBoosting)    |       0.2584 |        0.3544 | -0.3375 |