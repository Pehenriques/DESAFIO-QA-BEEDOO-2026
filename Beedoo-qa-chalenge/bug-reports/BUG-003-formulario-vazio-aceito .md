 BUG-003 — Sistema permite cadastro com data de fim anterior à data de início

### Identificação

- ID do bug: BUG-003
- Título: Sistema permite cadastro com data de fim anterior à data de início
- Projeto / Aplicação: Beedoo QA Tests — Módulo de Cursos
- Módulo / Tela: Cadastro de curso
- Data de registro: 10/03/2026
- Reportado por: Pedro Henrique

---

### Classificação

- Severidade: Alta
- Prioridade: Alta
- Tipo: Funcional (Regra de negócio / Validação de dados)

---

### Ambiente

- URL: https://creative-sherbet-a51eac.netlify.app/new-course
- Navegador: Google Chrome
- Sistema operacional: Windows 10

---

### Descrição

Durante a execução do cenário de teste de validação de datas, foi identificado que o sistema permite cadastrar um curso mesmo quando a **data de fim é anterior à data de início**.

Isso viola a regra de negócio esperada para cadastro de cursos, pois a data final deve ser sempre posterior à data inicial.
---

### Passos para reproduzir

1. Acessar a página de cadastro de curso
2. Preencher o campo **Nome do curso** com valor válido
3. Preencher o campo **Descrição do curso** com valor válido
4. Preencher o campo **Instrutor** com valor válido
5. Preencher o campo **URL da imagem de capa** com valor válido
6. Preencher o campo **Data de início** com a data atual
7. Preencher o campo **Data de fim** com uma data anterior à data de início
8. Preencher o campo **Número de vagas** com valor válido
9. Preencher outros campos (se houver)
10. Clicar em **Cadastrar curso**

---

### Resultado esperado

O sistema **não deve permitir o cadastro do curso** quando a data de fim for anterior à data de início.

O sistema deve:

- Bloquear a submissão do formulário
- Exibir mensagem de validação informando que a data é inválida

Exemplo de mensagem esperada:

"A data de fim deve ser posterior à data de início."

---

### Resultado atual (obtido)

O sistema permite concluir o cadastro do curso mesmo com a **data de fim anterior à data de início**.

Exemplo utilizado durante o teste:

- Data de início: **11/02/2026**
- Data de fim: **20/01/2026**

O sistema concluiu a criação do curso **sem exibir nenhuma mensagem de erro ou alerta**.

---

### Evidências

- evidencias/Print-005.png
- evidencias/Print-006.png

---

### Severidade ou impacto

- **Severidade:** Alta — permite criação de cursos com datas erradas.

- **Impacto:** Permite cadastro de cursos com datas inconsistentes, podendo gerar:

- Problemas em listagens
- Dados incorretos no sistema
- Inconsistência em relatórios
- Experiência negativa para o usuário
---

### Status e histórico

- **Status atual:**  Em análise 
- **Datas:** 10/03/2026
