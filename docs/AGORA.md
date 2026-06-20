# AGORA Design System

O [AGORA Design System](https://react.agora.gov.pt/) (Ágora Design System, ADS) é o sistema de design e desenvolvimento oficial do Estado português, criado para a evolução do **gov.pt** e do modelo de **serviços federados** (Decreto-Lei n.º 49/2024). Define regras e componentes para serviços públicos digitais coerentes, simples e acessíveis.

## Estado do acesso

⚠️ **A biblioteca de componentes tem acesso restrito.**

- O pacote npm **`@ama-pt/agora-design-system`** existe publicamente, mas o uso pleno (componentes React prontos) é disponibilizado mediante **pedido formal**.
- **Como pedir:** email para **`designsystem@ticapp.gov.pt`**, indicando:
  - Nome da entidade (no nosso caso: projeto cívico / individual).
  - Âmbito onde se pretende implementar o AGORA (protótipo de melhoria do Livro de Reclamações).
- **Prioridade de acesso:** entidades da administração central abrangidas pelo DL 49/2024, seguidas de municípios, fornecedores municipais e freguesias.

> Estado atual: **acesso ainda não pedido.** Passo previsto para a Iteração 6 (ou antes, se quisermos antecipar). Ver [`CANDIDATURA.md`](CANDIDATURA.md).

## Enquanto não há acesso pleno

Trabalhamos com o que é público e isolamos a dependência:

1. **Storybook público** — [react.agora.gov.pt](https://react.agora.gov.pt/) para estudar componentes, tokens, padrões e comportamento.
2. **Pacote npm** — `@ama-pt/agora-design-system` (React + Tailwind). Tokens e CSS podem ser usados como base.
3. **Camada de isolamento** — todos os componentes AGORA são embrulhados em `src/components/ui/`, para que a app nunca dependa diretamente do pacote (ver [`ARCHITECTURE.md`](ARCHITECTURE.md)). Se faltar um componente, criamos um equivalente acessível que segue os tokens AGORA, e substituímo-lo pelo oficial quando tivermos acesso.

## Integração técnica (Iteração 1)

> A confirmar contra a documentação da versão instalada. Notas iniciais:

```bash
npm install @ama-pt/agora-design-system
```

```ts
// Importar os estilos base
import '@ama-pt/agora-design-system/artifacts/dist/index.css';
```

- **Tailwind:** estender a configuração com o preset/tema do pacote (cores, tipografia, espaçamentos).
- **React:** confirmar a versão de React exigida pelo pacote antes de fixar a do projeto.
- **Tema:** o AGORA permite incorporar identidades visuais via variáveis de cor primária/secundária — útil se quisermos um tema próprio mantendo a base oficial.
- **Fontes e ícones:** confirmar quais o pacote fornece e como carregá-las.

## Referências

- Storybook: https://react.agora.gov.pt/
- Pacote npm: https://www.npmjs.com/package/@ama-pt/agora-design-system
- Mosaico (documentação do Estado): https://mosaico.gov.pt/ferramentas/agora-design-system
- Digital.gov.pt — Design System: https://digital.gov.pt/recursos/design-system
