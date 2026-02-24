# 📉 Banking Churn Analysis: Estratégias de Retenção Baseadas em Dados

Este projeto visa identificar padrões de comportamento e preditores de cancelamento (*churn*) em uma base de clientes de cartões de crédito, utilizando análise exploratória de dados para gerar insights acionáveis de retenção.

## 📌 1. O Problema de Negócio (The "Why")
O setor financeiro enfrenta um desafio constante com a retenção de clientes. O aumento na taxa de cancelamento de cartões impacta diretamente o faturamento e eleva o Custo de Aquisição de Clientes (CAC). 

**O Desafio:** Compreender quem são os clientes com maior tendência ao cancelamento e quais comportamentos precedem o encerramento da conta, permitindo que o time de CRM execute campanhas preventivas focadas em grupos de alto risco.

## 🛠️ 2. Decisões Técnicas & Stack
A metodologia focou em clareza estatística e visualização dinâmica:

* **Python & Pandas:** Utilizados para o ETL (Extração, Transformação e Carga), limpeza de dados e *Feature Engineering* (criação de faixas de transações).
* **Plotly Express:** Escolhido para a Análise Exploratória de Dados (EDA). A interatividade dos gráficos facilitou a identificação de correlações entre variáveis demográficas e financeiras.
* **Agrupamento e Discretização:** Uso de `pd.cut` para segmentar clientes por volume de uso, transformando dados contínuos em categorias de risco (Baixa, Média e Alta utilização).

## 🚀 3. Metodologia e Desafios
* **Tratamento de Dados:** Limpeza de registros nulos e exclusão de identificadores únicos (`CLIENTNUM`) para evitar sobreajuste e ruído na análise.
* **Análise Multivariada:** Desenvolvimento de histogramas comparativos para todas as colunas do dataset, permitindo visualizar a "fronteira de churn" em cada variável.
* **Normalização Estatística:** Uso de frequências relativas (porcentagem) para evitar conclusões precipitadas baseadas apenas em números absolutos.

## 📈 4. Insights Estratégicos (Impacto de Negócio)
A análise revelou padrões críticos que podem salvar a carteira de clientes:

1.  **Indicador de Transações:** Clientes com menos de 60 transações anuais são **zona crítica**. O engajamento ideal para retenção ocorre acima de 80 transações.
2.  **Sinal de Alerta no Atendimento:** Um número elevado de contatos com o SAC não é sinal de engajamento, mas sim o principal preditor de churn iminente, indicando problemas recorrentes não resolvidos.
3.  **Vulnerabilidade na Categoria Blue:** A maioria dos cancelamentos concentra-se na categoria de entrada, sugerindo baixa percepção de valor ou migração para bancos digitais com menos taxas.
4.  **Inatividade Progressiva:** A redução na utilização do limite de crédito é um sinal antecipado de que o cliente está transferindo seus gastos para outra instituição.

## 🔮 O que eu faria diferente? (Próximos Passos)
1.  **Modelagem Preditiva:** Implementar algoritmos de Machine Learning (como *Random Forest* ou *XGBoost*) para atribuir um "Score de Risco" individual a cada cliente.
2.  **Cálculo de LTV (Lifetime Value):** Estimar o prejuízo financeiro por cada ponto percentual de churn evitado.
3.  **Deploy de Dashboard:** Criar um painel no Power BI integrado ao Python para monitoramento contínuo dos indicadores de risco por parte da diretoria.

## 🚀 Como executar o projeto

```bash
pip install -r requirements.txt
jupyter notebook
```
---
Desenvolvido por **Guilherme Rodrigues** 
