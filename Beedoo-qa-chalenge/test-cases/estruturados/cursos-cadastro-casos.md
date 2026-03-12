# Casos de Teste Estruturados — Módulo de Cursos

Referência aos cenários Gherkin: `test-cases/gherkin/cursos-cadastro.md`

---

# 1. Resumo dos casos

| ID | Título | Requisito(s) | Prioridade | Tipo |
|----|------|-------------|------------|------|
| CT-C01 | Cadastro com todos os campos válidos | RF-04, RF-05, RF-06 | Alta | Funcional |
| CT-C02 | Cadastro com preenchimento mínimo obrigatório | RF-04, RF-05 | Alta | Funcional |
| CT-C03 | Navegação para tela de cadastro | RF-03 | Alta | Funcional |
| CT-C04 | Retorno à listagem após cadastro | RF-06, RF-07 | Alta | Funcional |
| CT-C05 | Cadastro com campo obrigatório em branco | RF-11 | Alta | Negativo |
| CT-C06 | Cadastro com formulário vazio | RF-12 | Alta | Negativo |
| CT-C07 | Campo obrigatório apenas com espaços | RF-13 | Média | Negativo |
| CT-C08 | Nome do curso com caracteres especiais | RF-17 | Média | Validação |
| CT-C09 | Nome do curso com texto muito longo | RF-17 | Média | Validação |
| CT-C10 | Duplo envio do formulário | RF-04 | Média | Comportamento |
| CT-C11 | Voltar para listagem sem cadastrar | RF-03 | Média | Funcional |
| CT-C12 | Campo número de vagas com valor inválido | RF-14, RF-15 | Alta | Negativo |
| CT-C13 | Submissão com tecla Enter | RF-04 | Baixa | Usabilidade |
| CT-C14 | Cadastro com data de fim anterior à data de início | RF-16 | Alta | Negativo |
| CT-C15 | Exclusão de curso | RF-08 | Alta | Funcional |
| CT-C16 | Confirmação de exclusão de curso | RF-09 | Alta | Funcional |
| CT-C17 | Atualização da listagem após exclusão | RF-10 | Alta | Funcional |

---

# 2. Detalhamento dos casos de teste

---

# CT-C01 — Cadastro com todos os campos válidos

**Pré-condição**

Aplicação acessível.

**Dados de teste**

Nome do curso: Curso de Testes 2026  
Descrição: Curso introdutório de QA  
Instrutor: João Silva  
URL da imagem: URL válida  
Data início: data atual  
Data fim: data futura  
Número de vagas: 30  

| Passo | Ação | Resultado esperado |
|------|------|--------------------|
| 1 | Acessar a aplicação | Página inicial exibida |
| 2 | Clicar em "Cadastrar curso" | Tela de cadastro exibida |
| 3 | Preencher todos os campos com dados válidos | Sistema aceita os valores |
| 4 | Clicar em "Cadastrar curso" | Mensagem de sucesso exibida |
| 5 | Acessar a listagem de cursos | Curso recém criado aparece na lista |

---

# CT-C02 — Cadastro com preenchimento mínimo obrigatório

**Pré-condição**

Tela de cadastro aberta.

| Passo | Ação | Resultado esperado |
|------|------|--------------------|
| 1 | Preencher apenas campos obrigatórios | Sistema aceita dados |
| 2 | Submeter formulário | Cadastro realizado |
| 3 | Verificar listagem | Curso aparece na lista |

---

# CT-C03 — Navegação para tela de cadastro

| Passo | Ação | Resultado esperado |
|------|------|--------------------|
| 1 | Acessar listagem de cursos | Lista exibida |
| 2 | Clicar em "Cadastrar curso" | Sistema redireciona para tela de cadastro |

---

# CT-C04 — Retorno à listagem após cadastro

| Passo | Ação | Resultado esperado |
|------|------|--------------------|
| 1 | Realizar cadastro de curso | Cadastro realizado |
| 2 | Acessar listagem | Curso recém cadastrado aparece na lista |

---

# CT-C05 — Cadastro com campo obrigatório em branco

| Passo | Ação | Resultado esperado |
|------|------|--------------------|
| 1 | Deixar campo obrigatório vazio | — |
| 2 | Submeter formulário | Sistema bloqueia envio |
| 3 | Verificar mensagem | Mensagem de validação exibida |

---

# CT-C06 — Cadastro com formulário vazio

| Passo | Ação | Resultado esperado |
|------|------|--------------------|
| 1 | Não preencher nenhum campo | — |
| 2 | Submeter formulário | Sistema bloqueia cadastro |
| 3 | Verificar mensagem | Erro de validação exibido |

---

# CT-C07 — Campo obrigatório apenas com espaços

| Passo | Ação | Resultado esperado |
|------|------|--------------------|
| 1 | Inserir apenas espaços no campo obrigatório | — |
| 2 | Submeter formulário | Sistema considera inválido |
| 3 | Mensagem exibida | Usuário informado sobre erro |

---

# CT-C12 — Campo número de vagas com valor inválido

(Relacionado ao **BUG-005**)

| Passo | Ação | Resultado esperado |
|------|------|--------------------|
| 1 | Inserir letra "e" no campo número de vagas | Sistema bloqueia inserção |
| 2 | Inserir "+" ou "-" | Sistema bloqueia caracteres |
| 3 | Submeter formulário | Sistema exibe erro de validação |

---

# CT-C14 — Cadastro com data de fim anterior à data de início

(Relacionado ao **BUG-003**)

| Passo | Ação | Resultado esperado |
|------|------|--------------------|
| 1 | Inserir data de início atual | Campo aceita valor |
| 2 | Inserir data de fim anterior | Sistema detecta inconsistência |
| 3 | Submeter formulário | Cadastro bloqueado |
| 4 | Verificar mensagem | Sistema informa que data final deve ser posterior |

---

# CT-C15 — Exclusão de curso

| Passo | Ação | Resultado esperado |
|------|------|--------------------|
| 1 | Acessar listagem de cursos | Lista exibida |
| 2 | Selecionar um curso | Curso localizado |
| 3 | Clicar em "Excluir curso" | Sistema inicia exclusão |

---

# CT-C16 — Confirmação de exclusão

| Passo | Ação | Resultado esperado |
|------|------|--------------------|
| 1 | Confirmar exclusão do curso | Sistema executa operação |
| 2 | Verificar mensagem exibida | Mensagem "Curso excluído com sucesso" |

---

# CT-C17 — Atualização da listagem após exclusão

(Relacionado ao **BUG-004**)

| Passo | Ação | Resultado esperado |
|------|------|--------------------|
| 1 | Excluir um curso | Operação executada |
| 2 | Verificar listagem | Curso não aparece mais na lista |
| 3 | Atualizar página (se necessário) | Curso continua ausente |