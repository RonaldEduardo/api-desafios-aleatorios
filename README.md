
# 🎯 API de Desafios Aleatórios

Uma API poderosa para fornecer desafios técnicos aleatórios, construída com **Laravel** e **MongoDB**. Perfeita para desenvolvedores que buscam aprimorar suas habilidades com desafios diários e categorizados!

---

## 🚀 Funcionalidades Principais

- **Desafios Aleatórios** com a opção de filtros por nível de dificuldade e categoria.
- **Operações CRUD** completas para gerenciar desafios.
- **Estrutura Flexível e Escalável** com MongoDB e boas práticas de arquitetura.
- **Documentação e Testes Automatizados** para garantir confiabilidade.

---

## 🛠️ Tecnologias Utilizadas

- **PHP 8.1** com **Laravel 10**
- **MongoDB** como banco de dados NoSQL
- **Postman** ou **Insomnia** para testes de API

---

## 📦 Configuração do Projeto

### Passos para Configurar Localmente

1. **Clone o Repositório**:
   ```bash
   git clone https://github.com/seu-usuario/api-desafios.git
   cd api-desafios
   ```

2. **Instale as Dependências**:
   ```bash
   composer install
   ```

3. **Configure o MongoDB no `.env`**:
   - Configure o arquivo `.env` com as informações de acesso ao MongoDB:
     ```env
     DB_CONNECTION=mongodb
     DB_HOST=127.0.0.1
     DB_PORT=27017
     DB_DATABASE=api_desafios
     ```

4. **Gere a Chave da Aplicação**:
   ```bash
   php artisan key:generate
   ```

5. **Inicie o Servidor**:
   ```bash
   php artisan serve
   ```

---

## 📖 Documentação das Rotas

### Endpoints da API

| Método | Endpoint              | Descrição                              |
|--------|------------------------|----------------------------------------|
| GET    | `/api/desafios`       | Retorna todos os desafios.             |
| GET    | `/api/desafios/aleatorio` | Retorna um desafio aleatório, com filtros opcionais de nível e categoria. |
| POST   | `/api/desafios`       | Cria um novo desafio.                  |
| PUT    | `/api/desafios/{id}`   | Atualiza um desafio específico.        |
| DELETE | `/api/desafios/{id}`   | Remove um desafio específico.          |

### Exemplos de Chamadas

#### 1. Obter Desafios Aleatórios
- **GET** `/api/desafios/aleatorio`
- **Descrição**: Retorna um desafio aleatório. Use parâmetros opcionais `nivel` e `categoria` para filtrar.

  **Exemplo**:
  ```bash
  curl -X GET "http://127.0.0.1:8000/api/desafios/aleatorio?nivel=intermediario&categoria=backend"
  ```

#### 2. Criar Novo Desafio
- **POST** `/api/desafios`
- **Parâmetros**: `titulo`, `descricao`, `nivel`, `categoria`

  **Exemplo**:
  ```json
  {
      "titulo": "Desafio API REST",
      "descricao": "Construa uma API completa em Laravel",
      "nivel": "intermediario",
      "categoria": "backend"
  }
  ```

---

## 🎯 Estrutura de Desafios

Cada desafio possui os seguintes campos:

- **ID** (gerado automaticamente)
- **Título**: Nome do desafio
- **Descrição**: Explicação do que o desafio requer
- **Nível**: Nível de dificuldade (`iniciante`, `intermediario`, `avançado`)
- **Categoria**: Tipo de desafio (ex.: `frontend`, `backend`, `fullstack`)

---

## 🧪 Testes e Boas Práticas

### Estrutura e Boas Práticas

- **Responsabilidades Bem Definidas**: Toda a lógica de negócios fica nos controladores.
- **Validação de Dados**: Valide dados recebidos para garantir integridade.
- **Tratamento de Erros**: Tratamento adequado para respostas consistentes.

### Testes Recomendados

1. **Testes de Unidade** para cada método do `DesafioController`.
2. **Testes de Integração** para confirmar que a API se comunica corretamente com o MongoDB.
3. **Testes de Rotas** usando Postman ou Insomnia para verificar o funcionamento dos endpoints.

---

## 🌟 Funcionalidades Futuras

- **Autenticação JWT** para acesso seguro.
- **Cache** para otimizar o retorno de desafios aleatórios.
- **Ranking e Pontuação** para engajamento dos usuários.

---

## 📜 Licença

Este projeto é licenciado sob a [Licença MIT](LICENSE).

---

**Comece agora** explorando a API e praticando suas habilidades com desafios aleatórios todos os dias! 🚀
