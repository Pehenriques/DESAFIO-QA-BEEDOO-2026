## Requisitos Não Funcionais — Beedoo QA (Módulo de Cursos)

### 1. Informações gerais

- **Aplicação:** Beedoo QA Tests (módulo de cursos)
- **Tipo:** Aplicação Web
- **Escopo:** Comportamento observável na interface web, incluindo usabilidade, consistência, feedback ao usuário e validação de dados.

---

# 2. Requisitos não funcionais

| ID RNF | Categoria | Descrição | Criticidade | Observações |
|------|-----------|-----------|-------------|-------------|
| RNF-01 | Usabilidade | A navegação entre as telas **Listar cursos** e **Cadastrar curso** deve ser clara e acessível através de links visíveis. | Alta | Fluxo principal |
| RNF-02 | Usabilidade | O sistema deve exibir **mensagens de sucesso ou erro compreensíveis** ao usuário após ações como cadastro ou exclusão. | Alta | |
| RNF-03 | Consistência | Mensagens exibidas ao usuário devem refletir corretamente o resultado da ação executada. | Alta | Relacionado ao BUG-004 |
| RNF-04 | Consistência | Elementos de interface como labels, botões e mensagens devem seguir padrão consistente na aplicação. | Média | |
| RNF-05 | Performance | A aplicação deve carregar páginas e responder às ações do usuário em tempo razoável. | Média | Ambiente Netlify |
| RNF-06 | Feedback visual | O sistema deve fornecer feedback visual após ações importantes (ex.: cadastro ou exclusão de curso). | Alta | |
| RNF-07 | Atualização de interface | A interface deve refletir imediatamente alterações realizadas pelo usuário (ex.: novo curso cadastrado ou curso excluído). | Alta | Relacionado ao BUG-002 |
| RNF-08 | Validação de dados | Campos do formulário devem validar entradas inválidas antes do envio. | Alta | Relacionado aos BUG-001, BUG-003 e BUG-005 |
| RNF-09 | Robustez | O sistema deve tratar entradas inválidas sem quebrar a interface ou gerar erros visíveis ao usuário. | Alta | |
| RNF-10 | Segurança de informação | Em caso de erro técnico, o sistema não deve exibir detalhes sensíveis como stack traces ou erros internos. | Média | Segurança/UX |

---

# 3. Restrições e premissas

### Restrições

- Aplicação web acessível via navegador.
- Ambiente hospedado em plataforma web (Netlify).
- Uso através de navegadores modernos (Chrome, Edge, Firefox).

### Premissas

- O usuário possui conexão de internet estável.
- O sistema deve manter consistência visual e funcional durante as interações.
- As mensagens apresentadas ao usuário devem ser claras e compreensíveis.