# Dados de Treinamento e Teste

Para garantir a avaliação adequada do modelo de clusterização, o conjunto de dados coletado será dividido em dois subconjuntos principais:

- **Conjunto de Treinamento:** Utilizado para ajustar e treinar o modelo de clusterização (como K-Means ou DBSCAN). O modelo aprende a identificar padrões e agrupar manifestações semelhantes com base nesse conjunto.
- **Conjunto de Teste:** Reservado para simular a chegada de novas manifestações e validar a capacidade do modelo de atribuir corretamente cada texto ao cluster mais apropriado. Essa validação é fundamental para medir a robustez e a generalização do modelo.

A divisão dos dados será feita de forma estratificada, sempre que possível, para garantir que a diversidade temática presente no conjunto total seja refletida em ambos os subconjuntos. Como o problema é não-supervisionado, a avaliação será feita por meio de métricas como F1-score, acurácia de clusterização e análise qualitativa dos agrupamentos.
