---
title: Chamados
parent: Módulos
nav_order: 1
role: [operador, supervisor]
screenshots: [mod-chamados-lista, mod-chamados-detalhe]
last_verified: 2026-07-09
status: publicado
description: A fila de chamados e o atendimento de cada um — respostas, notas internas, anexos, status e designação.
---

# Chamados
{: .no_toc }

É aqui que o suporte acontece. A tela **Chamados** tem duas partes: a **lista** (a fila) e o
**detalhe** de um chamado.

<details open markdown="block">
  <summary>Nesta página</summary>
- TOC
{:toc}
</details>

---

## A lista de chamados

Abra **V3RHelp! > Chamados**. Você vê todos os chamados, com código, assunto, categoria,
operador, status, SLA e data.

![Lista de chamados](../assets/mod-chamados-lista.png)

- **Filtros** por status e categoria, e uma **busca** por assunto ou código.
- **Ordenação** clicando nos cabeçalhos das colunas.
- **Ações rápidas** em cada linha: abrir, responder, ou "marcar como…" (mudar o status).
- **Novo Chamado** para abrir um chamado em nome de alguém (por telefone, por exemplo).

{: .importante }
> O **semáforo de SLA** na lista mostra, num olhar, quais chamados estão no prazo, em atenção
> ou vencidos. É ele que ajuda a equipe a decidir **o que atacar primeiro** — priorizar pelo
> vermelho evita estourar prazos e clientes insatisfeitos.

## O detalhe do chamado

Clique em um chamado para abri-lo. À esquerda ficam a conversa e as ações; à direita, um
resumo.

![Detalhe do chamado](../assets/mod-chamados-detalhe.png)

### Responder e anotar

- **Responder:** escreve uma mensagem que o **solicitante recebe** (por e-mail e no chamado).
- **Nota interna:** um registro **visível só para a equipe** — use para raciocínio,
  verificações e combinados internos.
- **Anexar:** adicione arquivos à sua resposta.

{: .importante }
> Diferenciar **resposta** de **nota interna** é o que mantém a comunicação limpa: o cliente
> recebe só o que interessa a ele, e a equipe preserva seu histórico técnico sem poluir a
> conversa. Registrar sempre evita que, ao trocar de operador, o atendimento recomece do zero.

### Mudar o status

Use **"Mudar status…"** para levar o chamado por seu ciclo (Aberto → Em andamento →
Aguardando → Resolvido). O sistema só oferece as transições válidas.

{: .importante }
> Manter o status **atualizado** é o que faz os relatórios e os prazos fazerem sentido. Um
> chamado resolvido que continua "Em andamento" distorce os números e some da conta de quem
> precisa de ação. Ao concluir, marque **Resolvido** — o solicitante é avisado na hora.

### Designar um operador

No resumo à direita, escolha o **operador** responsável. Chamados sem dono tendem a ser
esquecidos.

{: .importante }
> A **designação** dá um dono claro ao chamado. Sem responsável, ninguém sabe de quem é a vez
> — e é assim que pedidos "caem no vão". Se sua organização usa rodízio por categoria, a
> designação automática já cuida disso na abertura.

### Reabrir

Se um chamado resolvido volta a ter problema, use **Reabrir** e informe o motivo (há um
limite de reaberturas configurável).

### Ambiente do solicitante

No resumo, o painel **Ambiente do solicitante** mostra navegador, sistema operacional, tela e
versões — capturados automaticamente na abertura.

{: .importante }
> Saber o **ambiente** de quem abriu o chamado poupa uma rodada inteira de perguntas ("qual
> navegador? qual dispositivo?") e ajuda a reproduzir problemas que só acontecem em certas
> configurações. É diagnóstico na hora, sem incomodar o solicitante.
