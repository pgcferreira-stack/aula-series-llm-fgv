---
name: analise_de_evento
description: Explica por que a carga se comportou de forma anormal em um período, ligando os dados aos eventos históricos documentados.
---

# Análise de evento

Use esta skill quando perguntarem por que a carga caiu, subiu ou fugiu do padrão em algum período.

## Passos

1. Chame `maiores_desvios` para ver os meses com maior desvio em relação ao padrão esperado.
2. Para o período perguntado, chame `buscar_documentos` com uma descrição do período (por exemplo, "queda de carga em 2020").
3. Responda em três partes:
   - **O que os dados mostram:** o tamanho do desvio, em porcentagem, e quando começou e terminou.
   - **A explicação:** o evento que explica o desvio, citando o documento.
   - **O que isso significa para a previsão:** se o efeito é temporário (um choque que passa) ou permanente (uma quebra de nível), e se o modelo deveria tratar esse período de forma especial.

Se nenhum documento explicar o desvio, diga isso claramente em vez de inventar uma causa.
