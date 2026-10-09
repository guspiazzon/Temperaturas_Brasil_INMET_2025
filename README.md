# Temperaturas_Brasil_INMET_2025
Um painel em Tableau com as temperaturas registradas pelo INMET em 2025 no Brasil

# 🌡️ Análise Metrológica: Extremos de Temperatura no Brasil (INMET 2025)

## 📌 Visão Geral do Projeto
Este projeto analisa os dados meteorológicos históricos do Instituto Nacional de Meteorologia (**INMET**) referentes ao ano de 2025, mapeando os recordes e extremos de temperatura registrados em municípios por todo o Brasil.

O objetivo do painel interativo é permitir a navegação geográfica e temporal para identificar o comportamento das temperaturas mínimas e máximas ao longo do ano.

🔗 **[Acesse o Dashboard Interativo no Tableau Public] https://public.tableau.com/app/profile/gustavo.piazzon.torres/viz/dash_temperaturas/Painel1?publish=yes**

---

## 📊 Estrutura do Dashboard
O painel é composto por 4 visualizações geográficas (mapas de pontos por cidade com gradiente de cor do mais frio ao mais quente):

1. **Menor Temperatura Mínima:** Cidades e datas com as menores marcas registradas no ano.
2. **Maior Temperatura Mínima:** Regiões onde mesmo nas estações mais frias os dias foram mais quentes.
3. **Menor Temperatura Máxima:** Dias atípicos ou regiões onde as tardes registraram as menores máximas.
4. **Maior Temperatura Máxima:** Picos absolutos de calor por município.

---

## 🛠️ Recursos e Lógicas Aplicadas no Tableau

* **Agregações Mapeadas:** Uso de funções de agregação (`MIN`, `MAX`) para consolidar os registros por estação/cidade.
* **Tratamento de Datas:** Criação de campo calculado (`CASE` / `SWITCH`) para converter a numeração dos meses em nomes extensos (ex: `1` → `Janeiro`), facilitando a experiência do usuário.
* **Interatividade e Filtros no Painel:**
  * **Filtro por Estado (UF):** Permite isolar regiões específicas.
  * **Filtro Temporal por Mês:** Análise sazonal ao longo de 2025.
  * **Slicer Range de Temperatura:** Controle de intervalo contínuo do menor ao maior valor registrado.
  * **Mapas Geográficos:** Gradiente térmico ajustado (azul ao vermelho) para rápida leitura visual.

---

## 📂 Estrutura do Repositório

```text
├── data/                  # Base de dados ou extrato consolidado do INMET 2025
├── dashboard/             # Arquivo .twbx do Tableau
├── img/                   # Screenshots do painel para exibição no README
└── README.md              # Documentação completa do projeto
