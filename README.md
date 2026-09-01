# 📊 Diagnóstico de Desempenho Comercial e Logístico - E-commerce Olist

> Um projeto completo de Análise de Dados simulando uma consultoria estratégica para identificar gargalos de faturamento, categorias líderes de mercado e o impacto de prazos logísticos na satisfação dos clientes.

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-orange)
![Status](https://img.shields.io/badge/Status-Concluído-success)

---

## 🎯 1. O Problema de Negócio
A diretoria de uma grande varejista operando na plataforma Olist notou oscilações significativas no faturamento ao longo do tempo e recebeu reclamações esporádicas sobre prazos de entrega. Este projeto foi estruturado com uma abordagem de Business Intelligence e Analytics para responder a **quatro perguntas estratégicas cruciais**:

1. Qual é a evolução mensal da receita e existe sazonalidade evidente de vendas?
2. Quais são as Top 5 categorias de produtos que sustentam o faturamento da plataforma?
3. Qual é o impacto real dos atrasos de entrega na nota de avaliação (satisfação) dos clientes?
4. Quais são os padrões de comportamento e volume de vendas gerais?

---

## 🗂️ 2. Fonte de Dados e Ferramentas
Os dados utilizados são públicos e vêm do **Brazilian E-Commerce Public Dataset by Olist** (disponível no Kaggle). A base simula um ambiente real de e-commerce e é composta por múltiplas tabelas relacionais (`orders`, `order_items`, `products`, `reviews`, `payments`, etc.).

* **Linguagem:** Python
* **Ambiente de Desenvolvimento:** Google Colab / Jupyter Notebook
* **Biblioteca Principal de Manipulação:** Pandas & NumPy
* **Biblioteca de Visualização:** Matplotlib

---

## 🛠️ 3. Metodologia e Passo a Passo
O projeto foi desenvolvido seguindo as etapas fundamentais de um pipeline de dados:

1. **Limpeza e Tratamento:** Conversão de colunas de texto para o formato de data (*datetime*), tratamento de valores nulos e remoção de inconsistências.
2. **Modelagem e Joins (Cruzamentos):** Utilização da função `pd.merge()` baseada em chaves relacionais (`order_id`, `product_id`) para unificar informações dispersas entre pedidos, itens, produtos e avaliações de clientes.
3. **Análise Exploratória (EDA):** Agrupamento temporal por ano-mês, cálculo de métricas de faturamento bruto (`price`), derivação de colunas para cálculo de dias de atraso na entrega e cruzamento com notas de feedback (`review_score`).

---

## 📈 4. Principais Insights de Negócio

### A. Sazonalidade de Faturamento
* **Descoberta:** O faturamento demonstra picos expressivos em períodos específicos de campanhas promocionais, seguidos por estabilizações consistentes ao longo do ano analisado.
* *(Dica: Insira o print do seu gráfico de faturamento aqui abaixo)*
<!-- ![Faturamento Mensal](imagens/faturamento_mensal.png) -->

### B. Concentração de Receita por Categoria
* **Descoberta:** As 5 principais categorias de produtos representam uma fatia expressiva de todo o faturamento bruto da plataforma, evidenciando uma alta dependência desses nichos para a saúde financeira do e-commerce.
* *(Dica: Insira o print do seu gráfico de barras horizontais aqui abaixo)*
<!-- ![Top Categorias](imagens/top_categorias.png) -->

### C. O Preço do Atraso Logístico
* **Descoberta:** Há uma correlação direta e severa entre o cumprimento do prazo de entrega e a nota de avaliação do cliente. Pedidos entregues no prazo mantêm médias de satisfação consistentemente altas ($\approx 4.2+$), enquanto pedidos que sofrem **qualquer dia de atraso** enfrentam quedas drásticas na avaliação.

---

## 🚀 5. Como Executar o Projeto
Se você deseja baixar e rodar este código no seu computador ou no Google Colab:

1. Clone este repositório ou faça o download dos arquivos:
   ```bash
   git clone [https://github.com/SEU-USUARIO/analise-ecommerce-olist.git](https://github.com/SEU-USUARIO/analise-ecommerce-olist.git)
