Claro! Abaixo está um exemplo de um arquivo `README.md` para o seu projeto Streamlit. Esse arquivo explica o propósito da aplicação, como utilizá-la, os requisitos e como executá-la localmente.

---

# 📊 Ranking de Fundos de Investimento - Streamlit App

Esta aplicação em **Streamlit** permite analisar e classificar os melhores **fundos de investimento** registrados na CVM com base em dados públicos, utilizando métricas como retorno, drawdown e índice de Sharpe ajustado pelo CDI.

## 🔍 Funcionalidades

* Busca automática de **fundos em funcionamento normal**.
* Filtro por **classe de fundos**: Multimercado, Ações, Renda Fixa e Cambial.
* Filtragem por **mínimo de cotistas**.
* Seleção de **período de análise**.
* Análise de performance com:

  * Retorno acumulado
  * Drawdown (com gráfico e tabela)
  * Índice de Sharpe ajustado ao CDI
* Visualização dos melhores fundos com gráficos e métricas.

## 🛠️ Tecnologias utilizadas

* [Streamlit](https://streamlit.io/)
* [PyFolio](https://github.com/quantopian/pyfolio)
* [Empyrical](https://github.com/quantopian/empyrical)
* [Pandas](https://pandas.pydata.org/)
* [Matplotlib](https://matplotlib.org/)
* Módulo `sgs` (interface para séries temporais do Banco Central do Brasil)

## ▶️ Como executar

1. **Clone o repositório**:

   ```bash
   git clone https://github.com/seuusuario/nome-do-repo.git
   cd nome-do-repo
   ```

2. **Crie um ambiente virtual (opcional, mas recomendado)**:

   ```bash
   python -m venv venv
   source venv/bin/activate  # no Windows: venv\Scripts\activate
   ```

3. **Instale as dependências**:

   ```bash
   pip install -r requirements.txt
   ```

4. **Execute o app Streamlit**:

   ```bash
   streamlit run nome_do_arquivo.py
   ```

## 📁 Estrutura esperada dos dados

* **cad\_fi.csv**: Cadastro dos fundos, disponível no site da CVM.
* **inf\_diario\_fi\_202501.zip**: Informes diários da CVM para o mês desejado.

  * ⚠️ Atualmente o código está fixo para o arquivo de **Janeiro/2025**. Para outros períodos, é necessário adaptar a URL.

## 📌 Observações

* Os dados de CDI são obtidos diretamente via API do **Banco Central (SGS)**.
* A função `melhores_fundos()` utiliza o retorno da cota para classificar os fundos.
* Os gráficos de drawdown são gerados via `pyfolio`.

## ✅ Exemplo de uso

1. Selecione a **data de início e fim**.
2. Escolha a **quantidade de fundos** e o número mínimo de cotistas.
3. Opcionalmente, filtre por **classe de fundos**.
4. Clique em **"Buscar e Analisar"** para visualizar os fundos com melhor performance.

---

## 📄 Licença

Este projeto é open-source, sob licença [MIT](LICENSE).

