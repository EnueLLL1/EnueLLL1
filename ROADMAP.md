# 🗺️ Roadmap: Projetos Spring Boot

Este roadmap contém **7 projetos progressivos** para dominar **Spring Boot**, **PostgreSQL**, **APIs REST**, **DTOs**, **validações**, **relacionamentos**, **segurança**, **testes** e muito mais — tudo antes de avançar para Docker e microsserviços.

Cada projeto foi pensado para:
- Consolidar conceitos anteriores
- Introduzir novos desafios reais
- Gerar portfólio de valor
- Preparar para vagas **Junior/Pleno em Backend Java**

---

## 📊 Visão Geral por Nível

| Nível | Projeto(s) | Descrição |
|-------|-----------|----------|
| **⭐ Básico** | 1–2 | Fundamentos: CRUD, relações, validações, DTOs |
| **⚡ Intermediário** | 3–5 | Autenticação, paginação, transações, relatórios |
| **🚀 Avançado** | 6–7 | Permissões, agendamento, WebSocket, deploy |

---

## 📌 Projetos Detalhados

### 1. **Sistema de Biblioteca**  
**Nível**: Básico  
**Duração**: 2–3 dias  
**Dificuldade**: ⭐  
**Descrição**: Gerencie livros, gêneros, categorias e empréstimos.

#### ✅ O que você vai aprender:
- Relacionamentos entre tabelas (`@ManyToMany`)
- Validações de dados (`@NotBlank`, ISBN)
- Queries personalizadas no Repository
- DTOs (Data Transfer Objects)

#### 🗃️ Estrutura do Banco:
- `Livros` (id, titulo, isbn, ano, autor)
- `Gêneros` (id, nome)
- `Categorias` (id, nome)

#### ✅ Funcionalidades Obrigatórias:
- Cadastrar livros com gêneros e categorias
- Buscar livro por título, autor ou ISBN
- Listar livros por gênero ou categoria

#### 🌟 Desafios Extras (Opcional):
- Calcular multa por atraso
- Sistema de reserva
- Ranking de livros mais emprestados

