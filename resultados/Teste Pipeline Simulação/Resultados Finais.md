# Resumo dos Testes do Pipeline do Simulador

## Modelagem por Grupo
### Grupo inferior

| Modelo                             |   MAE (R$/L) |   RMSE (R$/L) |      R² |
|:-----------------------------------|-------------:|--------------:|--------:|
| Regressão Linear                   |       0.3409 |        0.4797 |  0.1378 |
| Random Forest                      |       0.305  |        0.4216 |  0.3343 |
| Gradient Boosting                  |       0.3168 |        0.4184 |  0.3441 |
| Rede Neural (Rasa - 64 neurônios)  |       0.7859 |        0.8738 | -1.8607 |
| Rede Neural (Média - 64x32)        |       0.3991 |        0.5437 | -0.1076 |
| Rede Neural (Profunda - 128x64x32) |       0.3393 |        0.4635 |  0.1951 |
| Regressão Ridge (Penalizada)       |       0.3251 |        0.4411 |  0.2711 |
| Elastic Net                        |       0.3514 |        0.4809 |  0.1336 |
| Support Vector Regression (SVR)    |       0.3285 |        0.4811 |  0.133  |
| LightGBM (HistGradientBoosting)    |       0.3554 |        0.4975 |  0.0729 |

### Intermediário

| Modelo                             |   MAE (R$/L) |   RMSE (R$/L) |      R² |
|:-----------------------------------|-------------:|--------------:|--------:|
| Regressão Linear                   |       0.3394 |        0.4776 |  0.1455 |
| Random Forest                      |       0.3047 |        0.4208 |  0.3366 |
| Gradient Boosting                  |       0.3074 |        0.4148 |  0.3553 |
| Rede Neural (Rasa - 64 neurônios)  |       0.5927 |        0.7144 | -0.9121 |
| Rede Neural (Média - 64x32)        |       0.3423 |        0.4682 |  0.1788 |
| Rede Neural (Profunda - 128x64x32) |       0.3501 |        0.4726 |  0.1632 |
| Regressão Ridge (Penalizada)       |       0.3238 |        0.4384 |  0.2801 |
| Elastic Net                        |       0.3496 |        0.4796 |  0.1382 |
| Support Vector Regression (SVR)    |       0.3365 |        0.4867 |  0.1125 |
| LightGBM (HistGradientBoosting)    |       0.3473 |        0.4904 |  0.0991 |

### Superior

| Modelo                             |   MAE (R$/L) |   RMSE (R$/L) |      R² |
|:-----------------------------------|-------------:|--------------:|--------:|
| Regressão Linear                   |       0.3184 |        0.4602 |  0.2066 |
| Random Forest                      |       0.3077 |        0.425  |  0.3235 |
| Gradient Boosting                  |       0.3124 |        0.415  |  0.3548 |
| Rede Neural (Rasa - 64 neurônios)  |       0.3975 |        0.5374 | -0.0818 |
| Rede Neural (Média - 64x32)        |       0.6827 |        0.8119 | -1.4697 |
| Rede Neural (Profunda - 128x64x32) |       0.4899 |        0.6063 | -0.377  |
| Regressão Ridge (Penalizada)       |       0.2987 |        0.4201 |  0.3387 |
| Elastic Net                        |       0.3427 |        0.4747 |  0.1557 |
| Support Vector Regression (SVR)    |       0.3373 |        0.489  |  0.1043 |
| LightGBM (HistGradientBoosting)    |       0.3487 |        0.4922 |  0.0923 |


## Modelagem agregando todos os grupos em uma base de dados só

| Modelo                             |   MAE (R$/L) |   RMSE (R$/L) |      R² |
|:-----------------------------------|-------------:|--------------:|--------:|
| Regressão Linear                   |       0.3779 |        0.464  |  0.1935 |
| Random Forest                      |       0.2172 |        0.3269 |  0.5996 |
| Gradient Boosting                  |       0.1963 |        0.3017 |  0.659  |
| Rede Neural (Rasa - 64 neurônios)  |       0.4451 |        0.5279 | -0.0441 |
| Rede Neural (Média - 64x32)        |       0.3542 |        0.4478 |  0.2486 |
| Rede Neural (Profunda - 128x64x32) |       0.2306 |        0.3254 |  0.6034 |
| Regressão Ridge (Penalizada)       |       0.3956 |        0.4649 |  0.1904 |
| Elastic Net                        |       0.2275 |        0.3727 |  0.4797 |
| Support Vector Regression (SVR)    |       0.2201 |        0.3755 |  0.4719 |
| LightGBM (HistGradientBoosting)    |       0.2168 |        0.3472 |  0.5483 |

## Modelagem agregando todos os grupos em uma base e os identificado como feature

| Modelo                             |   MAE (R$/L) |   RMSE (R$/L) |     R² |
|:-----------------------------------|-------------:|--------------:|-------:|
| Regressão Linear                   |       0.4317 |        0.5142 | 0.0096 |
| Random Forest                      |       0.1898 |        0.2917 | 0.6812 |
| **Gradient Boosting**                  |       **0.1789** |        **0.2822** | **0.7017** |
| Rede Neural (Rasa - 64 neurônios)  |       0.3057 |        0.3858 | 0.4423 |
| Rede Neural (Média - 64x32)        |       0.2605 |        0.3399 | 0.5671 |
| Rede Neural (Profunda - 128x64x32) |       0.2159 |        0.3163 | 0.6252 |
| Regressão Ridge (Penalizada)       |       0.4013 |        0.4702 | 0.1718 |
| Elastic Net                        |       0.2255 |        0.3611 | 0.5114 |
| Support Vector Regression (SVR)    |       0.2179 |        0.371  | 0.4844 |
| LightGBM (HistGradientBoosting)    |       0.2148 |        0.3457 | 0.5524 |

## Modelagem agregando todos os grupos em uma base, os identificado como feature e uso do percentual de gasto de concentrado como sendo a média do grupo em cada sistema

| Modelo                             |   MAE (R$/L) |   RMSE (R$/L) |      R² |
|:-----------------------------------|-------------:|--------------:|--------:|
| Regressão Linear                   |       0.4079 |        0.4858 |  0.1158 |
| Random Forest                      |       0.1924 |        0.303  |  0.656  |
| **Gradient Boosting**                  |       **0.183**  |        **0.295**  |  **0.6739** |
| Rede Neural (Rasa - 64 neurônios)  |       0.5216 |        0.5894 | -0.3015 |
| Rede Neural (Média - 64x32)        |       0.3621 |        0.4387 |  0.2789 |
| Rede Neural (Profunda - 128x64x32) |       0.2444 |        0.3385 |  0.5707 |
| Regressão Ridge (Penalizada)       |       0.3516 |        0.4215 |  0.3343 |
| Elastic Net                        |       0.2255 |        0.3611 |  0.5114 |
| Support Vector Regression (SVR)    |       0.2379 |        0.4013 |  0.3967 |
| LightGBM (HistGradientBoosting)    |       0.2291 |        0.3732 |  0.4782 |