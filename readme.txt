ANS Data Integration
Projeto desenvolvido em Python, SQL, Flask e Vue.js para coleta, processamento, armazenamento e disponibilização de dados públicos da Agência Nacional de Saúde Suplementar (ANS).
O projeto contempla desde a extração automatizada de documentos e tabelas até a criação de uma API e interface web para consulta das informações processadas.

Tecnologias Utilizadas
* Python
* Pandas
* Requests
* BeautifulSoup
* PDFPlumber
* MySQL
* Flask
* Vue.js
* Postman

Estrutura do Projeto
01_data_collection
Responsável pela coleta e transformação dos dados disponibilizados pela ANS.

pdf_downloader.py
* Realiza web scraping no portal da ANS.
* Localiza automaticamente os anexos publicados.
* Efetua o download dos arquivos PDF.
* Compacta os documentos em um arquivo ZIP.

pdf_table_extractor.py
* Extrai tabelas do Anexo I utilizando PDFPlumber.
* Realiza tratamento e limpeza dos dados extraídos.
* Substitui abreviações por descrições completas.
* Exporta os dados para CSV.
* Compacta o resultado em arquivo ZIP.


02_database
Responsável pela modelagem, carga e consulta dos dados.

estruturar_tabelas.sql
* Criação do banco de dados.
* Definição das tabelas e tipos de dados.
* Estruturação do modelo relacional.

importar_dados.sql
* Importação dos arquivos CSV para o MySQL.
* Tratamento e conversão de dados durante a carga.

busca_seletiva.sql
* Consultas analíticas sobre despesas de operadoras de saúde.
* Identificação das operadoras com maiores despesas médico-hospitalares.


03_api_and_frontend
Disponibilização dos dados através de API REST e interface web.

buscar_operadoras.py
* API desenvolvida em Flask.
* Consulta operadoras por Razão Social ou Nome Fantasia.
* Retorna resultados em formato JSON.

operadoras_interface
* Interface web desenvolvida em Vue.js.
* Permite pesquisar operadoras através da API.
* Exibe resultados de forma amigável ao usuário.
* Possui funcionalidade para exportação de coleção Postman.


Funcionalidades

* Coleta automatizada de documentos da ANS.
* Extração e transformação de dados em PDF.
* Armazenamento estruturado em banco de dados MySQL.
* Consultas SQL para análise das informações.
* API REST para busca de operadoras.
* Interface web para consulta dos dados.

---

## Objetivo

Demonstrar conhecimentos em coleta de dados, ETL, modelagem de banco de dados, desenvolvimento de APIs e construção de interfaces web utilizando tecnologias amplamente empregadas no mercado.
