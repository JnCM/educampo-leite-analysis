# Resumo dos Testes com Seleção de Features

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
- **59_gasto_com_mao_de_obra_contratada_na_atividade_renda_bruta_da_atividade_percentual**: MinMaxScaler
- **60_gasto_com_volumoso_na_atividade_renda_bruta_da_atividade_percentual**: StandardScaler
- **61_gasto_com_concentrado_na_atividade_renda_bruta_da_atividade_percentual**: StandardScaler

## Alvo

- **52_custo_total_do_leite_r_litro**

## Escalonadores das Features

### StandardScaler

Os dados possuem uma distribuição equilibrada/próxima do normal e quase não têm valores extremos. O StandardScaler padroniza-os mantendo a sua forma natural.

### MinMaxScaler

Os dados apresentam uma leve distorção / cauda prolongada. O MinMaxScaler tranca-os entre 0 e 1 (normaliza).

### RobustScaler

Os dados possuem picos muito agudos, distribuições altamente distorcidas ou muitas fazendas com valores extremos/outliers. O RobustScaler utiliza a mediana em vez da média, ignorando esses pontos fora da curva para não estragar o modelo.

## Divisão treino/teste:

- **Treino (2023):** 484 fazendas
- **Teste (2024):** 548 fazendas

## Resultados

| Modelo                             |   MAE (R$/L) |   RMSE (R$/L) |     R² |
|:-----------------------------------|-------------:|--------------:|-------:|
| **Regressão Linear**                   |       **0.1402** |        **0.26**   | **0.7468** |
| Random Forest                      |       0.1978 |        0.3096 | 0.6409 |
| Gradient Boosting                  |       0.1703 |        0.2503 | 0.7653 |
| Rede Neural (Rasa - 64 neurônios)  |       0.1509 |        0.2437 | 0.7774 |
| Rede Neural (Média - 64x32)        |       0.1523 |        0.2448 | 0.7755 |
| **Rede Neural (Profunda - 128x64x32)** |       **0.1411** |        **0.2366** | **0.7903** |
| Regressão Ridge (Penalizada)       |       0.1486 |        0.2521 | 0.7619 |
| Elastic Net                        |       0.2434 |        0.3708 | 0.4849 |
| Support Vector Regression (SVR)    |       0.1817 |        0.3416 | 0.5628 |
| LightGBM (HistGradientBoosting)    |       0.2163 |        0.3572 | 0.522  |