🛒 Análise do E-Commerce Brasileiro (Olist)
Este repositório contém a análise exploratória de dados (EDA) desenvolvida para avaliar o desempenho operacional, logístico e a satisfação dos clientes no e-commerce brasileiro.

🔗 Dataset Utilizado
Dataset: [Brazilian E-Commerce Public Dataset by Olist](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce)

📌 Resumo do que foi desenvolvido nos Notebooks

O objetivo do projeto foi integrar múltiplas bases de dados relacionais da Olist, realizar a limpeza e preparação dos dados, construir métricas de desempenho (KPIs) e analisar o perfil de avaliação dos consumidores.

1. Importação e Unificação dos Dados

  - Carga de Datasets: Leitura dos arquivos de pedidos (orders), avaliações (reviews), itens de pedidos (order_items), produtos (products) e tradução das categorias.
  - Tradução de Categorias: Cruzamento dos nomes de categorias em português com a tabela de tradução para inglês.
  - Consolidação em Tabela Única: Junção (merge) relacional das tabelas para criar uma base unificada para análise.

2. Tratamento e Limpeza

   - Conversão Temporal: Mapeamento e transformação das colunas de datas (order_purchase_timestamp, order_delivered_customer_date, order_estimated_delivery_date) para o formato datetime do Pandas.
   - Filtragem de Dados: Remoção de pedidos não entregues ou com tempo de entrega nulo.

3. Criação de Métricas e KPIs

   - delivery_time: Cálculo do tempo real de entrega em dias.
   - late_delivery: Mapeamento binário identificando se a entrega atrasou em relação à data estimada.
   - total_order_value: Valor total da compra (soma do preço do produto com o frete).
   - freight_percent: Percentual representativo do valor do frete sobre o preço do produto.

4. Análise Exploratória e Visualizações

Cálculo de Indicadores Chave:
   - Nota média das avaliações dos clientes (review_score)
   - Tempo médio de entrega (delivery_time)
   - Preço médio dos produtos (price) e frete médio (freight_value)
   - Contagem total de pedidos analisados
   - Distribuição das Avaliações: Análise e visualização gráfica (usando Seaborn e Matplotlib) da distribuição de notas atribuídas pelos clientes (de 1 a 5 estrelas).

5.  Mineração de texto de avaliações(text mining)
   - Realiza uma análise de texto (Text Mining) em avaliações de clientes da base Olist utilizando Python.
   - Foram aplicadas técnicas de pré-processamento, como remoção de acentos, pontuação e stopwords, além da padronização dos textos.
   - Em seguida, os comentários foram analisados por meio da frequência de palavras e n-gramas (bigramas), permitindo identificar os principais temas e padrões presentes nas avaliações.
   -  O projeto utiliza bibliotecas como Pandas, NLTK, Scikit-learn, Matplotlib e Seaborn para tratamento dos dados e visualização dos resultados.
  
   🛠️ Ferramentas Utilizadas

   - Python
   - Pandas e NumPy (Manipulação e estruturação de dados)  
   - Matplotlib e Seaborn (Visualização e gráficos)
   - NLTK (Processamento de linguagem natural)
   - Scikit-learn (Bigramas)
   - Unicodedata (Remover acentos e normalizar textos)
     
