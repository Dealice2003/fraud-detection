# 💳 Detecção de Fraudes Financeiras com Machine Learning

Este repositório contém meu Trabalho de Graduação em Ciência de Dados, no qual desenvolvi um sistema para **detecção de fraudes em transações com cartão de crédito** utilizando algoritmos de **aprendizado supervisionado**.

---

## 📌 Objetivo
Construir e avaliar modelos preditivos capazes de identificar transações fraudulentas, mesmo diante do **forte desbalanceamento entre classes** (menos de 0,2% das transações eram fraude).

---

## 🗂️ Conjunto de Dados
- Fonte: [Kaggle – Credit Card Fraud Detection](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud)  
- Total de registros: **284.807 transações**  
- Fraudes: **473 (0,1667%)**  
- Características:  
  - Variáveis `V1` a `V28` transformadas via **PCA** (anonimização).  
  - `Amount`: valor da transação.  
  - `Time`: tempo decorrido desde a primeira transação.  
  - `Class`: variável alvo (0 = legítima, 1 = fraude).  

---

## 🛠️ Tecnologias e Ferramentas
- **Python**  
- **Pandas, NumPy** → manipulação e análise de dados  
- **Matplotlib, Seaborn** → visualizações  
- **Scikit-learn** → modelos de Machine Learning  
- **Imbalanced-learn** → técnicas de balanceamento (SMOTE, undersampling)  
- **Skopt (BayesSearchCV)** → otimização de hiperparâmetros  

---

## ⚙️ Metodologia
1. **Pré-processamento**: limpeza de dados, remoção de duplicados, padronização.  
2. **Análise Exploratória (EDA)**: distribuição das classes, correlação de variáveis, análise temporal.  
3. **Engenharia de atributos**: transformação logarítmica e normalização.  
4. **Balanceamento**: combinação **SMOTE + undersampling**.  
5. **Modelagem**:  
   - Regressão Logística  
   - Random Forest  
   - Árvore de Decisão  
6. **Avaliação**: métricas adequadas a dados desbalanceados:  
   - Acurácia  
   - Precisão  
   - Recall  
   - F1-score  
   - AUC-ROC  
   - Matriz de confusão  

---

## 📊 Resultados
- **Random Forest** → melhor desempenho geral  
  - AUC: 0.9998  
  - F1-score: 0.9868  
  - Acurácia: 98,8%  

- **Regressão Logística** → alternativa eficiente em cenários com restrições de recursos  
  - AUC: 0.994  
  - F1-score: 0.960  

- **Árvore de Decisão** → modelo interpretável e competitivo  
  - AUC: 0.991  
  - F1-score: 0.962  

---

## 🔎 Conclusões
- O **Random Forest** se mostrou o modelo mais eficaz, equilibrando **precisão e recall**, essencial na detecção de fraudes.  
- A **Regressão Logística** se destaca em ambientes com **baixo custo computacional**.  
- A **Árvore de Decisão** é mais **explicável**, útil em contextos regulatórios e auditorias.  
- O balanceamento de classes foi fundamental para melhorar a detecção de fraudes.  

---

## 🚀 Próximos Passos
- Explorar algoritmos avançados como **XGBoost e LightGBM**.  
- Implementar **métricas financeiras baseadas em custo** (impacto de falsos positivos e negativos).  
- Testar abordagens **semi-supervisionadas** e **detecção de anomalias**.  

---

 
   ```bash
   git clone https://github.com/seu-usuario/seu-repositorio.git
