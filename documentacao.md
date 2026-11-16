## Requisitos

### 1.1 Requisitos Funcionais do Sistema

| ID | Requisito | Descrição |
| --- | --- | --- |
| RF01 | Realizar Login | Valida usuário e senha; se errados, avisa. |
| RF02 | Exibir Tela Principal | Mostra o usuário logado, o menu e o Sair. |
| RF03 | Encerrar Sessão | Sair apaga o token; sem Sair, ele expira em uma hora. |
| RF04 | Cadastrar Cliente | Nome e CPF obrigatórios; CPF não repete. |
| RF05 | Consultar Cliente | Busca por trecho do nome ou do CPF. |
| RF06 | Atualizar Cliente | Altera nome e CPF. |
| RF07 | Excluir Cliente | Exclui Cliente, porém bloqueia se tiver imoveis. |
| RF08 | Cadastrar Imóvel | Modelo e cliente obrigatórios. |
| RF09 | Atualizar Imóvel | Altera modelo e cliente. |
| RF10 | Excluir Imóvel | Exclui Imóvel, porém bloqueia se tiver Alugueis. |
| RF11 | Cadastrar Alugueis | Data e Imóvel obrigatórios. |
| RF12 | Listar Alugueis | Ordena por data, com dados do Imóvel e do cliente. |
| RF13 | Atualizar Alugueis | Altera data, Imóvel e Dono do Imóvel . |
| RF14 | Excluir Alugueis | Exclui Aluguel, após confirmação. |

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