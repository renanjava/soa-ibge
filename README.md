# 📈 Sistema SOA - Análise de Tendência de Nomes no Brasil

Este projeto tem como objetivo desenvolver um sistema orientado a serviços (SOA) que consome a [API pública de nomes do IBGE](https://servicodados.ibge.gov.br/api/docs) para fornecer análises de tendências de nomes próprios no Brasil desde a década de 1930.

## 🎯 Objetivo

Demonstrar, na prática, os conceitos de **arquitetura orientada a serviços (SOA)**, como:
- Separação de responsabilidades
- Reutilização de componentes
- Comunicação via REST
- Baixo acoplamento e alta coesão

---

## 🧩 Funcionalidades

### 1. 📊 Evolução do Ranking de um Nome
- O usuário informa um nome e seleciona o intervalo de décadas.
- O sistema exibe um **gráfico de linha** mostrando a posição do nome ao longo do tempo.

### 2. 🗺️ Ranking de Nomes por Localidade
- O usuário escolhe uma **UF** ou **município**.
- O sistema exibe os **três nomes mais populares** por década na localidade.
- Os dados são apresentados em uma **tabela interativa**.

### 3. ⚖️ Comparação de Dois Nomes (Brasil)
- O usuário informa dois nomes.
- O sistema exibe um **gráfico comparativo** de popularidade desde a década de 1930.

---

## 🏛️ Arquitetura SOA

O sistema é dividido em três principais componentes orientados a serviços:

### 1. **Interface do Usuário (Frontend)**
- Desenvolvido com HTML/CSS/JavaScript ou framework como React.
- Responsável por interagir com os serviços via REST.

### 2. **Serviço de Agregação e Processamento (Backend)**
- Desenvolvido com Node.js/Express (ou outro de sua preferência).
- Responsável por consumir a API do IBGE, processar e transformar os dados.
- Expõe endpoints REST para o frontend.

### 3. **Serviço Externo**
- API pública de nomes do IBGE.
- Fonte oficial de dados demográficos usados pelas demais camadas do sistema.

---

## 🔧 Tecnologias Utilizadas

- 🟨 JavaScript / TypeScript
- 🧰 Node.js + Express
- 🌐 HTML, CSS e JS (ou React)
- 📊 Chart.js (ou D3.js, Google Charts)
- 📡 REST APIs
- 🧪 Axios ou Fetch API
- 🛠️ Vite / Webpack (opcional)

---

## ▶️ Como Executar o Projeto

### 1. Clone o repositório:
```bash
git clone https://github.com/seu-usuario/nome-do-repositorio.git
cd nome-do-repositorio
```

### 2. Instale as dependências:
```bash
npm install
```

### 3. Inicie o backend:
```bash
npm run start:server
```

### 4. Inicie o frontend:
```bash
npm run start:client
```

> Acesse `http://localhost:3000` no navegador para utilizar o sistema.

---

## 📁 Estrutura de Pastas

```
/soa-nomes-ibge
├── /client         # Interface do usuário
├── /server         # API intermediária (Backend)
├── /services       # Lógica de integração com o IBGE
├── README.md       # Este arquivo
└── package.json
```

---

## 📌 Como Aplicamos SOA

| Elemento         | Descrição |
|------------------|-----------|
| **Serviços**     | A aplicação foi dividida em serviços REST que consomem a API do IBGE, processam os dados e retornam ao cliente de forma desacoplada. |
| **Reutilização** | Os serviços podem ser reutilizados por outras interfaces ou até outros sistemas. |
| **Desacoplamento** | O frontend apenas consome dados processados pelo backend, sem conhecer os detalhes da API do IBGE. |
| **Interoperabilidade** | Comunicação via HTTP/JSON permite interoperabilidade entre tecnologias diferentes. |

---

## 📽️ Pitch de Apresentação (13/05/2025)

Durante o pitch de até 5 minutos, abordaremos:
- Processo de desenvolvimento e divisão de responsabilidades
- Desafios encontrados na integração com a API do IBGE
- Demonstração das três funcionalidades
- Aplicação prática dos conceitos de SOA

---

## 🧑‍🤝‍🧑 Integrantes

- Fulano da Silva - RMXXXXXX
- Ciclano Pereira - RMXXXXXX
- Beltrano Souza - RMXXXXXX

---

## 📜 Licença

Este projeto está licenciado sob a [MIT License](LICENSE).

---

## 📎 Referências

- [API de Nomes do IBGE - Documentação Oficial](https://servicodados.ibge.gov.br/api/docs)
- [Chart.js](https://www.chartjs.org/)
- [MDN Web Docs - Fetch API](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API)