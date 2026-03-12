# Checklist de Teste Exploratório — Módulo de Cursos (Beedoo QA)

> Use este checklist como apoio em sessões de teste exploratório na aplicação Beedoo QA (cadastro e listagem de cursos).  
> **URL:** https://creative-sherbet-a51eac.netlify.app/

---

## 1. Informações da sessão

- **Projeto / aplicação:** Beedoo QA Tests — Módulo de Cursos
- **Objetivo da sessão:** Explorar fluxos de cadastro e listagem; identificar comportamentos inesperados e possíveis bugs
- **Charter (missão da sessão):** Validar fluxo de cadastro, validações de formulário, listagem e exclusão de cursos
- **Duração prevista:** 60 minutos
- **Tester:** [Seu nome]

---

## 2. Listagem de cursos

- [ ] A tela de listagem carrega ao acessar a aplicação
- [ ] Os cursos cadastrados são exibidos corretamente na lista
- [ ] O link **Cadastrar curso** está visível e direciona corretamente
- [ ] O link **Listar cursos** retorna à tela de listagem
- [ ] Quando não há cursos cadastrados, o sistema exibe estado vazio ou mensagem adequada
- [ ] A ordem da listagem é consistente
- [ ] Nomes de cursos muito longos não quebram o layout da página
- [ ] Após cadastrar um novo curso, ele aparece na listagem
- [ ] Após excluir um curso, ele é removido da listagem

---

## 3. Cadastro de curso — fluxo principal

- [ ] Ao clicar em **Cadastrar curso**, a tela de cadastro é exibida
- [ ] Os campos do formulário estão visíveis e compreensíveis
- [ ] É possível preencher todos os campos e cadastrar um curso válido
- [ ] Após o cadastro, o sistema exibe mensagem de sucesso
- [ ] Após cadastrar, o sistema redireciona para a listagem
- [ ] O curso recém cadastrado aparece na lista sem necessidade de atualização manual da página

---

## 4. Cadastro de curso — validações e testes negativos

### Validação de campos obrigatórios

- [ ] O sistema impede cadastro com campo obrigatório vazio  
- [ ] O sistema impede envio de formulário completamente vazio  
- [ ] Campos preenchidos apenas com espaços são tratados como inválidos  

*(Relacionados aos bugs encontrados: BUG-001 e BUG-003)*

---

### Validação de campos numéricos

- [ ] O campo **Número de vagas** aceita apenas números
- [ ] O campo bloqueia letras como "e"
- [ ] O campo bloqueia símbolos como "+" ou "-"
- [ ] O sistema impede envio do formulário com valor inválido

*(Relacionado ao BUG-005)*

---

### Validação de datas

- [ ] O sistema impede cadastro quando **data de fim é anterior à data de início**
- [ ] O sistema exibe mensagem de erro para datas inválidas

*(Relacionado ao BUG-003 – validação de datas)*

---

### Validação de conteúdo

- [ ] O campo **Nome do curso** aceita caracteres especiais sem quebrar a aplicação
- [ ] Textos muito longos não quebram o layout ou geram erro
- [ ] O formulário não permite cadastro duplicado ao clicar várias vezes no botão

---

## 5. Navegação e usabilidade

- [ ] Navegação entre **Listar cursos** e **Cadastrar curso** funciona corretamente
- [ ] Os botões respondem corretamente ao clique
- [ ] As mensagens de erro são claras e compreensíveis
- [ ] As mensagens de sucesso representam ações realmente concluídas
- [ ] Não há mensagens técnicas ou erros de sistema visíveis para o usuário

---

## 6. Operações de exclusão

- [ ] É possível excluir um curso existente
- [ ] O sistema exibe mensagem de confirmação de exclusão
- [ ] Após excluir, o curso desaparece da listagem

*(Relacionado ao BUG-004)*

---

## 7. Comportamentos inesperados / testes de borda

- [ ] Submissão do formulário utilizando a tecla **Enter**
- [ ] Atualização da página após cadastro
- [ ] Cadastro de múltiplos cursos em sequência
- [ ] Recarregar a página durante preenchimento do formulário
- [ ] Navegar diretamente para URL de cadastro ou listagem
- [ ] Verificar se há duplicação de cursos após recarregar a página

---

## 8. Observações da sessão

**Notas relevantes:**  
[Registrar comportamentos observados durante os testes exploratórios.]

**Ideias de melhoria:**  
[Sugestões de melhorias de interface, validação ou experiência do usuário.]

**Riscos identificados:**  
[Possíveis problemas de persistência de dados, validações ausentes ou inconsistências.]

---

## 9. Bugs encontrados nesta sessão

| ID Bug | Resumo |
|------|--------|
| BUG-001 | Cadastro permite envio com campo obrigatório vazio |
| BUG-002 | Listagem não atualiza após cadastro |
| BUG-003 | Sistema aceita datas inconsistentes (data fim anterior à início) |
| BUG-004 | Sistema exibe sucesso ao excluir curso, mas curso permanece na lista |
| BUG-005 | Campo "Número de vagas" aceita caracteres não numéricos |