---
name: relatorio_executivo
description: Escreve o memorando de recomendação de contratação de energia para a diretoria, com previsão, modelo, riscos e impacto financeiro.
---

# Relatório executivo para a diretoria

Use esta skill quando pedirem um relatório, memorando ou recomendação para a diretoria.

## Passos

1. Chame `ranking_modelos` para saber qual modelo teve o menor erro no backtest e qual foi esse erro.
2. Chame `previsao_12_meses` para obter a previsão central e o intervalo dos próximos 12 meses.
3. Chame `buscar_documentos` com "política de contratação" para conferir as regras da empresa.
4. Chame `custo_do_erro` com o erro médio do melhor modelo, em MWmed, para estimar o impacto financeiro.
5. Escreva o memorando no formato abaixo.

## Formato do memorando

- **Recomendação:** uma frase com a carga média prevista para os próximos 12 meses, em MWmed.
- **Intervalo:** o intervalo de 80%.
- **Modelo:** qual modelo foi usado e por que (erro no backtest).
- **Riscos:** dois ou três riscos, citando os documentos quando houver.
- **Impacto financeiro:** o custo estimado de um erro do tamanho do erro médio do modelo.

Seja direto: no máximo 150 palavras. Não invente números: use apenas os que as ferramentas devolverem.
