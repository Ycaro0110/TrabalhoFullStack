# Sistema de Gerenciamento de Tarefas

Este é um sistema de gerenciamento de tarefas full-stack que permite aos usuários criar, ler, atualizar e deletar tarefas (CRUD). O projeto é dividido em duas partes principais: um backend desenvolvido em Java com Spring Boot e um frontend desenvolvido em HTML, CSS e JavaScript puro.

## Estrutura do Projeto

```
TrabalhoFullStack/
├── backend/                 # Aplicação Spring Boot
│   ├── src/
│   │   └── main/
│   │       ├── java/       # Código fonte Java
│   │       └── resources/  # Configurações
│   └── pom.xml            # Dependências Maven
└── frontend/              # Interface do usuário
    ├── app.js            # Lógica JavaScript
    ├── index.html       # Estrutura HTML
    └── styles.css       # Estilos CSS
```

## Backend

### Tecnologias Utilizadas

- Java
- Spring Boot
- Spring Data JPA
- H2 Database (banco de dados em memória)
- Maven

### Estrutura do Backend

- **Controller**: Gerencia as requisições HTTP
- **Service**: Contém a lógica de negócio
- **Repository**: Interface com o banco de dados
- **Model**: Entidade Task que representa uma tarefa

### API Endpoints

| Método | Endpoint | Descrição |
|--------|----------|-----------|
| GET    | /tasks   | Lista todas as tarefas |
| POST   | /tasks   | Cria uma nova tarefa |
| PUT    | /tasks   | Atualiza uma tarefa existente |
| DELETE | /tasks/{id} | Remove uma tarefa |

### Modelo de Dados (Task)

```java
{
    "id": long,
    "name": String,
    "description": String,
    "status": boolean
}
```

## Frontend

### Tecnologias Utilizadas

- HTML5
- CSS3
- JavaScript (Vanilla)

### Funcionalidades

- Interface intuitiva para gerenciamento de tarefas
- Formulário para adicionar/editar tarefas
- Lista de tarefas com opções de edição e exclusão
- Marcação de status de conclusão
- Design responsivo

## Como Executar o Projeto

### Backend

1. Navegue até a pasta do backend:
   ```bash
   cd backend
   ```

2. Execute o projeto usando Maven:
   ```bash
   ./mvnw spring-boot:run
   ```
   O servidor será iniciado na porta 8080.

### Frontend

1. Navegue até a pasta do frontend:
   ```bash
   cd frontend
   ```

2. Abra o arquivo `index.html` em um navegador web
   - Para desenvolvimento, recomenda-se usar um servidor local como Live Server

## Funcionalidades Principais

- Criar novas tarefas com nome, descrição e status
- Visualizar lista de todas as tarefas
- Editar tarefas existentes
- Excluir tarefas
- Marcar tarefas como concluídas/pendentes

## Contribuição

Para contribuir com o projeto:

1. Faça um fork do repositório
2. Crie uma branch para sua feature (`git checkout -b feature/NovaFeature`)
3. Commit suas mudanças (`git commit -m 'Adicionando nova feature'`)
4. Push para a branch (`git push origin feature/NovaFeature`)
5. Abra um Pull Request

## Licença

Este projeto está sob a licença [MIT](https://opensource.org/licenses/MIT).
