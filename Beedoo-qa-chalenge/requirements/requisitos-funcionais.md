## Requisitos Funcionais — Beedoo QA (Módulo de Cursos)

### 1. Informações gerais

- **Nome da aplicação:** Beedoo QA Tests
- **Tipo de aplicação:** Web
- **Contexto/objetivo de negócio:** Permitir o cadastro, listagem e gerenciamento de cursos para fins de demonstração e avaliação de testes de software.
- **Stakeholders principais:** Equipe de QA, candidatos em processo seletivo, estudantes de testes.

---

# 2. Requisitos funcionais

| ID RF | Título | Descrição resumida | Prioridade | Observações |
|------|--------|--------------------|------------|-------------|
| RF-01 | Listagem de cursos | O sistema deve exibir na tela principal a lista de cursos cadastrados. | Alta | Fluxo principal |
| RF-02 | Navegação para listagem | O usuário deve poder acessar a tela de listagem de cursos através do link **"Listar cursos"**. | Alta | |
| RF-03 | Navegação para cadastro | O usuário deve poder acessar a tela de cadastro de curso através do link **"Cadastrar curso"**. | Alta | Rota `/new-course` |
| RF-04 | Cadastro de curso | O sistema deve permitir cadastrar um novo curso através de um formulário de cadastro. | Alta | Fluxo principal |
| RF-05 | Campos do cadastro | O formulário de cadastro deve conter os seguintes campos: Nome do curso, Descrição, Instrutor, URL da imagem, Data de início, Data de fim e Número de vagas. | Alta | Conforme interface |
| RF-06 | Feedback de sucesso no cadastro | Após cadastro bem-sucedido, o sistema deve informar o usuário através de mensagem ou redirecionamento. | Alta | |
| RF-07 | Inclusão do curso na lista | O curso recém cadastrado deve aparecer na listagem de cursos após o cadastro. | Alta | Não deve exigir atualização manual da página |
| RF-08 | Exclusão de curso | O sistema deve permitir que o usuário exclua um curso existente na listagem. | Alta | Deve remover o curso da lista |
| RF-09 | Confirmação de exclusão | Após excluir um curso, o sistema deve exibir mensagem de confirmação de exclusão bem-sucedida. | Alta | |
| RF-10 | Atualização da listagem | A listagem deve ser atualizada automaticamente após operações de cadastro ou exclusão. | Alta | |

---

# 3. Validações de formulário

| ID RF | Título | Descrição | Prioridade |
|------|--------|-----------|------------|
| RF-11 | Validação de campos obrigatórios | O sistema deve impedir o envio do formulário quando campos obrigatórios estiverem vazios. | Alta |
| RF-12 | Validação de formulário vazio | O sistema deve impedir a submissão do formulário quando nenhum campo estiver preenchido. | Alta |
| RF-13 | Validação de espaços em branco | Campos obrigatórios não devem aceitar apenas espaços em branco. | Média |
| RF-14 | Validação de campo numérico | O campo **Número de vagas** deve aceitar apenas números inteiros positivos. | Alta |
| RF-15 | Bloqueio de caracteres inválidos | O campo **Número de vagas** não deve aceitar letras ou caracteres especiais como "e", "+" ou "-". | Alta |
| RF-16 | Validação de datas | O sistema não deve permitir cadastro quando a **data de fim for anterior à data de início**. | Alta |
| RF-17 | Mensagem de erro | O sistema deve exibir mensagens claras quando ocorrer erro de validação no formulário. | Média |

---

# 4. Regras de negócio

- **RB-01:** Cada curso deve possuir um **nome válido**.
- **RB-02:** O cadastro só deve ser concluído quando **todos os campos obrigatórios forem preenchidos corretamente**.
- **RB-03:** A **data de fim deve ser posterior à data de início**.
- **RB-04:** O campo **Número de vagas** deve conter apenas **números inteiros positivos**.
- **RB-05:** Após cadastrar um curso, ele deve aparecer na listagem de cursos.
- **RB-06:** Após excluir um curso, ele não deve mais aparecer na listagem.
- **RB-07:** O sistema deve garantir consistência entre a mensagem exibida ao usuário e a ação realizada (ex.: sucesso de exclusão apenas se realmente excluído).

---

# 5. Restrições e premissas

### Restrições

- Aplicação web acessível via navegador.
- Compatibilidade com navegadores modernos (Chrome, Edge, Firefox).
- Interface acessada através de URL pública hospedada.

### Premissas

- A aplicação está disponível em ambiente de demonstração (Netlify).
- O sistema deve manter consistência dos dados apresentados ao usuário.
- As operações de cadastro e exclusão devem refletir imediatamente na interface da aplicação.