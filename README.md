# Livro de Reclamações — Redesenho (projeto cívico)

Redesenho **open-source** e **independente** do [Livro de Reclamações eletrónico](https://www.livroreclamacoes.pt/Inicio/) português, construído com o **[AGORA Design System](https://react.agora.gov.pt/)** — o design system oficial do Estado português.

> ⚠️ **Aviso:** Este é um projeto cívico **independente e não oficial**. **Não** substitui o serviço legal operado pela Direção-Geral do Consumidor (DGC). O objetivo é demonstrar uma melhor experiência de utilização e, posteriormente, propô-la às entidades competentes como contributo. Ver [`docs/VISION.md`](docs/VISION.md) e [`docs/CANDIDATURA.md`](docs/CANDIDATURA.md).

## Porquê

O serviço atual tem problemas sérios de usabilidade e acessibilidade. Os cidadãos têm o direito a reclamar de forma simples, clara e acessível. Este projeto reconstrói o **fluxo de reclamação do cidadão** seguindo os padrões oficiais do Estado, com foco em acessibilidade (WCAG 2.1 AA), clareza e respeito pelo utilizador.

## Estado

🚧 **Iteração 0 — Fundação.** Apenas documentação e estrutura. O código da aplicação começa na Iteração 1. Ver [`docs/ROADMAP.md`](docs/ROADMAP.md).

## Stack (planeado)

- **Next.js** (App Router) + **TypeScript**
- **Tailwind CSS** + **AGORA Design System** (`@ama-pt/agora-design-system`)
- Camada de dados **mock**, desenhada para ligar a backend real sem reescrever o frontend

## Como correr

> Ainda não aplicável (sem código de app na Iteração 0). A partir da Iteração 1:

```bash
npm install
npm run dev
```

## Documentação

| Documento | Conteúdo |
|-----------|----------|
| [`docs/VISION.md`](docs/VISION.md) | O problema, princípios e o que (não) somos |
| [`docs/ROADMAP.md`](docs/ROADMAP.md) | Plano por iterações |
| [`docs/ARCHITECTURE.md`](docs/ARCHITECTURE.md) | Stack e organização do código |
| [`docs/AGORA.md`](docs/AGORA.md) | Integração do AGORA Design System |
| [`docs/ACCESSIBILITY.md`](docs/ACCESSIBILITY.md) | Compromisso de acessibilidade |
| [`docs/CANDIDATURA.md`](docs/CANDIDATURA.md) | Enquadramento legal e proposta ao Estado |
| [`docs/DECISIONS.md`](docs/DECISIONS.md) | Registo de decisões técnicas |

## Contribuir

Ver [`CONTRIBUTING.md`](CONTRIBUTING.md).

## Licença

**EUPL-1.2** (European Union Public Licence). Ver [`LICENSE`](LICENSE) e [`docs/DECISIONS.md`](docs/DECISIONS.md).
