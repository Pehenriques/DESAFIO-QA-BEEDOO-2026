# BUG-002 — Sistema aceita submissão de formulário totalmente vazio

### Identificação

- ID: BUG-003
- Título: Sistema aceita cadastro com formulário totalmente vazio
- Projeto: Beedoo QA Tests
- Tela: Cadastro de curso
- Data: 10/03/2026
- Reportado por: Pedro Henrique

---

### Classificação

- Severidade: Alta
- Prioridade: Alta
- Tipo: Funcional (validação)

---

### Ambiente

- URL: https://creative-sherbet-a51eac.netlify.app/new-course
- Navegador: Chrome
- Sistema operacional: Windows 10

---

### Descrição

Durante a execução do caso de teste **Print-003**, foi possível enviar o formulário de cadastro de curso sem preencher nenhum campo.

O sistema deveria impedir o envio e apresentar mensagens de validação.

---

### Passos para reproduzir

1. Acessar a aplicação
2. Clicar em **Cadastrar curso**
3. Não preencher nenhum campo
4. Clicar em **Cadastrar**

---

### Resultado esperado

- O sistema deve impedir o envio e exigir preenchimento dos campos obrigatórios.
- Destacar os campos.

- Exibir mensagem específica para cada campo não preenchido

Exemplo:

"Todos os campos precisam ser preenchidos para criar o curso."

---

### Resultado atual (obtido)

O sistema aceita o envio do formulário vazio.
---

### Evidências

- evidencias/Print-003.png
- evidencias/Print-004.png

---

### Severidade ou impacto

- **Severidade:** Alta — permite criação de dados inválidos.

- **Impacto:** Dados inconsistentes na base; usuário pode não perceber que não preencheu nada e achar que cadastrou corretamente.
- Pode gerar problemas em listagem, relatórios e experiência do usuário.
- Falta de Campos Obrigatórios.

---

### Status e histórico

- **Status atual:** Novo
- **Datas:** 10/03/2026
