Desafio Técnico: API de Desafios Aleatórios
Este projeto consiste em uma API desenvolvida em Laravel para fornecer desafios aleatórios ao usuário. Abaixo estão as tarefas e requisitos para melhorar a API, implementar boas práticas e realizar testes de funcionalidade.

Objetivo
Implementar uma API que forneça desafios aleatórios para o usuário.
Aplicar boas práticas de desenvolvimento, incluindo organização de rotas, arquitetura REST e tratamento de erros.
Utilizar um banco de dados MongoDB para armazenar e gerenciar desafios de forma dinâmica.
Requisitos de Implementação
1. Configuração Básica
 Configure um banco de dados MongoDB com uma coleção desafios.
 Insira alguns desafios de exemplo no banco de dados, cada um com os campos id, titulo, descricao, nivel (iniciante, intermediário, avançado) e categoria.
2. Estrutura das Rotas
Crie as seguintes rotas RESTful para gerenciar e obter desafios:

Rotas para Operações CRUD (Desafios)
GET /api/desafios
Retorna uma lista de todos os desafios disponíveis.

POST /api/desafios
Permite a criação de um novo desafio. Valide os dados para garantir que titulo, descricao, nivel e categoria estão presentes e possuem valores aceitáveis.

PUT /api/desafios/{id}
Atualiza um desafio existente baseado em seu id. Certifique-se de validar os dados recebidos.

DELETE /api/desafios/{id}
Remove um desafio específico pelo id.

Rota para Desafio Aleatório
GET /api/desafios/aleatorio
Retorna um desafio aleatório da coleção desafios. Considere aplicar filtros de nivel ou categoria usando parâmetros de query (opcional).
3. Boas Práticas de Desenvolvimento
 Divisão de responsabilidades: Coloque a lógica de negócios no controlador DesafioController e utilize serviços ou repositórios se necessário para separar o acesso ao banco de dados.
 Validação de Dados: Utilize Form Request Validation do Laravel para validar as entradas nas rotas POST e PUT.
 Tratamento de Erros: Implemente tratamento de erros para garantir que respostas adequadas sejam retornadas em caso de dados inválidos ou falha ao acessar o banco de dados.
 Organização das Rotas: Use o agrupamento de rotas com prefixo desafios para manter o código limpo e organizado.
 Documentação: Documente as rotas usando um padrão, como OpenAPI, para facilitar o entendimento e uso da API.
4. Testes
Implemente testes automatizados para garantir que a API funcione corretamente:

 Testes de Unidade: Crie testes para validar a lógica dos métodos no DesafioController.
 Testes de Integração: Implemente testes para garantir que a API retorne os dados corretos ao acessar o MongoDB.
 Testes de API com HTTP: Teste as rotas principais (/desafios, /desafios/aleatorio, etc.) para validar respostas esperadas e tratamento de erros.
5. Extra: Melhorias Adicionais
Implemente as seguintes melhorias para um projeto mais robusto:

 Filtros e Paginação: Adicione parâmetros de query para filtrar desafios por nivel ou categoria, e implemente paginação na rota GET /api/desafios.
 Autenticação Básica: Proteja as rotas de criação, atualização e exclusão usando autenticação baseada em token (JWT ou Laravel Sanctum).
 Cache: Implemente cache para a rota /api/desafios/aleatorio para melhorar o desempenho em caso de acessos frequentes.
