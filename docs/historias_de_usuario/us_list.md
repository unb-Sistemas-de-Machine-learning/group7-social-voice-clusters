
# Histórias de Usuário

## Introdução
Este documento apresenta as histórias de usuário do projeto Vozes em Rede, organizadas em épicos. Cada história descreve, do ponto de vista do usuário, as principais funcionalidades e necessidades do sistema, servindo de base para o desenvolvimento e validação do produto.


## Épico 1: Coleta e Preparação de Dados

**US01**
Como gestor público, eu quero que o sistema colete manifestações de diferentes fontes (redes sociais, sites de notícias, canais institucionais), para que eu tenha uma base de dados ampla e atualizada para análise.

*Requisitos Relacionados:* RF01, RMF03

**US02**
Como analista de dados, eu quero que o sistema normalize e limpe os textos coletados, para garantir que as análises sejam feitas sobre dados padronizados e sem ruídos.

*Requisitos Relacionados:* RF02, RMF03


## Épico 2: Clusterização e Análise Temática

**US03**
Como gestor público, eu quero que o sistema agrupe manifestações em clusters temáticos automaticamente, para identificar padrões e temas recorrentes nas demandas da população.

*Requisitos Relacionados:* RF05, RMF01, RMF02, RMF04, RMF05

**US04**
Como analista de dados, eu quero visualizar o grau de pertencimento de cada manifestação a múltiplos clusters, para compreender a complexidade e a sobreposição de temas em cada mensagem.

*Requisitos Relacionados:* RMF02, RMF05

**US05**
Como gestor público, eu quero que o sistema identifique e rotule o sentimento predominante em cada manifestação, para avaliar o tom geral das demandas e opiniões recebidas.

*Requisitos Relacionados:* RF04


## Épico 3: Visualização e Relatórios

**US06**
Como gestor público, eu quero acessar dashboards interativos com gráficos e mapas dos clusters formados, para acompanhar tendências e tomar decisões baseadas em evidências.

*Requisitos Relacionados:* RF06, RMF05, RNF04

**US07**
Como gestor público, eu quero gerar relatórios customizáveis sobre volume, temas e sentimentos das manifestações, para compartilhar análises com outros setores e apoiar a formulação de políticas.

*Requisitos Relacionados:* RF07

**US08**
Como gestor público, eu quero exportar os dados e relatórios em formatos como PDF e CSV, para facilitar o armazenamento e o compartilhamento das informações.

*Requisitos Relacionados:* RF08


## Épico 4: Acesso e Usabilidade

**US09**
Como gestor público, eu quero acessar o sistema de diferentes dispositivos, para poder acompanhar as análises mesmo fora do ambiente de trabalho.

*Requisitos Relacionados:* RNF04, RNF08

**US10**
Como analista de dados, eu quero que o sistema seja intuitivo e fácil de usar, para que eu possa realizar análises sem necessidade de treinamento avançado.

*Requisitos Relacionados:* RNF04, RNF06
