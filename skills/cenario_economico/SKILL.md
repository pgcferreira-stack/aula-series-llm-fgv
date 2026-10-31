---
name: cenario_economico
description: Simula o efeito de um cenário de crescimento econômico sobre a carga dos próximos 12 meses.
---

# Cenário econômico

Use esta skill quando perguntarem "e se a economia crescer (ou cair) X%?".

## Passos

1. Chame `previsao_12_meses` para obter a previsão base.
2. Chame `cenario_atividade` com a variação do IBC-Br perguntada, em porcentagem.
3. Chame `custo_do_erro` com a diferença de carga entre o cenário e a previsão base, para traduzir em reais.
4. Responda com: a carga média do cenário, a diferença em relação à base (em MWmed e em %), e o impacto financeiro de não ajustar os contratos.

Explique que a sensibilidade vem de uma relação histórica simples (elasticidade) e que não captura choques como racionamentos ou pandemias.
