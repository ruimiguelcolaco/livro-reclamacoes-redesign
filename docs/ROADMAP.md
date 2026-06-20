# Roadmap

Documento vivo. Cada iteração é pequena, fechada e verificável. **Não fazemos tudo de uma vez** — cada iteração corresponde tipicamente a uma sessão de trabalho separada, para manter o esforço (e os custos) controlados.

## Iterações

| # | Iteração | Objetivo | Entregável | Estado |
|---|----------|----------|------------|--------|
| 0 | **Fundação** | Documentação + estrutura de repositório | Todos os `.md` + repo GitHub público | 🟡 Em curso |
| 1 | **Scaffold técnico** | Next.js a arrancar com Tailwind + camada de UI e tokens AGORA (versão pública) | App "hello world" com tema AGORA local | ⬜ Por fazer |
| 2 | **Fluxo de reclamação (UI)** | Formulário multi-passo com componentes AGORA, validação e confirmação | Fluxo navegável com dados mock | ⬜ Por fazer |
| 3 | **Acessibilidade + i18n** | WCAG 2.1 AA, PT/EN, responsivo | Auditoria a11y passada | ⬜ Por fazer |
| 4 | **Camada de dados** | Mock API com contrato pronto para backend real | Submissão "persiste" via mock | ⬜ Por fazer |
| 5 | **Polish + deploy** | Deploy público, README com screenshots | Demo online partilhável | ⬜ Por fazer |
| 6 | **Candidatura** | Dossier de proposta + contactos formais | Email a AMA/DGC + pedido de acesso AGORA | ⬜ Por fazer |

Legenda: ⬜ por fazer · 🟡 em curso · ✅ concluído

## Detalhe por iteração

### Iteração 0 — Fundação
- [ ] Criar `docs/` e todos os ficheiros `.md`
- [ ] Decidir licença, nome do repo e conta GitHub
- [ ] `git init` + primeiro commit
- [ ] Criar repo GitHub público + `git push`

### Iteração 1 — Scaffold técnico
- [ ] `create-next-app` (App Router, TS, Tailwind, ESLint)
- [ ] Instalar e configurar `@ama-pt/agora-design-system`
- [ ] Criar camada `src/components/ui/` que isola o AGORA
- [ ] Página inicial mínima com tema aplicado
- [ ] `npm run build` e lint a passar

### Iteração 2 — Fluxo de reclamação (UI)
- [ ] Passos: tipo → entidade → descrição → dados → revisão → confirmação
- [ ] Validação por passo + estados acessíveis
- [ ] Dados mock

### Iteração 3 — Acessibilidade + i18n
- [ ] Auditoria axe / `design:accessibility-review` sem violações críticas
- [ ] PT (default) + EN
- [ ] Responsivo (mobile-first)

### Iteração 4 — Camada de dados
- [ ] Interface `src/lib/api` (`submitComplaint`, etc.)
- [ ] Implementação mock (MSW ou handlers locais)
- [ ] Contrato documentado para futura API real

### Iteração 5 — Polish + deploy
- [ ] Deploy (Vercel ou GitHub Pages)
- [ ] Screenshots no README
- [ ] Revisão de copy (skill `design:ux-copy`)

### Iteração 6 — Candidatura
- [ ] Pedir acesso ao AGORA (`designsystem@ticapp.gov.pt`)
- [ ] Dossier de proposta (ver [`CANDIDATURA.md`](CANDIDATURA.md))
- [ ] Contactar DGC / AMA / Mosaico / Simplex
