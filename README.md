# Planejamento do Projeto: API RESTful para E-commerce

Este repositório contém o planejamento e a documentação para o desenvolvimento de uma API RESTful para um sistema de e-commerce. O objetivo é criar uma API robusta, escalável e segura, seguindo as melhores práticas de desenvolvimento.

## Sumário
- [Objetivo do Projeto](#objetivo-do-projeto)
- [Tecnologias Escolhidas](#tecnologias-escolhidas)
- [Modelagem do Banco de Dados](#modelagem-do-banco-de-dados)
- [Endpoints da API](#endpoints-da-api)
- [Fluxo de Desenvolvimento](#fluxo-de-desenvolvimento)
- [Boas Práticas](#boas-práticas)
- [Referências e Recursos](#referências-e-recursos)
- [Como Contribuir](#como-contribuir)

## Objetivo do Projeto

Desenvolver uma API RESTful para um sistema de e-commerce que permita:
- Cadastro e gerenciamento de usuários.
- Listagem e gerenciamento de produtos.
- Funcionalidades de carrinho de compras.
- Processamento de pedidos e pagamentos.
- Autenticação e autorização segura.

## Tecnologias Escolhidas

- **Linguagem de Programação:** Node.js com Express.js.
- **Banco de Dados:** PostgreSQL (relacional) e MongoDB (NoSQL para flexibilidade).
- **Autenticação:** JWT (JSON Web Tokens).
- **Ferramentas de Teste:** Postman, Jest.
- **Documentação da API:** Swagger/OpenAPI.
- **Versionamento:** Git e GitHub.
- **Containerização:** Docker.
- **Implantação:** Heroku ou AWS.

## Modelagem do Banco de Dados

### Entidades Principais
**Usuários:**
- id, nome, email, senha, endereço, telefone.

**Produtos:**
- id, nome, descrição, preço, estoque, categoria_id.

**Categorias:**
- id, nome.

**Pedidos:**
- id, usuário_id, data, status.

**Itens do Pedido:**
- id, pedido_id, produto_id, quantidade, preço_unitário.

**Pagamentos:**
- id, pedido_id, método, status.

### Diagrama do Banco de Dados
([Link DB Diagram](https://drawsql.app/teams/luis-alves-1/diagrams/e-commerce))
<img src="drawSQL-image-export-2025-01-28.png">

## Endpoints da API

### Usuários
- `POST /api/users` - Criar usuário.
- `GET /api/users/{id}` - Obter detalhes do usuário.
- `PUT /api/users/{id}` - Atualizar usuário.
- `DELETE /api/users/{id}` - Deletar usuário.

### Produtos
- `GET /api/products` - Listar todos os produtos.
- `GET /api/products/{id}` - Obter detalhes de um produto.
- `POST /api/products` - Criar produto (admin apenas).
- `PUT /api/products/{id}` - Atualizar produto (admin apenas).

### Carrinho
- `POST /api/cart` - Adicionar item ao carrinho.
- `GET /api/cart` - Ver carrinho.
- `DELETE /api/cart/{item_id}` - Remover item do carrinho.

### Pedidos
- `POST /api/orders` - Criar pedido.
- `GET /api/orders/{id}` - Obter detalhes do pedido.
- `GET /api/orders/user/{user_id}` - Listar pedidos de um usuário.

### Pagamentos
- `POST /api/payments` - Processar pagamento.

## Fluxo de Desenvolvimento

1. **Configuração do Projeto:**
   - Inicializar o projeto com Node.js e Express.
   - Configurar o banco de dados e as migrações.
   
2. **Implementação dos Endpoints:**
   - Criar endpoints básicos (ex.: listar produtos).
   - Implementar autenticação e autorização.
   - Adicionar validações de dados.

3. **Testes:**
   - Escrever testes unitários e de integração com Jest.
   - Testar endpoints com Postman.

4. **Documentação:**
   - Documentar a API com Swagger/OpenAPI.
   - Incluir exemplos de requisições e respostas.

5. **Implantação:**
   - Configurar Docker para containerização.
   - Realizar deploy na nuvem (Heroku, AWS, etc.).

## Boas Práticas

### Segurança
- Usar HTTPS.
- Validar e sanitizar todas as entradas.
- Proteger contra SQL Injection e XSS.
- Armazenar senhas com hash (bcrypt).

### Performance
- Implementar paginação em listagens.
- Usar cache com Redis.

### Versionamento
- Versionar a API (ex.: `/api/v1/products`).

### Logs e Monitoramento
- Implementar logs para depuração.
- Usar ferramentas como Prometheus e Grafana para monitoramento.

## Referências e Recursos

- [Documentação do Express.js](https://expressjs.com)
- [Documentação do PostgreSQL](https://www.postgresql.org/docs/)
- [JWT Introduction](https://jwt.io/introduction)
- [Swagger/OpenAPI](https://swagger.io/specification/)
- [Docker Documentation](https://docs.docker.com)

## Como Contribuir

1. Faça um fork do repositório.
2. Crie uma branch para sua feature (`git checkout -b feature/nova-feature`).
3. Commit suas mudanças (`git commit -m 'Adiciona nova feature'`).
4. Push para a branch (`git push origin feature/nova-feature`).
5. Abra um Pull Request.

---

Desenvolvido por [Luis Alves]  
📧 **Contato:** [contato.alvesluis@gmail.com]  
🌐 **LinkedIn:** [luisalvessilva](https://www.linkedin.com/in/luisalvessilva/)
