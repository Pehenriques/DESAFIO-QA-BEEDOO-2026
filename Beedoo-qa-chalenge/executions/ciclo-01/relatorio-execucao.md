# Relatório de Execução — Ciclo 01

**Projeto:** Beedoo QA Challenge — Módulo de Cursos  
**Ciclo:** 01  
**Data da execução:** 10/03/2026  
**Responsável:** [Seu nome]  
**Ambiente:** Google Chrome 120 / Windows 11

---

## 1. Objetivo do ciclo

Executar os cenários e casos de teste criados para o módulo de cursos (cadastro e listagem), registrar resultados e evidências (prints e/ou gravação de tela) e documentar bugs encontrados.

---

## 2. Ambiente de execução

| Item | Descrição |
|------|-----------|
| URL da aplicação | https://creative-sherbet-a51eac.netlify.app/ |
| Navegador(s) | Google Chrome 120 |
| Sistema operacional | Windows 11 |
| Data/hora | 10/03/2026 |

---

# 3. Resultados por caso de teste

## 3.1 Cadastro de curso

| ID caso | Título | Status | Observações / Evidências |
|---------|--------|--------|--------------------------|
| CT-C01 | Cadastro com todos os campos válidos | Aprovado | evidencias/CT-C01-cadastro-sucesso.png |
| CT-C02 | Cadastro com preenchimento mínimo obrigatório | Aprovado | evidencias/CT-C02-cadastro-minimo.png |
| CT-C03 | Navegação para tela de cadastro | Aprovado | Navegação funcionando corretamente |
| CT-C04 | Retorno à listagem após cadastro | Aprovado | Redirecionamento correto |
| CT-C05 | Cadastro com campo obrigatório em branco | Reprovado | Sistema permite envio sem validação — BUG-001 |
| CT-C06 | Cadastro com formulário vazio | Reprovado | Sistema aceita envio de formulário vazio — BUG-002 |
| CT-C07 | Campo obrigatório apenas com espaços | Reprovado | Sistema aceita campo apenas com espaços |
| CT-C08 | Nome do curso com caracteres especiais | Aprovado | Sistema aceita caracteres sem quebrar |
| CT-C09 | Nome do curso com texto muito longo | Aprovado | Layout permanece estável |
| CT-C10 | Duplo envio do formulário | Aprovado | Não houve duplicidade |
| CT-C11 | Voltar para listagem sem cadastrar | Aprovado | Navegação correta |
| CT-C12 | Campo numérico com texto | Reprovado | Campo aceita caractere "e", "+" e "-" — BUG-005 |
| CT-C13 | Submissão com tecla Enter | Aprovado | Formulário submetido corretamente |

---

## 3.2 Listagem de cursos

| ID caso | Título | Status | Observações / Evidências |
|---------|--------|--------|--------------------------|
| CT-L01 | Visualizar lista de cursos cadastrados | Aprovado | Cursos exibidos corretamente |
| CT-L02 | Acesso à listagem via link "Listar cursos" | Aprovado | Navegação funcional |
| CT-L03 | Curso recém-cadastrado visível na listagem | Reprovado | Listagem não atualiza automaticamente — BUG-002 |
| CT-L04 | Listagem exibe mais de um curso | Aprovado | Vários cursos exibidos corretamente |
| CT-L05 | Comportamento da listagem sem cursos | Aprovado | Sistema não apresenta erro |
| CT-L06 | Listagem atualizada após cadastro | Reprovado | Necessário atualizar página manualmente — BUG-002 |
| CT-L07 | Navegação entre listagem e cadastro | Aprovado | Navegação consistente |
| CT-L08 | Acesso direto à URL da listagem | Aprovado | Página carrega corretamente |
| CT-L09 | Ordem dos cursos na listagem | Aprovado | Ordem consistente |
| CT-L10 | Nome de curso longo na listagem | Aprovado | Layout não quebra |

---

# 4. Resumo do ciclo

| Métrica | Quantidade |
|---------|------------|
| Total de casos executados | 23 |
| Aprovados | 16 |
| Reprovados | 7 |
| Bloqueados | 0 |
| Não executados | 0 |

---

# 5. Evidências da execução

Conforme solicitado no desafio, foram registradas evidências da execução através de **capturas de tela**.

As evidências estão organizadas na pasta:

Exemplos de arquivos:

- evidencias/Print_001
- evidencias/Print_003
- evidencias/Print_005


Essas imagens demonstram os resultados obtidos durante a execução dos testes.

---

# 6. Bugs encontrados neste ciclo

| ID Bug | Caso de teste relacionado | Resumo |
|------|---------------------------|--------|
| BUG-001 | CT-C05 | Sistema permite cadastro com campo obrigatório em branco |
| BUG-002 | CT-L03 / CT-L06 | Listagem não atualiza após cadastro |
| BUG-003 | CT-C07 | Sistema aceita data de fim anterior à data de início |
| BUG-004 | CT-L11 | Exclusão de curso exibe sucesso mas não remove da lista |
| BUG-005 | CT-C12 | Campo "Número de vagas" aceita caracteres não numéricos |

---

# 7. Observações e conclusões

Durante a execução dos testes foram identificados **problemas de validação de formulário e inconsistências na atualização da listagem de cursos**.

Principais pontos observados:

- Falta de validação em campos obrigatórios
- Validação inadequada de campos numéricos
- Problemas na atualização da listagem após operações de cadastro
- Inconsistência na exclusão de cursos

Esses problemas podem comprometer a **integridade dos dados e a experiência do usuário**.

Recomenda-se:

- Implementar validações adequadas nos campos do formulário
- Garantir atualização automática da listagem após operações
- Validar corretamente operações de exclusão
- Reexecutar os testes após correções para validar o comportamento esperado.
