# Segmentação de Clientes
Este repositório contém um script Python para realizar a segmentação de clientes em um conjunto de dados de cartão de crédito. A análise envolve várias técnicas de pré-processamento de dados, visualização e clustering, incluindo clustering K-Means, Análise de Componentes Principais (PCA) e Autoencoders. Abaixo está um resumo das etapas-chave e descobertas da análise:

## Descrição do Conjunto de Dados
O conjunto de dados usado nesta análise contém informações sobre clientes de cartão de crédito, incluindo seu comportamento de gastos, limites de crédito e outras métricas financeiras. O conjunto de dados é carregado usando a biblioteca Pandas, e suas estatísticas básicas e informações são exploradas.

## Pré-Processamento de Dados
O pré-processamento de dados é uma etapa crucial em qualquer projeto de análise de dados. Nesta análise, as seguintes etapas de pré-processamento de dados são realizadas:

- Tratamento de valores ausentes: Valores ausentes nas colunas "MINIMUM_PAYMENTS" e "CREDIT_LIMIT" são imputados com a média das respectivas colunas.
- Remoção de entradas duplicadas: Linhas duplicadas são removidas do conjunto de dados.
- Normalização de recursos: É aplicada a normalização padrão ao conjunto de dados para normalizar os recursos.

## Análise Exploratória de Dados
A Análise Exploratória de Dados (AED) é essencial para obter insights sobre o conjunto de dados. Algumas das etapas de AED realizadas nesta análise incluem:

- Visualização das distribuições de dados: Histogramas são usados para visualizar as distribuições de vários recursos no conjunto de dados.
- Análise de correlação: A matriz de correlação é visualizada usando um mapa de calor para identificar relacionamentos entre diferentes recursos.

## Determinação do Número de Clusters
Para determinar o número ideal de clusters para a segmentação dos clientes, foi utilizado o Método do Cotovelo. Esse método envolve a execução do algoritmo K-Means com diferentes números de clusters e o cálculo do somatório dos quadrados das distâncias intracluster (WCSS) para cada configuração. O valor de WCSS é então plotado em um gráfico, e o ponto de "cotovelo" representa o número ótimo de clusters, onde a adição de mais clusters não fornece ganhos significativos na explicação da variação dos dados.

## Clustering K-Means
Com o número ideal de clusters determinado, o algoritmo K-Means é aplicado para segmentar os clientes em grupos homogêneos. Cada cliente é atribuído a um cluster com base em sua semelhança com outros clientes no mesmo grupo.

Os resultados do clustering são visualizados por meio de histogramas que mostram a distribuição de características específicas em cada cluster. Isso ajuda a identificar padrões e tendências exclusivas em cada grupo de clientes.

Além disso, os centros dos clusters são calculados e transformados de volta para a escala original dos dados. Isso fornece informações sobre o perfil médio de cada grupo de clientes, incluindo médias de gastos, limites de crédito e outras métricas.

## Aplicação de PCA (Análise de Componentes Principais) e Visualização dos Resultados
A análise de componentes principais (PCA) é usada para reduzir a dimensionalidade dos dados a fim de visualizar os resultados do clustering em um espaço bidimensional. Isso facilita a identificação de tendências e separação dos clusters.

Os resultados do PCA são plotados em um gráfico de dispersão, onde cada ponto representa um cliente e é colorido de acordo com o cluster a que pertence. Isso permite uma representação visual dos grupos de clientes e como eles se distribuem no espaço de duas dimensões.

## Aplicação de Autoencoders
Além do K-Means e do PCA, é explorada a aplicação de autoencoders para redução de dimensionalidade e segmentação de clientes. Os autoencoders são uma técnica de aprendizado profundo que permite criar representações compactas dos dados originais.

Os dados são transformados por meio de uma rede neural que codifica as informações em um espaço de menor dimensão. Em seguida, a reconstrução dos dados é realizada para avaliar a eficácia da representação compacta. O resultado é uma representação compacta dos clientes que é utilizada para realizar o clustering.

## Resultados
Os resultados do clustering, tanto com K-Means quanto com autoencoders, são apresentados em gráficos e tabelas. Isso inclui a distribuição dos clientes em clusters, as características médias de cada cluster e visualizações de clusters em duas dimensões.

Os resultados finais podem ser úteis para a equipe de marketing ou análise de dados, pois permitem segmentar os clientes com base em seu comportamento de gastos e outras métricas financeiras. Isso, por sua vez, pode informar estratégias de marketing direcionadas e personalizadas para cada grupo de clientes.

O código e os resultados completos podem ser encontrados nos arquivos fornecidos neste repositório.
