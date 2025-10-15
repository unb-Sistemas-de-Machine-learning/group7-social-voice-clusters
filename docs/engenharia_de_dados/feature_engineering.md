# Feature Engineering

O processo de feature engineering é fundamental para garantir que o modelo de clusterização trabalhe com dados limpos, relevantes e representativos. A seguir, detalhamos como cada etapa é tratada no projeto.

## Pré-processamento e Tratamento de Dados

- **Missing values:** Durante a coleta, entradas com valores nulos ou vazios são automaticamente descartadas. Isso evita que textos incompletos ou inválidos prejudiquem a qualidade do modelo.
- **Outliers:** Textos considerados outliers (muito curtos, excessivamente longos ou com caracteres incomuns) são removidos na etapa de pré-processamento. Isso garante que apenas manifestações genuínas e informativas sejam analisadas.
- **Enriquecimento dos dados:** Não realizamos enriquecimento externo (ex: cruzamento com outras bases). O foco está em extrair o máximo de informação do próprio texto, aplicando técnicas como tokenização, lematização e remoção de stopwords para preparar o dado para os embeddings.
- **Excluir variáveis inúteis:** Apenas o texto principal e metadados essenciais (data, fonte) são mantidos. Informações irrelevantes ou redundantes são descartadas antes da modelagem, otimizando o processamento e a memória.
- **Normalização e padronização:** Todo texto é convertido para minúsculas, pontuações e stopwords são removidas, e caracteres especiais são tratados. Isso padroniza a entrada e facilita a comparação semântica entre manifestações.
- **One Hot Encoding:** Não utilizamos One Hot Encoding, pois trabalhamos com dados textuais. A representação numérica dos textos é feita por meio de **embeddings de texto** (ex: BERTimbau), que capturam o significado semântico das palavras e frases, sendo mais adequados para clusterização.

## Data Augmentation

Não aplicamos técnicas de *data augmentation* para textos, pois a diversidade natural das manifestações coletadas já proporciona variação suficiente para o aprendizado do modelo. Caso o volume de dados se mostre insuficiente, poderemos reavaliar essa decisão em etapas futuras.
