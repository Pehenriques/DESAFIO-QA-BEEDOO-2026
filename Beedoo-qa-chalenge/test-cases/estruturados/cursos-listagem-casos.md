# Casos de Teste Estruturados — Listagem de Cursos

Referência aos cenários Gherkin: `test-cases/gherkin/cursos-listagem.md`

---

# 1. Resumo dos casos

| ID | Título | Requisito(s) | Prioridade | Tipo |
|----|------|-------------|------------|------|
| CT-L01 | Visualizar lista de cursos cadastrados | RF-01 | Alta | Funcional |
| CT-L02 | Acesso à listagem via link "Listar cursos" | RF-02 | Alta | Funcional |
| CT-L03 | Curso recém cadastrado visível na listagem | RF-06, RF-07 | Alta | Funcional |
| CT-L04 | Listagem exibe mais de um curso | RF-01 | Alta | Funcional |
| CT-L05 | Comportamento da listagem sem cursos | RF-01 | Média | Negativo |
| CT-L06 | Atualização da listagem após cadastro | RF-07, RF-10 | Alta | Funcional |
| CT-L07 | Navegação entre listagem e cadastro | RF-02, RF-03 | Média | Funcional |
| CT-L08 | Acesso direto à URL da listagem | RF-01 | Média | Funcional |
| CT-L09 | Ordem dos cursos na listagem | RF-01 | Baixa | Comportamento |
| CT-L10 | Nome de curso longo na listagem | RF-01, RNF-04 | Baixa | Usabilidade |
| CT-L11 | Exclusão de curso remove item da listagem | RF-08, RF-10 | Alta | Funcional |
| CT-L12 | Mensagem de sucesso após exclusão | RF-09 | Alta | Funcional |

---

# 2. Detalhamento (passos e resultados esperados)

---

# CT-L01 — Visualizar lista de cursos cadastrados

**Pré-condição**

Existem cursos cadastrados no sistema.

| Passo | Ação | Resultado esperado |
|------|------|--------------------|
| 1 | Acessar a aplicação | Tela inicial exibida |
| 2 | Acessar a página "Listar cursos" | Tela de listagem exibida |
| 3 | Verificar lista de cursos | Cursos cadastrados aparecem na listagem |

---

# CT-L02 — Acesso à listagem via link "Listar cursos"

**Pré-condição**

Usuário em outra tela da aplicação.

| Passo | Ação | Resultado esperado |
|------|------|--------------------|
| 1 | Clicar no link "Listar cursos" | Sistema redireciona para a listagem |
| 2 | Verificar conteúdo da tela | Lista de cursos exibida corretamente |

---

# CT-L03 — Curso recém cadastrado visível na listagem

**Pré-condição**

Um curso foi cadastrado com sucesso.

| Passo | Ação | Resultado esperado |
|------|------|--------------------|
| 1 | Acessar ou retornar à listagem | Listagem carregada |
| 2 | Localizar curso recém criado | Curso aparece na lista com dados corretos |

---

# CT-L04 — Listagem exibe mais de um curso

**Pré-condição**

Existem pelo menos dois cursos cadastrados.

| Passo | Ação | Resultado esperado |
|------|------|--------------------|
| 1 | Acessar listagem | Tela exibida |
| 2 | Verificar itens da lista | Todos os cursos aparecem corretamente |

---

# CT-L05 — Comportamento da listagem sem cursos

**Pré-condição**

Nenhum curso cadastrado.

| Passo | Ação | Resultado esperado |
|------|------|--------------------|
| 1 | Acessar a listagem | Tela carregada |
| 2 | Verificar conteúdo da página | Sistema exibe lista vazia ou mensagem informativa |
| 3 | Verificar interface | Nenhum erro técnico exibido |

---

# CT-L06 — Atualização da listagem após cadastro

(Relacionado ao **BUG-002**)

**Pré-condição**

Usuário na listagem de cursos.

| Passo | Ação | Resultado esperado |
|------|------|--------------------|
| 1 | Anotar quantidade atual de cursos | — |
| 2 | Cadastrar novo curso | Cadastro realizado |
| 3 | Retornar à listagem | Lista atualizada |
| 4 | Verificar quantidade de cursos | Quantidade aumentada |

---

# CT-L07 — Navegação entre listagem e cadastro

**Pré-condição**

Aplicação acessível.

| Passo | Ação | Resultado esperado |
|------|------|--------------------|
| 1 | Na listagem clicar "Cadastrar curso" | Tela de cadastro exibida |
| 2 | Clicar em "Listar cursos" | Sistema retorna à listagem |

---

# CT-L08 — Acesso direto à URL da listagem

**Pré-condição**

URL da aplicação conhecida.

| Passo | Ação | Resultado esperado |
|------|------|--------------------|
| 1 | Abrir URL da aplicação no navegador | Página carregada |
| 2 | Verificar conteúdo | Lista de cursos ou estado vazio exibido |

---

# CT-L09 — Ordem dos cursos na listagem

**Pré-condição**

Existem vários cursos cadastrados.

| Passo | Ação | Resultado esperado |
|------|------|--------------------|
| 1 | Acessar listagem | Lista exibida |
| 2 | Verificar ordem dos cursos | Ordem consistente e previsível |

---

# CT-L10 — Nome de curso longo na listagem

**Pré-condição**

Curso com nome muito longo cadastrado.

| Passo | Ação | Resultado esperado |
|------|------|--------------------|
| 1 | Acessar listagem | Lista exibida |
| 2 | Verificar nome do curso longo | Nome exibido corretamente |
| 3 | Verificar layout | Layout não quebra |

---

# CT-L11 — Exclusão de curso remove item da listagem

(Relacionado ao **BUG-004**)

**Pré-condição**

Existe curso cadastrado.

| Passo | Ação | Resultado esperado |
|------|------|--------------------|
| 1 | Acessar listagem | Lista exibida |
| 2 | Localizar curso | Curso encontrado |
| 3 | Clicar em "Excluir curso" | Sistema executa exclusão |
| 4 | Verificar lista | Curso removido da listagem |

---

# CT-L12 — Mensagem de sucesso após exclusão

**Pré-condição**

Curso excluído com sucesso.

| Passo | Ação | Resultado esperado |
|------|------|--------------------|
| 1 | Excluir curso | Sistema executa ação |
| 2 | Verificar mensagem exibida | Sistema mostra mensagem "Curso excluído com sucesso" |