Spring Boot Demo API

Este projeto é uma aplicação simples desenvolvida em Spring Boot utilizando Spring Data JPA.
Ele expõe uma API REST para explorar conceitos básicos de criação, configuração e execução de serviços com Spring.

🚀 Tecnologias

Java 17+

Spring Boot

Spring Data JPA

H2 Database (memória)

📂 Estrutura do projeto

Demo → entidade mapeada com JPA

DemoRepository → interface que estende JpaRepository

DemoService → camada de serviço com regras básicas

DemoController → expõe endpoints REST

▶️ Como rodar o projeto
1. Clone o repositório
git clone https://github.com/HenricoHosaki/demo_spring_boot.git
cd demo_spring_boot

2. Compile e rode com Maven
./mvnw spring-boot:run


ou com Java direto:

./mvnw clean package
java -jar target/demo-0.0.1-SNAPSHOT.jar

🌐 Endpoints disponíveis
Buscar por ID
GET http://localhost:8080/demo/{id}

Criar novo registro
POST http://localhost:8080/demo
Content-Type: application/json

{
  "nome": "Exemplo",
  "descricao": "Primeiro registro"
}

Listar todos
GET http://localhost:8080/demo

📝 Observações

O banco H2 roda em memória.

Acesse o console em: http://localhost:8080/h2-console

JDBC URL: jdbc:h2:mem:testdb

User: sa

Password: (vazio)
