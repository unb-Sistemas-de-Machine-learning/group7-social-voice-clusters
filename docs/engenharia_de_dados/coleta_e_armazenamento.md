# Coleta e Armazenamento de Dados

A coleta de dados é uma etapa fundamental para garantir a qualidade e a representatividade das manifestações analisadas pelo modelo de clusterização. Como a API do Fala.Br não está disponível para acesso imediato, optamos por uma estratégia de coleta automatizada, utilizando técnicas de **web scraping** para extrair dados textuais de fontes públicas relevantes.

O processo é realizado de forma automatizada, com scrapers Python que acessam sites de notícias, fóruns e canais de redes sociais. Cada scraper envia os registros coletados para o serviço central de ingestão via HTTP (`POST /ingest`) ou — em cenários offline ou especializados — escreve diretamente no MongoDB usando `pymongo`.

Observação importante sobre volume: este projeto NÃO pretende coletar grandes massas de dados. O objetivo é obter um conjunto enxuto e de qualidade, entre 100 e 300 manifestações, e construir um modelo eficiente e interpretável a partir desse volume. 

## Armazenamento e esquema pretendido (MongoDB)

- Banco: `vozes_em_rede`
- Coleção `raw_manifestacoes` — documentos brutos recebidos da coleta. Campos pretendidos:
	- `_id` (ObjectId)
	- `texto` (string)
	- `fonte` (string)
	- `url` (string)
	- `id_origem` (string)
	- `metadata` (object)
	- `timestamp_coleta` (datetime)
	- `status` (string) — ex.: `raw`, `processing`, `processed`, `error`

- Coleção `processed_manifestacoes` — documentos resultantes do pré-processamento e enriquecimento. Campos pretendidos:
	- `raw_id` (ObjectId) — referência ao documento em `raw_manifestacoes`
	- `texto` (string) — versão limpa/normalizada
	- `embedding` (array[float] ou referência para vector-db)
	- `sentiment` (string) — opcional
	- `topic_tags` (array[string]) — opcional, a partir de heurísticas
	- `status` (string)

Essa organização separa claramente a fonte original (`raw_manifestacoes`) do dado pronto para modelagem (`processed_manifestacoes`), facilitando reprocessamentos e auditoria.

## Fontes de Dados para Web Scraping

Para a nossa estratégia de web scraping, focaremos nas seguintes fontes:

- **Reclame Aqui**: Uma fonte rica em textos de reclamações que, apesar de focar no setor privado, possui uma estrutura e um vocabulário semelhantes às manifestações de ouvidoria.
- **Fóruns e Comunidades Online**: Plataformas onde cidadãos discutem problemas urbanos e serviços públicos.
- **Canais Governamentais em Redes Sociais**: Comentários em postagens de órgãos públicos em plataformas como o Instagram e o Twitter (X).
