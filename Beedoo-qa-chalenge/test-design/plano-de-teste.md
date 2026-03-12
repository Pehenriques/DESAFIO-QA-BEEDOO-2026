## Plano de Teste — Beedoo QA Challenge (Módulo de Cursos)

### 1. Informações gerais

- **Nome do projeto:** Beedoo QA Challenge — Cadastro e Listagem de Cursos
- **Versão / release:** Aplicação em ambiente Netlify (link fixo do desafio)
- **Responsável pelos testes:** QA / Candidato / Estudante
- **Data de início prevista:** Conforme cronograma do desafio
- **Data de término prevista:** Conforme cronograma do desafio

---

### 2. Objetivos do teste

- **Objetivo geral:** Validar o módulo de cursos da aplicação Beedoo QA (cadastro e listagem), documentando cenários, casos de teste, execução e bugs conforme critérios do desafio.
- **Objetivos específicos:**
  - Avaliar **raciocínio analítico** (observar, decompor e entender o sistema).
  - Exercitar **modelagem de testes** (requisitos e fluxos em cenários e casos de teste).
  - Desenvolver **atenção a detalhes** (identificar nuances e possíveis problemas).
  - Garantir **clareza na documentação** (achados e planos de teste compreensíveis e organizados).

---

### 3. Escopo

- **Escopo incluído:**
  - Fluxo principal de cadastro de curso.
  - Funcionalidade de listagem de cursos.
  - Cenários negativos (entradas inválidas, condições de erro).
  - Validações de campos.
  - Comportamentos inesperados / casos de borda.
- **Escopo excluído (fora de escopo):**
  - Módulos fora do escopo “cursos” (se a aplicação tiver outros no futuro).
  - Testes de carga/estresse (a menos que solicitado).
  - Testes automatizados (escopo do desafio é manual).

---

### 4. Itens de teste

- Tela de listagem de cursos (lista, links, estado vazio).
- Tela de cadastro de curso (formulário, campos, botões).
- Navegação entre “Listar cursos” e “Cadastrar curso”.
- Validações no formulário de cadastro.
- Inclusão do curso cadastrado na listagem.
- Mensagens de sucesso e erro.

---

### 5. Tipos e níveis de teste

- **Níveis:** Teste de sistema (funcionalidade de ponta a ponta na interface).
- **Tipos:** Funcional, regressão básica, negativos, validação de campos, exploratório guiado.

---

### 6. Abordagem e estratégia de teste

- Testes **baseados em requisitos** (RF-01 a RF-10) e em **fluxos** (listagem e cadastro).
- Priorização: fluxo principal de cadastro e listagem (alta); validações e negativos (alta/média); bordas e usabilidade (média).
- Regressão: após correções ou para validar que cadastro e listagem continuam funcionando.
- Exploração guiada: uso de checklist para cobrir cadastro e listagem de forma sistemática.

---

### 7. Ambiente de teste

- **Ambiente:** Aplicação em produção/homologação (Netlify) — [https://creative-sherbet-a51eac.netlify.app/](https://creative-sherbet-a51eac.netlify.app/)
- **Configuração de hardware:** Conforme máquina do executor.
- **Configuração de software:** Navegador moderno (Chrome, Edge, Firefox — indicar versão no relatório de execução); SO (Windows/macOS/Linux).
- **Dados de teste:** Cursos com nomes válidos, campos vazios, dados inválidos e caracteres especiais conforme casos de teste.

---

### 8. Critérios de entrada e saída

- **Critérios de entrada:** Aplicação acessível; requisitos e plano de teste definidos; casos de teste escritos (Gherkin e estruturado).
- **Critérios de saída:** Execução dos cenários planejados documentada; evidências (prints/gravações) registradas; bugs encontrados documentados com título, passos, resultado atual/esperado e severidade.

---

### 9. Riscos e mitigações

| Risco ID | Descrição do risco | Probabilidade | Impacto | Mitigação sugerida |
|----------|--------------------|---------------|---------|--------------------|
| R-01 | Aplicação indisponível ou instável | Baixa | Alto | Testar em horário de menor carga; documentar indisponibilidade. |
| R-02 | Campos do formulário diferentes do documentado | Média | Médio | Revisar casos após primeira exploração; atualizar requisitos/casos se necessário. |

---

### 10. Cronograma (alto nível)

- **M1** – Análise e exploração da aplicação.
- **M2** – Criação de cenários e casos de teste (Gherkin e estruturado).
- **M3** – Execução dos testes e registro de evidências.
- **M4** – Registro de bugs e consolidação do relatório de execução.

---

### 11. Responsabilidades

- **Responsável pelo plano de teste:** QA / executor do desafio.
- **Executores dos testes:** QA / estudante.
- **Aprovadores:** Conforme critério do processo seletivo ou do curso.
