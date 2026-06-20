# Arquitetura

> Documento de intenção. A estrutura concreta nasce na Iteração 1. Atualizar à medida que o código evolui.

## Stack

| Camada | Tecnologia | Porquê |
|--------|-----------|--------|
| Framework | **Next.js** (App Router) | SSR/SSG, SEO, acessibilidade e performance — padrão para serviços públicos sérios |
| Linguagem | **TypeScript** | Segurança de tipos, manutenção a longo prazo |
| Estilos | **Tailwind CSS** | Exigido pelo AGORA Design System |
| UI | **AGORA Design System** (`@ama-pt/agora-design-system`) | Design system oficial do Estado |
| Dados | **Camada mock** trocável por API real | Prototipar sem backend, sem fechar portas |

## Estrutura de pastas (planeada)

```
src/
  app/                 # Rotas (App Router)
  components/
    ui/                # Camada que ISOLA o AGORA — única fronteira com o pacote
  features/
    reclamacao/        # Fluxo de reclamação (passos, validação, estado)
  lib/
    api/               # Interface de dados + implementação mock
  i18n/                # Traduções PT/EN
docs/                  # Documentação
```

## Decisões arquiteturais centrais

### 1. Isolar o AGORA atrás de `components/ui/`

O acesso à biblioteca AGORA é **restrito** e a sua versão/API pode mudar (ver [`AGORA.md`](AGORA.md)). Por isso, **nenhum componente de aplicação importa diretamente** de `@ama-pt/agora-design-system`. Em vez disso:

```
features/  →  components/ui/  →  @ama-pt/agora-design-system
```

A app importa sempre de `components/ui/`. Se o acesso, a versão ou até o próprio design system mudarem, o impacto fica contido a uma única camada.

### 2. Camada de dados como interface

`lib/api/` define **interfaces** (ex.: `submitComplaint(payload): Promise<Result>`). Hoje existe uma **implementação mock**; amanhã, uma implementação real (REST/GraphQL) cumpre a mesma interface. O frontend não muda.

```
features/reclamacao  →  lib/api (interface)  →  [ mock | real ]
```

### 3. Acessibilidade não é opcional

Componentes próprios respeitam semântica HTML, foco, `aria-*` e contraste. Ver [`ACCESSIBILITY.md`](ACCESSIBILITY.md).

### 4. i18n desde cedo

PT é o idioma por omissão; EN é suportado (tal como o site oficial). Strings nunca hardcoded em componentes.

## Fluxo de reclamação (MVP)

```
tipo de reclamação → entidade visada → descrição → dados do reclamante → revisão → confirmação
```

Cada passo: validação própria, estados de erro acessíveis, possibilidade de recuar sem perder dados.
