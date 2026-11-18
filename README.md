# Convergência de renda per capita entre os estados brasileiros (2002–2023)

Notebooks em Python (Jupyter) do Trabalho de Conclusão de Curso de Pedro Sassi, apresentado em 2026/2 ao Departamento de Economia e Relações Internacionais da Faculdade de Ciências Econômicas da Universidade Federal do Rio Grande do Sul (UFRGS), sob orientação do Prof. Dr. Sabino da Silva Pôrto Júnior.

## Notebooks

| Notebook | O que faz | Onde aparece no trabalho |
|---|---|---|
| `CONTEXTO/01_contexto.ipynb` | Crescimento da renda per capita nacional, renda relativa das regiões, participações no PIB e na população e índice de Theil | Seção 4.1 (Figuras 1 a 3 e Tabela 1) |
| `BETACONVERGENCIA/02_beta_absoluta.ipynb` | Beta-convergência absoluta e especificações de robustez | Seção 4.2.1 (Tabela 2 e Figura 4) |
| `BETACONVERGENCIA/03_beta_condicional.ipynb` | Beta-convergência condicional (especificação de Solow) e relação entre escolaridade e renda inicial | Seção 4.2.2 (Tabela 3 e Figura 5) |
| `SIGMA/04_sigma.ipynb` | Sigma-convergência (desvio-padrão do logaritmo e coeficiente de variação) | Seção 4.3 (Figura 6 e Tabela 4) |
| `QUAH/05_kernel.ipynb` | Densidades kernel da renda per capita relativa em 2002, 2012 e 2023 | Seção 4.4.1 (Figura 7) |
| `QUAH/06_markov.ipynb` | Cadeia de Markov: matriz de transição, distribuição projetada e distribuição de longo prazo | Seção 4.4.2 (Tabelas 5 e 6) |

Os notebooks são independentes entre si e podem ser executados em qualquer ordem. Cada um grava suas tabelas e figuras em uma subpasta `resultados/`, criada automaticamente.

## Dados

Os dados são públicos e foram obtidos no Ipeadata (www.ipeadata.gov.br). Eles não estão incluídos neste repositório. Para executar os notebooks, baixe as séries abaixo e salve-as na pasta `dados_usados/`, com os nomes indicados.

| Arquivo esperado em `dados_usados/` | Série (código Ipeadata) | Fonte |
|---|---|---|
| `PIBPCE_pib_estadual_per_capita_precos_2010_[17-08-2026].csv` | PIB Estadual per capita – preços de mercado (preços de 2010) (PIBPCE) | IBGE |
| `GAC_PIBCAPN_pib_per_capita_brasil_nominal_[04-11-2026].xls` | PIB per capita (GAC_PIBCAPN) | Ipea | 
| `SCN10_DIPIBG10_deflator_implicito_pib_[04-11-2026].xls` | PIB – preços de mercado – deflator implícito – variação anual (SCN10_DIPIBG10) | IBGE | 
| `PIBPMCE_pib_estadual_precos_correntes_[10-11-2026].csv` | PIB Estadual – preços de mercado (PIBPMCE) | IBGE | 
| `POP_PROJE_populacao_residente_projecao_IBGE_[10-11-2026].csv` | População residente – 1º de julho – projeção (POP_PROJE) | IBGE |
| `DINVESTE_despesa_capital_investimento_estadual_[10-11-2026].csv` | Despesa de capital – investimento e inversão financeira – empenhada – estadual (DINVESTE) | Ministério da Fazenda/STN | 
| `MEDUCA_anos_medios_estudo_25_anos_ou_mais_censo_[10-11-2026].csv` | Média de anos de estudo – pessoas 25 anos e mais (MEDUCA) | Ipea |

Nos arquivos `.csv`, a primeira linha traz o nome da série e a segunda, os rótulos `Sigla,Código,Estado` seguidos dos anos, com separador vírgula e decimal ponto. Os valores nulos de Roraima em 2010 e 2011 na série DINVESTE são tratados como dados ausentes.

## Bibliotecas

pandas, NumPy, statsmodels, SciPy e Matplotlib. A leitura dos arquivos `.xls` requer também o pacote `xlrd`.

## Observação

Os códigos foram elaborados com o apoio da ferramenta de inteligência artificial generativa Claude (Anthropic), versão Opus 5.5.
