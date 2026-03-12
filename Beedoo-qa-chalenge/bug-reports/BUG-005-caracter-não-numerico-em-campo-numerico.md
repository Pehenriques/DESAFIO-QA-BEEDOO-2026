# BUG-005 — Sistema permite inserir caractere não numérico no campo "Número de vagas"

### Identificação

- ID do bug: BUG-005
- Título: Sistema permite inserir caractere não numérico no campo "Número de vagas"
- Projeto / Aplicação: Beedoo QA Tests — Módulo de Cursos
- Módulo / Tela: Cadastro de curso
- Data de registro: 10/03/2026
- Reportado por: Pedro Henrique

---

### Classificação

- Severidade: Média
- Prioridade: Média
- Tipo: Funcional (Validação de campo)

---

### Ambiente

- URL: https://creative-sherbet-a51eac.netlify.app/new-course
- Navegador: Google Chrome
- Sistema operacional: Windows 10

---

### Descrição

Durante a execução dos testes de validação do campo **Número de vagas**, foi observado que o sistema permite inserir caracteres não numéricos, como a letra **"e"** e os símbolos **"+"** e **"-"**.

Esse comportamento permite a entrada de valores inválidos em um campo que deveria aceitar apenas números inteiros positivos.

### Passos para reproduzir

1. Acessar a página de **Cadastro de curso**
2. Localizar o campo **Número de vagas**
3. Inserir o caractere **"e"**
4. Inserir também os símbolos **"+"** ou **"-"**
5. Tentar prosseguir com o preenchimento do formulário

---

### Resultado esperado

O campo **Número de vagas** deve:

- Aceitar apenas **números inteiros positivos**
- Bloquear a inserção de **letras ou caracteres especiais**
- Exibir mensagem de erro caso valor inválido seja inserido
- Impedir o envio do formulário com valor inválido

Exemplo de mensagem esperada:

"O campo Número de vagas deve conter apenas números."

---

### Resultado atual (obtido)

O sistema permite inserir caracteres não numéricos no campo **Número de vagas**, incluindo:

- letra **"e"**
- símbolo **"+"**
- símbolo **"-"**

Nenhuma mensagem de erro ou validação é exibida ao usuário.
---

### Evidências

- evidencias/Print-009.png

---

### Severidade ou impacto

- **Severidade:** Media 

- **Impacto:** Esse problema pode gerar:

- Inserção de dados inválidos no sistema
- Inconsistência nas informações armazenadas
- Possíveis erros em cálculos ou relatórios futuros

A severidade pode ser considerada **Alta** caso o sistema permita salvar o valor inválido na base de dados ou gere erros posteriores no sistema.

### Status e histórico

- **Status atual:**  Em análise 
- **Datas:** 10/03/2026
