# Gestoria

**ðŸ‡§ðŸ‡· [PortuguÃªs](README.md) Â· ðŸ‡ºðŸ‡¸ [English](README.en.md) Â· ðŸ‡ªðŸ‡¸ [EspaÃ±ol](README.es.md)**

MÃ©todo, plano de formaÃ§Ã£o INEMA e laboratÃ³rio web de GestÃ£o de IA. A unidade de trabalho Ã© **um processo empresarial com resultado mensurÃ¡vel**.

**[Abrir ferramenta](https://inematds.github.io/gestoria/)** Â· **[Guia de uso](https://inematds.github.io/gestoria/guia/)** Â· **[Plano do curso](https://inematds.github.io/curso-gestao-ia/)**

ðŸŽ¬ VÃ­deo: https://www.youtube.com/watch?v=EtBGK2Hgz9E

## Abrir a ferramenta

Requer Node.js 22.12+ ou 24+ e npm.

```bash
npm install
npm run dev
```

Abra o endereÃ§o informado pelo Vite (normalmente `http://localhost:5173`). Para gerar os arquivos estÃ¡ticos:

```bash
npm run build
npm run preview
```

O diretÃ³rio `dist/` Ã© a saÃ­da de produÃ§Ã£o. `npm run build` gera a versÃ£o para a raiz de um domÃ­nio. `npm run build:pages` configura a base `/gestoria/` e inclui guia e capa. O workflow `.github/workflows/pages.yml` publica esse pacote no GitHub Pages a cada push em `main`.

## Documentos

- [Plano do curso](docs/PLANO-CURSO.md): 10 mÃ³dulos, 60 horas propostas, aulas, laboratÃ³rios, entregas e projeto final.
- [MÃ©todo](docs/METODO.md): contratos, cargos digitais, autonomia, mÃ©tricas e LOOP-R.
- [Plano do produto](docs/PLANO-PRODUTO.md): escopo, arquitetura, dados, fases e critÃ©rios de evoluÃ§Ã£o.
- [Templates](docs/TEMPLATES.md): modelos para aplicar o mÃ©todo a uma operaÃ§Ã£o.

Os quatro documentos tambÃ©m podem ser baixados na tela **MÃ©todo e curso**.

## Roteiro de uso

1. Abra **Processos** e examine o exemplo de qualificaÃ§Ã£o comercial ou crie um processo.
2. Em **ForÃ§a de trabalho**, crie um cargo, indique seu responsÃ¡vel, escopo e autonomia inicial.
3. Na **VisÃ£o geral**, selecione o processo e simule um caso normal, duvidoso ou fora da polÃ­tica.
4. Abra **DecisÃµes humanas**, revise a saÃ­da e registre aprovaÃ§Ã£o ou devoluÃ§Ã£o com justificativa.
5. Em **AvaliaÃ§Ãµes**, registre casos distintos com esperado, produzido e classificaÃ§Ã£o humana.
6. Abra a ficha do agente para consultar os critÃ©rios de promoÃ§Ã£o. A aprovaÃ§Ã£o promove um nÃ­vel e cria nova versÃ£o; avaliaÃ§Ãµes histÃ³ricas continuam visÃ­veis.
7. Em **Melhoria contÃ­nua**, registre uma hipÃ³tese e avance o experimento com evidÃªncias.
8. Em **Dados do laboratÃ³rio**, exporte seu trabalho em JSON. ImportaÃ§Ã£o e restauraÃ§Ã£o substituem o espaÃ§o atual apÃ³s confirmaÃ§Ã£o.

## Limites desta versÃ£o

Ã‰ um **MVP local de gestÃ£o com simulador didÃ¡tico**, sem backend e sem chamada a modelos. NÃ£o conecta CRM, ERP, e-mail ou MCP. Ferramentas, modelo, Skills e conhecimento na ficha sÃ£o descriÃ§Ãµes planejadas, nÃ£o integraÃ§Ãµes ativas.

Os exemplos iniciais sÃ£o fictÃ­cios. Cada nova simulaÃ§Ã£o usa R$ 0,38 e 42 segundos como valores didÃ¡ticos, sem cobranÃ§a. Indicadores sÃ£o calculados sobre o acumulado do laboratÃ³rio: autonomia usa apenas casos concluÃ­dos; custo inclui tentativas pendentes/devolvidas; avaliaÃ§Ãµes usam somente versÃµes atuais. O indicador de acerto nÃ£o equivale a validaÃ§Ã£o em produÃ§Ã£o.

Dados ficam no `localStorage` deste navegador e origem (`gestoria.workspace.v1`). NÃ£o hÃ¡ identidade autenticada, isolamento por empresa, backup automÃ¡tico, autorizaÃ§Ã£o real ou auditoria imutÃ¡vel. O histÃ³rico local conserva atÃ© 300 eventos. NÃ£o inserir segredos ou informaÃ§Ãµes sensÃ­veis. ExportaÃ§Ãµes sÃ£o editÃ¡veis; regras de produÃ§Ã£o precisam ser aplicadas no servidor.

Uma importaÃ§Ã£o Ã© validada quanto a versÃ£o, tipos, limites, IDs e relaÃ§Ãµes; campos desconhecidos sÃ£o descartados. Arquivos tÃªm limite de 5 MB. Dados locais invÃ¡lidos sÃ£o preservados e bloqueiam gravaÃ§Ãµes atÃ© recuperaÃ§Ã£o/importaÃ§Ã£o/restauraÃ§Ã£o. Se outra aba alterar os dados, formulÃ¡rios abertos sÃ£o fechados para evitar sobrescrita.

O curso estÃ¡ planejado; aulas completas, vÃ­deos, pÃ¡ginas de apostila e dataset revisado de 100 casos ainda nÃ£o foram produzidos. O roadmap descreve a passagem deste laboratÃ³rio para uma operaÃ§Ã£o real.

## VerificaÃ§Ã£o

```bash
npm test
npx playwright install chromium
npm run test:e2e
npm run build
```

Testes de domÃ­nio verificam mÃ©tricas, orÃ§amento, autonomia, revisÃ£o, promoÃ§Ã£o e importaÃ§Ã£o. Testes de navegador cobrem o fluxo de cadastro atÃ© avaliaÃ§Ã£o, persistÃªncia, LOOP-R, importaÃ§Ã£o, conteÃºdo HTML tratado como texto, recuperaÃ§Ã£o de dados invÃ¡lidos, downloads e layouts desktop/mobile. Capturas sÃ£o gravadas em `artifacts/`.

## Estrutura

```text
docs/               mÃ©todo, plano do curso, plano do produto e templates
src/domain.ts       regras de gestÃ£o e validaÃ§Ã£o das cÃ³pias
src/seed.ts         exemplos fictÃ­cios iniciais
src/main.ts         telas, formulÃ¡rios e persistÃªncia local
src/style.css       interface responsiva
tests/              testes de domÃ­nio e navegador
```

---

Projeto adaptado da comunidade INEMA TDS · Marca **Arckhé**

Feito pelo **[ARCKHÉ.AI](https://linnoff88-dev.github.io/arckhe-ai)**.