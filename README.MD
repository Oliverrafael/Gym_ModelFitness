# Descrição do projeto
### Contexto
A rede de academias Model Fitness está desenvolvendo uma estratégia de interação com o cliente baseados em dados analíticos.
Um dos problemas mais comuns que academias e outros serviços enfrentam é a rotatividade de clientes. Como você sabe se um cliente não está mais com você? Você pode calcular a rotatividade baseado nas pessoas que se livram das suas contas ou não renovam seus contratos. No entanto, às vezes não é óbvio que um cliente saiu: eles podem sair de fininho.

Indicadores de rotatividade varia de área para área. Se um usuário compra de uma loja online raramente mas regularmente, você não pode dizer que é um fujão. Mas se por duas semanas eles não abriam o canal que é atualizado diariamente, essa é uma razão para se preocupar: seu seguidor pode ter ficado aborrecido e deixado você.

Para uma academia, faz sentido dizer que os clientes saíram se eles não aparecem há um mês. É claro, é possível que eles estejam em Cancun e virão tornar a frequentar quando retornarem, mas esse não é um caso comum. Normalmente, se um cliente ingressa, vem algumas vezes, depois desaparece, ele provavelmente não voltará.

Em vez de lutar com a rotatividade, Model Fitness digitalizou uma parte dos perfis dos clientes. Sua tarefa é analisá-los e vir com uma estratégia de retenção de clientes.

# Objetivo do projeto
- Aprender a predizer a probabilidade de rotatividade (para o mês seguinte) para cada cliente
- Elabore retratos de usuários típicos: selecione os grupos mais marcantes e descreva suas principais características
- Analise os fatores que mais impactam a rotatividade
- Tire conclusões básicas e desenvolva recomendações sobre como melhorar o serviço de clientes:
- Identifique grupos alvo
- Sugira medidas para diminuir a rotatividade
- Descreva qualquer outro padrão que você vir com respeito às interações com clientes


## Datasets
- gym_churn_us.csv

# Descrição dos dados

- 'Churn' — a rotatividade do mês em questão
- Campos de dados atuais:
- Dados do mês anterior
- 'gender'
- 'Near_Location' — se o cliente morar ou trabalhar na vizinhança onde a academia está localizada
- 'Partner' — se o usuário for um funcionário de uma companhia parceira (a academia tem empresas parceiras cujos funcionários conseguem descontos; nesses casos, a academia armazena - informações sobre clientes de são funcionários)
- Promo_friends — se o cliente originalmente se inscreveu através de uma oferta "traga um amigo" eles normalmente usam o código de promoção do amigo quando pagam pela primeira filiação)
- 'Phone' — se o usuário fornece o seu número de telefone
- 'age' (idade)
- 'Lifetime' — o tempo (em meses) desde a primeira vez que o cliente veio à academia
- Dados do log de frequência e compras e dados sobre status de filiação atual
- 'Contract_period' — 1 mês, 3 meses, 6 meses, ou um ano
- 'Month_to_end_contract' — os meses remanescentes até que o contrato expira
- 'Group_visits' — se o cliente participa de sessões em grupo
- 'Avg_class_frequency_total' — frequência média de idas por semana por toda a vida do cliente
- 'Avg_class_frequency_current_month' — frequência média de visitas por semana durante o mês corrente
- 'Avg_additional_charges_total' — a quantidade total de dinheiro gasto em outros serviços da academia: café, artigos esportivos, cosméticos, massagem, etc.

## Etapas para conclusão do projeto

# Etapa 1: Baixar os dados
Model Fitness forneceu a você dados CSV contendo dados sobre rotatividade em um determinado mês e informações sobre o mês anterior. O conjunto de dados inclui os seguintes campos:

# Etapa 2: Realize análise exploratória dos dados (EDA)
* Olhe para o conjunto de dados: ele contém alguma característica ausente? Estude a média de valores e desvio padrão (use o método describe()).
* Observe a média dos valores médios das características em dois grupos: para aqueles que ficaram (use o método groupby()).
* Faça histogramas de barra e distribuições de características para aqueles que saíram (rotatividade) e aqueles que ficaram.
* Construa a matriz de correlação e a exiba.

# Etapa 3: Construa um modelo para predizer a rotatividade de clientes

Construa um modelo de classificação binária para clientes onde a variável objetivo é a saída de usuários do próximo mês.

* Divida os dados de treinamento e validação em dois conjuntos usando a função train_test_split().
* Treine o modelo no conjunto com dois métodos:
* regressão logística
* floresta aleatória
* Avalie acurácia, precisão e sensibilidade para ambos os modelos usando dados de validação. Use-os para comparar os modelos. Qual modelo rendeu melhores resultados?

