# Candidatura / Proposta ao Estado

Este documento explica **o enquadramento legal** do Livro de Reclamações, **quem decide**, e **como propor** este redesenho como contributo. É deliberadamente realista: como projeto cívico independente, o caminho provável é **proposta de melhoria / contributo open-source**, não adjudicação direta.

## Enquadramento legal (quem manda)

O Livro de Reclamações eletrónico **não é um espaço livre** — é um serviço público legalmente mandatado:

- **Operador:** **Direção-Geral do Consumidor (DGC)**, integrada no Ministério da Economia.
- **Parceiro tecnológico:** **Imprensa Nacional-Casa da Moeda (INCM)**.
- **Base legal principal:**
  - **Decreto-Lei n.º 156/2005**, de 15 de setembro (regime do livro de reclamações), com alterações posteriores.
  - **Decreto-Lei n.º 74/2017**, de 21 de junho (implementa o SIMPLEX+ 2016, "livro de reclamações eletrónico").
  - **Portaria n.º 201-A/2017**, de 30 de junho (formato eletrónico, edição, preço, distribuição).
  - **Portaria n.º 866/2009**, de 13 de agosto (rede telemática de informação comum — RTIC).
- **Modernização / design:** **AMA — Agência para a Modernização Administrativa** (gov.pt, serviços federados, **Decreto-Lei n.º 49/2024**) e o **AGORA Design System**.

**Implicação:** não podemos "substituir" o serviço. Podemos demonstrar uma alternativa melhor e **oferecê-la** às entidades acima.

## Estratégia de proposta

### 1. Pedir acesso ao AGORA
Email para **`designsystem@ticapp.gov.pt`** (ver rascunho abaixo). Mesmo que negado, o pedido documenta boa-fé e abre canal de diálogo.

### 2. Construir o protótipo público (Iterações 1–5)
Ter uma **demo online** funcional e um **repositório auditável** é o que torna a proposta credível. Falar é barato; um protótipo a funcionar não.

### 3. Preparar o dossier
- **Problema** — evidência concreta dos defeitos de UX/acessibilidade do serviço atual (screenshots, auditoria Lighthouse/axe do site oficial, exemplos de fricção).
- **Solução** — o protótipo, com link para a demo e para o repo.
- **Ganhos** — acessibilidade (WCAG 2.1 AA), redução de passos, clareza, alinhamento com o AGORA.
- **Oferta** — código open-source, sem custo, reutilizável; disponibilidade para colaborar.
- **Limites** — deixar claro que não é substituto legal e que respeita o enquadramento existente.

### 4. Submeter pelos canais certos
| Canal | Papel | Como |
|-------|-------|------|
| **DGC** | Dono do serviço | Contacto institucional / formulário de contacto |
| **AMA** | Modernização, gov.pt, design system | Contacto institucional; comunidade Mosaico |
| **Mosaico** | Comunidade do AGORA Design System | [mosaico.gov.pt](https://mosaico.gov.pt/) |
| **Simplex** | Programa de simplificação administrativa | Submissão de ideias/medidas |
| **Portugal Digital / Consulta pública** | Eventuais consultas abertas | Quando existirem |

### 5. Acompanhar
Registar contactos, datas e respostas (criar `docs/CONTACTOS.md` quando começar). Iterar a proposta conforme feedback.

## Rascunho de email — pedido de acesso ao AGORA

> Adaptar antes de enviar. Manter curto e concreto.

```
Para: designsystem@ticapp.gov.pt
Assunto: Pedido de acesso ao AGORA Design System — protótipo cívico de melhoria do Livro de Reclamações

Exmos. Senhores,

Sou um cidadão a desenvolver, de forma independente e open-source, um protótipo
de redesenho do fluxo de reclamação do Livro de Reclamações eletrónico, com o
objetivo de demonstrar uma experiência mais simples e acessível e, eventualmente,
propô-la como contributo às entidades competentes.

Gostaria de solicitar acesso à biblioteca do AGORA Design System para garantir
total alinhamento com os padrões oficiais do Estado.

- Entidade: projeto cívico individual (sem fins lucrativos)
- Âmbito: protótipo de melhoria do Livro de Reclamações (não substitui o serviço
  oficial; respeita o enquadramento legal existente)
- Repositório (auditável): <LINK_GITHUB>

Agradeço desde já a atenção e fico ao dispor para esclarecimentos.

Com os melhores cumprimentos,
<NOME>
<CONTACTO>
```

## Notas de risco

- O acesso ao AGORA pode ser **negado** a um particular — daí a camada de isolamento em `components/ui/` (ver [`ARCHITECTURE.md`](ARCHITECTURE.md)).
- A proposta pode **não ter resposta**. O valor do projeto não depende disso: fica um exemplo público de como o serviço poderia ser.
- **Não usar dados reais de terceiros** nem fazer scraping abusivo do site oficial. Evidência de problemas deve ser obtida de forma ética (uso normal, ferramentas de auditoria sobre páginas públicas).
