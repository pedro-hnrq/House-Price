

<h1 align="center"> House-Price 🏘️ </h1>


<p align="center">

<img alt="GitHub Language Count" src="https://img.shields.io/github/languages/count/pedro-hnrq/House-Price" />
<img alt="GitHub Top Language" src="https://img.shields.io/github/languages/top/pedro-hnrq/House-Price" />
<img alt="" src="https://img.shields.io/github/repo-size/pedro-hnrq/House-Price" />
<img alt="GitHub Issues" src="https://img.shields.io/github/issues/pedro-hnrq/House-Price" />
<img alt="GitHub Closed Issues" src="https://img.shields.io/github/issues-closed/pedro-hnrq/House-Price" />
<img alt="GitHub Pull Requests" src="https://img.shields.io/github/issues-pr/pedro-hnrq/House-Price" />
<img alt="GitHub Closed Pull Requests" src="https://img.shields.io/github/issues-pr-closed/pedro-hnrq/House-Price" />
<img alt="Github License" src="https://img.shields.io/github/license/pedro-hnrq/House-Price" />

</p>

<p align="center"> 
 <img src="img/img_2.png" width=250 alt="Kaggle" > 
<img src="img/img_1.png"> </p>

> <p align="justify"> Criado para a <a href="https://www.kaggle.com/competitions/house-prices-advanced-regression-techniques">   competição do Kaggle</a> sobre a previsão de preço das casas na cidade de Ames, Iowa (Estados Unidos) </p>



## 📊 [Etapa 1: Primeiro modelo](https://github.com/pedro-hnrq/House-Price/blob/main/house_prices_1module.ipynb)
- Nesta fase, realizamos uma análise inicial dos dados sem aplicar tratamentos ou engenharia de dados, visando avaliar o desempenho dos modelos básicos.
- Optamos por **substituímos todos os valores vazios por -1** e **eliminamos todas as colunas de texto**
- Utilizamos **três algoritmos de regressão**: **[Regressão Linear](https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.LinearRegression.html)**, **[Árvore de Regressão](https://scikit-learn.org/stable/modules/tree.html#regression)** e **[KNeighborsRegressor](https://scikit-learn.org/stable/modules/generated/sklearn.neighbors.KNeighborsRegressor.html#sklearn.neighbors.KNeighborsRegressor)** e **avaliamos os resultados** utilizando o **[erro médio absoluto](https://scikit-learn.org/stable/modules/generated/sklearn.metrics.mean_absolute_error.html)** e o **[erro quadrático médio](https://scikit-learn.org/stable/modules/generated/sklearn.metrics.mean_squared_error.html)**, dando preferência ao segundo pois era o critério usando na competição
- O **score público retornado pelo Kaggle foi: 0,25476**

## 💹 [Etapa 2: Limpeza dos dados](https://github.com/pedro-hnrq/House-Price/blob/main/Limpeza_dos_Dados.ipynb)
- Focamos na limpeza dos dados, identificando e tratando valores vazios e informações faltantes para melhorar a qualidade dos modelos.
- Em algumas colunas, valores vazios representavam **ausência dos atributos na casa**, como por exemplo o valor vazio na coluna de piscina significava que aquele imóvel não possuia piscina. Nesse caso o vazio **era uma informação**
- Em outros casos onde a informação realmente estava ausente, usamos tratamentos como **substituir pela média da coluna**, **utilizar uma agregação para encontrar a melhor média para o atributo**, **utilizar a moda**, entre outros tratamentos
- O **score público retornado pelo Kaggle foi: 0,1812**

## 📉 [Etapa 3: Tratamento dos dados](https://github.com/pedro-hnrq/House-Price/blob/main/Analise_Exploratoria_dos_Dados.ipynb)
- Após a limpeza dos dados, exploramos a  **correlação entre as variáveis numéricas e os valores mais frequentes das variáveis de texto**
- Para tratar colunas do tipo texto, começamos **eliminando as colunas com muitos valores iguais** e depois **utilizamos lambda function e criamos nossas próprias funções para aplicar e fazer o tratamento**
- Implementamos técnicas como **OneHotEncoder e OrdinalEncoder** para o tratamento de variáveis categóricas, e analisamos detalhadamente as colunas relacionadas à garagem.
- Os **resultados variaram entre 0,18433 e 0,45474 no score público do Kaggle**, indicando áreas para refinamento nas próximas etapas do projeto.


## 📝 Licença

Esse projeto está sob licença. Veja o arquivo [LICENÇA](LICENSE.md) para mais detalhes.