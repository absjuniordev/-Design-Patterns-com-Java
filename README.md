# Projeto: Padrões de Projeto com Spring Boot

Este projeto exemplifica a implementação de alguns padrões de projeto utilizando o Spring Boot. O objetivo principal é demonstrar a criação de uma API REST que gerencia clientes e seus endereços, utilizando integração com a API ViaCEP para consulta de endereços a partir do CEP informado.

## Tecnologias Utilizadas

- **Java 17**: Linguagem de programação utilizada.
- **Spring Boot 3.3.4**: Framework principal para criação da API.
- **Spring Data JPA**: Utilizado para manipulação de dados e comunicação com o banco de dados.
- **H2 Database**: Banco de dados em memória, utilizado para desenvolvimento e testes.
- **OpenFeign**: Feign Client utilizado para integração com APIs externas, no caso, a API do ViaCEP.
- **Swagger (Springdoc OpenAPI)**: Ferramenta para documentação da API e realização de testes.
- **Maven**: Ferramenta de gerenciamento de dependências e build da aplicação.

## Funcionalidades

- **Cadastro de Clientes**: A API permite criar, listar, atualizar e deletar clientes.
- **Consulta de Endereços**: Ao cadastrar um cliente, o endereço é automaticamente preenchido a partir do CEP utilizando a API ViaCEP.
- **Integração com APIs externas**: Feito através do OpenFeign, a aplicação consulta os dados de endereço na API pública ViaCEP.
- **Documentação da API com Swagger**: Toda a documentação da API é gerada automaticamente pelo Swagger.

## Arquitetura e Padrões de Projeto

Este projeto segue uma estrutura de camadas com as seguintes abordagens:

- **Repository Pattern**: Utilizado para separar a lógica de persistência de dados em repositórios, facilitando a manutenção e a escalabilidade da aplicação.
- **Service Layer**: A lógica de negócios é implementada em uma camada de serviços, abstraindo as operações relacionadas a clientes e endereços.
- **Feign Client**: A integração com APIs externas (ViaCEP) é feita de maneira simples e desacoplada utilizando o Feign Client.
- **OpenAPI/Swagger**: Utilizado para expor a documentação da API REST, permitindo que seja explorada e testada facilmente.

## Como Executar o Projeto

### Pré-requisitos

- **Java 17** ou superior instalado.
- **Maven** instalado para gerenciamento de dependências.

### Passos para execução

1. Clone o repositório:
   ```bash
   git clone https://github.com/seu-usuario/lab-padroes-projeto-spring.git
   ```

2. Acesse o diretório do projeto:
   ```bash
   cd lab-padroes-projeto-spring
   ```

3. Execute a aplicação com Maven:
   ```bash
   mvn spring-boot:run
   ```

4. A aplicação estará disponível em:
   ```
   http://localhost:8080
   ```

## Acessando a Documentação da API

Após iniciar o projeto, a documentação interativa da API estará disponível no Swagger, acessível no seguinte endereço:
```
http://localhost:8080/swagger-ui/index.html
```
Através do Swagger, é possível visualizar todas as rotas disponíveis e testar as requisições diretamente na interface.



Os testes cobrem o funcionamento da aplicação, garantindo a integridade dos principais fluxos de negócio.
