# Projeções Epidemiológicas - COVID-19

<hr>

## Descrição do projeto

<p align="justify">

O objetivo desse trabalho é realizar a modelagem de dados e a projeção da trajetória da pecuária e lavouras temporárias do estado do Pará, suas regiões e municípios. Essa modelagem de dados é possível usando os métodos computacionais de mineração de dados e inteligencia artificial que auxiliam na identificação de tendências das atividades agropecuárias do estado. 

Assim, o estudo desses dados e técnicas avançadas se torna fundamental para o planejamento e a definição de estratégias, seja para aproveitar o desempenho produtivo do setor agropecuário, com o atendimento da demanda de mão-de-obra ou oferta de produtos e serviços, seja para conter alguma externalidade, como a degradação ambiental.
</p>

## Pré-requisitos

- Acesso ao <a href="https://colab.research.google.com/">Google Colab.</a>
- Conhecimento da linguagem de programação <a href="https://www.python.org/">Python</a>

- Conhecimento básico das bibliotecas:
  - <a href="https://matplotlib.org/">Matplotlib</a>
  - <a href="https://www.tensorflow.org/">TensorFlow</a>
  - <a href="https://unit8co.github.io/darts/">Darts</a>
  - <a href="https://numpy.org/">NumPy</a>
  - <a href="https://pandas.pydata.org/">Pandas</a>

## Começando

<p align="justify">
Para começar de forma local, faça um clone do repositório em sua máquina. <br>
Abra o terminal de comando ou o <a href="https://git-scm.com/">Git Bash</a> na sua máquina e, na pasta desejada, digite o seguinte código:
    <pre><code class="html"> git clone https://github.com/npcateam2/data_agro.git</code></pre>
</p>

<p align="justify">
Se desejar, basta criar um fork do repositório seguindo normalmente os passos padrões.</p>

## Execução dos Scripts

<p align="justify">
Para visualizarmos todas as projeções, devemos passar por algumas etapas antes.

1. [Coleta de dados](https://github.com/npcateam2/data_agro/tree/main/Colab%20Notebooks/ETL#:~:text=Coleta_map_biomas.ipynb)

   Onde é coletado os dados para realização das transformações necessárias
   <br>

2. [União das tabelas da SIDRA](https://github.com/npcateam2/data_agro/tree/main/Colab%20Notebooks/ETL#:~:text=unification%2Dof%2DSIDRA%2Dtables.ipynb)

   Onde é unificado os dados da SIDRA que foram extraídos individualmente
   
3. [União de tabelas](https://github.com/npcateam2/data_agro/tree/main/Colab%20Notebooks/ETL#:~:text=uniao_de_%20tabelas.ipynb)

   Onde dos dados da SIDRA e MAPBIOMAS são unidos em uma unica tabela

4. [Modelagem](https://github.com/npcateam2/data_agro/blob/main/Colab%20Notebooks/modelos/modelagem.ipynb)

   Dados são modelados de acordo com a modelagem hierarquica proposta no projeto.

5. [GRID SEARCH](https://github.com/npcateam2/data_agro/tree/main/Colab%20Notebooks/modelos#:~:text=.%E2%80%8A.-,grid_search.ipynb,-Add%20files%20via)

   Script que irá realizar o processo de treinamento, criar e salvar métricas de erro e forecasting e gerar os gráficos que foram adicionados ao projeto.
   
## Arquivos gerados

1. [Erros gerados pelos modelos](https://github.com/npcateam2/data_agro/tree/main/Dados/standarized/erros)

2. [Forecast gerado pelos modelos](https://github.com/npcateam2/data_agro/tree/main/Dados/standarized/forecast_ts)

3. [Historical Forecast](https://github.com/npcateam2/data_agro/tree/main/Dados/standarized#:~:text=20%20minutes%20ago-,historical_forecast,-Adi%C3%A7%C3%A3o%20de%20dados)

  Forecasting histórico que foi utilizado para validar o resultado dos forecasting e determinar melhor conjunto de parâ
   Script onde é realizado uma avalização nos dados do script de predição, onde ao final dele é gerado uma tabela de erro.todmetros
