# Biblioteca de Skills

Biblioteca pessoal de skills para apoiar discovery, análise, planejamento e melhoria contínua.

As skills ficam em [`skills/`](./skills/), organizadas por categoria. O índice completo está em [`skills/index.md`](./skills/index.md).

## Padrão de uma skill

Cada skill deve ser um arquivo Markdown direto dentro de uma pasta de categoria:

```text
skills/
└── Categoria/
    └── Nome-da-Skill.md
```

Use nomes de categoria com a primeira letra maiúscula e nomes de arquivo em Pascal Case com hífens, por exemplo `Analise/Analise-de-Riscos.md`, `Planejamento/Registro-de-Decisoes.md` e `Planejamento/Cinco-W-Dois-H.md`.

## Frontmatter da skill

Cada arquivo `.md` de skill deve começar com o frontmatter documental:

```yaml
---
id: nome-da-skill
title: Título da skill
description: Descreva o que a skill faz e em quais situações ela deve ser usada.
lastUpdated: 2026-07-30
creator: Eudes Carvalho
tags: [categoria, assunto]
---
```

Regras:

- `id` deve usar lowercase, números e hífens.
- O nome do arquivo deve ser legível e corresponder ao título da skill.
- `description` deve explicar a capacidade e os principais gatilhos de uso.
- A descrição deve ter no máximo 1024 caracteres.
- Os campos documentais devem permanecer no início do arquivo.

## Metadados de catálogo

Índices e documentos de catálogo usam o padrão completo:

```yaml
---
id: nome-do-documento
title: Título do documento
description: Descrição curta do documento.
lastUpdated: 2026-07-30
creator: Eudes Carvalho
tags: [categoria, assunto]
---
```

O [`skills/index.md`](./skills/index.md) deve listar cada arquivo com título, link relativo e descrição curta.

## Padrão de conteúdo

Escreva em português do Brasil, preservando termos técnicos consolidados em inglês, como AS IS, TO BE, stakeholders, Root Cause Analysis, Run the Business, Change the Business e Transform the Business.

Cada skill deve:

- Explicar o papel que o Codex deve desempenhar.
- Indicar quando deve ser usada por meio do frontmatter.
- Orientar o fluxo de trabalho em etapas claras.
- Fazer perguntas antes de concluir quando houver informação insuficiente.
- Diferenciar fatos, hipóteses, decisões, riscos e pendências.
- Não inventar dados, regras, responsáveis, prazos ou custos.
- Produzir um resultado final definido, reutilizável e acionável.
- Usar critérios, tabelas ou checklists quando melhorarem a consistência.
- Manter o conteúdo essencial no próprio arquivo `.md` e evitar documentação auxiliar desnecessária.

Prefira instruções no imperativo ou no infinitivo:

```markdown
Colete o contexto da iniciativa.
Identifique os responsáveis.
Gere o plano de ação.
```

## Padrão para skills de entrevista

Skills de discovery, diagnóstico ou levantamento devem:

1. Começar entendendo objetivo e contexto.
2. Fazer no máximo cinco perguntas por rodada.
3. Analisar as respostas antes da próxima rodada.
4. Pedir exemplos quando a resposta for vaga.
5. Identificar lacunas, riscos, dependências e contradições.
6. Evitar gerar o documento final antes de obter informação suficiente.
7. Sinalizar hipóteses e pendências explicitamente.

## Padrão para entregáveis

Quando aplicável, o resultado deve conter resumo executivo, contexto, objetivo, problema, escopo, envolvidos, dependências, regras, premissas, restrições, riscos, decisões, recomendações, plano de ação, critérios de conclusão, pendências e próximos passos.

Não preencher campos desconhecidos com valores inventados. Usar `A definir`, `Pendente` ou uma seção de pendências quando necessário.

## Como criar uma nova skill

1. Escolha a categoria adequada em `skills/`.
2. Crie um arquivo `.md` com o nome iniciando em maiúscula.
3. Adicione o frontmatter documental completo.
4. Escreva a descrição com os gatilhos de uso.
5. Defina o fluxo, os critérios e o formato do resultado.
6. Adicione a skill na seção correspondente de [`skills/index.md`](./skills/index.md).
7. Atualize `lastUpdated` quando alterar o catálogo.
8. Valide a skill antes de finalizar.

## Validação

Como as skills desta biblioteca são documentos Markdown planos, valide manualmente:

```powershell
Get-ChildItem .\skills -Filter *.md -Recurse
```

Confira também se o arquivo `.md` existe na categoria correta, se o `id` é único, se a descrição informa quando usar a skill, se o índice foi atualizado e se todos os links apontam para arquivos existentes.

## Categorias atuais

- **Discovery:** descoberta de features, iniciativas e mudanças.
- **Análise:** diagnóstico, maturidade, causa raiz e riscos.
- **Planejamento:** 5W2H, decisões e organização da execução.
- **Melhoria contínua:** retrospectivas, aprendizados e ações corretivas.
