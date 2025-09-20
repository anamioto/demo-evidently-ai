# 🧠 Observabilidade e Monitoramento de Modelos com Evidently (Iris Dataset)

Este repositório contém um **notebook prático** para aprender e demonstrar conceitos de **observabilidade e monitoramento em modelos de Machine Learning** utilizando a biblioteca [Evidently AI](https://www.evidentlyai.com/) e o dataset clássico **Iris**.

O objetivo é mostrar, de forma didática, como:
- Detectar **data drift** (mudanças na distribuição dos dados).
- Medir a **degradação de performance** de um modelo em produção.
- Gerar relatórios interativos do Evidently para análise e tomada de decisão.
- Aplicar boas práticas de MLOps e monitoramento de modelos.

---


## 📂 Estrutura do Repositório

```

├── evidently\_observabilidade\_iris.ipynb   # Notebook principal
├── reports/                               # Saída dos relatórios HTML
│   ├── iris\_data\_drift\_report.html
│   └── iris\_classification\_performance\_report.html
├── requirements_evidently.txt
└── README.md

````

---

## 🚀 Pré-requisitos

- **Python 3.10+**
- Pacotes listados abaixo:

```bash
pip install -U pandas numpy scikit-learn evidently
````

⚠️ Recomendado utilizar um **ambiente virtual** (`venv` ou `conda`) para isolar dependências.

---

## 📊 Conceitos Abordados

* **Data Drift:** quando a distribuição estatística dos dados de entrada muda ao longo do tempo.
* **Model Performance Degradation:** queda da performance preditiva após mudanças no ambiente.
* **Observabilidade:** monitoramento contínuo dos dados, do modelo e das métricas.
* **Relatórios Evidently:** geração de dashboards HTML para inspecionar drift e performance.

---

## ▶️ Como Executar

1. Clone o repositório:

   ```bash
   git clone https://github.com/<seu-usuario>/<nome-repo>.git
   cd <nome-repo>
   ```

2. Crie e ative um ambiente virtual:

   ```bash
   python -m venv .venv
   source .venv/bin/activate  # Linux/Mac
   .venv\Scripts\activate     # Windows
   ```

3. Instale as dependências:

   ```bash
   pip install -r requirements.txt
   ```

   *(ou manualmente os pacotes listados acima).*

4. Abra o Jupyter Notebook:

   ```bash
   jupyter notebook evidently_observabilidade_iris.ipynb
   ```

5. Execute as células em ordem.
   Ao final, os relatórios HTML estarão na pasta `./reports/`.

---

## 📂 Relatórios Gerados

* **`iris_data_drift_report.html`** → compara distribuições do *baseline* e dados atuais, sinalizando drift.
* **`iris_classification_performance_report.html`** → mostra métricas de classificação (acurácia, precisão/recall, matriz de confusão).

Exemplo de interpretação:

* **Drift detectado** em `petal_length` → modelo pode estar recebendo dados diferentes dos de treino.
* **Queda de acurácia** de 95% → 82% → pode indicar necessidade de **re-treino**.

---

## 🛠️ Boas Práticas e Extensões/Próximos passos

* **Logs estruturados:** salvar entradas, saídas e versão do modelo em produção.
* **Coleta de ground truth:** sempre que possível, para avaliar métricas reais.
* **Alertas automáticos:** definir thresholds (ex.: ≥30% de colunas com drift) e disparar notificações.
* **Ciclo de re-treino:** integrar este fluxo em pipelines de MLOps (Airflow, Azure ML, GitHub Actions).
* **Explainability:** monitorar a importância das features com SHAP/LIME.

---

## 📚 Referências

* [Evidently AI Docs](https://docs.evidentlyai.com/)
* [Scikit-learn: RandomForestClassifier](https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.RandomForestClassifier.html)
* Nelson, C. *Engenharia de Software para Cientistas de Dados* (2024)
* Huyen, C. *Designing Machine Learning Systems* (2022)

---

## 🤝 Contribuindo

Contribuições são bem-vindas!
Sugestões de melhorias, correções de bugs ou novas ideias de relatórios e estudos podem ser abertas via **Pull Request** ou **Issue**.

---

```