> 📦 **Status**: Em andamento ([repositório](https://github.com/EnueLLL1/biblioteca-spring))

---

### 2. **Sistema de Tarefas (To-Do List)**  
**Nível**: Básico/Intermediário  
**Duração**: 2–3 dias  
**Dificuldade**: ⭐⭐  
**Descrição**: To-Do List com categorias, prioridades e usuários.

#### ✅ O que você vai aprender:
- Enums (Status, Prioridade)
- Filtros e buscas complexas
- `LocalDateTime` para datas
- Organização em packages por camada

#### 🗃️ Estrutura do Banco:
- `Usuarios` (id, nome, email, senha)
- `Categorias` (id, nome, cor)
- `Tarefas` (id, título, descrição, status, prioridade, data_criação, usuario_id, categoria_id)

#### ✅ Funcionalidades Obrigatórias:
- CRUD completo de tarefas
- Filtrar por status (Pendente, Concluída)
- Buscar por palavra-chave
- Estatísticas de conclusão

#### 🌟 Desafios Extras:
- Subtarefas
- Notificações de prazo
- Compartilhamento entre usuários

---

### 3. **API de Blog / Rede Social**  
**Nível**: Intermediário  
**Duração**: 4–5 dias  
**Dificuldade**: ⭐⭐⭐  
**Descrição**: Blog com posts, comentários, likes e seguidores.

#### ✅ O que você vai aprender:
- Relacionamentos `@ManyToMany`
- Paginação de resultados
- Upload de imagens
- Spring Security (autenticação básica)
- JWT (JSON Web Token)

#### 🗃️ Estrutura do Banco:
- `Usuarios`, `Posts`, `Comentarios`, `Likes`, `Seguidores`

#### ✅ Funcionalidades Obrigatórias:
- Registrar e fazer login
- Criar/editar posts
- Comentar e dar like
- Feed de seguidos
- Busca por hashtag

#### 🌟 Desafios Extras:
- Notificações
- Posts privados
- Trending topics

---

### 4. **Sistema de E-commerce Simples**  
**Nível**: Intermediário  
**Duração**: 5–6 dias  
**Dificuldade**: ⭐⭐⭐  
**Descrição**: Loja virtual com produtos, carrinho e pedidos.

#### ✅ O que você vai aprender:
- Modelagem de dados complexa
- Cálculos (total, frete)
- Estados de pedido (Enum)
- Transações (múltiplos saves)
- Exception Handling personalizado

#### 🗃️ Estrutura do Banco:
- `Produtos`, `Usuarios`, `Carrinho`, `ItensCarrinho`, `Pedidos`, `ItensPedido`

#### ✅ Funcionalidades Obrigatórias:
- Adicionar/remover do carrinho
- Finalizar pedido com validação de estoque
- Listar histórico de pedidos

#### 🌟 Desafios Extras:
- Cupons de desconto
- Avaliações de produtos
- Integração com API de CEP

---

### 5. **API de Gerenciamento Financeiro**  
**Nível**: Intermediário/Avançado  
**Duração**: 6–7 dias  
**Dificuldade**: ⭐⭐⭐⭐  
**Descrição**: Controle de receitas, despesas, categorias e relatórios.

#### ✅ O que você vai aprender:
- Queries complexas com JPQL
- Relatórios com agregações (`SUM`, `GROUP BY`)
- Exportação para CSV/Excel
- Dados para gráficos (frontend)

#### 🗃️ Estrutura do Banco:
- `Transacoes`, `Categorias`, `Metas`, `Usuarios`

#### ✅ Funcionalidades Obrigatórias:
- Registrar receitas e despesas
- Relatório mensal por categoria
- Alertas de metas
- Transações recorrentes

#### 🌟 Desafios Extras:
- Previsão de gastos
- Importação de extrato (CSV)
- Dashboard com cards

---

### 6. **Sistema de Gestão Escolar**  
**Nível**: Avançado  
**Duração**: 7–10 dias  
**Dificuldade**: ⭐⭐⭐⭐⭐  
**Descrição**: Escola completa: alunos, professores, turmas, notas.

#### ✅ O que você vai aprender:
- Sistema de permissões (Admin, Professor, Aluno)
- Spring Security avançado
- Envio de e-mails
- Agendamento de tarefas (`@Scheduled`)
- Validações customizadas

#### 🗃️ Estrutura do Banco:
- `Usuarios`, `Alunos`, `Professores`, `Turmas`, `Matriculas`, `Aulas`, `Notas`, `Presenças`

#### ✅ Funcionalidades Obrigatórias:
- Login por role
- Lançamento de notas e presenças
- Cálculo de média e aprovação
- Boletim em PDF
- E-mail de notificação

#### 🌟 Desafios Extras:
- Chat entre usuários
- Upload de material didático
- Fórum por disciplina

---

### 7. **Projeto Final: Plataforma de Cursos Online**  
**Nível**: Projeto Final  
**Duração**: 10–14 dias  
**Dificuldade**: ⭐⭐⭐⭐⭐  
**Descrição**: Udemy/Coursera simplificado com tudo que aprendeu.

#### ✅ O que você vai aprender:
- Integração de **todos os conceitos**
- Boas práticas de arquitetura
- Preparação para microservices
- Testes automatizados (JUnit)
- Deploy na nuvem (Render, Railway)

#### ✅ Funcionalidades Obrigatórias:
- Instrutor cria cursos
- Aluno compra e assiste aulas
- Sistema de progresso (% concluído)
- Avaliações e certificados
- Busca avançada e wishlist

#### 🌟 Desafios Extras:
- Pagamento real (Stripe)
- Upload de vídeos (AWS S3)
- WebSocket (chat ao vivo)
- Gamificação (badges)

---

## 🎯 Depois de Completar Todos os Projetos, Você Terá:

✅ Domínio sólido de **Spring Boot + JPA + PostgreSQL**  
✅ Experiência com **APIs REST, DTOs, validações e segurança**  
✅ **7 projetos reais no GitHub** para seu portfólio  
✅ Capacidade de **modelar bancos de dados complexos**    
✅ Base sólida para aprender **Docker, Kafka, Redis, microsserviços**

---

> ❤️ Criado com propósito por [EnueLLL1](https://github.com/EnueLLL1)  
> 🌱 Aprendizado contínuo > Perfeição imediata
