

# Predição de Indicadores de Saúde e Diabetes 🩺

Este projeto utiliza técnicas de Aprendizagem de Máquina (Machine Learning) Supervisionada para analisar e prever indicadores de saúde relacionados com a diabetes, utilizando o dataset **CDC Diabetes Health Indicators**.

## 📋 Objetivos do Projeto

* Estudar e compreender as features e rótulos do repositório CDC.
* Implementar um pipeline de **ETL** (Extração, Transformação e Carga) robusto.
* Avaliar a necessidade de pré-processamento (normalização, tratamento de nulos, etc.).
* Criar e comparar dois modelos de classificação:
* **KNN** (K-Nearest Neighbors)
* **Redes Neurais** (MLP - Multi-Layer Perceptron)


* Medir e analisar métricas de desempenho: Acurácia, Precisão e Recall.

## 🛠️ Tecnologias Utilizadas

* **Linguagem:** Python
* **Bibliotecas de ML:** Scikit-learn (KNeighborsClassifier, MLPClassifier)
* **Manipulação de Dados:** Pandas, NumPy, SQLite3
* **Visualização:** Seaborn, Matplotlib
* **Fonte de Dados:** Kagglehub (Dataset BRFSS 2015).

## 🔄 Pipeline de Dados (ETL)

O projeto implementa uma arquitetura de dados organizada em:

1. **Extração:** Download automatizado do dataset via API do Kaggle.
2. **Transformação:** * Remoção de duplicatas para evitar enviesamento.
* Otimização de tipos de dados (float para int) para eficiência de memória.
* Verificação de valores nulos.


3. **Carga (Data Warehousing):** Armazenamento dos dados limpos num banco de dados **SQLite**, permitindo consultas complexas e garantindo a integridade dos dados para os modelos.

## 📊 Análise Exploratória (EDA)

Através de consultas SQL e integração com Pandas, o projeto analisa:

* **Balanceamento de Classes:** Distribuição entre registros de indivíduos saudáveis e diabéticos.
* **Correlação:** Identificação dos fatores que mais impactam a diabetes (como IMC, Pressão Alta e Colesterol).
* **Perfil Médio:** Comparativo visual entre grupos através de gráficos de violino, boxplots e contagens.

## 🤖 Modelos de Machine Learning

O projeto foca na comparação entre dois algoritmos distintos:

* **KNN:** Um modelo baseado em instâncias que classifica os dados com base na proximidade.
* **Redes Neurais (MLP):** Um modelo de aprendizagem profunda (deep learning) supervisionada para capturar padrões complexos nos indicadores de saúde.

## 📈 Resultados e Análise Crítica

Os modelos são avaliados utilizando uma partição de dados de teste, gerando:

* Matrizes de Confusão.
* Relatórios de classificação (Precision, Recall, F1-Score).
* Análise comparativa para justificar as diferenças de desempenho entre a simplicidade do KNN e a complexidade da Rede Neural.

---

### Como Executar

1. Instale as dependências: `pip install pandas numpy scikit-learn seaborn matplotlib kagglehub`.
2. Execute o notebook `Apt_Maq_Supervisionado (3).ipynb` num ambiente Jupyter ou Google Colab.
3. O pipeline ETL criará automaticamente o ficheiro `diabetes_warehouse.db` para as análises.
