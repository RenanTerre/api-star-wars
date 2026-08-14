# 🌌 Star Wars API (SWAPI Integration / Custom API)

> API backend desenvolvida para consulta, gerenciamento e integração de dados do universo de Star Wars (personagens, planetas, naves e filmes).

---

## 📌 Sobre o Projeto

O **Star Wars API** é um serviço backend criado para fornecer dados estruturados do universo Star Wars. Ele permite consultar informações detalhadas sobre personagens (*people*), planetas (*planets*), naves (*starships*), veículos e filmes da franquia, servindo como base para aplicações web, mobile ou integrações de catálogo.

---

## 🚀 Tecnologias Utilizadas / Sugeridas

- **Linguagem / Runtime:** Node.js (TypeScript / JavaScript) / Python / Java
- **Framework Web:** Express / NestJS / FastAPI / Spring Boot
- **Consumo de API Externa:** Axios / Fetch API (Integração com SWAPI - The Star Wars API)
- **Banco de Dados:** MongoDB / PostgreSQL (para cache ou armazenamento próprio de favoritos/dados)
- **Documentação:** Swagger / OpenAPI
- **Testes:** Jest / PyTest / JUnit

---

## ⚙️ Funcionalidades

- [x] **Consulta de Personagens:** Busca e listagem de personagens (Jedi, Sith, caçadores de recompensa, etc.).
- [x] **Exploração de Planetas:** Detalhes sobre clima, terreno, população e localização.
- [x] **Naves e Veículos:** Especificações técnicas de naves espaciais e veículos da galáxia.
- [x] **Filtros e Busca:** Pesquisa por nome, espécie ou filmes de aparição.
- [x] **Cache de Dados:** Otimização de chamadas para APIs externas para alta performance.

---

## 🛠️ Como Executar o Projeto

### Pré-requisitos

Certifique-se de ter instalado em sua máquina:
- [Git](https://git-scm.com)
- Runtime correspondente ao projeto (ex: [Node.js](https://nodejs.org/) ou [Python 3.x](https://www.python.org/))

### Passo a Passo

1. **Clone o repositório:**
   ```bash
   git clone [https://github.com/RenanTerre/api-star-wars.git](https://github.com/RenanTerre/api-star-wars.git)
   cd api-star-wars

   Configure as Variáveis de Ambiente:
Crie um arquivo .env na raiz do projeto com base no .env.example:

cp .env.example .env

Instale as dependências:

Se for um projeto Node.js:
npm install

Se for projeto Python:
python -m venv venv
source venv/bin/activate  # No Windows: venv\Scripts\activate
pip install -r requirements.txt

Inicie o servidor:
npm run dev
# ou
python main.py

A API estará acessível por padrão em http://localhost:3000 (ou porta configurada no arquivo .env).

📂 Estrutura do Projeto Sugerida
api-star-wars/
├── src/
│   ├── controllers/    # Controladores de requisições e respostas
│   ├── services/       # Lógica de integração com SWAPI e regras de negócio
│   ├── models/         # Schemas e representação de entidades
│   ├── routes/         # Definição das rotas REST
│   └── utils/          # Handlers de erro e funções auxiliares
├── .env.example        # Modelo de variáveis de ambiente
├── package.json        # Dependências do projeto
└── README.md           # Documentação

📡 Endpoints Principais
GET /api/people Retorna a lista de personagens
GET /api/people/:id Retorna os detalhes de um personagem específico
GET /api/planets Lista os planetas do universo Star Wars
GET /api/starships Lista as naves registradas
GET /api/films Retorna os filmes e episódios da saga
