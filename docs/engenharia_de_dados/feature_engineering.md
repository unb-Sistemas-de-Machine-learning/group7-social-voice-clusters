> **Objetivo:** Descrever as técnicas de feature engineering utilizadas.

# Feature Engineering

<!-- Listar e descrever técnicas de feature engineering aplicadas. -->
### **Pré-processamento e Tratamento de Dados**

* **Missing values:** As entradas com valores nulos serão descartadas durante a coleta.
* **Outliers:** O tratamento de outliers será feito na etapa de pré-processamento, removendo textos com tamanhos fora do padrão ou que contenham caracteres incomuns.
* **Enriquecimento dos dados:** Não foi realizado enriquecimento externo. A engenharia de features se concentra em processar o próprio texto para extrair informações relevantes para o modelo, como a tokenização e a lematização.
* **Excluir variáveis inúteis:** O foco do nosso projeto é em dados textuais. Variáveis irrelevantes, como metadados de coleta, são descartadas antes da etapa de modelagem para otimizar o processamento.
* **Normalização e padronização:** Realizamos a normalização textual no pré-processamento, convertendo o texto para minúsculas e removendo pontuações e *stop words*.
* **One Hot Encoding:** Não utilizamos One Hot Encoding. A representação numérica dos textos é feita através de **embeddings de texto**, utilizando um modelo de linguagem pré-treinado em português (**BERTimbau**), que captura o significado semântico das palavras e frases.

### **Data Augmentation**

Não foi aplicada *data augmentation* para os dados textuais. Acreditamos que a riqueza e a variedade natural da linguagem humana nos textos coletados já oferecem a diversidade necessária para que o modelo aprenda a identificar padrões de forma robusta.
