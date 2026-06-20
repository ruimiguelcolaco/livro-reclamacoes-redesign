# Registo de Decisões (ADR leve)

Decisões com impacto, em formato curto. Adicionar no topo as mais recentes.

---

## ADR-0005 — Licença do projeto
**Estado:** ✅ Decidido
**Contexto:** Projeto destinado a ser contributo open-source para o Estado.
**Opções:** MIT (permissiva, simples) vs **EUPL-1.2** (licença oficial da União Europeia, alinhada com software do setor público europeu, compatível com várias copyleft).
**Decisão:** **EUPL-1.2** — sinaliza intenção de software público europeu e facilita reutilização pelo Estado. Texto oficial em [`LICENSE`](../LICENSE).

---

## ADR-0004 — Repositório público desde o dia 1
**Estado:** ✅ Decidido
**Contexto:** O projeto quer ser auditável pelo Estado.
**Decisão:** GitHub **público** desde o início. Transparência total alinha-se com a filosofia de software público.

---

## ADR-0003 — Camada de dados mock trocável por API real
**Estado:** ✅ Decidido
**Contexto:** Não há (nem deve haver agora) backend; mas não queremos fechar a porta a um.
**Decisão:** `lib/api/` define interfaces; implementação **mock** primeiro, implementação real depois, sem mudar o frontend.

---

## ADR-0002 — Stack: Next.js (App Router) + TypeScript + Tailwind
**Estado:** ✅ Decidido
**Contexto:** O AGORA é React + Tailwind. Serviço público beneficia de SSR, SEO e acessibilidade.
**Decisão:** **Next.js (App Router)** + TypeScript + Tailwind, integrando `@ama-pt/agora-design-system`.

---

## ADR-0001 — Isolar o AGORA atrás de `components/ui/`
**Estado:** ✅ Decidido
**Contexto:** O acesso à biblioteca AGORA é restrito e a sua API/versão pode mudar.
**Decisão:** Nenhum componente de app importa diretamente do pacote; tudo passa por `src/components/ui/`. Reduz o risco de bloqueio/alteração a uma única camada.
