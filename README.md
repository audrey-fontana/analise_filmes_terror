# analise_filmes_terror
Aproveitando o clima de terror que antecede o Halloween...  Esse é um projeto de Data Science focado em Horror Movies (Filmes de Terror)!

# 📜 Descrição

Este projeto é uma Análise Exploratória de Dados (EDA) detalhada e uma Análise de Processamento de Linguagem Natural (NLP) sobre filmes do gênero terror. O objetivo principal é extrair insights sobre a produção, qualidade percebida, sucesso financeiro, tendências temporais, subgêneros e a comunicação textual (sinopses) que define o gênero.

O código foi desenvolvido em Python e utiliza o ambiente Google Colab, com foco nas bibliotecas pandas, numpy, matplotlib, wordcloud, nltk (VADER) e gensim (LDA).


# ✨ Funcionalidades e Insights Chave

O script executa análises abrangentes, gerando gráficos e tabelas para documentar os seguintes insights:

* Limpeza de Dados:

  Conversão de tipos (string, datetime, category), tratamento de valores nulos (NaN) e tokenização de gêneros.

  Otimização de memória e preparação dos dados para análises financeiras (substituição de 0 por NaN em budget e revenue).

* Popularidade:

  Distribuição de vote_average e popularity, cálculo do Top 10 filmes mais bem avaliados (aplicando limiar de votos).

  As métricas de popularidade, contagem de votos e nota média são fracamente correlacionadas, sugerindo que medem aspectos diferentes do sucesso.

* Análise temporal:

  Tendência de lançamentos anuais e média de qualidade (vote_average) e popularity ao longo do tempo.

  Tendência de produção crescente (com viés de sobrevivência em filmes antigos). Filmes em anos recentes são exponencialmente mais populares, mas a nota média (vote_average) se manteve estável ou ligeiramente decrescente nas últimas décadas.

* Análise Financeira:

  Cálculo e distribuição do Retorno Sobre o Investimento (ROI = revenue / budget).

  O gênero de terror é altamente lucrativo. A mediana do ROI é 2.01, indicando que mais da metade dos filmes que reportam finanças geram lucro.

* Gênero/Idioma:

  Distribuição dos top 10 subgêneros e desempenho de ROI por idioma.

  Filmes em "Outros Idiomas" (não-inglês) são, em média, melhor avaliados e apresentam um ROI médio muito superior (64.14) em comparação com filmes em Inglês (15.29).

* NLP (Sinopses):

  Geração de Nuvem de Palavras (Termos e Bigrams) dos filmes mais aclamados (Top 5% em vote_average).

  Palavras como "horrir", "night" e "house" dominam as sinopses de filmes de terror de alta qualidade.

* NLP (Sentimento):

  Análise de Sentimento (VADER) das sinopses e correlação com vote_average e vote_count.

  A polaridade geral das sinopses é marcadamente negativa (Score Médio de -0.38), o que é esperado no gênero. O score de sentimento não é um preditor significativo do desempenho de qualidade ou engajamento do filme.

* NLP (Tópicos):

  Modelagem de Tópicos (LDA) com base nas sinopses.

  (Resultado gerado em arquivo HTML para análise interativa).


# ⚙️ Tecnologias Utilizadas

* Python (Ambiente Google Colab)

* Análise de Dados: pandas, numpy

* Visualização: matplotlib, wordcloud

* Processamento de Linguagem Natural (NLP):

  nltk (VADER para Análise de Sentimento)

  gensim (LDA para Modelagem de Tópicos)

  pyLDAvis (Visualização de Tópicos)


# 📂 Arquivos e Estrutura

  * horror_movies.csv: O dataset original utilizado para a análise.

  * analise_filmes_terror.ipynb (ou .py): O script Python completo da análise.


# 📊 Dataset (Fonte de Dados)

  O dataset utilizado, horror_movies.csv, foi extraído do Kaggle, e contém informações detalhadas de mais de 32.000 filmes de terror, incluindo métricas como:

* id, title, original_language, release_date, runtime, status, vote_average, vote_count, popularity, budget, revenue, overview (sinopse), tagline, genre_names (gêneros associados)


# 🚀 Como Executar o Projeto

* Pré-requisitos: o código foi desenvolvido no Google Colab e inclui comandos específicos para montagem do Google Drive para acesso ao arquivo de dados.

* Google Colab/Jupyter Notebook: O projeto funciona melhor em um ambiente de Notebook.

* Dataset: Faça o download do arquivo horror_movies.csv e coloque-o no seu Google Drive, seguindo o caminho usado no código:

    terror = pd.read_csv("/content/drive/MyDrive/SUA_PASTA/horror_movies.csv")

    Altere o caminho dentro da função pd.read_csv para o local onde você salvou o arquivo no seu Drive.

1. Clonar o Repositório:
  
git clone https://github.com/SEU_USUARIO/NOME_DO_SEU_PROJETO.git
cd NOME_DO_SEU_PROJETO

2. Instalar Dependências:

* Crie e ative um ambiente virtual (opcional, mas recomendado)
  
python -m venv venv

source venv/bin/activate

* Instale as dependências
  
pip install pandas numpy matplotlib wordcloud nltk gensim pyldavis

3. Executar o Código:

Abra o arquivo .ipynb no Google Colab ou execute o script Python.

* Se você salvou como .py e ajustou o caminho do arquivo .csv localmente
python analise_filmes_terror.py

# 🤝 Contribuição

Sinta-se à vontade para abrir issues ou sugerir melhorias via Pull Requests!


























  
