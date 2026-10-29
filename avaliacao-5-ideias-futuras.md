# Avaliação de 5 ideias com problema "futuro"

**Data:** 29/10/2026. Avaliação independente, com 6 buscas de verificação nesta rodada, somadas às pesquisas anteriores.
**Legenda:** ✅ verificado · 🟡 declarado (empresa, blog ou relato) · 🔢 estimativa minha · ❓ não verificado.
**Limitações:** leitura direta de páginas bloqueada pela rede da sessão (usei só trechos indexados); LinkedIn não pesquisado. Os concorrentes que você citou (SolarView, Groner, Revoluna, Quero Plantão, BotZero, Tangerin AI) **não foram auditados por inteiro**. Parti da sua leitura e só confirmei o que apareceu nas buscas.

---

## Veredito resumido

| # | Ideia | Nota (0–10) | Veredito | Em uma frase |
|---|---|:-:|---|---|
| 1 | **Solar Warranty Intelligence** | **6,6** | **Validar, trocando o comprador** | A dor é real e documentada, mas **a instaladora é a parte acusada**, não a compradora natural. Vender para quem perde dinheiro com a geração baixa: donos de usinas de GD remota/compartilhada, O&M terceirizado e financiadores de solar |
| 2 | **Agent Action Ledger** | **5,8** | **Ajustar (open-source primeiro) ou esperar** | É a tendência mais forte das cinco, mas o mercado global está sendo capitalizado agora (OpenBox, JetStream, WitnessAI, AIUC) e o comprador brasileiro com agentes escrevendo em sistemas financeiros ainda é raro |
| 3 | **Medical Credential Passport** | **5,4** | **Ajustar ou descartar** | Revoluna e Quero Plantão já cobrem a gestão documental. O "passaporte compartilhável entre instituições" depende de efeito de rede: difícil de iniciar sozinho |
| 4 | **Property Risk Passport** | **4,9** | **Descartar na forma atual** | Categoria cheia (vistoria, gestão condominial, inspeção predial), pouca disposição a pagar e benchmark (Jupiter) de outra categoria |
| 5 | **Tax Exception Monitor** | **4,6** | **Descartar** | A própria SEFAZ já rejeita XML inválido, e ERPs, emissores e plataformas fiscais (Sovos, Qive, Systax, e-Auditoria, SIEG) disputam esse espaço; o risco normativo é contínuo |

---

## 1. Solar Warranty Intelligence (6,6): a melhor das cinco, com outro comprador

