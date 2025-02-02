# 📚 Sistema de Cadastro de Livros - Spring Boot

Apresento-lhes **Sistema de Cadastro de Livros**, um projeto desenvolvido com **Spring Boot** para gerenciamento de livros. Este sistema permite **criar, listar, atualizar e excluir livros** por meio de uma API RESTful.

## 🚀 Tecnologias Utilizadas

- **Spring Boot** - Framework principal
- **Spring Data JPA** - Gerenciamento do banco de dados
- **MySQL** - Banco de dados relacional
- **Swagger** - Documentação interativa da API

## 📌 Funcionalidades

✅ Criar um novo livro (título, autor, ano, gênero, ISBN)  
✅ Listar todos os livros cadastrados  
✅ Buscar um livro por ID  
✅ Atualizar informações de um livro  
✅ Excluir um livro do sistema  
✅ Documentação interativa com Swagger  

## 🔧 Configuração do Ambiente

1. Clone este repositório:
   ```bash
   git clone https://github.com/GremlinX/basic-spring-crud.git
   cd library
   ```

2. Configure o banco de dados SQL Server Management Studio (SSMS):
   - Crie um banco de dados (eu chamei de `library_db` quando implementei 😁)
   - Atualize o `application.properties` com suas credenciais do SSMS
   - OBS.: Atenção quanto as portas do SSMS pois isso pode te dar uma enorme dor de cabeça se você insistir na porta errada (Sim, eu tive 🥲)

3. Execute o projeto:
   ```bash
   mvn spring-boot:run
   ```
   Ou instale alguma IDE como Spring Tool Suite (STS) ou IntelliJ (Particularmente prefiro esta opção, pois posso brincar mais com debug)

4. Acesse a API no navegador ou Postman:
   - **Swagger:** [http://localhost:8080/swagger-ui.html](http://localhost:8080/swagger-ui.html)
   - **Endpoints REST:** `http://localhost:8080/api/books`

## 🛠 Exemplos de Uso (cURL)

### Criar um livro
```bash
curl -X POST "http://localhost:8080/api/books" -H "Content-Type: application/json" -d '{"title":"O Senhor dos Anéis", "author":"J.R.R. Tolkien", "publicationYear":1954, "genre":"Fantasia", "isbn":"978-1234567890"}'
```

### Listar todos os livros
```bash
curl -X GET "http://localhost:8080/api/books"
```

### Buscar um livro por ID
```bash
curl -X GET "http://localhost:8080/api/books/1"
```

### Atualizar um livro
```bash
curl -X PUT "http://localhost:8080/api/books/1" -H "Content-Type: application/json" -d '{"title":"O Hobbit", "author":"J.R.R. Tolkien", "publicationYear":1937, "genre":"Fantasia", "isbn":"978-9876543210"}'
```

### Excluir um livro
```bash
curl -X DELETE "http://localhost:8080/api/books/1"
```

## 📜 Licença
Este projeto está sob a licença MIT - sinta-se livre para usá-lo e modificá-lo como quiser! 😊

