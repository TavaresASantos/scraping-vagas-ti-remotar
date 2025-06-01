# scraping-vagas-ti-remotar

projeto que realiza o scraping automatizado de vagas na aréa tech do site REMOTAR


## objetivo

extrair informação relevantes de vagas de tech psotadas no site,
armazená-las em formato CSV e integrá-las com ferramentas de visualização para análise exploratória, como:



- Principais tecnologias demandadas
- Empresas que mais contratam
- Tipos de contratação (PJ, CLT, Freelance)
- Frequência de novas vagas
- Localização e modalidade (Remoto, Híbrido, Presencial)

---

##  Tecnologias e Ferramentas

- [n8n](https://n8n.io/) – Para automação do scraping
- HTML Extract / HTTP Request Nodes
- Google Drive / CSV Writer
- [Power BI](https://powerbi.microsoft.com/) – Para análise e visualização de dados
- GitHub – Para versionamento e documentação do projeto

---

##  Estrutura do Projeto



scraping-vagas-ti-remotar/

├── docs/ → Imagens, capturas de tela

├── fluxo-n8n/ → Arquivo .json do fluxo pronto

├── datasets/ → Arquivos CSV exportados

├── dashboards/ → Arquivos .pbix do Power BI

├── README.md → Este arquivo



---

##  Funcionamento do Fluxo no n8n

1. `HTTP Request`: acessa a página principal do Remotar
2. `HTML Extract`: captura os blocos de vagas (título, empresa, local, tags, link)
3. `Set`: organiza os dados em formato tabular
4. `Spreadsheet File`: exporta para CSV
5. `Google Drive`: envia o CSV para nuvem
6. `Cron`: agenda execuções automáticas (ex: todo dia às 8h)

---

##  Power BI

O CSV gerado pode ser importado no Power BI para criar visualizações como:

- Vagas por tecnologia
- Vagas por tipo de contratação
- Frequência semanal de novas vagas
- Empresas mais ativas

---

##  Agendamento

O fluxo pode ser executado automaticamente todos os dias utilizando o nó `Cron` do n8n, permitindo análises temporais (ex: evolução das vagas ao longo do tempo).

---

##  Avisos

- Este projeto utiliza scraping de site público com fins educacionais e não viola autenticação, cookies ou políticas comerciais.
- Consulte os termos de uso do site caso deseje uso em produção.

---

##  Autora

Amanda Tavares – [tavaresamandasantos@hotmail.com](mailto:tavaresamandasantos@hotmail.com)  
Graduanda em Sistemas de Informação – IFBaiano  
Interesse em ciência de dados, tecnologia e 

---
