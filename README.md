# Módulo 30 - K-Means: Segmentação de Espécies de Pinguins 🐧

## 📌 Descrição

Neste projeto, apliquei o algoritmo de clusterização **K-Means** usando dados biológicos da base `penguins`, do pacote seaborn. A ideia foi segmentar diferentes espécies de pinguins com base em características físicas como comprimento e profundidade do bico, comprimento da barbatana e massa corporal.

## 📊 Base de Dados

A base `penguins` possui registros de três espécies de pinguins:

- **Espécies:** Adelie, Chinstrap, Gentoo  
- **Variáveis usadas:**  
  - `bill_length_mm`: comprimento do bico  
  - `bill_depth_mm`: profundidade do bico  
  - `flipper_length_mm`: comprimento da barbatana  
  - `body_mass_g`: massa corporal

Variáveis como `species`, `island`, `sex` e `year` foram removidas por serem categóricas ou não necessárias para o modelo.

## 🧪 Etapas do Projeto

### 1. Limpeza dos Dados
- Verifiquei a presença de valores nulos (missing) e os removi do dataset.
- Excluí colunas categóricas para focar apenas nas variáveis numéricas necessárias ao K-Means.

### 2. Análise Exploratória
- Utilizei `pairplot` para explorar visualmente a distribuição dos dados.
- Foi possível perceber indícios de **3 agrupamentos**, o que faz sentido já que temos 3 espécies diferentes.

### 3. Padronização
- Apliquei `StandardScaler` para normalizar os dados antes do K-Means.

### 4. K-Means
- Utilizei o `KMeans` com **n_clusters=3**, conforme o número de espécies existentes.
- Modelei os dados e gerei os rótulos de cluster.

### 5. Visualização dos Resultados
- Criei gráficos de dispersão com Plotly destacando os clusters e os **centroides**.
- Também montei duas matrizes de dispersão para mostrar como os agrupamentos se formam.

## 📌 Conclusão

Foi possível ver que o algoritmo conseguiu identificar padrões consistentes entre as espécies com base nas variáveis físicas.
