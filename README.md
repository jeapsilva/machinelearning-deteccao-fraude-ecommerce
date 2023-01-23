<h1 align='center'> Detecção de fraude em E-commerce </h1>

![Badge em Desenvolvimento](http://img.shields.io/static/v1?label=STATUS&message=EM%20DESENVOLVIMENTO&color=GREEN&style=for-the-badge)


# Descrição do projeto

Uma loja virtual verificou que no último ano houve muitos casos de fraude no cartão crédito. O cliente comprava através do gateway de pagamento e após receber o produto em casa, a compra era cancelada no cartão de crédito. Logo a loja virtual além de perder o valor da venda, também perde o valor de custo do seu produto. Para evitar isso, a loja buscou utilizar a sua série histórica de compras para o desenvolvimento de um algoritmo para detecção de fraude nas compras que eram feitas no ecommerce.

Temos disponíveis dois datasets, sendo um referente a movimentação na loja virtual e outro que contêm uma descrição de IPs por país. 

# Features


| Feature  | Descrição |
| ------------- | ------------- |
| fraude  | variável binária que identifica a fraude (1) ou não (0) |
| id  | identificação do cliente na loja |
| cadastro  | data e horário do cadastrp |
| compra  | data e horário da compra |
| valor  | valor da compra |
| id_dispositivo  | string que mapeia a identificação do dispositivo do cliente |
| fonte  | Local de origem do tráfego do cliente |
| browser  | navegador utilizado |
| genero  | gênero do usuário |
| idade  | idade do cliente |
| Ip  | Ip do dispositivo do cliente |

# Descrição da Solução
**Solução**

Atualmente para fazer a detecção de fraudes em cartão de crédito utiliza-se diversos métodos de Machine Learning para detectar fraude em dados transacionais de cartão de crédito. Na literatura há diversos algoritmos para realizar a classificação do usuário para essa detecção, como Naive Bayes, Random Forest, Regressão Logística e máquinas de vetores de suporte. 

Aqui nesse projeto optou-se por ampliar e explorar outros algoritmos de classificação para que possamos fazer uma análise do comportamento que tais algoritmos tem. Portanto, aqui utilizaremos o algortimo ExtraTreeClassifier, Floresta Isolada e OneClassSVM disponívels na biblioteca do Scikit Learn. 

**Limpeza e manipulação dos dados**

Na fase de limpeza dos dados buscou-se fazer a transformação do tipo de variáveis, verificação de valores nulos e NaN. Em seguida, buscou-se visualizar as distribuições das features, para que possamos identificar outliers. Feita essa identificação foi realizada a remoção dos outliers para que esses não influenciassem no algoritmo. 

**Análise Exploratória de Dados (EDA)**

Na análise exploratória de dados buscou-se analisar a correlação entre features e casos de fraude, como por exemplo se havia muita discrepância entre os valores médio de compra e a presença de fraude. De todas essas análises feitas, houve identicação de 3 variáveis suspeitas em casos de fraude: local do IP, número de dispositivos e tempo entre cadastro/compra. 

Diante disso, foi identificado que a maioria das fraudes vinham de IPs dos EUA. Também foi identificado que usuários que utilizam diversos IPs para logar na loja também são grandes suspeitos para fraude. Por fim, o tempo curto entre o cadastro e o ato da compra também indicava fraudes. 

**Feature Engineering**



**Seleção de features**


**Otimização do modelo**


**Avaliação do modelo**


# Resultados e conclusão


# Tecnologias utilizadas

<div style="display: inline_block"><br/>
    <img align="center" alt="Jupyter" src="https://img.shields.io/badge/Jupyter-F37626.svg?&style=for-the-badge&logo=Jupyter&logoColor=white" />  
    <img align="center" alt="Scikit Learn" src="https://img.shields.io/badge/scikit_learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white" /> 
    <img align="center" alt="Matplotlib" src="https://img.shields.io/badge/Matplotlib-%23ffffff.svg?style=for-the-badge&logo=Matplotlib&logoColor=black" />
    <img align="center" alt="Pandas" src="https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white" />
</div><br/>

# Pessoas Desenvolvedoras do Projeto

<a href="https://github.com/jesapsilva">Jéssica Aparecida Silva - Cientista de dados</a>

# Licença

<img src="https://mirrors.creativecommons.org/presskit/buttons/88x31/svg/by-nc.svg" />

Esta licença permite que outros remixem, adaptem e criem a partir do seu trabalho para fins não comerciais e, embora os novos trabalhos tenham de lhe atribuir o devido crédito e não possam ser usados para fins comerciais, os usuários não têm de licenciar esses trabalhos derivados sob os mesmos termos.

# Referências:
