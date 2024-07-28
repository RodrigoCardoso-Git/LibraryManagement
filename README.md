<h1> LibraryManagement </h1>
Projeto final da disciplina de algoritmo do curso de ADS, que consiste no desenvolvimento de um sistema que faça o gerenciamento de uma biblioteca.

> Requisitos funcionais do LibraryManagement 

## 1. Gerenciamento de Perfis de Usuários

### 1.1. Criação de Perfis de Usuários

#### Campos Necessários:
- Nome completo
- Nome de usuário
- Senha (com critérios de segurança, como mínimo de caracteres e mistura de letras e números)
- Email
- Endereço
- Telefone
- Data de nascimento
- Tipo de usuário (bibliotecário ou membro)

#### Funcionalidades:
- Formulário para entrada de dados do usuário.
- Validação dos dados inseridos (e.g., formato de email, força da senha).
- Criação de um registro no banco de dados com os dados do usuário.
- Envio de um email de confirmação (opcional).

### 1.2. Leitura de Perfis de Usuários

#### Funcionalidades:
- Listagem de todos os usuários (com filtros para facilitar a busca, como por nome ou tipo de usuário).
- Exibição dos detalhes de um usuário específico.

### 1.3. Atualização de Perfis de Usuários

#### Campos Atualizáveis:
- Nome completo
- Nome de usuário
- Senha
- Email
- Endereço
- Telefone
- Data de nascimento

#### Funcionalidades:
- Formulário para edição de dados do usuário.
- Validação dos dados atualizados.
- Atualização do registro no banco de dados.

### 1.4. Exclusão de Perfis de Usuários

#### Funcionalidades:
- Opção para excluir um usuário da listagem.
- Confirmação de exclusão (para evitar exclusões acidentais).
- Remoção do registro no banco de dados.

## 2. Autenticação de Usuários (Login e Logout)

Para garantir a segurança e a personalização do acesso, o sistema deve incluir funcionalidades de autenticação.

### 2.1. Login

#### Campos Necessários:
- Nome de usuário ou email
- Senha

#### Funcionalidades:
- Validação das credenciais do usuário.
- Geração de um token de autenticação (para sessões).
- Redirecionamento para a página principal do sistema após login bem-sucedido.
- Mensagens de erro para credenciais inválidas.

### 2.2. Logout

#### Funcionalidades:
- Invalidar o token de autenticação.
- Redirecionamento para a página de login.
- Mensagem de confirmação de logout.

## 3. Gerenciamento de Privilégios e Permissões dos Usuários

Para controlar o acesso a diferentes funcionalidades do sistema, é necessário implementar um sistema de gerenciamento de privilégios.

### 3.1. Níveis de Privilégios

#### Tipos de Usuários:
- **Bibliotecário:** Acesso total ao sistema, incluindo gerenciamento de livros, usuários, empréstimos e relatórios.
- **Membro:** Acesso limitado, focado em busca e reserva de livros, visualização de histórico de empréstimos e 
perfil.
- **Professores:** 

### 3.2. Definição de Permissões

#### Funcionalidades:
- Permitir que bibliotecários gerenciem as permissões de outros usuários.
- Interface para definir quais ações cada tipo de usuário pode realizar.
- Aplicação das permissões em todas as funcionalidades do sistema (e.g., membros não podem excluir livros).

### 3.3. Implementação de Controle de Acesso

#### Funcionalidades:
- Middleware para verificar permissões antes de permitir acesso a determinadas rotas ou funcionalidades.
- Mensagens de erro ou redirecionamento para usuários tentando acessar funcionalidades não permitidas.

## 1. Gerenciamento de Registros de Livros

### 1.1. Criação de Registros de Livros

#### Campos Necessários:
- Título do livro
- Autor(es)
- ISBN
- Editora
- Ano de publicação
- Número de páginas
- Idioma
- Resumo/Sinopse
- Categoria(s)
- Etiqueta(s)
- Quantidade disponível
- Localização na biblioteca (seção, prateleira, etc.)
- Imagem da capa

#### Funcionalidades:
- Formulário para entrada de dados do livro.
- Validação dos dados inseridos (e.g., formato do ISBN, ano de publicação válido).
- Criação de um registro no banco de dados com os dados do livro.
- Upload e armazenamento da imagem da capa.

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
- Número de páginas
- Idioma
- Resumo/Sinopse
- Categoria(s)
- Etiqueta(s)
- Quantidade disponível
- Localização na biblioteca
- Imagem da capa

#### Funcionalidades:
- Formulário para edição de dados do livro.
- Validação dos dados atualizados.
- Atualização do registro no banco de dados.

### 1.4. Exclusão de Registros de Livros

#### Funcionalidades:
- Opção para excluir um livro da listagem.
- Confirmação de exclusão (para evitar exclusões acidentais).
- Remoção do registro no banco de dados.

## 2. Atribuição de Categorias e Etiquetas aos Livros

### 2.1. Categorias

#### Funcionalidades:
- Definição de categorias hierárquicas (e.g., Ficção > Ficção Científica, Não-Ficção > História).
- Interface para associar um ou mais livros a uma ou mais categorias.
- Filtro de busca por categorias.

### 2.2. Etiquetas

#### Funcionalidades:
- Criação e gerenciamento de etiquetas (tags) para livros.
- Interface para associar um ou mais livros a uma ou mais etiquetas.
- Filtro de busca por etiquetas.

## 3. Upload de Imagens das Capas dos Livros

### 3.1. Upload de Imagens

#### Funcionalidades:
- Interface para upload de imagem durante a criação ou atualização de registros de livros.
- Validação do formato e tamanho da imagem (e.g., JPG, PNG, tamanho máximo de 5MB).
- Armazenamento da imagem em um servidor ou serviço de armazenamento de arquivos.

### 3.2. Exibição de Imagens

#### Funcionalidades:
- Exibição da imagem da capa na listagem e nos detalhes dos livros.
- Opção para visualizar a imagem em tamanho completo.

# Sistema de Gerenciamento de Biblioteca

## Funcionalidades Principais

### 1. Empréstimo e Devolução

#### Funcionalidades:

1.1. **Registrar o Empréstimo de Livros a Membros:**
   - Formulário para registrar o empréstimo de livros, incluindo campos para:
     - Nome do membro
     - Identificação do livro (título, ISBN, etc.)
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
   - Notificação ao usuário sobre multas acumuladas.

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
     - Número de páginas
     - Idioma
     - Resumo/Sinopse
     - Categoria(s)
     - Etiqueta(s)
     - Quantidade disponível
     - Localização na biblioteca
     - Imagem da capa

### 3. Reserva de Livros

#### Funcionalidades:

3.1. **Permitir que os Membros Reservem Livros:**
   - Formulário para reserva de livros, incluindo campos para:
     - Nome do membro
     - Identificação do livro
   - Registro da reserva no banco de dados.

3.2. **Notificar Membros Quando um Livro Reservado Está Disponível:**
   - Envio de notificações por email ou SMS quando um livro reservado se torna disponível para empréstimo.

### 4. Histórico de Empréstimos

#### Funcionalidades:

4.1. **Manter um Registro do Histórico de Empréstimos de Cada Usuário:**
   - Registro detalhado dos empréstimos e devoluções de cada usuário.

4.2. **Permitir que os Usuários Visualizem Seu Histórico de Empréstimos e Devoluções:**
   - Interface para os usuários acessarem e visualizarem seu histórico completo de empréstimos e devoluções.

### 5. Notificações e Alertas

#### Funcionalidades:

5.1. **Enviar Notificações por Email ou SMS sobre Prazos de Devolução Iminentes:**
   - Alertas automáticos enviados aos usuários para lembrar sobre prazos de devolução próximos.

5.2. **Notificar sobre Multas Acumuladas:**
   - Notificações aos usuários sobre multas pendentes devido a atrasos na devolução.

5.3. **Informar sobre a Disponibilidade de Livros Reservados:**
   - Notificações quando livros reservados ficam disponíveis para empréstimo.

### 6. Relatórios e Análises

#### Funcionalidades:

6.1. **Gerar Relatórios de Uso da Biblioteca:**
   - Relatórios sobre livros mais emprestados, menos emprestados, etc.

6.2. **Fornecer Análises sobre a Utilização dos Recursos da Biblioteca:**
   - Análises detalhadas para auxiliar na gestão e tomada de decisões sobre a coleção e o uso da biblioteca.

### 7. Leitura Digital e E-books

#### Funcionalidades:

7.1. **Gerenciamento e Empréstimo de E-books e Outros Materiais Digitais:**
   - Registro e controle de empréstimos de e-books.
   - Suporte para diferentes formatos de e-books.

7.2. **Suporte para Leitura Online ou Download de E-books:**
   - Plataforma integrada para leitura online.
   - Opção para download seguro de e-books.

7.3. **Registro de Uso e Estatísticas de Leitura Digital:**
   - Registro de acessos e tempo de leitura.
   - Relatórios de uso de materiais digitais.

### 8. Sistema de Recomendação

#### Funcionalidades:

8.1. **Implementação de um Sistema de Recomendação:**
   - Recomendações baseadas no histórico de empréstimos dos usuários.
   - Sugestões de livros populares e relacionados.

### 9. Histórico de Alterações e Log de Atividades

#### Funcionalidades:

9.1. **Registro de Todas as Atividades Realizadas no Sistema:**
   - Logs de alterações em perfis, gerenciamento de livros e operações de empréstimo.

9.2. **Visualização e Auditoria do Log de Atividades:**
   - Interface para visualização e auditoria de logs.
   - Ferramentas de segurança e análise.

### 10. Gerenciamento de Doações

#### Funcionalidades:

10.1. **Registro de Doações de Livros e Outros Materiais:**
   - Formulário de registro de doações.
   - Controle do estado de processamento das doações.

10.2. **Relatórios de Doações Recebidas:**
   - Relatórios detalhados sobre doações recebidas e processadas.

### 11. Biblioteca Infantil

#### Funcionalidades:

11.1. **Área Dedicada com Interface Amigável para Crianças:**
   - Interface intuitiva e visual atraente para crianças.

11.2. **Catálogo de Livros Infantis e Atividades Interativas:**
   - Catálogo específico para livros infantis.
   - Atividades educativas e interativas.

### 12. Feedback e Avaliações

#### Funcionalidades:

12.1. **Permitir que os Membros Deixem Feedback ou Avaliem Livros:**
   - Formulário para comentários e avaliações.

12.2. **Gerenciamento de Comentários e Avaliações:**
   - Moderação de feedbacks e avaliações.

12.3. **Exibição de Avaliações Médias e Feedbacks nos Detalhes dos Livros:**
   - Exibição de avaliações e comentários nos detalhes dos livros.

### 13. Sugestões de Aquisição

#### Funcionalidades:

13.1. **Permitir que Membros Sugiram Novos Livros para Aquisição:**
   - Formulário para sugestão de novos livros.

13.2. **Sistema de Aprovação de Sugestões pelos Bibliotecários:**
   - Interface para aprovação e gerenciamento de sugestões.

13.3. **Notificações sobre o Status das Sugestões:**
   - Notificações automáticas sobre o status das sugestões enviadas.

### 14. Relatórios Personalizados

#### Funcionalidades:

14.1. **Criação de Relatórios Personalizados com Base em Diferentes Critérios:**
   - Ferramentas para criação de relatórios customizados.

14.2. **Exportação de Relatórios em Múltiplos Formatos (PDF, Excel):**
   - Opção para exportar relatórios em diferentes formatos.

### 15. Controle de Qualidade

#### Funcionalidades:

15.1. **Sistema de Feedback Contínuo sobre Serviços da Biblioteca:**
   - Coleta de feedback sobre serviços prestados.

15.2. **Avaliação de Desempenho e Qualidade dos Serviços Prestados:**
   - Ferramentas para avaliação de desempenho dos serviços.

### 16. Gerenciamento de Multas e Pagamentos Online

#### Funcionalidades:

16.1. **Sistema de Cálculo de Multas por Atraso:**
   - Cálculo automático de multas.

16.2. **Integração com Sistemas de Pagamento Online para Quitação de Multas:**
   - Opção para pagamento de multas online.

### 17. Gerenciamento de Revistas e Periódicos

#### Funcionalidades:

17.1. **Registro de Edições de Revistas e Periódicos:**
   - Controle de registros de revistas e periódicos.

17.2. **Disponibilização para Leitura Online ou Download:**
   - Plataforma para leitura online e download.

### 18. Apoio à Pesquisa Acadêmica

#### Funcionalidades:

18.1. **Ferramentas de Busca Avançada com Filtros Detalhados:**
   - Busca avançada para pesquisa acadêmica.

18.2. **Integração com Bases de Dados Acadêmicas e Indexadores:**
   - Conexão com Google Scholar, PubMed, etc.

### 19. Gerenciamento de Inventário

#### Funcionalidades:

19.1. **Controle de Estoque de Livros e Outros Materiais:**
   - Registro de aquisições e descartes.

19.2. **Relatórios sobre o Estado do Inventário:**
   - Relatórios detalhados sobre o inventário.

### 20. Integração com Sistemas Externos

#### Funcionalidades:

20.1. **Integrar com Sistemas de Pagamento para Multas:**
   - Conexão com sistemas de pagamento.

20.2. **Conectar com APIs Externas para Importar/Exportar Dados de Livros:**
   - Integração com APIs para sincronização de dados.

<!--19 - Chatbot para Suporte ao Usuário(Podia trocar chatbot páginas de perguntas frequentes e dúvidas sobre como funciona plataforma) -->
    
