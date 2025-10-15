# Introdução

Este documento detalha os critérios de aceitação para cada história de usuário do projeto Vozes em Rede, além de apresentar a priorização das funcionalidades utilizando a técnica MoSCoW. Os critérios servem como referência para validação e acompanhamento do desenvolvimento do sistema.

# Critérios de Aceitação

### US01
- O sistema coleta manifestações de pelo menos duas fontes distintas.
- A coleta é realizada de forma automatizada e periódica.

### US02
- Os textos coletados são padronizados, sem duplicidades ou caracteres especiais.
- O sistema remove ruídos e normaliza os dados antes da análise.

### US03
- O sistema agrupa manifestações em clusters temáticos automaticamente.
- Os clusters são interpretáveis e refletem temas recorrentes.

### US04
- Cada manifestação pode pertencer a mais de um cluster.
- O grau de pertencimento é apresentado de forma clara ao usuário.

### US05
- O sistema identifica o sentimento predominante (positivo, negativo, neutro) em cada manifestação.
- O sentimento é exibido junto ao tema/cluster correspondente.

### US06
- O dashboard apresenta gráficos e mapas interativos dos clusters.
- O usuário pode filtrar e explorar os dados visualmente.

### US07
- O sistema gera relatórios customizáveis com volume, temas e sentimentos.
- Os relatórios podem ser salvos e compartilhados.

### US08
- O usuário pode exportar dados e relatórios em PDF e CSV.
- Os arquivos exportados mantêm a formatação e integridade dos dados.

### US09
- O sistema é acessível em diferentes dispositivos (desktop, tablet, smartphone).
- A interface se adapta ao tamanho da tela.

### US10
- O sistema possui interface intuitiva, com navegação clara.
- O usuário consegue realizar análises sem treinamento avançado.

# Priorização (MoSCoW)

| US   | Descrição Resumida                                      | Prioridade |
|------|---------------------------------------------------------|------------|
| US01 | Coleta multicanal de manifestações                      | Must       |
| US02 | Normalização e limpeza de textos                        | Must       |
| US03 | Clusterização automática de temas                       | Must       |
| US04 | Visualização do grau de pertencimento a múltiplos temas | Should     |
| US05 | Análise de sentimento                                   | Should     |
| US06 | Dashboard interativo de clusters                        | Must       |
| US07 | Geração de relatórios customizáveis                     | Could      |
| US08 | Exportação de dados e relatórios                        | Could      |
| US09 | Acesso multiplataforma                                  | Could      |
| US10 | Interface intuitiva e fácil de usar                     | Must       |
