# BUG-004 — Sistema exibe mensagem de sucesso ao excluir curso, porém o curso permanece na listagem

### Identificação

- ID do bug: BUG-004
- Título: Sistema exibe mensagem de sucesso ao excluir curso, porém o curso permanece na listagem
- Projeto / Aplicação: Beedoo QA Tests — Módulo de Cursos
- Módulo / Tela: Listagem de cursos
- Data de registro: 10/03/2026
- Reportado por: Pedro Henrique

---

### Classificação

- Severidade: Alta
- Prioridade: Alta
- Tipo: Funcional (remoção de registro)

---

### Ambiente

- URL: https://creative-sherbet-a51eac.netlify.app/
- Navegador: Google Chrome
- Sistema operacional: Windows 10

---

### Descrição

Durante a execução do cenário de exclusão de cursos, foi observado que o sistema exibe a mensagem **"Curso excluído com sucesso!"**, porém o curso continua sendo exibido na listagem.

Esse comportamento gera inconsistência entre a mensagem apresentada ao usuário e o estado real dos dados no sistema.

### Passos para reproduzir

1. Acessar a página **Cadastrar Curso**.
2. Criar um curso preenchendo todos os campos.
3. Acessar a página **Lista de cursos**.
4. Localizar o curso que foi criado.
5. Clicar na opção **Excluir curso**.
6. Verificar a mensagem de confirmação de exclusão.
7. Verificar novamente a listagem de cursos.

---

### Resultado esperado

Após confirmar a exclusão:

- O curso deve ser removido da listagem imediatamente
- O curso não deve permanecer na base de dados
- A mensagem de sucesso deve ser exibida somente após a confirmação real da exclusão

---

### Resultado atual (obtido)

Após clicar em **Excluir curso**, o sistema exibe a mensagem:

"Curso excluído com sucesso!"

Porém, o curso **permanece visível na listagem**, indicando que a exclusão não foi realizada corretamente.

---

### Evidências

- evidencias/Print-007.png
- evidencias/Print-008.png

---

### Severidade ou impacto

- **Severidade:** Alta — permite que cursos que foram removidos continuem na base de dados.

- **Impacto:** Esse problema pode causar:

- Inconsistência entre interface e dados do sistema
- Falta de confiabilidade nas ações realizadas pelo usuário
- Possível falha na integração entre frontend e backend
- Confusão para o usuário ao tentar gerenciar cursos


### Status e histórico

- **Status atual:**  Em análise 
- **Datas:** 10/03/2026
