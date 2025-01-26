# 📊 Análise de Heatmap de Transações de Pagamento PIX em Sistema POS

[![Python](https://img.shields.io/badge/Python-3.9%2B-blue?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![Pandas](https://img.shields.io/badge/Pandas-1.3.3-green?style=for-the-badge&logo=pandas&logoColor=white)](https://pandas.pydata.org/)
[![Flask](https://img.shields.io/badge/Flask-2.0.1-orange?style=for-the-badge&logo=flask&logoColor=white)](https://flask.palletsprojects.com/)
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-13.3-yellowgreen?style=for-the-badge&logo=postgresql&logoColor=white)](https://www.postgresql.org/)
[![Docker](https://img.shields.io/badge/Docker-🐳-blue?style=for-the-badge&logo=docker&logoColor=white)](https://www.docker.com/)
[![JWT](https://img.shields.io/badge/JWT-🔑-yellow?style=for-the-badge&logo=jsonwebtokens&logoColor=black)](https://jwt.io/)
[![Qdrant](https://img.shields.io/badge/Qdrant-🌐-lightgrey?style=for-the-badge&logo=dataverse&logoColor=black)](https://qdrant.tech/)
[![YAML](https://img.shields.io/badge/YAML-📜-purple?style=for-the-badge&logo=yaml&logoColor=white)](https://yaml.org/)

## 🚀 Introdução

Este projeto envolve a análise de **dados históricos** de um **sistema POS** após a implementação de **automação**. O foco está nas **transações de pagamento PIX**, examinando períodos de tempo e métricas para identificar padrões nos valores das transações.

Através do uso de **heatmaps**, podemos visualizar áreas de interesse, variando de valores de transação baixos a altos, e fornecer insights sobre indicadores-chave de desempenho. Os heatmaps utilizam um gradiente de cores que varia de **amarelo claro** 🌼, indicando valores baixos, a **laranja** 🍊 e **vermelho** 🔴, destacando áreas de maior concentração de transações.

---

## 🎯 Objetivos

Os principais objetivos desta análise são:

- **Avaliar o comportamento transacional** pós-automação em um ambiente POS.
- **Identificar anomalias** ou padrões nos valores das transações em vários períodos de tempo.
- **Apresentar insights visuais** através de heatmaps que auxiliem as partes interessadas a compreender rapidamente as tendências de transação e pontos de interesse.

---

## 🛠️ Stack Tecnológico

As seguintes tecnologias e bibliotecas foram utilizadas na análise e geração dos heatmaps:

- **Python 3.9+**: Linguagem de programação principal para análise de dados e visualizações.
- **Pandas** 📊: Biblioteca para manipulação e análise de dados.
- **Matplotlib & Seaborn** 🌈: Bibliotecas para geração de heatmaps e outros tipos de visualizações.
- **Numpy** ➗: Para computações numéricas.
- **Flask** 🚀: Framework backend para servir os dados e a API.
- **PostgreSQL** 🗄️: Banco de dados para armazenamento de dados de transação.
- **Docker** 🐳: Para conteinerização e consistência do ambiente.
- **Autenticação JWT** 🔑: Utilizada para proteger os endpoints da API que fornecem dados de transação.
- **Qdrant** 🌐: Para gerenciamento de banco de dados vetorial e consultas otimizadas.
- **YAML** 📜: Para gerenciamento de configuração de servidores e endpoints.

---

## 📈 Heatmaps

![mapa_calor_ociosidade_por_hora_loja](https://github.com/user-attachments/assets/355f8769-7ebc-43e8-b3fb-aedc858fe30c)

![mapa_calor_precos_baixos_por_hora_cidade](https://github.com/user-attachments/assets/d6456d74-a6f0-4684-951a-e09e71733f65)

![mapa_calor_tempo_medio_por_hora_cidade](https://github.com/user-attachments/assets/46675733-dcf7-42cd-9771-d90d04b2ea45)

![mapa_calor_precos_baixos_por_dia](https://github.com/user-attachments/assets/33bdb700-9e83-48db-848f-d4dc88e475d9)

![mapa_calor_tempo_medio_por_dia](https://github.com/user-attachments/assets/2bebe6fc-77d4-414b-b318-a5129c105169)

![mapa_calor_media_transacoes_por_dia](https://github.com/user-attachments/assets/7252bfd5-8c8a-4de3-85c0-293d4aaf0b1e)

![mapa_calor_minimos_por_dia](https://github.com/user-attachments/assets/641ed4ea-a7b5-4fce-8fb4-74b483daa0eb)

![mapa_calor_tempo_medio_por_semana](https://github.com/user-attachments/assets/746ec069-3f1e-4f18-b769-d043ae08ddfc)

![mapa_calor_minimos_por_semana](https://github.com/user-attachments/assets/eff1f167-a8bd-4fbb-8a3d-b41724bade87)

![mapa_calor_dia_mean](https://github.com/user-attachments/assets/89ac3c92-3eca-484d-880c-337f537a00e9)

![mapa_calor_dia_min](https://github.com/user-attachments/assets/75cc5141-a6be-4b06-b615-17ace33617a7)

---

## 🔄 Fluxo de Processamento de Dados

O pipeline de processamento de dados para esta análise segue estas etapas principais:

1. **Coleta de Dados** 📥: Os dados são extraídos do **banco de dados PostgreSQL**, que armazena todos os registros de transações PIX relevantes.

2. **Pré-processamento** 🧹: Os dados são limpos e formatados usando **Pandas**, garantindo que entradas ausentes ou inconsistentes sejam tratadas. Os recursos de data e hora também são processados para alinhar os dados no período de tempo.

3. **Cálculo de Métricas** 🔢:
   - **Transação Máxima Ajustada**: Calculada normalizando os valores das transações para levar em consideração a inflação ou alterações operacionais.
   - **Transação Mínima Ajustada**: Semelhante à máxima, mas com foco nos valores mais baixos.
   - **Transação Média**: Valor médio calculado para cada período de tempo.
   - **Transação Máxima e Mínima**: Métricas básicas que mostram extremos nos valores das transações.

4. **Visualização** 🎨: Usando **Matplotlib** e **Seaborn**, os dados limpos são passados para a função de heatmap para gerar as visualizações.
