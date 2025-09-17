# 📌 CRUD de Cadastro de Usuário - Java Spring Boot  

Este projeto é um sistema simples de **CRUD (Create, Read, Update, Delete)** para gerenciamento de usuários, desenvolvido com **Java 23** e **Spring Boot**.  

## 🚀 Tecnologias Utilizadas  
- ☕ **Java 23 (JDK 23)**  
- 🌱 **Spring Boot**  
- 🗄️ **H2 Database**  
- 🔗 **Spring Data JPA**  
- 📝 **Lombok**  
- 📦 **Maven**  

## 📂 Estrutura do Projeto  


```text
cadastro-usuario
├─ src
│  └─ main
│     └─ java
│        └─ com
│           └─ projeto
│              └─ cadastro_usuario
│                 ├─ controller       # Endpoints REST
│                 │   └─ UsuarioController.java
│                 ├─ business         # Lógica de negócio (Service)
│                 │   └─ UsuarioService.java
│                 └─ infrastructure
│                     ├─ entitys      # Entidades
│                     │   └─ Usuario.java
│                     └─ repository   # Repositórios (Spring Data JPA)
│                         └─ UsuarioRepository.java
├─ resources
│  ├─ application.properties         # Configurações do Spring Boot
│  └─ data.sql                        # (Opcional) script inicial de banco de dados
└─ CadastroUsuarioApplication.java    # Classe principal para iniciar a aplicação
```


## 🛠️ Endpoints da API  

| Método | Endpoint        | Descrição |
|--------|----------------|------------|
| `POST` | `/usuario`     | Cadastrar novo usuário |
| `GET`  | `/usuario`     | Listar todos os usuários |
| `GET`  | `/usuario/{id}` | Buscar usuário por ID |
| `PUT`  | `/usuario/{id}` | Atualizar usuário |
| `DELETE` | `/usuario/{id}` | Deletar usuário |

### 📌 Exemplo de JSON para cadastro (`POST /usuario`)  
```json
{
  "nome": "João da Silva",
  "email": "joao.silva@email.com",
  "senha": "123456"
}
