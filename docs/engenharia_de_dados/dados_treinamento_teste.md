# Dados de Treinamento e Teste

Para garantir a avaliação adequada do modelo de clusterização, o conjunto de dados coletado será dividido em dois subconjuntos principais:

- Holdout temporal / simulação de streaming:como os dados terão carimbo temporal, reservaremos ~10–20% (ou um período delimitado) como conjunto de teste para simular novos dados em produção.

- Amostra rotulada pequena: criaremos um conjunto rotulado de 80–200 exemplos (dependendo do total disponível) para validação extrínseca — esse conjunto será suficiente para NMI/ARI e análises qualitativas.

## Avaliação e métricas práticas:

- Métricas intrínsecas: Silhouette score e Davies-Bouldin (simples e informativas). Como a base é pequena, interpretar essas métricas junto com revisão humana.
- Métricas extrínsecas (com small labeled set): NMI e ARI para medir concordância entre clusters e rótulos humanos.
- Análise qualitativa: revisaremos manualmente o conteúdo de 5–10 exemplos por cluster para validar interpretabilidade.

