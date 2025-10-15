> **Objetivo:** Descrever os processos de coleta e armazenamento de dados.

# Coleta e Armazenamento de Dados

<!-- Detalhar métodos e ferramentas para coleta e armazenamento de dados. -->

- A coleta de dados é justificada pela necessidade de adquirir informações textuais para a clusterização. Como a API do Fala.Br não está disponível para acesso imediato, a nossa estratégia é a coleta automatizada por meio de **web scraping**. Utilizamos bibliotecas como Scrapy ou Beautiful Soup em Python para extrair de forma contínua dados textuais de fontes públicas, como sites de notícias, fóruns e canais de redes sociais, que simulam o tipo de manifestação que gostaríamos de analisar. Para armazenamento, optamos por um banco de dados NoSQL, como o **MongoDB**, que é flexível e escalável, ideal para lidar com a natureza semi-estruturada dos textos e seus metadados.