Lembre-se de indicar o parâmetro random_state quando dividir os dados e definir o algoritmo.

# Etapa 4:  Crie agrupamentos de clientes
Defina ao lado colunas com dados sobre rotatividade e identifique agrupamentos do objeto (cliente):

* Padronize os dados.
* Use a função linkage() para construir a matriz das distâncias baseada na matriz de características padronizada e construa um dendrograma. Perceba: renderizar o dendrograma pode demorar um tempo! Use o gráfico resultante para estimar o número de agrupamentos que você pode destacar.
* Treine o modelo de agrupamento com o algoritmo K-means e preveja agrupamentos de clientes. (Deixe que o número de agrupamentos seja n=5,para que seja fácil comparar seus resultados com os de outros estudantes. No entanto, na vida real, ninguém vai te dar essas dicas, para que você tenha que decidir baseados nos gráficos das etapas anteriores.)
* Olhe para os valores médios das características para agrupamentos. Nada chama a sua atenção?
* Faça distribuições de características para os agrupamentos. Você notou alguma coisa?
* Calcule a taxa de rotatividade para cada agrupamento (use o método groupby()). Eles diferem em termos de taxa de rotatividade? Quais agrupamentos são propensos a sair, e quais são leais?

# Etapa 5: Chegue a conclusões e faça recomendações básicas sobre trabalhar com cliente

* Tirar conclusões e formular recomendações sobre a estratégia de interação e retenção de clientes.

## 🛠 Habilidade
Métricas de negócios
Teste de Hipóteses (Teste A/B)
Fundamentos de aprendizado de máquina (scikit-learn)


<svg xmlns="http://www.w3.org/2000/svg" width="256" height="256" fill="none" viewBox="0 0 256 256"><rect width="256" height="256" fill="#242938" rx="60"/><path fill="url(#paint0_linear_2_47)" d="M127.279 29C76.5066 29 79.6772 51.018 79.6772 51.018L79.7338 73.8284H128.185V80.6772H60.4893C60.4893 80.6772 28 76.9926 28 128.222C28 179.452 56.3573 177.636 56.3573 177.636H73.2812V153.863C73.2812 153.863 72.369 125.506 101.186 125.506H149.24C149.24 125.506 176.239 125.942 176.239 99.4123V55.5461C176.239 55.5461 180.338 29 127.279 29ZM100.563 44.339C105.384 44.339 109.28 48.2351 109.28 53.0556C109.28 57.8761 105.384 61.7723 100.563 61.7723C95.7426 61.7723 91.8465 57.8761 91.8465 53.0556C91.8465 48.2351 95.7426 44.339 100.563 44.339Z"/><path fill="url(#paint1_linear_2_47)" d="M128.721 227.958C179.493 227.958 176.323 205.941 176.323 205.941L176.266 183.13H127.815V176.281H195.511C195.511 176.281 228 179.966 228 128.736C228 77.5062 199.643 79.323 199.643 79.323H182.719V103.096C182.719 103.096 183.631 131.453 154.814 131.453H106.76C106.76 131.453 79.7607 131.016 79.7607 157.546V201.412C79.7607 201.412 75.6615 227.958 128.721 227.958ZM155.437 212.619C150.616 212.619 146.72 208.723 146.72 203.903C146.72 199.082 150.616 195.186 155.437 195.186C160.257 195.186 164.154 199.082 164.154 203.903C164.154 208.723 160.257 212.619 155.437 212.619Z"/><defs><linearGradient id="paint0_linear_2_47" x1="47.22" x2="146.333" y1="46.896" y2="145.02" gradientUnits="userSpaceOnUse"><stop stop-color="#387EB8"/><stop offset="1" stop-color="#366994"/></linearGradient><linearGradient id="paint1_linear_2_47" x1="108.056" x2="214.492" y1="109.905" y2="210.522" gradientUnits="userSpaceOnUse"><stop stop-color="#FFE052"/><stop offset="1" stop-color="#FFC331"/></linearGradient></defs></svg>




## Bibliotecas utilizadas
- pandas
- matplotlib
- seaborn
- sklearn.model_selection
- sklearn.linear_model
- sklearn.ensemble
- sklearn.metrics
- sklearn.preprocessing
- scipy.cluster.hierarchy
- sklearn.cluster

## 🔗 Links
[![portfolio](https://img.shields.io/badge/my_portfolio-000?style=for-the-badge&logo=ko-fi&logoColor=white)](https://github.com/Oliverrafael
)
[![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/rafael-oliveira-528400335/
)