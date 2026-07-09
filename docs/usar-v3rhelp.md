---
title: Como usar bem o V3RHelp
nav_order: 5
description: O passo a passo do V3RHelp para cada perfil, com o fluxo de um chamado do início ao fim.
---

# Como usar bem o V3RHelp
{: .no_toc }

Aqui o conceito vira prática. Primeiro, entenda **a jornada de um chamado** do começo ao
fim; depois, veja o passo a passo para o **seu perfil**.

<details open markdown="block">
  <summary>Nesta página</summary>
- TOC
{:toc}
</details>

---

## A jornada de um chamado

Todo chamado percorre um caminho parecido. O diagrama abaixo mostra esse fluxo — do momento
em que alguém pede ajuda até o encerramento.

```mermaid
flowchart TD
    A([Solicitante abre o chamado]):::req --> B[Status: Aberto]:::open
    B --> C{Operador designado?}:::dec
    C -- Automático rodízio / manual --> D[Operador atende]:::prog
    C -- Ninguém disponível --> E[Aguardando triagem]:::wait
    E --> D
    D --> F[Status: Em andamento]:::prog
    F --> G{Precisa de mais informações?}:::dec
    G -- Sim --> H[Status: Aguardando]:::wait
    H --> I([Solicitante responde]):::req
    I --> F
    G -- Não --> J[Operador resolve]:::prog
    J --> K[Status: Resolvido]:::done
    K --> L([Solicitante é avisado por e-mail]):::req
    L --> M{Problema resolvido?}:::dec
    M -- Sim --> N([Fim 🎉]):::done
    M -- Não --> O[Status: Reaberto]:::reopen
    O --> F

    classDef req fill:#eef6ee,stroke:#93b493,color:#071b07;
    classDef open fill:#eff6ff,stroke:#bfdbfe,color:#1d4ed8;
    classDef prog fill:#eef2ff,stroke:#c7d2fe,color:#4338ca;
    classDef wait fill:#fffbeb,stroke:#fde68a,color:#b45309;
    classDef done fill:#e3ece3,stroke:#93b493,color:#071b07;
    classDef reopen fill:#fff7ed,stroke:#fed7aa,color:#c2410c;
    classDef dec fill:#ffffff,stroke:#cbd5e1,color:#334155;
```

{: .dica }
> Cada caixa colorida corresponde a um **status** do chamado. Os mesmos nomes aparecem no
> painel e no [glossário](/definicoes/#status).

---

## Para a equipe de suporte

Você é **operador** ou **supervisor**. Seu trabalho acontece no painel do WordPress, no menu
**V3RHelp!**.

### Seu dia a dia como operador

1. Abra o menu **V3RHelp! > Chamados** e veja a fila.
2. Use os **filtros** (status, categoria) e a **busca** para achar o que importa.
3. Abra um chamado, **leia o pedido** e, se ainda não tiver dono, **assuma** (designe-se).
4. **Responda** ao solicitante de forma clara; use **nota interna** para registros da equipe.
5. Precisa de algo do solicitante? Mude para **Aguardando** e peça a informação.
6. Resolveu? Mude para **Resolvido** — o solicitante é avisado automaticamente.

O detalhe do chamado também mostra o **Ambiente do solicitante** (navegador, sistema, tela),
capturado na abertura — isso ajuda a diagnosticar sem precisar perguntar.

### Como supervisor, além disso

1. Acompanhe o **Dashboard** (abertos, tempo médio, sem operador) para enxergar a operação.
2. Ajuste **Categorias** e **políticas de SLA** conforme a realidade da equipe.
3. Cuide da **Equipe** (operadores e supervisores) e do que cada um atende.
4. Configure as **Notificações** (inclusive lembretes de chamados parados) em **Configurações**.

Cada uma dessas telas é detalhada em [Módulos](/modulos/).

---

## Para quem abre chamados

Você acessa o V3RHelp por uma **página do site** (a Central de Atendimento), não pelo painel.

1. Acesse a página de atendimento indicada pela sua organização.
2. Clique/role até **Abrir chamado** e preencha: assunto, categoria e uma boa descrição.
   (Veja como caprichar no relato em [Guia de Quem Abre Chamados](/guia-solicitante/).)
3. **Anexe** prints ou arquivos que ajudem a entender.
4. Envie. Você recebe um **e-mail de confirmação** com o número do chamado e um botão para
   acompanhar.
5. A cada resposta da equipe, você é avisado por e-mail. Responda pelo próprio chamado.

{: .exemplo }
> Se você **não tem conta** no site, tudo bem: ao abrir o chamado você informa seu nome e
> e-mail e recebe um **magic link** — um link seguro para acompanhar e responder sem precisar
> criar login.
