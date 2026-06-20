# Contribuir

Obrigado pelo interesse! Este é um projeto cívico open-source. Toda a ajuda — código, design, acessibilidade, testes, documentação — é bem-vinda.

## Antes de começar

- Lê a [`docs/VISION.md`](docs/VISION.md) e o [`docs/ROADMAP.md`](docs/ROADMAP.md) para perceber o rumo.
- Lê a [`docs/ARCHITECTURE.md`](docs/ARCHITECTURE.md) para perceber a organização do código.
- A **acessibilidade é obrigatória** — ver [`docs/ACCESSIBILITY.md`](docs/ACCESSIBILITY.md).

## Fluxo de trabalho

1. Abre uma _issue_ a descrever o que queres fazer (ou comenta numa existente).
2. Cria um _branch_ a partir de `main`: `feat/...`, `fix/...`, `docs/...`.
3. Faz as alterações em commits pequenos e claros.
4. Garante que `npm run lint` e `npm run build` passam (a partir da Iteração 1).
5. Abre um _Pull Request_ a referenciar a issue.

## Mensagens de commit

Seguir [Conventional Commits](https://www.conventionalcommits.org/):

```
feat: adiciona passo de identificação da entidade
fix: corrige foco do teclado no formulário
docs: atualiza roadmap da iteração 2
a11y: melhora contraste dos botões secundários
```

Tipos comuns: `feat`, `fix`, `docs`, `a11y`, `refactor`, `chore`, `test`.

## Estilo de código

- **TypeScript**, sem `any` sem justificação.
- Componentes de UI vão para `src/components/ui/` (a fronteira com o AGORA); a app importa de lá.
- Strings de interface passam por i18n — nada hardcoded.
- Formatação via ESLint/Prettier (config a definir na Iteração 1).

## Idioma

- **Código e nomes técnicos:** inglês.
- **Interface, documentação e commits:** português (PT-PT) por omissão.

## Conduta

Sê respeitoso e construtivo. Este projeto existe para servir cidadãos — tratamo-nos da mesma forma.
