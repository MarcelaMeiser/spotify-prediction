# 🎵 Projeto Spotify

> **Feito para prever suas futuras músicas favoritas**

👩‍💻 **Autora:** Marcela Philippe Meiser Lima

---

## 📌 Sobre o Projeto

Este projeto tem como objetivo desenvolver um **sistema inteligente** capaz de identificar detalhes e características do gosto musical do usuário, a partir de dados estruturados extraídos do Spotify.

A solução utiliza uma base de dados de treinamento e teste para classificar preferências musicais, sendo construída a partir de um exemplo real de uma pessoa e seus gostos musicais, permitindo prever futuras músicas favoritas.

---

## 🎯 Objetivos

- Analisar e tratar uma base de dados musicais do Spotify  
- Identificar padrões e características do gosto musical do usuário  
- Gerar análises gráficas (gênero, artista, duração e popularidade)  
- Treinar e testar diferentes algoritmos de Machine Learning  
- Escolher o melhor algoritmo para prever se uma música será curtida (`liked = 1`) ou não (`liked = 0`)

---

## 🗂️ Organização do Projeto

```
📁 Projeto-Spotify
│
├── 📁 análises_e_tratamentos    → Notebook de análise exploratória e Notebook de tratamento dos dados   
├── 📁 gráficos                  → Notebook e imagens dos gráficos gerados
├── 📁 dados                     → Bases de dados (CSV e Pickle)
├── 📁 machine learning          → Notebook do modelo de regressão logística
├── 📈 Projeto Spotify.pptx      → Apresentação do projeto
└── 📈 Projeto Spotify.pdf       → Sobre o projeto
```

### 📓 Notebooks

| Notebook | Descrição |
|----------|-----------|
| `analise_exploratoria.ipynb` | Estrutura, padrões, outliers, duplicatas e nulos |
| `tratamento.ipynb` | Edição, dummies, escalonamento e exportação |
| `graficos.ipynb` | Visualizações gráficas das preferências musicais |
| `modelo.ipynb` | Comparação entre algoritmos de Machine Learning |
| `regressao_logistica.ipynb` | Modelo final escolhido e previsões |

---

## 🛠️ Bibliotecas Utilizadas

![pandas](https://img.shields.io/badge/pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![numpy](https://img.shields.io/badge/numpy-013243?style=for-the-badge&logo=numpy&logoColor=white)
![matplotlib](https://img.shields.io/badge/matplotlib-11557C?style=for-the-badge&logo=python&logoColor=white)
![seaborn](https://img.shields.io/badge/seaborn-4C72B0?style=for-the-badge&logo=python&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)

```python
import pandas as pd
import seaborn as sns
import numpy as np
import matplotlib.pyplot as plt
import matplotlib.patches as mpatches
from sklearn.preprocessing import MultiLabelBinarizer
from sklearn.preprocessing import StandardScaler
from sklearn.model_selection import train_test_split
from sklearn.metrics import classification_report, accuracy_score, confusion_matrix, roc_curve, roc_auc_score
from sklearn.linear_model import LogisticRegression
```

---

## 🔍 Etapas do Projeto

### 1️⃣ Análise Exploratória
- Leitura de dados  
- Comandos estruturais (`head`, `tail`, `info`, `dtypes`)  
- Tratamento de duplicatas  
- Tratamento de outliers  
- Descrição estatística (`describe`)  
- Heatmap de correlação  
- Exportação final  

### 2️⃣ Tratamento dos Dados
- Conversão de duração (`ms → min`)  
- Transformação de gêneros em lista  
- Criação da coluna `qt_genres`  
- Geração de **dummies** com `MultiLabelBinarizer`  
- Drop de colunas irrelevantes  
- **Escalonamento** com `StandardScaler`  
- Concatenação final e exportação em `.pkl`  

### 3️⃣ Análise Gráfica
- 🎯 Distribuição de **liked = 0** e **liked = 1**  
- ⏱️ Preferência por tempo de música  
- 📈 Preferência por popularidade da música e do artista  
- 🎤 Top 10 artistas mais e menos curtidos  
- 🎸 Top 10 gêneros mais e menos curtidos  
- 🎼 Top 20 músicas mais longas x liked  
- 🔢 Quantidade de gêneros por música curtida e não curtida  

### 4️⃣ Machine Learning

Foram testados **6 algoritmos**, cada um com 3 execuções:

| Algoritmo | Precisão |
|-----------|----------|
| Árvore de Decisão | 93,1% |
| k-Nearest Neighbors (KNN) | 96,5% |
| Naive Bayes | 91,0% |
| Random Forest | 93,1% |
| ✅ **Regressão Logística** | **100,0%** |
| SVM | 96,5% |

> 🏆 **Algoritmo escolhido:** Regressão Logística

---

## 📊 Resultados

O modelo de **Regressão Logística** atingiu excelente performance na previsão das preferências musicais do usuário, sendo capaz de classificar corretamente se uma nova música será curtida ou não com base nos padrões aprendidos.

---

## ✅ Conclusão

Este projeto desenvolveu um modelo preditivo capaz de determinar a probabilidade de um usuário gostar de uma nova música, utilizando dados extraídos do Spotify. A partir de uma base inicial, foram realizadas as etapas de análise exploratória, tratamento dos dados, geração de gráficos analíticos e teste comparativo entre diferentes algoritmos de Machine Learning.

A análise gráfica permitiu identificar padrões importantes de preferência por gênero, artista, duração e popularidade, enquanto a etapa de Machine Learning comprovou a viabilidade da previsão automatizada, tendo a **Regressão Logística** como o algoritmo de melhor desempenho.

Os resultados demonstram o potencial da solução para **otimizar sistemas de recomendação** e **personalizar a experiência musical**, tornando-a mais alinhada com o gosto individual de cada usuário.

---

## 🚀 Como Executar

1. Clone este repositório:
   ```bash
   git clone https://github.com/seu-usuario/projeto-spotify.git
   ```

2. Instale as dependências:
   ```bash
   pip install pandas seaborn numpy matplotlib scikit-learn
   ```

3. Execute os notebooks na ordem:
   1. `analise_exploratoria.ipynb`
   2. `tratamento.ipynb`
   3. `graficos.ipynb`
   4. `modelo.ipynb`
   5. `regressao_logistica.ipynb`

---

## 👩‍💻 Autora

Desenvolvido por **Marcela Philippe Meiser Lima**

⭐ Se este projeto te ajudou ou te inspirou, deixe uma estrela no repositório! ⭐
