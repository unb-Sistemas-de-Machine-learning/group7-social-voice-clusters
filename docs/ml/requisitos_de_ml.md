# Requisitos de Machine Learning

## Introdução

Esta seção apresenta os requisitos funcionais e não funcionais do(s) modelo(s) de machine learning do projeto Vozes em Rede, com base no planejamento realizado no ML Canva. O foco é garantir entregáveis viáveis, priorizando a clusterização de manifestações públicas e a geração de insights temáticos para gestores.

## Requisitos Funcionais

| **Código** | **Nome do Requisito**           | **Descrição**                                                                                       |
| ---------- | ------------------------------- | --------------------------------------------------------------------------------------------------- |
| **RMF01**  | Clusterização Semântica         | O modelo deve agrupar manifestações públicas em clusters temáticos de acordo com similaridade textual.|
| **RMF02**  | Classificação Multitemática     | Cada manifestação pode pertencer a múltiplos clusters, com indicação do grau de pertencimento.       |
| **RMF03**  | Processamento de Texto Bruto    | O pipeline deve aceitar textos brutos como entrada, realizando pré-processamento básico.             |
| **RMF04**  | Avaliação Periódica do Modelo   | O modelo deve ser reavaliado periodicamente e refeito caso a acurácia caia abaixo de 80%.           |
| **RMF05**  | Geração de Dashboards de Clusters | Os resultados da clusterização devem ser apresentados em dashboards interativos para o usuário.     |
| **RMF06**  | Simulação de Impacto            | O sistema deve permitir simular critérios de aceitação/veracidade usando modelos auxiliares.         |

## Requisitos Não Funcionais

| **Código** | **Nome do Requisito**     | **Descrição**                                                                                       |
| ---------- | ------------------------- | --------------------------------------------------------------------------------------------------- |
| **RMNF01** | Tempo de Processamento    | O pipeline de clusterização deve processar lotes de dados em até 5 minutos.                         |
| **RMNF02** | Modularidade              | O código do pipeline deve ser modular, facilitando ajustes e reuso de componentes.                  |
| **RMNF03** | Explicabilidade           | O sistema deve fornecer informações sobre os critérios usados para agrupar manifestações.            |
| **RMNF04** | Reprodutibilidade         | Os experimentos de clusterização devem ser reprodutíveis, com controle de versões e random seeds.   |
| **RMNF05** | Portabilidade             | O pipeline deve ser executável em ambiente local ou nuvem, sem dependências proprietárias.           |

## Métricas de Sucesso

- **F1-score**: O modelo deve atingir F1-score mínimo de 0,80 na avaliação de agrupamento temático.
- **Acurácia de Clusterização**: A taxa de acerto do modelo (validação manual ou por modelo auxiliar) deve ser superior a 80%.
- **Cobertura Temática**: O modelo deve identificar pelo menos 80% dos temas relevantes presentes no conjunto de dados.
