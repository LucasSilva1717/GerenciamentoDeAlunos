# 📚 Sistema de Gerenciamento de Alunos<br> `Em desenvolvimento`

Sistema completo para controle acadêmico, matrículas e gestão de alunos em instituições de ensino técnico.

---

## 🛠️ Arquitetura e Tecnologias

O sistema é dividido em duas aplicações independentes (Decoupled Architecture):

### ☕ Back-end (API Rest)
- **Java 17**
- **Spring Boot 3** (Data JPA, Web, Validation)
- **PostgreSQL** (Banco de dados relacional)
- **Mockito & JUnit 5** (Testes unitários e de integração)

### 🎨 Front-end (Interface Web)
- **React** (via **Vite** para inicialização rápida)
- **Tailwind CSS** (Estilização utilitária e responsiva)
- **Axios** (Integração e consumo da API Spring Boot)
- **Lucide React** (Pacote de ícones da interface)
- **Vercel** (Hospedagem e deploy contínuo da interface)

---

## 📋 Funcionalidades Principais

- **Cadastro de Alunos:** Criação, edição, exclusão e listagem de estudantes.
- **Gestão de Matrículas:** Vínculo de alunos a cursos técnicos disponíveis.
- **Histórico Acadêmico:** Registro de notas, médias e frequências.
- **Regras de Negócio:** Validações de documentos (CPF/RG) e idade mínima por curso.

---

## 🚀 Como Executar o Projeto

### Pré-requisitos
- Java JDK 17+ instalado
- Maven instalado
- Node.js instalado (para o Front-end)
- Instância do PostgreSQL ativa

### 1. Configurando o Back-end

1. **Clonar o repositório:**
   ```bash
   git clone https://github.com
   cd seu-repositorio
   ```

2. **Configurar o banco de dados:**
   Altere as credenciais no arquivo `src/main/resources/application.properties`:
   ```properties
   spring.datasource.url=jdbc:postgresql://localhost:5432/nome_do_banco
   spring.datasource.username=seu_usuario
   spring.datasource.password=sua_senha
   ```

3. **Compilar e rodar a aplicação:**
   ```bash
   mvn clean install
   mvn spring-boot:run
   ```
   A API estará disponível em `http://localhost:8080`.

### 2. Configurando o Front-end

1. **Acessar a pasta do front-end (ou iniciar o projeto Vite):**
   ```bash
   # Para criar o projeto do zero se ainda não criou:
   npm create vite@latest front-end -- --template react
   cd front-end
   npm install
   ```

2. **Instalar dependências adicionais:**
   ```bash
   npm install axios lucide-react
   # Siga a documentação oficial do Tailwind para instalar o tailwindcss no Vite
   ```

3. **Executar em modo de desenvolvimento:**
   ```bash
   npm run dev
   ```
   A interface estará disponível em `http://localhost:5173`.

---

## 🧪 Testes Automatizados (Back-end)

O projeto conta com testes unitários focados nas regras de negócio utilizando Mockito e JUnit 5 para garantir a confiabilidade das matrículas e cadastros.

Para rodar os testes, execute:
```bash
mvn test
```

---

## 🌐 Deploy (Vercel)

O deploy do front-end foi realizado na Vercel e pode ser acessado através do link:  
🔗 [Link do Projeto na Vercel](https://vercel.app)

---
Desenvolvido por [LucasSilva1717](https://github.com)
