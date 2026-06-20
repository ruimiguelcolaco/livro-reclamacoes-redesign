# Acessibilidade

A acessibilidade é um **requisito**, não um extra. Serviços públicos digitais em Portugal estão legalmente obrigados a cumprir critérios de acessibilidade (Decreto-Lei n.º 83/2018, que transpõe a Diretiva (UE) 2016/2102), com base nas **WCAG 2.1 nível AA**.

## Compromisso

- **Mínimo:** WCAG 2.1 **AA**.
- **Alvo:** ir além onde for barato fazê-lo (ex.: AAA em contraste de texto).

## Checklist por componente / página

- [ ] **Semântica** — HTML correto (`<button>`, `<label>`, `<nav>`, `<main>`, headings hierárquicos).
- [ ] **Teclado** — tudo operável só com teclado; ordem de foco lógica; sem armadilhas de foco.
- [ ] **Foco visível** — indicador de foco claro e com contraste suficiente.
- [ ] **Labels e instruções** — todos os campos têm `label` associada; erros descritos em texto.
- [ ] **Erros acessíveis** — mensagens associadas ao campo (`aria-describedby`), anunciadas a leitores de ecrã.
- [ ] **Contraste** — texto ≥ 4.5:1 (normal) / 3:1 (grande); elementos de UI ≥ 3:1.
- [ ] **Alvos de toque** — ≥ 44×44px.
- [ ] **Imagens** — `alt` significativo; decorativas com `alt=""`.
- [ ] **Movimento** — respeitar `prefers-reduced-motion`.
- [ ] **Idioma** — `lang` correto no `<html>` e em trechos noutro idioma.
- [ ] **Zoom** — utilizável até 200% sem perda de conteúdo/função.
- [ ] **Leitor de ecrã** — testado com VoiceOver (macOS) e/ou NVDA.

## Ferramentas

- **axe DevTools** / `@axe-core/react` — deteção automática.
- **Lighthouse** (aba Accessibility).
- Skill **`design:accessibility-review`** — auditoria WCAG 2.1 AA assistida.
- **Teste manual de teclado** — navegar o fluxo inteiro só com Tab/Shift+Tab/Enter/Esc.
- **Leitores de ecrã** — VoiceOver, NVDA.

## Quando

- A cada componente novo em `src/components/ui/`.
- Auditoria dedicada na **Iteração 3**.
- Verificação antes de cada deploy (Iteração 5+).
