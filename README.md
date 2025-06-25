# 📈 Ranking de Fundos de Investimento (CVM) – Streamlit App

Este projeto é uma aplicação interativa desenvolvida com **Streamlit** para **analisar e ranquear fundos de investimento brasileiros**, com base nos dados públicos fornecidos pela **CVM (Comissão de Valores Mobiliários)** e no **CDI** via Banco Central (SGS).

## 🔎 Funcionalidades

* Leitura automatizada dos **cadastros de fundos** e **informes diários da CVM**.
* Análise de performance com base em:

  * Retorno acumulado
  * Drawdown (tabela e gráfico)
  * Índice de Sharpe ajustado ao CDI
* Filtros por:

  * Período de análise
  * Quantidade mínima de cotistas
  * Classe do fundo (Multimercado, Ações, Renda Fixa, Cambial)
  * Quantidade de fundos exibidos

## 🧪 Tecnologias Utilizadas

* [Streamlit](https://streamlit.io/)
* [Pandas](https://pandas.pydata.org/)
* [Matplotlib](https://matplotlib.org/)
* [PyFolio](https://github.com/quantopian/pyfolio)
* [Empyrical](https://github.com/quantopian/empyrical)
* Módulo `sgs` para séries temporais do Banco Central do Brasil

## 📁 Estrutura esperada de arquivos

Certifique-se de ter os seguintes arquivos na raiz do projeto:

* `cad_fi.csv`: Cadastro de fundos da CVM
* `inf_diario_fi_202501.zip`: Informes diários do mês desejado (atualmente fixado em Janeiro/2025)

> ⚠️ Caso deseje analisar outros períodos, será necessário modificar o nome do arquivo dentro da função `busca_informes_diarios_cvm_por_periodo()`.

## ▶️ Como executar

### 1. Clone o repositório

```bash
git clone https://github.com/seu-usuario/nome-do-repo.git
cd nome-do-repo
```

### 2. (Opcional) Crie um ambiente virtual

```bash
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate
```

### 3. Instale as dependências

```bash
pip install -r requirements.txt
```

Se você ainda não possui o módulo `sgs`, instale manualmente:

```bash
pip install sgs
```

### 4. Execute o aplicativo

```bash
streamlit run app.py  # substitua pelo nome do arquivo, se necessário
```

## 🧮 Exemplo de uso

1. Selecione a **data inicial** e **final** da análise no menu lateral.
2. Escolha a **quantidade de fundos** que deseja exibir.
3. Defina um número mínimo de cotistas.
4. Filtre por **classe de fundo**, se desejar.
5. Clique em **"Buscar e Analisar"**.
6. Veja os resultados com gráficos de drawdown e métricas de retorno e risco.

## ✅ Saída esperada

* Tabela com os melhores fundos, exibindo:

  * Nome
  * Classe
  * Retorno acumulado
  * Patrimônio líquido (PL)
  * Índice de Sharpe (ajustado pelo CDI)
* Tabelas e gráficos de **drawdown**

## ⚠️ Observações

* O código atualmente processa apenas o arquivo `inf_diario_fi_202501.zip`.
* A aplicação ignora fundos **fora de funcionamento normal**.
* Requer conexão com a internet para acessar o CDI via Banco Central (SGS).

## 📜 Licença

Este projeto está licenciado sob a Licença MIT.
