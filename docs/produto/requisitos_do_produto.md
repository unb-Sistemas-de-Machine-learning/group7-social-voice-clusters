# Requisitos do Produto

## Introdução

Este documento apresenta os requisitos funcionais e não funcionais do projeto Vozes em Rede, detalhando as capacidades essenciais e as restrições técnicas que orientam o desenvolvimento do sistema. Os requisitos foram definidos com base na visão do produto e nas necessidades identificadas para apoiar gestores públicos na análise de manifestações cidadãs por meio de clusterização e análise automatizada de dados.

## Requisitos Funcionais

| **Código** | **Nome do Requisito**        | **Descrição**                                                                                                                          |
| ---------- | ---------------------------- | -------------------------------------------------------------------------------------------------------------------------------------- |
| **RF01**   | Coleta Multicanal            | O sistema deve coletar manifestações públicas de múltiplas fontes, incluindo redes sociais, sites de notícias e canais institucionais. |
| **RF02**   | Normalização de Texto        | O sistema deve limpar e padronizar o conteúdo textual coletado, removendo ruídos, duplicidades e caracteres especiais.                 |
| **RF03**   | Classificação Automática     | O modelo deve classificar manifestações em categorias temáticas predefinidas.                       |
| **RF04**   | Análise de Sentimento        | Deve identificar e rotular o sentimento predominante em cada manifestação (positivo, negativo ou neutro).                              |
| **RF05**   | Clusterização de Tópicos     | O sistema deve agrupar manifestações semelhantes por meio de algoritmos de clusterização.                                              |
| **RF06**   | Dashboard Interativo de Clusters | O sistema deve apresentar dados e tendências de clusterização por meio de gráficos, mapas e filtros interativos.                   |
| **RF07**   | Geração de Relatórios        | Deve gerar relatórios customizáveis contendo volume, temas e emoções predominantes.                                                    |
| **RF08**   | Exportação de Dados          | Deve permitir exportar resultados e relatórios em formatos como PDF e CSV.                                                             |
| **RF09**   | Chatbot Integrado            | O sistema deve disponibilizar um chatbot para consulta rápida via Telegram ou interface web.                                           |

## Requisitos Não Funcionais

| **Código** | **Nome do Requisito**     | **Descrição**                                                                                           |
| ---------- | ------------------------- | ------------------------------------------------------------------------------------------------------- |
| **RNF01**  | Desempenho                | O sistema deve processar e exibir resultados de consultas em até 5 segundos.                            |
| **RNF02**  | Escalabilidade            | Deve suportar aumento progressivo de fontes e volume de dados sem perda de desempenho.                  |
| **RNF03**  | Conformidade com LGPD     | O sistema deve anonimizar informações pessoais e garantir conformidade com a LGPD.                      |
| **RNF04**  | Usabilidade               | A interface deve ser intuitiva, responsiva e acessível em múltiplos dispositivos.                       |
| **RNF05**  | Disponibilidade           | O sistema deve estar disponível pelo menos 99% do tempo mensal.                                         |
| **RNF06**  | Manutenibilidade          | O código deve seguir boas práticas de modularidade e documentação.                                      |
| **RNF07**  | Explicabilidade do Modelo | O sistema deve oferecer informações sobre os critérios usados pela IA em classificações e agrupamentos. |
| **RNF08**  | Portabilidade             | Deve ser executável em ambiente de nuvem pública ou privada sem dependência de hardware específico.     |
