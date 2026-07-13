---
title: Configurações
parent: Módulos
nav_order: 6
role: [supervisor]
screenshots: [mod-configuracoes-01]
last_verified: 2026-07-13
status: publicado
description: A identidade da organização, as notificações por e-mail e o comportamento da Central de Atendimento.
---

# Configurações
{: .no_toc }

Em **V3RHelp! > Configurações** ficam os ajustes gerais do sistema, organizados em grupos.

<details open markdown="block">
  <summary>Nesta página</summary>
- TOC
{:toc}
</details>

![Configurações](../assets/mod-configuracoes-01.png)

---

## Geral (a identidade da organização)

- **Nome da organização** — aparece no painel e no **cabeçalho dos e-mails**.
- **E-mail de suporte** — usado como remetente das mensagens automáticas.
- **Logo da organização** — enviada para a biblioteca de mídia; aparece nas páginas públicas
  de chamado e no **topo dos e-mails**.

{: .importante }
> Preencher o **nome, o e-mail e a logo** dá aos e-mails e às páginas a cara da sua
> organização. Quem recebe um chamado confia mais numa mensagem que parece vir de "você" do
> que de um sistema genérico — e isso reduz e-mails ignorados como se fossem spam.

## Chamados

- **Limite de reaberturas por chamado** — quantas vezes um chamado resolvido pode ser reaberto.
- **Designar operador automaticamente por rodízio ao abrir o chamado** — quando **ligado**
  (padrão), todo chamado novo já sai com um operador, escolhido por rodízio entre os elegíveis
  da categoria. **Desligado**, os chamados abrem **sem operador**, para a equipe designar à mão.

{: .importante }
> O limite de reaberturas evita que um único chamado vire uma conversa infinita. Quando o
> limite é atingido, o sistema abre **automaticamente** um novo chamado vinculado — o que
> mantém o histórico organizado sem perder a nova mensagem.

{: .dica }
> Deixe a **designação automática** ligada se você usa rodízio por categoria e quer que nada
> fique sem dono. Desligue se prefere que um supervisor **triagem** os chamados e distribua
> manualmente.

## Notificações

A **chave geral** liga ou desliga os e-mails automáticos. Abaixo dela, você controla **cada
tipo** de aviso:

- Confirmar a abertura do chamado ao solicitante
- Avisar sobre novas respostas
- Avisar o solicitante quando o chamado for resolvido
- Avisar o operador quando o chamado for reaberto
- **Avisar o operador (novo e anterior) quando o chamado for (re)designado**
- **Enviar cópia de cada chamado aberto aos supervisores** — todo supervisor recebe uma cópia
  de acompanhamento quando um chamado é aberto (sem duplicar quem já é o solicitante ou o
  operador). Vem **ligado**
- **Lembrete de SLA** (chamado em risco ou vencido) aos operadores
- **Lembrete de chamados parados (inatividade)** — e, ao lado, **quantos dias** sem
  movimentação disparam o lembrete

{: .importante }
> Os **lembretes** são o que impede um chamado de ser esquecido. O aviso de SLA faz a equipe
> agir antes de estourar o prazo; o lembrete de inatividade cutuca chamados que ficaram
> parados — sugerindo, inclusive, marcar como Resolvido o que já foi concluído. Ajuste os
> dias para o ritmo real da sua equipe: um número baixo demais vira spam; alto demais deixa
> chamados esfriarem.

{: .dica }
> Os lembretes rodam por uma tarefa agendada (a cada hora) do WordPress. Se os e-mails
> automáticos não estiverem chegando, confira com o responsável técnico se o **WP-Cron** do
> site está ativo.

## Frontend público

- **Permitir que visitantes (sem login) abram chamados** — habilita a abertura por quem não
  tem conta (com nome + e-mail e magic link).
- **Papéis que podem abrir chamados** — se vazio, qualquer usuário logado pode; senão,
  restringe aos papéis escolhidos.
- **URL da página da Central de Atendimento** — o endereço da página onde você publicou o
  shortcode `[v3rhelp_central]`. É usado para montar os **links dos e-mails**.
- **Exibir a logo da organização nas telas públicas** — liga ou desliga a logo no topo dos
  shortcodes/blocos públicos. Vem **ligada**; desligue se preferir as páginas de atendimento
  sem a logo (por exemplo, quando a página do site já tem o cabeçalho da marca).
- **Proteção anti-spam na abertura por visitantes** — vem **ligada**. Sem captcha e sem
  incomodar quem é gente de verdade: barra robôs por trás dos panos (campo-isca invisível,
  tempo mínimo de preenchimento e um limite de aberturas por origem). Só afeta **visitantes
  sem login**; quem já está logado passa direto.

{: .importante }
> Definir a **URL da Central** garante que os botões "Acompanhar meu chamado" dos e-mails
> levem a pessoa exatamente para a página certa — inclusive nos avisos enviados
> automaticamente, que não têm como adivinhar esse endereço sozinhos.

{: .atencao }
> Liberar a abertura para **visitantes** é ótimo para acessibilidade, mas expõe o formulário a
> spam. Por isso a **proteção anti-spam** (acima) já vem ligada — deixe-a ativa quando permitir
> visitantes. Ela é invisível para o público e não pede captcha.
