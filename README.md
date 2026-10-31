# Previsão de carga de energia com séries temporais e IA generativa

Material hands-on da aula de 4 horas do MBA FGV em IA Generativa para Negócios.

**O caso:** a Aurora Energia, uma comercializadora fictícia, precisa prever a carga mensal de energia do Sistema Interligado
Nacional (SIN) para os próximos 12 meses e recomendar à diretoria quanto contratar.

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/pgcferreira-stack/aula-series-llm-fgv/blob/main/previsao_carga_com_ia.ipynb)

## Como rodar

1. Clique no botão **Open in Colab** acima e entre com sua conta Google.
2. **Arquivo → Salvar uma cópia no Drive**.
3. **Ambiente de execução → Alterar o tipo de ambiente de execução → GPU T4 → Salvar**.
4. Rode as células de cima para baixo com **Shift + Enter**. A primeira instala as bibliotecas e baixa este repositório.

## O que tem no notebook

| Parte | Conteúdo |
|---|---|
| 1. Exploração | Tendência, sazonalidade, decomposição STL, autocorrelação, estacionariedade, relação com o IBC-Br |
| 2. Previsão | Naive sazonal, AutoETS, AutoARIMA, AutoTheta, LightGBM, Chronos-2 e TimesFM 2.5 em backtest de 12 meses |
| 3. Agente analista | LLM aberto (Qwen3-4B) com ferramentas, RAG sobre documentos e skills |
| 4. O LLM melhora a previsão? | Variáveis de eventos extraídas de texto pelo LLM; o LLM como previsor direto |

## Estrutura

- `previsao_carga_com_ia.ipynb`: o notebook
- `dados/carga_sin_mensal.csv`: carga mensal do SIN (MWmed) e IBC-Br, jan/2000 a set/2026
- `documentos/`: textos usados pelo RAG (eventos históricos, política de contratação fictícia, glossário)
- `skills/`: procedimentos do agente no formato `SKILL.md`

## Fontes e licenças

- Carga: ONS, dados abertos, [Carga de Energia Diária](https://dados.ons.org.br/dataset/carga-energia). Somamos os quatro subsistemas e tiramos a média mensal.
- IBC-Br: Banco Central do Brasil, SGS, série 24363.
- Modelos abertos do Hugging Face: [Qwen3-4B-Instruct-2507](https://huggingface.co/Qwen/Qwen3-4B-Instruct-2507), [Chronos-2](https://huggingface.co/amazon/chronos-2), [TimesFM 2.5](https://huggingface.co/google/timesfm-2.5-200m-pytorch) (Apache 2.0) e [multilingual-e5-small](https://huggingface.co/intfloat/multilingual-e5-small) (MIT).
- A Aurora Energia e sua política de contratação são fictícias.

Nenhuma conta no Hugging Face nem chave de API é necessária.
