## Requisitos

### 1.1 Requisitos Funcionais do Sistema

| ID | Requisito | Descrição |
| --- | --- | --- |
| RF01 | Realizar Login | Valida usuário e senha; se errados, avisa. |
| RF02 | Exibir Tela Principal | Mostra o usuário logado, o menu e o Sair. |
| RF03 | Encerrar Sessão | Sair apaga o token; sem Sair, ele expira em uma hora. |
| RF04 | Cadastrar Cliente | Nome e CPF obrigatórios; CPF não repete. |
| RF05 | Consultar Cliente | Busca por trecho do nome ou do CPF. |
| RF06 | Atualizar Cliente | Altera nome e CPF pelo ID. |
| RF07 | Excluir Cliente | Exclui pelo ID; bloqueia se tiver veículos. |
| RF08 | Cadastrar Veículo | Modelo e cliente obrigatórios; placa opcional. |
| RF09 | Atualizar Veículo | Altera modelo, placa e cliente pelo ID. |
| RF10 | Excluir Veículo | Exclui pelo ID; bloqueia se tiver agendamentos. |
| RF11 | Cadastrar Agendamento | Data e veículo obrigatórios. |
| RF12 | Listar Agendamentos | Ordena por data, com dados do veículo e do cliente. |
| RF13 | Atualizar Agendamento | Altera data e veículo pelo ID. |
| RF14 | Excluir Agendamento | Exclui pelo ID, após confirmação. |

### 1.2 Requisitos Não Funcionais

| ID | Requisito | Descrição |
| --- | --- | --- |
| RNF01 | Proteção de Dados | CPF em AES-256-CBC; senha em bcrypt. |
| RNF02 | Integridade dos Dados | PK, FK e UNIQUE; bloqueia exclusão com vínculos. |
| RNF03 | Controle de Acesso | Proxy valida o JWT; cookie HttpOnly. |

## 2 Requisitos de Infraestrutura

| Tecnologia | Versão / ambiente |
| --- | --- |
| JavaScript | Node.js 24 |
| Next.js | 16 |
| React e React DOM | 19 |
| bcryptjs | 3 |
| jsonwebtoken | 9 |
| node:crypto | Integrado ao Node.js |
| PostgreSQL | 18 |
| Prisma e Prisma Client | 6 |
| Ant Design | 6 |