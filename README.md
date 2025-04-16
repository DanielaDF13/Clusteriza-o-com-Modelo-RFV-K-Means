# 📊 Clusterização de Clientes com Modelo RFV + K-Means

Este é um aplicativo interativo desenvolvido com **Streamlit** que permite segmentar clientes com base no modelo **RFV (Recência, Frequência, Valor)** e o algoritmo de **clusterização K-Means**.

O objetivo é ajudar negócios a entenderem melhor seus clientes por meio da análise de comportamento de compra, possibilitando ações mais estratégicas de marketing, retenção e fidelização.

---

## 🔍 O que é o modelo RFV?

O modelo **RFV (ou RFM em inglês: Recency, Frequency, Monetary)** é uma técnica de análise de clientes muito utilizada em marketing, baseada em três dimensões principais:

- **Recência (R):** Quantos dias se passaram desde a última compra do cliente.  
  - Quanto menor a recência, mais ativo é o cliente.

- **Frequência (F):** Quantas compras o cliente fez em um determinado período.  
  - Clientes mais frequentes são considerados mais engajados.

- **Valor (V):** Quanto o cliente gastou no total.  
  - Clientes que gastam mais têm maior valor para o negócio.

Esse modelo permite identificar **clientes valiosos, leais, inativos, promissores, em risco**, entre outros perfis, ajudando a personalizar estratégias e priorizar recursos.

---

## 🤖 O que é K-Means?

**K-Means** é um algoritmo de **aprendizado não supervisionado** usado para **clusterização** de dados. Ele agrupa pontos (clientes, no nosso caso) em **K grupos (clusters)** com base em similaridades.

### Como funciona:
1. Define-se o número de clusters `K`.
2. O algoritmo seleciona `K` centros (chamados de centróides) aleatoriamente.
3. Cada ponto (cliente) é atribuído ao centróide mais próximo.
4. Os centróides são recalculados com base nos pontos atribuídos.
5. O processo se repete até que os centróides se estabilizem.

### Por que usar no projeto?
- Permite **descobrir padrões de comportamento de clientes** sem a necessidade de rotulagem manual.
- Junto com o modelo RFV, ajuda a identificar segmentos como:
  - Clientes VIPs
  - Clientes recentes com baixo valor
  - Clientes inativos de alto valor
  - Clientes com frequência alta, mas gasto baixo

Além disso, o app implementa o **método do cotovelo** para sugerir o número ideal de clusters, tornando a análise mais objetiva.

---

##  Funcionalidades do App

- Upload de arquivos CSV com histórico de compras
- Cálculo automático das métricas **RFV**
- Clusterização dos clientes com o algoritmo **K-Means**
- Sugestão automática do número ideal de clusters via **método do cotovelo**
- Visualizações:
  - Tabela RFV
  - Clientes com seus respectivos clusters
  - Gráfico de dispersão (Recência x Valor e Frequência vs Valor)
  - Resumo estatístico por cluster
- Download dos dados clusterizados em CSV
