<h1> LibraryManagement </h1>
Projeto final da disciplina de algoritmo do curso de ADS, que consiste no desenvolvimento de um sistema que faça o gerenciamento de uma biblioteca.

> Requisitos funcionais do LibraryManagement 

## 1. Gerenciamento de Perfis de Usuários

### 1.1. Criação de Perfis de Usuários

#### Campos Necessários:
- Nome completo
- matricula
- Senha (com critérios de segurança, como mínimo de caracteres e mistura de letras e números)
- Endereço
- Tipo de usuário (bibliotecário ou aluno)gg

#### Funcionalidades:
- Formulário para entrada de dados do usuário.
- Validação dos dados inseridos (e.g., formato de email, força da senha).
- Criação de um registro no banco de dados com os dados do usuário.

### 1.2. Leitura de Perfis de Usuários(Bibliotecário)

#### Funcionalidades:
- Listagem de todos os usuários (com filtros para facilitar a busca, como por nome ou tipo de usuário).
- Exibição dos detalhes de um usuário específico.

### 1.3. Atualização de Perfis de Usuários

#### Campos Atualizáveis:
- Nome completo
- matricula
- livro
- Data de Entrega

#### Funcionalidades:
- Controle e registro de empréstimo de livros

## 2. Autenticação de Usuários (Login e Logout) - Bibliotecario e Aluno

Para garantir a segurança e a personalização do acesso, o sistema deve incluir funcionalidades de autenticação.

### 2.1. Login

#### Campos Necessários:
- Matricula
- Senha

#### Funcionalidades:
- Validação das credenciais do usuário.
- Redirecionamento para a página principal do sistema após login bem-sucedido.
- Mensagens de erro para credenciais inválidas.

### 2.2. Logout

#### Funcionalidades:
- Redirecionamento para a página de login.
- Mensagem de confirmação de logout.

## 3. Gerenciamento de Privilégios e Permissões dos Usuários

Para controlar o acesso a diferentes funcionalidades do sistema, é necessário implementar um sistema de gerenciamento de privilégios.

### 3.1. Níveis de Privilégios

#### Tipos de Usuários:
- **Bibliotecário:** Acesso total ao sistema, incluindo gerenciamento de livro, empréstimos e controle de multa.
- **Aluno:** Acesso limitado, focado em busca e reserva de livros, visualização de histórico de empréstimos e 
perfil.

## 1. Gerenciamento de Registros de Livros - Bibliotecario

### 1.1. Criação de Registros de Livros

#### Campos Necessários:
- Título do livro
- Autor(es)
- ISBN
- Editora
- Ano de publicação
- Quantidade disponível

#### Funcionalidades:
- Formulário para entrada de dados do livro.
- Validação dos dados inseridos (e.g., formato do ISBN, ano de publicação válido).
- Criação de um registro no banco de dados com os dados do livro.


### 1.2. Leitura de Registros de Livros

#### Funcionalidades:
- Listagem de todos os livros cadastrados (com filtros por título, autor, ISBN, categoria, etc.).
- Exibição dos detalhes de um livro específico.
- Pesquisa avançada com múltiplos critérios.

### 1.3. Atualização de Registros de Livros

#### Campos Atualizáveis:
- Título do livro
- Autor(es)
- ISBN
- Editora
- Ano de publicação
- Quantidade disponível

#### Funcionalidades:
- Formulário para edição de dados do livro.
- Validação dos dados atualizados.
- Atualização do registro no banco de dados.

### 1.4. Exclusão de Registros de Livros

#### Funcionalidades:
- Opção para excluir um livro da listagem.
- Confirmação de exclusão (para evitar exclusões acidentais).
- Remoção do registro no banco de dados.

## Funcionalidades Principais

### 1. Empréstimo e Devolução

#### Funcionalidades:

1.1. **Registrar o Empréstimo de Livros a aluno:**
   - Formulário para registrar o empréstimo de livros, incluindo campos para:
     - Nome do aluno
     - Identificação do livro (ISBN)
     - Data de empréstimo
     - Data prevista para devolução
   - Validação dos dados inseridos.
   - Criação de um registro de empréstimo no banco de dados.

1.2. **Gerenciar a Devolução de Livros:**
   - Formulário para registrar a devolução de livros, incluindo campos para:
     - Identificação do livro
     - Data de devolução
   - Validação dos dados inseridos.
   - Atualização do registro de empréstimo no banco de dados.

1.3. **Calcular e Registrar Multas por Atraso na Devolução:**
   - Cálculo automático de multas com base na data de devolução e na data prevista de devolução.
   - Registro das multas no banco de dados.

### 2. Catálogo e Pesquisa

#### Funcionalidades:

2.1. **Permitir a Busca de Livros no Catálogo:**
   - Campo de busca para pesquisa por título, autor, ISBN, categoria, etc.
   - Filtro de resultados por critérios específicos, como disponibilidade, data de publicação, etc.

2.2. **Exibir Detalhes dos Livros:**
   - Visualização dos detalhes do livro, incluindo:
     - Título
     - Autor(es)
     - ISBN
     - Editora
     - Ano de publicação
     - Quantidade disponível

### 3. Reserva de Livros

#### Funcionalidades:

3.1. **Permitir que os alunos reservem Livros:**
   - Formulário para reserva de livros, incluindo campos para:
     - Nome do membro
     - Identificação do livro
   - Registro da reserva no banco de dados.

### 4. Histórico de Empréstimos

#### Funcionalidades:

4.1. **Manter um Registro do Histórico de Empréstimos de Cada Usuário:**
   - Registro detalhado dos empréstimos e devoluções de cada usuário.

4.2. **Permitir que os Usuários Visualizem Seu Histórico de Empréstimos e Devoluções:**
   - Interface para os usuários acessarem e visualizarem seu histórico completo de empréstimos e devoluções.

### 16. Gerenciamento de Multas

#### Funcionalidades:

16.1. **Sistema de Cálculo de Multas por Atraso:**
   - Cálculo automático de multas.
