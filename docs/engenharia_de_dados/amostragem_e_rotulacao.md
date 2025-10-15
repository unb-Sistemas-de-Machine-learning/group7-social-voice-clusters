# Amostragem e Rotulação

## Amostragem

Devido à limitação de acesso a grandes bases oficiais, não foi possível aplicar técnicas tradicionais de amostragem probabilística. Adotamos a **amostragem por conveniência**, coletando todos os dados disponíveis nas fontes acessíveis (sites de notícias, redes sociais, fóruns). Essa abordagem visa maximizar o volume de dados para garantir que o modelo de clusterização tenha material suficiente para identificar padrões relevantes, mesmo que a representatividade estatística não seja garantida.

## Rotulação

Não foi necessário realizar rotulação manual dos dados, pois o problema abordado é de **clusterização de textos**, uma tarefa de aprendizado de máquina não-supervisionada. O próprio algoritmo (como K-Means ou DBSCAN) é responsável por identificar grupos de manifestações semelhantes, sem a necessidade de rótulos prévios. Isso simplifica o pipeline e reduz o esforço de preparação dos dados.

## Balanceamento de Classes

O conceito de balanceamento de classes não se aplica neste projeto, já que não há classes ou rótulos definidos previamente. O objetivo é justamente descobrir agrupamentos naturais nos dados, sem impor categorias artificiais. Caso, após a clusterização, seja identificada uma grande disparidade no tamanho dos clusters, isso será analisado como um resultado do próprio fenômeno social e não como um problema de modelagem.
