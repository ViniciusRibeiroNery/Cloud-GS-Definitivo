# SafeHeat - Backend Java

API Java desenvolvida para o projeto **SafeHeat**, parte da entrega do Global Solution FIAP. Esta aplicação fornece um CRUD completo e se conecta a um banco de dados Oracle, tudo rodando em containers Docker.

---

## 🚀 Tecnologias Utilizadas

- Java 21
- Spring Boot
- Maven
- Oracle Database
- Docker

---

## 📁 Estrutura do Projeto

```
Cloud GS/
│
├── safeheat-backend-java-main/
│   └── target/
│       └── safeheat-backend-java-0.0.1-SNAPSHOT.jar
│
└── Dockerfile
```

---

## ⚙️ Pré-requisitos

Antes de rodar a aplicação, certifique-se de ter instalado:

- [Docker](https://www.docker.com/)
- [Java 21](https://jdk.java.net/21/) (para build local)
- [Maven](https://maven.apache.org/) (para compilar o projeto)

---

## 🛠️ Como compilar o projeto

Se ainda não compilou o `.jar`, vá até a pasta do projeto e execute:

```bash
cd safeheat-backend-java-main
mvn clean package
```

Isso irá gerar o arquivo `safeheat-backend-java-0.0.1-SNAPSHOT.jar` na pasta `target/`.

---

## 🐳 Como rodar com Docker

1. No diretório raiz (`Cloud GS`), certifique-se de que o `Dockerfile` está presente.
2. Execute o build da imagem:

```bash
docker build -t safeheat-api .
```

3. Rode o container:

```bash
docker run -d -p 8080:8080 --name safeheat-container safeheat-api
```

---

## 🌐 Acessando a API

A API estará acessível em:

```
http://localhost:8080
```

### Exemplos de endpoints:

- `GET /api/usuarios`
- `POST /api/usuarios`
- `PUT /api/usuarios/{id}`
- `DELETE /api/usuarios/{id}`

*(Os endpoints variam conforme sua implementação — ajuste conforme necessário.)*

---

## 🧼 Comandos úteis

Parar o container:

```bash
docker stop safeheat-container
```

Remover o container:

```bash
docker rm safeheat-container
```

Ver logs do container:

```bash
docker logs safeheat-container
```

---

## 📌 Observação

- Certifique-se de que o banco Oracle esteja rodando (pode ser em outro container).
- O backend pode usar variáveis de ambiente e configurações externas — edite conforme necessário.

---

## 👨‍💻 Autor

##👥 Integrantes
Felipe Ulson Sora – RM555462 – @felipesora
Augusto Lope Lyra – RM558209 – @lopeslyra10
Vinicius Ribeiro Nery Costa – RM559165 – @ViniciusRibeiroNery

FIAP – Global Solution 2025.
