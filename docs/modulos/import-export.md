---
title: Importar / Exportar
parent: Módulos
nav_order: 7
role: [supervisor]
screenshots: [mod-import-export-01]
last_verified: 2026-07-09
status: publicado
description: Levar e trazer configurações e chamados — para backup, migração ou réplica entre sites.
---

# Importar / Exportar
{: .no_toc }

<details open markdown="block">
  <summary>
    Sumário
  </summary>
  {: .text-delta }
1. TOC
{:toc}
</details>

O módulo **Importação/Exportação** permite levar e trazer dados do V3RHelp!: configurações completas ou chamados, em JSON ou CSV. Ele fica em **V3RHelp! > Importação/Exportação**.

{: .atencao }
> Este recurso faz parte do plano Pro. Se o seu site ainda estiver no plano gratuito, o módulo aparece bloqueado.

![Importar e exportar](../assets/mod-import-export-01.png)

## Exportar

Três opções de exportação estão disponíveis:

- **Configuração completa (JSON)**: exporta configurações gerais, políticas de SLA, categorias e a equipe (operadores) em um único arquivo. É o backup mais completo do módulo.
- **Chamados (JSON)**: exporta todos os chamados em formato JSON, preservando a estrutura de dados por completo.
- **Chamados (CSV)**: exporta todos os chamados em formato de planilha (CSV), ideal para abrir no Excel, Google Sheets ou similar.

Clique no botão correspondente e o arquivo é baixado automaticamente para o seu computador.

{: .importante }
> Exportar a configuração completa é o seu seguro contra perda de dados ou erros de configuração. Faça isso antes de qualquer mudança grande (ex.: alterar políticas de SLA, reorganizar categorias) para poder recuperar o estado anterior se algo sair errado.

## Importar

Duas opções de importação estão disponíveis:

- **Configurações (JSON)**: importa um arquivo de configuração completa exportado anteriormente, restaurando configurações gerais, políticas de SLA, categorias e equipe.
- **Chamados (JSON/CSV)**: importa chamados a partir de um arquivo JSON ou CSV exportado anteriormente (ou gerado por outra fonte compatível).

Selecione o arquivo e confirme a importação. O sistema processa os dados e informa quantos itens foram importados.

### Deduplicação por código

Ao importar chamados, o sistema verifica o código de cada chamado no arquivo. Se já existir um chamado com aquele código no site, ele é **ignorado** — não é duplicado nem sobrescrito.

{: .importante }
> Graças à deduplicação por código, você pode reimportar um arquivo de chamados quantas vezes precisar sem medo de criar duplicatas. Isso é útil, por exemplo, para reprocessar uma importação que falhou parcialmente.

## Casos de uso comuns

- **Backup periódico**: exporte a configuração completa regularmente (ex.: antes de atualizações do plugin ou mudanças estruturais) e guarde os arquivos em local seguro.
- **Migrar de um site para outro**: exporte configuração e chamados no site de origem, depois importe ambos no site de destino.
- **Replicar a configuração-padrão em uma nova instalação**: exporte a configuração completa de um site já ajustado e importe-a em uma nova instalação para começar com categorias, SLA e equipe já prontos.

{: .atencao }
> Guarde os arquivos exportados em local seguro — eles podem conter dados dos chamados, incluindo informações de clientes. Prefira CSV quando quiser abrir e analisar os dados em uma planilha; use JSON quando o objetivo for reimportar os dados no V3RHelp!, pois ele preserva a estrutura completa.
