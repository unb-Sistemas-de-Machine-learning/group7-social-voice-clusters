> **Objetivo:** Descrever os processos de amostragem e rotulação de dados.

# Amostragem e Rotulação

<!-- Detalhar processos de amostragem e rotulação de dados. -->
### **Amostragem**

Não foi aplicada uma técnica de amostragem tradicional. Devido ao baixo volume de dados acessíveis nas fontes alternativas, a estratégia adotada é a de **amostragem por conveniência**. Coletamos todos os dados disponíveis nas fontes para garantir um volume significativo o suficiente para o treinamento do modelo de clusterização.

### **Rotulação**

Não foi necessário rotular os dados. O problema de IA que estamos resolvendo é a **clusterização de textos**, que é uma técnica de aprendizado de máquina não-supervisionada. Isso significa que o próprio algoritmo, ao encontrar semelhanças entre os textos, irá agrupar as manifestações em "tópicos" que ele mesmo descobre.

### **Balanceamento de Classes**

O projeto não lida com balanceamento de classes. Como o modelo é de aprendizado não-supervisionado e não utiliza rótulos pré-definidos, o conceito de balanceamento não se aplica.
