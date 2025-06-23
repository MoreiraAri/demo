# 🔐 API de Autenticação JWT com Spring Boot

## 📌 Descrição

API RESTful para autenticação via JWT, desenvolvida com Spring Boot. Oferece:

- Segurança via Spring Security + JWT
- Usuários em banco H2 em memória
- Documentação automática via Swagger UI
- Testes de carga com Apache JMeter

---

## ⚙️ Funcionalidades

- Login com geração de token JWT
- Validação de token
- Rotas protegidas por autenticação
- Console H2 para inspeção do banco
- Interface Swagger para testar a API

---

## 🛠 Tecnologias

- Java 17+
- Spring Boot 3.x
- Spring Security
- JWT (Auth0)
- H2 Database (in-memory)
- Maven
- Swagger/OpenAPI
- Apache JMeter (teste de carga)

---

## 🚀 Como Rodar o Projeto

### Passo 1 - Clonar repositório

```bash
git clone https://github.com/seu-usuario/seu-repositorio.git
cd seu-repositorio
Passo 2 - Build e execução
bash
Copiar
Editar
./mvnw spring-boot:run
Ou execute a classe principal DemoApplication na IDE.

⚙️ Configurações importantes
Porta padrão
A aplicação roda em http://localhost:8080.

Banco H2
Console acessível em:
http://localhost:8080/h2-console


Usuário: sa
Senha: (deixe em branco)

📌 Endpoints principais
Endpoint	Método	Descrição	Acesso
/auth/login	POST	Realiza login e gera JWT	Público
/auth/validate	POST	Valida token JWT	Público
/swagger-ui.html	GET	Documentação interativa Swagger	Público
Outros endpoints	—	Protegidos via JWT	Autenticados

📚 Documentação Swagger UI
Acesse em:
http://localhost:8080/swagger-ui.html


🗄 Banco de Dados H2
O banco está configurado para rodar em memória.
O console é útil para visualizar os dados e a estrutura.

🧪 Testes Automatizados (JUnit)
Os testes estão na pasta:
src/test/java/com/api/demo/

Execute-os via IDE ou comando Maven:

bash
Copiar
Editar
./mvnw test
⚡ Testes de Carga com JMeter
Arquivo de teste de carga:
jmeter-tests/login_stress_test.jmx

Como usar:
Abra o Apache JMeter

Importe o arquivo .jmx

Execute o teste e analise os resultados nos listeners "View Results Tree" e "Summary Report"

📁 Estrutura do Projeto
swift
Copiar
Editar
src/
├── main/
│   ├── java/com/api/demo/
│   │   ├── controller/
│   │   ├── config/
│   │   ├── model/
│   │   ├── repository/
│   │   ├── service/
│   ├── resources/
│       ├── application.yml
│
├── test/
│   └── java/com/api/demo/
│       └── (Testes JUnit)
├── jmeter-tests/
│   └── login_stress_test.jmx