**O problema existe e é recorrente ✅.** Há dezenas de reclamações de "sistema não entrega a geração prometida" no Reclame Aqui:
- desempenho medido de **73%** do previsto ✅ ([Reclame Aqui: Sou Energy](https://www.reclameaqui.com.br/sou-energy/sistema-de-energia-solar-nao-entrega-a-geracao-prometida-e-empresa-nao-resolve-o-problema_c9UkQ_FS23Zh0ljV/));
- tabela mês a mês com **84–98%** do previsto ✅ ([Reclame Aqui: Global Solar](https://www.reclameaqui.com.br/global-solar/energia-solar-nao-atinge-a-geracao-contratada-e-cobranca-integral-de-boletos_ZhSjO_ysG7sJhO_r/)).

A base instalada é de mais de 3,1 milhões de sistemas ✅ (pesquisa anterior).

**O ponto que muda a ideia.** As respostas das empresas mostram que **instaladoras evitam prometer geração em contrato** ("não promete contratualmente uma quantidade específica de geração" ✅ [Catarinna's](https://www.reclameaqui.com.br/catarinna-s-energia-solar/problema-com-o-servicos-prestados-e-falha-na-comunicacao-com-cliente_nMBmIJlEz60uzgfU/); "contrato não contém promessas de geração fixa" ✅ [Nian](https://www.reclameaqui.com.br/nian-energia-sustentavel/comprei-um-kit-de-placa-solares_TgJXo8Iy6ESZngxD/)). A distribuidora de equipamentos diz que a performance é responsabilidade de quem vendeu e instalou ✅ ([Alumifix](https://www.reclameaqui.com.br/alumifix-solar/garantia-de-placas-solar_C4tN9YqqFj1w9TNJ/)). Na via jurídica, geração abaixo do prometido por erro de dimensionamento pode configurar vício do art. 18 do CDC 🟡 ([Correio Braziliense](https://www.correiobraziliense.com.br/cbradar/energia-solar-conta-alta-promessa-eficiencia-cdc/)).

Consequência: **"auditar perdas contra o contrato" é um produto contra a instaladora.** Ela até pode usá-lo para triagem de chamados e para acionar garantia de fabricante (RMA), mas a dor de pagar fica do outro lado. Os compradores com dor financeira direta são:

| Comprador | Por que paga | Hipótese de preço |
|---|---|---|
| **Donos e gestores de usinas de GD remota/compartilhada** (consórcios, cooperativas, fundos) | Geração abaixo do esperado reduz diretamente a receita de créditos vendidos | R$ 3–8/kWp/mês ou R$ 999–3.000/mês por portfólio 🔢 |
| **O&M terceirizado** com contratos de *performance ratio* (PR) garantido | Precisa provar ao cliente que o PR foi cumprido, ou separar culpa (clima × equipamento × O&M) | R$ 999–2.000/mês 🔢 |
| **Financiadores de solar** (fintechs e bancos com carteira de crédito solar) | A capacidade de pagamento do cliente depende da economia gerada; subperformance vira inadimplência | Contrato enterprise ❓ |
| Instaladoras grandes com carteira de pós-venda | Triagem de chamados e RMA ao fabricante (redução de custo de visita) | R$ 499–999/mês |

**Concorrência:** SolarView aparece como O&M e gestão de energia (BH) 🟡 ([diretório](https://thesmartere.com/business-directory/solarview)). Groner, SolarZ e os portais dos fabricantes fazem monitoramento ✅. **Não verifiquei** se algum deles já faz "geração esperada (com irradiância real) × realizada × contrato × fluxo de garantia". **Classificação: B, confiança baixa-média.**

**Ajustes ao seu MVP:**
- **Calcular a geração esperada com irradiância real** (dados satelitais/meteorológicos) e não só pelo projeto. Sem isso, o produto não separa "dia nublado" de "defeito" e perde credibilidade.
- Começar pelo **dossiê de RMA** (inversor ou módulo), que tem retorno imediato para o O&M, e pela **prova de PR** para o dono do ativo.
- Preço **por kWp ou por sistema**, não fixo. R$ 999 fixo é caro para uma instaladora pequena e barato para um portfólio de GD.

**Matar a ideia se:**
- os donos de GD já recebem esse relatório do O&M ou da plataforma de monitoramento;
- a irradiância confiável for cara demais para o MVP;
- menos de 3 portfólios aceitarem um piloto pago.

---

## 2. Agent Action Ledger (5,8): tendência forte, timing e concorrência difíceis

**A tendência é real ✅.** Governança e trilha de auditoria de agentes viraram um dos temas mais financiados de 2026:
- **OpenBox AI**: US$ 5M de seed, mar/2026, "audit trail for every agent action" 🟡 ([TechIntelPro](https://techintelpro.com/news/ai/enterprise-ai/openbox-launches-ai-governance-platform-with-5m-seed-funding));
- **JetStream Security**: US$ 34M de seed 🟡;
- **WitnessAI**: US$ 58M 🟡;
- **AIUC**: certificação e auditoria de agentes 🟡;
- **Aigentsphere**: US$ 4M 🟡 ([Pulse](https://www.pulse.bot/entrepreneurship/news/ai-governance-startup-pockets-4-million-seed-round-447700ff-300d-4dac-b3fc-74938b977a59/)).

No Brasil, você mesmo apontou BotZero e Tangerin AI.

**Problemas:**
1. **Comprador brasileiro imaturo:** poucas empresas daqui têm agentes com permissão de escrita em sistemas financeiros em produção ❓. O ciclo de venda é de segurança e compliance (longo).
2. **Pressão de cima e de baixo:** plataformas de observabilidade de LLM e os próprios frameworks e provedores de agentes estão adicionando logs e aprovações, e players globais capitalizados descem para o mercado.
3. **"Reversibilidade" é difícil de prometer:** desfazer um Pix ou um lançamento contábil depende do sistema de destino, não da camada de log.

**Ajuste viável para fundador solo:** um **SDK open-source** (Node e .NET) de "ledger de ações + aprovação humana + compensação" com versão hospedada paga. Primeiro nicho: **software houses brasileiras que constroem agentes para clientes financeiros** e precisam entregar evidência ao cliente. O open-source reduz o CAC e testa a demanda antes de vender.

**Classificação:** B no global, D no Brasil. Matar se, em 60 dias, menos de 5 times usarem o SDK em produção.

---

## 3. Medical Credential Passport (5,4)

- **Tendência ✅:** expansão de escolas médicas e pejotização. Credenciamento exige CRM, RQE, CNPJ, contrato social, inscrição da PJ no CRM etc. ✅ (editais e CREMERN, pesquisa anterior).
- **Concorrência:** Revoluna já faz cadastro, documentação, aprovação e trilha de auditoria ✅ (pesquisa anterior); Quero Plantão divulga validação 🟡; Managefy também 🟡. **Classificação: C/B.**
- **O diferencial proposto ("passaporte compartilhável entre instituições") tem dois problemas:**
  1. **Efeito de rede:** só vale se várias instituições aceitarem o mesmo perfil, e cada hospital quer a própria verificação (responsabilidade técnica).
  2. **Fonte da verdade:** a validação de CRM e RQE depende dos conselhos ✅ ([CFM: RQE](https://portal.cfm.org.br/noticias/registro-de-qualificacao-de-especialidade-medica-podera-ser-solicitado-gratuitamente-a-partir-de-1o-de-fevereiro/)). Se o CFM ou os CRMs oferecerem consulta oficial fácil, o "passaporte" vira commodity.
- **Ajuste possível:** vender às **empresas médicas/gestoras PJ** que fornecem médicos a vários hospitais e precisam montar **pacotes documentais diferentes por hospital**, com vencimentos. Ainda assim, a sobreposição com Revoluna é alta. **Recomendo não priorizar.**

---

## 4. Property Risk Passport (4,9)

- **Tendência:** eventos climáticos e exigência documental de seguradoras são plausíveis 🟡. Um advogado do setor aponta que a seguradora pode exigir comprovação de inspeção predial ✅ ([SíndicoNet](https://www.sindiconet.com.br/Informese/19416/Alexandre-Marques/NBR-16747-aspectos-praticos-juridicos-e-responsabilidades)). A NBR 16747 e a NBR 5674 definem laudo e plano de manutenção ✅.
- **Concorrência alta e difusa:**
  - apps de inspeção e checklist (Produttivo publica conteúdo e modelos de inspeção predial ✅ [Produttivo](https://www.produttivo.com.br/blog/inspecao-predial));
  - plataformas condominiais (Superlógica e outras) 🟡;
  - apps de vistoria imobiliária 🟡.

  **Classificação: C** para "histórico do imóvel + fotos + checklist".
- **Disposição a pagar:** administradoras compram gestão completa, não um repositório. O benchmark Jupiter é de modelagem de risco climático para grandes carteiras (outra categoria).
- **Única variação que eu testaria:** dossiê de **sinistro** para condomínios em áreas de risco (enchente, vendaval), vendido com corretoras de seguro condominial. Mesmo assim, ticket e frequência são baixos.

---

## 5. Tax Exception Monitor (4,6)

- **Tendência ✅:** os layouts de NF-e e NFC-e mudaram com IBS e CBS, com rejeições e validações entrando em produção em 2026 ([Sovos](https://sovos.com/pt-br/blog/tributos/nf-e-nfc-e-sem-ibs-cbs-rejeitadas/), [Senior](https://documentacao.senior.com.br/exigenciaslegais/noticias/federal/2026/2026-09-25-nf-e-novas-validacoes-entram-em-producao-em-05-10-2026-sua-empresa-esta-preparada), [Qive](https://qive.com.br/blog/nfe-ibs-cbs-reforma-tributaria)).
- **Por que cai:**
  1. **A SEFAZ já rejeita** o XML estruturalmente inválido na emissão, e há validadores públicos e comerciais ✅ ([Treeunfe](https://treeunfe.com.br/blog/novo-validador-de-xml-da-reforma-tributaria-entenda-como-funciona)).
  2. As inconsistências que restam (enquadramento, crédito, alíquota por operação) são **interpretação tributária**, território de Systax, Sovos, e-Auditoria, SIEG, Qive e ERPs ✅/🟡, e trazem responsabilidade.
  3. **Manutenção normativa contínua** (notas técnicas a cada 1–2 meses ✅ [nfe.io](https://nfe.io/docs/release-notes/2026-10-nfe-nfce-nts-ago-out-2026/index.md)) é o oposto de um produto enxuto para fundador solo.
- **Classificação: C.** Descartar.

---

## Recomendação

1. **Validar a Ideia 1 com o comprador trocado.**
   - **Primeiro cliente:** gestor ou dono de **portfólio de usinas de GD remota/compartilhada** (1–20 MWp) ou **empresa de O&M com contratos de PR**.
   - **Experimento (3 semanas):** pedir 12 meses de dados de geração de 3 usinas, calcular a geração esperada com irradiância real e entregar um **relatório de perdas por causa** (clima, indisponibilidade, degradação, defeito com garantia acionável), com o dossiê de RMA pronto.
   - **Oferta:** piloto de R$ 1.500 por portfólio.
   - **GO:** 3 pilotos pagos e pelo menos 1 garantia acionada ou perda reconhecida.
2. **A Ideia 5 só como experimento open-source paralelo**, se você tiver interesse técnico. Ela não deve ser o negócio principal agora.
3. **Descartar as Ideias 3, 4 e 5 na forma atual.** A numeração aqui é a do seu texto original (Credential, Property, Tax).

**Comparação com as finalistas anteriores:** a Ideia 1 ajustada (6,6) fica **abaixo** de campos de prática/internato (7,3), do assessor de mercado livre de energia (7,1) e do software de cuidado de longa duração (7,0), todos em `pesquisa-oportunidades-tendencias-2026.md`. Ela supera as outras quatro desta lista.
