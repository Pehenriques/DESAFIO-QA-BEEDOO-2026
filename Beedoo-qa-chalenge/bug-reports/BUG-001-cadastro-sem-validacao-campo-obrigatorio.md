# BUG-001 — Cadastro permite envio com campo obrigatório em branco

### Identificação

- ID do bug: BUG-001
- Título: Cadastro permite envio com campo obrigatório em branco
- Projeto / Aplicação: Beedoo QA Tests — Módulo de Cursos
- Módulo / Tela: Cadastro de curso
- Data de registro: 10/03/2026
- Reportado por: Pedro Henrique

---

### Classificação

- Severidade: Alta
- Prioridade: Alta
- Tipo: Funcional (validação)

---

### Ambiente

- URL: https://creative-sherbet-a51eac.netlify.app/new-course
- Navegador: Google Chrome
- Sistema operacional: Windows 10

---

### Descrição

Durante a execução do caso de teste **CT-**, foi observado que o sistema permite submeter o formulário de cadastro de curso mesmo quando o campo **Nome do curso** ou o campo **Link para inscrição** está em branco.

Isso viola a regra de negócio esperada de validação de campos obrigatórios.

---

### Passos para reproduzir

1. Acessar a aplicação em https://creative-sherbet-a51eac.netlify.app/
2. Acessar a aplicação
3. Clicar em **Cadastrar curso**
4. Deixar o campo **Nome do curso** vazio
5. Preencher outros campos (se houver)
6. Clicar em **Cadastrar Curso**

---

### Resultado esperado

- O sistema não permitir a criação de um novo curso sem os campos estarem preenchidos 
- Deve exibir sempre uma mensagem de erro ou alerta informando o prrenchimento dos campos.

- O sistema deve:

Bloquear a criação do curso

Destacar os campos.

Exibir mensagem específica para cada campo não preenchido

Exemplo:
"O campo Nome do curso deve ser preenchido"
"O campo Link de inscrição deve ser preenchido"

---

### Resultado atual (obtido)

- O sistema permite a crição do curso sem o preechimento dos campos sem trazer alguma mensagem de erro ou alerta informando a necessidades do preenchimento dos mesmos. 
Campos: "Nome do curso" e "Link de inscrição" 

---

### Evidências

- evidencias/Print_001.png
- evidencias/Print_002png

---

### Severidade ou impacto

- **Severidade:** Alta — violação de regra de negócio e possibilidade de dados inconsistentes na listagem.

- **Impacto:** 
- Impacta diretamente na integridade dos dados
    Ex: busca pelo curso, onde se cadastrar.
- Permissão de cadastros inconsistentes.
- Pode gerar problemas em listagem, relatórios e experiência do usuário.
- Falta de Campos Obrigatórios.
- Pode afetar regras de negócio e integrações futuras.

---

### Status e histórico

- **Status atual:** Reaberto 
- **Responsável técnico:** Pedo Henrique
- **Datas:** Abertura 10/03/2026; demais conforme acompanhamento.

