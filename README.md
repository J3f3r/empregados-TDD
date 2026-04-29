# Projeto Empregados TDD (Employees TDD)


### Descrição
Este projeto foi desenvolvido para praticar o desenvolvimento orientado a testes (TDD) utilizando o ecossistema Spring Boot. O objetivo principal foi implementar um sistema de gerenciamento de empregados e departamentos, garantindo a integridade das camadas de serviço e controladores através de testes unitários e de integração.

### Tecnologias Utilizadas
- **Java 17**
- **Spring Boot 3**
- **Spring Data JPA**
- **H2 Database** (Banco de dados em memória para testes)
- **JUnit 5 & Mockito** (Testes)
- **Maven**

### O que foi implementado
- **Camada Web:** Endpoints REST para listagem paginada e inserção de registros.
- **Camada de Serviço:** Lógica de negócio e mapeamento DTO.
- **Testes Unitários:** Validação de comportamentos isolados com Mockito.
- **Testes de Integração:** Validação do fluxo completo (Controller -> Service -> Repository -> DB).

### Desafios Superados
O maior desafio foi a transição dos testes unitários (Mocks) para os testes de integração. Lidar com a persistência real no H2 exigiu uma atenção rigorosa à ordenação alfabética dos dados (conforme definido no `import.sql`) e à matemática da paginação do Spring Data, garantindo que os asserts de `totalElements` e índices de conteúdo estivessem sincronizados com o estado do banco.

---


### Description
This project was developed to practice Test-Driven Development (TDD) using the Spring Boot ecosystem. The main goal was to implement an employee and department management system, ensuring the integrity of the service and controller layers through unit and integration tests.

### Technologies
- **Java 17**
- **Spring Boot 3**
- **Spring Data JPA**
- **H2 Database** (In-memory database for testing)
- **JUnit 5 & Mockito** (Testing)
- **Maven**

### Features Implemented
- **Web Layer:** REST endpoints for paginated listing and record insertion.
- **Service Layer:** Business logic and DTO mapping.
- **Unit Tests:** Validation of isolated behaviors using Mockito.
- **Integration Tests:** Validation of the full flow (Controller -> Service -> Repository -> DB).

### Key Challenges
The biggest challenge was transitioning from unit tests (Mocks) to integration tests. Dealing with real persistence in H2 required strict attention to the alphabetical ordering of data (as defined in `import.sql`) and Spring Data's pagination math, ensuring that `totalElements` asserts and content indexes were synchronized with the database state.

---

## 🚀 Como executar / How to run
1. Clone o repositório / Clone the repository.
2. Importe como projeto Maven no STS/IntelliJ / Import as a Maven project.
3. Para rodar os testes / To run tests: `Right click on project -> Run As -> JUnit Test`.