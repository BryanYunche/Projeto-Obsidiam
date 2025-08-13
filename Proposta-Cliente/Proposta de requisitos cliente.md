# Proposta de Requisitos do Sistema de Biblioteca Online

## 1. Requisitos Funcionais (RF)

| ID    | Requisito Funcional        | Descrição                                                                                       |
| ----- | -------------------------- | ----------------------------------------------------------------------------------------------- |
| [[RF001]] | Cadastro de Usuário        | O sistema deve permitir que novos usuários se cadastrem fornecendo nome, email e senha.         |
| [[RF002]] | Login de Usuário           | O sistema deve permitir que usuários cadastrados façam login com email e senha.                 |
| [[RF003]] | Busca de Livros            | O sistema deve permitir que usuários busquem livros por título, autor ou categoria.             |
| [[RF004]] | Empréstimo de Livros       | O sistema deve permitir que usuários façam empréstimo de livros disponíveis.                    |
| [[RF005]] | Devolução de Livros        | O sistema deve permitir que usuários devolvam livros emprestados e atualizar o status do livro. |
| [[RF006]] | Histórico de Empréstimos   | O sistema deve disponibilizar ao usuário um histórico de livros emprestados e devolvidos.       |
| [[RF007]] | Notificações de Vencimento | O sistema deve enviar notificações por email quando o prazo de devolução estiver próximo.       |

---

## 2. Requisitos Não Funcionais (RNF)

| ID         | Requisito Não Funcional | Descrição                                                                                                    |
| ---------- | ----------------------- | ------------------------------------------------------------------------------------------------------------ |
| [[RNF001]] | Performance             | O sistema deve responder às buscas de livros em até 2 segundos.                                              |
| [[RNF002]] | Segurança               | Senhas dos usuários devem ser armazenadas de forma criptografada (hash + salt).                              |
| [[RNF003]] | Usabilidade             | A interface do usuário deve ser intuitiva, permitindo que novos usuários realizem cadastro em até 2 minutos. |
| [[RNF004]]     | Disponibilidade         | O sistema deve ter disponibilidade mínima de 99,5% durante o horário de funcionamento (8h às 22h).           |
| [[RNF005]] | Escalabilidade          | O sistema deve suportar até 5000 usuários simultâneos.                                                       |

---

## 3. Regras de Negócio (RN)

| ID     | Regra de Negócio | Descrição |
|--------|-----------------|-----------|
| [[RN001]]  | Limite de Empréstimos | Cada usuário pode ter no máximo 5 livros emprestados simultaneamente. |
| [[RN002]]  | Prazo de Empréstimo | O prazo máximo para empréstimo de um livro é de 14 dias. |
| [[RN003]]  | Penalidade por Atraso | Usuários com devoluções atrasadas não poderão realizar novos empréstimos até regularizar os livros. |
| [[RN004]]  | Disponibilidade de Livro | Um livro só pode ser emprestado se houver exemplares disponíveis. |
| [[RN005]]  | Renovação de Empréstimo | Um livro pode ser renovado uma vez por mais 7 dias, desde que não haja reserva do livro por outro usuário. |
