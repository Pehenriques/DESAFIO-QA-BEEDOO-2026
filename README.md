# DESAFIO-QA-BEEDOO-2026


Google sheets: https://docs.google.com/spreadsheets/d/1EZVVVtc21dF-wgcKhzfxrFpq-btVWLyJx60mapwIiek/edit?usp=sharing
Google Drive: https://drive.google.com/drive/folders/1Qfx-1G4ru_mDvY3am5mGwQYI8G_EUTnK?usp=drive_link

Este projeto foi desenvolvido como parte do Beedoo QA Challenge, com o objetivo de aplicar conceitos de análise de requisitos, modelagem de testes, execução e registro de bugs em uma aplicação web de cadastro e listagem de cursos.

A aplicação testada é uma aplicação web simples, com foco em:

Cadastro de cursos

Listagem de cursos

Exclusão de cursos

Este repositório reúne todos os artefatos de teste produzidos durante a análise.

## Objetivo da aplicação (interpretação)

A aplicação **Beedoo QA Tests** tem como objetivo permitir que o usuário:

- **Listar** os cursos já cadastrados no sistema.
- **Cadastrar** novos cursos, preenchendo os campos do formulário e submetendo os dados.

Ela serve como ambiente de prática e avaliação para testes manuais, permitindo exercitar análise de fluxos, elaboração de cenários/casos de teste, execução e registro de bugs.

---

## Principais fluxos disponíveis na aplicação

1. **Fluxo de listagem de cursos**
   - Acesso à tela principal (lista de cursos).
   - Visualização dos cursos existentes (ex.: "Curso introdutório para análise de testes em Qualidade de Software (QA)", "Python do Zero").
   - Navegação entre "Listar cursos" e "Cadastrar curso" via links no cabeçalho.

2. **Fluxo de cadastro de curso**
   - Acesso à tela "Cadastrar curso".
   - Preenchimento dos campos do formulário (nome do curso e demais campos disponíveis).
   - Submissão do formulário e retorno/feedback do sistema (sucesso ou erro).

---

## Pontos considerados mais críticos para teste

- **Cadastro de curso:** fluxo principal (campos obrigatórios, validações, mensagens de sucesso/erro).
- **Listagem de cursos:** exibição correta dos dados, Categorização dos cursos cadastrados por data de inicio e fim.
- **Validações de campos:** comportamento com campos vazios, valores invalidos com o tipo do campo (aceitar somente numeros ou letras) .
- **Cenários negativos:** entradas inválidas, duplicidade (se aplicável), comportamento em erro.
- **Comportamentos inesperados:** casos de borda (ex.: muitos caracteres, caracteres especiais, espaços em branco).
