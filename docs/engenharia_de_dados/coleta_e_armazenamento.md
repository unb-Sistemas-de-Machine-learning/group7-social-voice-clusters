# Coleta e Armazenamento de Dados

A coleta de dados é uma etapa fundamental para garantir a qualidade e a representatividade das manifestações analisadas pelo modelo de clusterização. Como a API do Fala.Br não está disponível para acesso imediato, optamos por uma estratégia de coleta automatizada, utilizando técnicas de **web scraping** para extrair dados textuais de fontes públicas relevantes.

O processo é realizado de forma contínua e automatizada, com scripts Python (utilizando bibliotecas como Scrapy ou Beautiful Soup) que acessam periodicamente sites de notícias, fóruns e canais de redes sociais. Essa abordagem garante que o volume de dados seja maximizado, mesmo diante da limitação de acesso a bases oficiais, e que o conjunto de dados reflita a diversidade de temas e opiniões presentes nas manifestações públicas.

O armazenamento dos dados é feito em um banco de dados NoSQL, especificamente o **MongoDB**. Essa escolha se deve à flexibilidade do MongoDB para lidar com dados semi-estruturados (textos e metadados variados), além de sua escalabilidade e facilidade de integração com pipelines de processamento em Python. Cada documento armazenado contém o texto da manifestação, informações sobre a fonte, data de coleta e eventuais metadados úteis para análises futuras.

Essa arquitetura permite que a coleta seja facilmente expandida para novas fontes e que o armazenamento acompanhe o crescimento do volume de dados, atendendo aos requisitos de automação, flexibilidade e robustez necessários para o projeto.

### Fontes de Dados para Web Scraping

Para a nossa estratégia de web scraping, focaremos nas seguintes fontes:

- **Reclame Aqui**: Uma fonte rica em textos de reclamações que, apesar de focar no setor privado, possui uma estrutura e um vocabulário semelhantes às manifestações de ouvidoria.
- **Fóruns e Comunidades Online**: Plataformas onde cidadãos discutem problemas urbanos e serviços públicos.
- **Canais Governamentais em Redes Sociais**: Comentários em postagens de órgãos públicos em plataformas como o Instagram e o Twitter (X).
