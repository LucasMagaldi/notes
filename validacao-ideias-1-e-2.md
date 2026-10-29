# Validação de duas ideias de SaaS no Brasil

**Data:** 29/10/2026. **Analista:** validação independente, com pesquisa real na web.

**Legenda:**
- ✅ fato verificado (com link);
- 🟡 declaração de empresa, vendedor ou blog;
- 🔢 estimativa minha (premissa explícita);
- ❓ não verificado.

> **Como a pesquisa foi feita (e o que falhou)**
> - Foram 25 buscas nesta rodada, além de cerca de 30 buscas anteriores sobre os mesmos temas (arquivos `ideia-1-...` e `ideia-2-...`).
> - **A leitura direta de páginas está bloqueada** pela política de rede da sessão: o WebFetch falhou em `developer.ifood.com.br`, `99app.com`, `blog-parceiros.ifood.com.br`, `alloy.al`, `chejefe.com` e `ajuda.beefood.com.br`, e o mesmo bloqueio vale para os sites de concorrentes. Tudo o que está abaixo vem dos **trechos indexados pelo buscador**, não da leitura completa das páginas.
> - **LinkedIn:** sem login, e o buscador ignorou o operador `site:linkedin.com` nas 4 tentativas. **Nenhuma pesquisa no LinkedIn foi feita.**
> - Buscas que voltaram **vazias** para o ponto pesquisado:
>   - prazos de contestação em manuais de fornecedor de redes;
>   - módulo de verbas/abatimentos no TOTVS Protheus;
>   - clientes da HighRadius no Brasil;
>   - consultorias brasileiras de "recuperação de abatimentos";
>   - status recente do Arker;
>   - política oficial do Programa de Proteção Full;
>   - produtos de SellSync, Lupfy e Koncili ligados ao Full;
>   - número de sellers no Full.
>
> **Ausência de resultado não foi tratada como ausência de concorrente.**

---

## 1. Veredito executivo

| Ideia | Veredito | Confiança | Em uma frase |
|---|---|:-:|---|
| **1. Deduções comerciais** | **VALIDAR (com ajuste de formato)** | **Média-baixa** | O problema está documentado no Brasil e não encontrei fornecedor brasileiro que faça o fluxo completo para a indústria média. Ainda faltam provas de que **as redes aceitam contestação** e de que o **valor indevido é material**. Começar como diagnóstico pago, não como SaaS. |
| **2. Auditoria do ML Full** | **AJUSTAR** | **Média** | A dor é real e os dados existem via API oficial, e não encontrei ferramenta que reconstrua o estoque do Full para reclamar perdas. Mas o **Mercado Livre decide sozinho e paga por teto/valor declarado** 🟡, o que pode tornar o valor recuperável pequeno. Ajuste: vender **monitoramento contínuo do Full + margem**, com a recuperação como gancho. |

**Nenhum concorrente encontrado resolve o fluxo inteiro para o mesmo cliente** em nenhuma das duas ideias. Na Ideia 1, o único que cobre o fluxo completo é a **HighRadius** (global, enterprise), sem presença comprovada no Brasil ❓.

---

## 2. Ideia 1: recuperação de deduções comerciais

### 2.1 Problema e demanda

| Evidência | Status |
|---|---|
| As redes pagam a duplicata com abatimentos (verba cooperada, enxoval de inauguração, rebate, trocas/logística reversa, multas de nível de serviço) informados no **aviso de pagamento** | ✅ guias de fornecedor por rede (Atacadão, Assaí, Carrefour, Muffato, Grupo Mateus), publicados por uma empresa de antecipação de recebíveis: [Atacadão](https://antecipafacil.com.br/atacadao/prazos-e-pagamento), [Muffato](https://antecipafacil.com.br/muffato/contabilizacao) (fonte comercial) |
| Abatimentos também chegam como **Avisos de Crédito** discriminando descontos, prorrogações e divergências de preço | ✅ [CreditoeCobranca](https://www.creditoecobranca.com/artigos/grandes-redes-verbas-e-abatimentos) |
| Uma indústria de alimentos construiu um **sistema para identificar e controlar abatimentos indevidos** no contas a receber (dissertação UNESP, 2016) | ✅ [UNESP](https://repositorio.unesp.br/bitstreams/45ec6279-07ca-4f84-9e0c-1523f2fa61e5/download): o problema existe a ponto de justificar uma solução interna |
| A indústria destina 3–8% (Arker) ou ~10% (Neogrid) da receita a verbas, "na maioria das vezes sem controle" | 🟡 [ABC da Comunicação](https://www.abcdacomunicacao.com.br/neogrid-anuncia-a-terceira-aquisicao-apos-seu-ipo/), [Brazil Journal](https://braziljournal.com/?p=74816) |
| **Quanto das deduções é indevido no Brasil** | ❓ Não encontrado. Nos EUA, a Stuut cita 1,2–2,4% da receita baixados por deduções não recuperadas 🟡 |
| Prazo e processo de contestação por rede | ❓ Não encontrado (busca vazia). **É a evidência mais crítica que falta.** |

- **Quem sofre mais (hipótese 🔢):** indústrias e distribuidores médios (R$ 30–500M/ano) com várias redes como clientes e sem área dedicada. As grandes indústrias têm SAP, HighRadius ou equipe própria; as pequenas vendem pouco a grandes redes.
- **Quem aprova:** gerente financeiro, controller ou crédito e cobrança. O diretor comercial é aliado ou bloqueador, porque teme o atrito com a rede.
- **Recorrência:** os abatimentos ocorrem **a cada pagamento**, então a demanda tende a ser recorrente. Mas, se a primeira auditoria corrigir o processo interno, o valor mensal pode cair (risco de virar auditoria pontual).

### 2.2 Concorrentes e substitutos no Brasil

| Nome / site | Cliente atendido | Funcionalidades comprovadas | Quanto do fluxo resolve (1 importar · 2 comparar · 3 identificar · 4 dossiê · 5 acompanhar) | Preço | Diferença possível |
|---|---|---|---|---|---|
| **Neogrid / Arker** ([Baguete](https://www.baguete.com.br/noticias/neogrid-compra-arker-por-r-26-milhoes), [Mercado & Consumo](https://mercadoeconsumo.com.br/25/08/2021/noticias/solucoes-de-trade-promotion-management-ganham-forca-na-industria-e-no-varejo-brasileiros/)) | Indústria | TPM: planejamento orçamentário, distribuição de verbas, efetividade e comprovação de execução ✅ (fontes de 2021) | 2 ◐ (verba planejada); 1, 3, 4 e 5 **não verificados** | ❓ | Contestação do abatimento efetivamente descontado. Status do produto em 2025–26 ❓ |
| **Bluesoft** ([ajuda](https://ajuda.bluesoft.com.br/modulo-de-compras/acordo-comercial/1243)) | **Varejista** | Lança acordos que geram débitos ao fornecedor ✅ | Atende a contraparte | ❓ | Não compete; é a fonte dos débitos |
| **Sults** ([página](https://www.sults.com.br/solucoes/gestao/4-melhores-sistemas-supermercado)) | Varejista | "Reconciliação de deduções e verbas cooperadas" 🟡 | Contraparte | ❓ | Idem |
| **Renov Retail** ([página](https://www.renovretail.com.br/produto/gestao-de-verbas/)) | Varejista | "Conciliador de Verbas" 🟡; existência não confirmada em outras fontes | Contraparte | ❓ | Idem |
| **Sankhya** ([página](https://www.sankhya.com.br/gestao-de-negocios/gestao-de-verbas-comerciais/)) | Distribuidores/revendas | Controle de verbas de fornecedores 🟡 | 2 ◐; demais ❓ | ❓ | Contestação ❓ |
| **TOTVS Protheus / SAP** | Indústria | Contas a receber e conciliação de recebimentos ✅ (SAP Cash App) | 1 ◐, 5 ◐; módulo de deduções ❓ (busca vazia) | ❓ | Casamento com acordo, canhoto e dossiê ❓ |
| **HighRadius** ([deductions](https://www.highradius.com/resources/platform/deductions-management/)) | Enterprise global (Danone, McCormick, Land O'Lakes) | Gestão de deduções, envio a portais, notas de crédito ✅ | **1–5 ✅** (fora do Brasil) | ❓ (enterprise) | Mid-market brasileiro e avisos de crédito locais; **presença no Brasil não verificada** |
| **SPS Commerce Revenue Recovery** ([GS1](https://en.pine.gs1.de/solutions/revenue-recovery-von-sps-commerce)) | Fornecedores (EUA/Europa) | Recuperação de deduções, chargebacks e multas do varejo ✅ | 3–5 ✅ (fora do Brasil) | ❓ | Brasil ❓ |
| **Consultorias / BPOs de recuperação de verbas** | Indústria | **Não encontrados** (busca vazia) | ❓ | ❓ | **Classificar como D: podem existir offline ou só no LinkedIn** |

**Referências estrangeiras:**
- **Glimpse:** 200+ marcas e parceiros; US$ 35M de Série A (a16z), mar/2026 ✅ ([BevNET](https://bevnet.com/pr/2026/03/25/glimpse-raises-35m-to-bring-ainative-infrastructure-to-cpg-and-retail)). Preço segundo terceiros: **US$ 1.000/mês + 10% sobre disputas ganhas** 🟡 ([Salesbox](https://salesbox.ai/blog/top-deduction-management-platforms-2026)).
- **Stuut:** US$ 29,5M de Série A (a16z), nov/2025 ✅ ([PYMNTS](https://www.pymnts.com/news/fintech-investments/2025/stuut-raises-29-million-dollars-ai-powered-accounts-receivable-automation-platform/)).
- **Confido:** US$ 20M no total 🟡.

**Classificação: B/D.** Cobertura parcial no Brasil (TPM e ERPs), sem player encontrado no fluxo de contestação. Porém consultorias e BPOs **não foram verificados**, e a ausência deles nas buscas não prova que não existam.

### 2.3 Implantação e operação solo

| Item | Avaliação |
|---|---|
| **Dados necessários** | Avisos de pagamento, crédito e débito por rede; títulos do contas a receber; acordos comerciais; XML de NF-e e de devolução; canhotos/comprovantes de entrega |
| **APIs oficiais** | **Nenhuma API pública das redes encontrada.** Os padrões EDI de remessa e liquidação (DESADV, RECADV, REMADV) existem ✅ ([EDICOM](https://edicomgroup.com/br/blog/edi-varejo-mensagens-desadv-recadv)), mas o uso pelas redes brasileiras para débitos ❓. NF-e: XML padrão SEFAZ ✅ |
| **Restrições** | Portais de fornecedor exigem credenciais do cliente; **evitar RPA** no MVP |
| **MVP em 30–60 dias** | Upload de avisos de 2–3 redes (PDF/XLS) → extração por LLM + regras → comparação com planilha de acordos e XML de NF-e → lista de "possivelmente indevidos" com evidência → dossiê em PDF → controle manual de status |
| **Trabalho manual** | **Alto no início:** cada rede tem layout próprio e os acordos são despadronizados. O fundador opera como analista (concierge) nos 3–5 primeiros clientes. Customização por rede é inevitável |
| **Riscos** | **Contratual:** o contrato de fornecimento pode limitar a contestação ❓. **Comercial:** medo de atrito com a rede. **LGPD:** baixo (dados B2B). **Jurídico:** contestação administrativa não exige advogado; cobrança judicial ficaria fora |

**Operação solo:** viável para 5–15 clientes com forte componente de serviço. Escalar exige padronizar parsers por rede.

### 2.4 Três fatos que matariam a ideia

1. **As redes não aceitam contestação** (contrato ou prática comercial) ou a taxa de reversão é próxima de zero. **Teste:** perguntar a 10 analistas de contas a receber "quanto você reverteu em 12 meses?".
2. **Os abatimentos indevidos são < 0,3% da receita** do cliente-alvo, o que não paga R$ 2.500/mês. **Teste:** diagnóstico em 3 empresas.
3. **Já existe consultoria ou BPO por êxito consolidado** atendendo esse público. **Teste:** perguntar nas entrevistas "quem já te ofereceu isso?" e fazer busca nativa no LinkedIn.

---

## 3. Ideia 2: auditoria de perdas no Mercado Livre Full

### 3.1 Problema e demanda

| Evidência | Status |
|---|---|
| Sellers relatam **unidades perdidas no Full** sem resposta, e o ML "não encontrou divergência" após recontagem | ✅ Reclame Aqui: [unidades "perdidas" no Full](https://www.reclameaqui.com.br/mercado-livre/unidades-perdidas-no-full-e-falta-de-resposta-a-reclamacao-envio-52225082_rHqpVSAql6qPyo8-/), [envios ao CD não confiáveis](https://www.reclameaqui.com.br/mercado-livre/envios-ao-centro-de-distribuicao-full-nao-sao-confiaveis_Z_iNDCbvN-lYDH4i/), [extravio após coleta](https://www.reclameaqui.com.br/mercado-livre/extravio-de-volume-apos-coleta-no-servico-mercado-livre-full-e-pedido-de-r_HsdAPqqnMAV3q_4d/), [reembolso parcial indevido no Full](https://www.reclameaqui.com.br/mercado-livre/contestacao-de-reembolso-parcial-indevido-em-venda-pelo-mercado-livre-full_SpNjj5WIKhiFjqBL/), [frete cobrado após devolução](https://www.reclameaqui.com.br/mercado-livre/mercado-livre-cobranca-indevida-de-frete-apos-devolucao-de-produto-danific_m9pOENq_ijECZvGe/) |
| O ML tem programa de proteção que indeniza perdas e avarias no armazém | ✅ [ML Global Selling](https://global-selling.mercadolibre.com/help/23703). **A página brasileira oficial não foi encontrada** ❓ |
| O reembolso administrativo segue **tabela/teto por unidade baseado no custo declarado**; quem não declarou valor acima do teto recebe parcial | 🟡 [Mercado Advogados](https://www.mercadoadvogados.com.br/conteudo/produto-sumiu-full-mercado-livre) (escritório interessado) |
| O ML não reintegra automaticamente todo produto devolvido ao estoque vendável | 🟡 [SellSync](https://sellsync.ai/pt/blog/erros-mercado-livre-full-prejudicam-lucro/) |
| Devolução no Full: revisão em até 3 dias úteis; contestação em até 60 dias | 🟡 [GoBots](https://gobots.ai/blog/devolucao-full-mercado-livre-como-funciona-a-revisao-e-como-proteger-sua-margem/) |
| Escala do Full: 42 CDs Fulfillment no Brasil até o fim de 2026 (+14) | ✅ [Gironews](https://gironews.com/varejo-digital/mercado-livre-preve-chegar-a-72-centros-logisticos-no-brasil-em-2026/) |
| Número de sellers no Full | ❓ Não encontrado |
| **Quanto o ML já compensa automaticamente** | ❓ **Não confirmado.** É a evidência mais crítica que falta |

- **Quem sofre mais (hipótese 🔢):** sellers com muitas unidades e SKUs no Full (R$ 100 mil a R$ 5M/mês), produtos de ticket médio ou alto e sem pessoa dedicada a inventário.
- **Quem aprova:** o dono ou sócio.
- **Recorrência:** perdas e devoluções ocorrem continuamente, mas o **valor recuperável pode cair** após a primeira limpeza.

### 3.2 Concorrentes e substitutos no Brasil

| Nome / site | Cliente | Funcionalidades comprovadas | Quanto do fluxo resolve (1 importar · 2 comparar · 3 identificar · 4 evidência/reclamação · 5 acompanhar crédito) | Preço | Diferença possível |
|---|---|---|---|---|---|
| **Recursos nativos do ML** | Seller | Programa de proteção ✅; investigação sob pedido (recontagem) ✅ (relatos); claims e devoluções ✅ | 3 ◐, 5 ◐ | — | O ML é juiz e parte; não reconstrói o razão para o seller |
| **Koncili** ([site](https://www.koncili.com/?p=4034)) | Sellers multicanal | Conciliação de repasses ML, Amazon, Shopee e outros ✅ | 1 ✅; 2 ◐ (financeiro); 3–5 ❓ | ❓ | Estoque do Full não verificado |
| **TrackCash + Bling** ([blog](https://blog.bling.com.br/bling-e-trackcash-conciliacao-das-vendas-em-marketplaces/)) | Sellers | Conciliação pedido → repasse ✅ | 1 ✅, 2 ◐ | ❓ | Idem |
| **Equals, GeFinance, Boa Vista View** ([comparativo](https://marketplace.anymarket.com.br/conciliacao-financeira-marketplace-comparativo/)) | Empresas | Conciliação financeira ✅ | 1–2 ◐ | ❓ | Idem |
| **Hunter Hub** ([blog](https://hunterhub.com.br/blog/auditar-taxas-divergentes-2026-passo-a-passo/), [Full](https://hunterhub.com.br/blog/fulfillment-mercado-livre/)) | Sellers ML | Guia e ferramenta de auditoria de **taxas divergentes** 🟡 | 3 ◐ (taxas); estoque ❓ | ❓ | **O mais próximo; investigar antes de construir** |
| **SellerFiscal** ([Product Hunt](https://www.producthunt.com/products/sellerfiscal/reviews)) | Sellers ML/Shopee | P&L por venda via upload de relatório 🟡 | 2 ◐ | ❓ | Sem recuperação |
| **UpSeller** ([ajuda](https://upseller.com/pt/help-doc-article-532)) | Sellers | Controle de reclamações e devoluções ML ✅ | 4 ◐ | ❓ | Sem razão do Full |
| **Jaguar Sheet** ([blog](https://jaguarsheet.com/pt/blog/que-es-mercado-livre-full)) · **SellSync** · **Lupfy** ([blog](https://www.lupfyapp.com/blog/estoque-full-mercado-livre-o-custo-de-cada-mes-parado)) | Sellers | Conteúdo sobre Full e estoque 🟡; funcionalidades de recuperação ❓ | ❓ | ❓ | **Não verificados** |
| **Mercado Advogados** ([extravio](https://www.mercadoadvogados.com.br/conteudo/extravio-mercado-livre-direitos-ressarcimento)) | Sellers | Cobrança administrativa e judicial de extravio, estoque sumido e tarifas ✅ | 4–5 ✅ (manual, jurídico) | ❓ | Software e escala; **possível parceiro** |
| **GETIDA / Carbon6** (ref.) | Amazon FBA | Reembolsos a ~25% do recuperado 🟡 | Amazon apenas | ~25% | Não atuam no ML |

**Classificação: B.** A conciliação de repasses é coberta por vários players (para esse subproblema seria **C**). A **reconstrução do estoque do Full + reclamação** não aparece em nenhum produto encontrado, mas Hunter Hub, SellSync, Lupfy e Jaguar Sheet **não foram verificados por inteiro**.

### 3.3 Implantação e operação solo

| Item | Avaliação |
|---|---|
| **Dados** | Saldo e operações do Full; pedidos; devoluções/claims; faturamento (tarifas e fretes); NF de remessa ao Full (do ERP do seller) |
| **API oficial** | ✅ Estoque Full: `GET /inventories/{id}/stock/fulfillment`. ✅ Operações: `GET /stock/fulfillment/operations/search`, com **padrão de 15 dias e máximo de 60 por consulta**. ✅ Notificações de operações de estoque Full ([docs](https://developers.mercadolibre.cl/en_us/fulfillment), [docs BR](https://developers.mercadolivre.com.br/pt-br/envios-fulfillment)). ✅ Claims e devoluções: `/post-purchase/v2/claims/{id}/returns` e `/post-purchase/v1/claims/search`; v1 legada descontinuada em mai/2024 ([docs BR](https://developers.mercadolivre.com.br/pt-br/gerenciar-devolucoes)) |
| **O que não está confirmado** | **API para abrir reclamação/indenização do Full pelo seller** ❓. Endpoints de faturamento por venda ❓. Página oficial brasileira do programa de proteção ❓ |
| **Permissões** | App no DevCenter + OAuth por seller; somente leitura no estoque Full |
| **MVP em 30–45 dias** | OAuth → backfill de 60 dias + notificações → razão de unidades por SKU (com NF de remessa via upload) → 4 regras (recebido a menor, perda no CD, devolução não reintegrada, tarifa/frete não estornados) → fila com evidência e texto → **seller envia manualmente** → marcação de crédito |
| **Trabalho manual** | Médio: suporte para o seller enviar reclamações e revisar falsos positivos |
| **Riscos** | **Plataforma (o maior):** o ML pode automatizar indenizações, mudar a API ou restringir apps. **Valor:** teto por unidade 🟡. **Termos do DevCenter** ❓. **LGPD:** dados de compradores nos pedidos (minimizar) |

**Operação solo:** viável. É a ideia mais "produto" e menos "serviço" das duas.

**Para não cobrar sobre reembolsos automáticos ou já solicitados:** cobrar êxito **só sobre casos abertos pela ferramenta** (com ID e data anteriores ao crédito) e excluir créditos que o ML lançou sem reclamação. Isso exige identificar a origem do crédito; a viabilidade via API ❓.

### 3.4 Três fatos que matariam a ideia

1. **O ML já compensa automaticamente a maior parte das perdas no Full** (como a Amazon passou a fazer). **Teste:** auditar 10 contas e medir quanto já foi creditado sem pedido.
2. **O valor por unidade é limitado por teto/valor declarado**, e o recuperável médio fica abaixo de R$ 500/mês por seller. **Teste:** as mesmas 10 auditorias.
3. **O seller não executa as reclamações manuais** (sem API de envio) e o churn é alto após a primeira limpeza. **Teste:** medir a % de casos efetivamente enviados no piloto.

---

## 4. Comparação econômica simples (🔢 premissas)

| | Ideia 1: deduções | Ideia 2: ML Full |
|---|---|---|
| **Assinatura base** (premissa) | R$ 2.500/mês | R$ 249/mês (média entre R$ 149 e R$ 399) |
| **Êxito** (premissa) | 10% do recuperado; recuperado médio de R$ 15 mil/mês por cliente → **R$ 1.500/mês variável** | 15% do recuperado; recuperado médio de R$ 2 mil/mês por seller → **R$ 300/mês variável** |
| Receita por cliente (base + êxito) | ~R$ 4.000 | ~R$ 549 |
| **Clientes para R$ 30 mil de MRR só com assinatura** | **12** | **121** |
| Clientes para R$ 30 mil com base + êxito | **8** | **55** |
| Clientes para R$ 30 mil só com êxito (20%) | — | 75 (com R$ 2 mil recuperados/mês cada) |
| Custo direto (IA, infra, parsers) | 10–20% | 5–12% |
| **Custo que pode inviabilizar a operação solo** | Horas de análise por cliente (layouts por rede, acordos despadronizados) | Suporte a muitos sellers pequenos; churn |
| CAC provável | Alto (outbound B2B; ciclo de 30–90 dias) | Baixo (comunidades; auditoria gratuita) |
| Comparação de preço | Glimpse: US$ 1.000/mês + 10% 🟡 | GETIDA/Carbon6: ~25% do recuperado 🟡 |

**Leitura:** a Ideia 1 chega a R$ 30 mil de MRR com **muito menos clientes**, mas depende de vendas consultivas e de um valor recuperável que ainda não foi provado. A Ideia 2 tem aquisição e implantação mais fáceis, porém precisa de **dezenas de clientes** e está exposta ao ML.

**Separação recorrente × variável:** em ambas, trate o êxito como **receita variável** e só conte como MRR a assinatura base no planejamento.

---

## 5. Recomendação

**Validar primeiro a Ideia 1**, com a Ideia 2 em paralelo e baixo esforço. Motivos:
- a Ideia 1 tem o melhor potencial por cliente e nenhuma contraparte com incentivo para resolver o problema por ela;
- a Ideia 2 tem um risco existencial (o ML automatizar ou limitar as indenizações) que um teste barato de 10 auditorias resolve rápido, sem bloquear a Ideia 1.

- **Cliente da Ideia 1:** indústria ou distribuidor de alimentos, bebidas, higiene ou limpeza com **R$ 50–300M/ano**, vendendo para **3 ou mais redes** (atacarejos e supermercados regionais e nacionais), com 1–2 analistas de contas a receber e ERP TOTVS, Sankhya ou SAP B1.
- **Cliente da Ideia 2:** seller com **mais de 300 SKUs ou mais de 2.000 unidades no Full**, faturando acima de R$ 300 mil/mês.

---

## 6. Teste comercial de 30 dias

### Ideia 1

| Item | Definição |
|---|---|
| **Lista** | 60 empresas do perfil (associados de ABIA/ABAD, fornecedores listados em portais de redes; busca nativa no LinkedIn por "analista de contas a receber" + "indústria de alimentos" e "crédito e cobrança" + "redes") |
| **Oferta** | **Diagnóstico retroativo de 6 meses** de abatimentos de 2 redes: relatório de abatimentos sem lastro + dossiês prontos |
| **Preço experimental** | R$ 3.000 fixos, **ou** 15% do valor efetivamente recuperado em 90 dias (o cliente escolhe). Conversão posterior para R$ 2.500/mês + 10% |
| **Meta** | 15 conversas → 5 empresas enviando dados → **3 diagnósticos pagos ou contratados por êxito** |
| **GO** | ≥ 3 pagantes; indevido identificado ≥ 0,5% do faturamento com as redes analisadas; ≥ 1 rede revertendo pelo menos um débito em 30–60 dias |
| **PIVOT** | A dor existe, mas as redes não revertem → reposicionar como **gestão interna de verbas e provisão** (sem contestação), ou vender a BPOs financeiros |
| **NO-GO** | < 2 pagantes após 25 conversas qualificadas, **ou** indevido < 0,3% da receita, **ou** as redes recusam sistematicamente |

### Ideia 2

| Item | Definição |
|---|---|
| **Lista** | 30 sellers do perfil em grupos de WhatsApp/Telegram de sellers, comunidades do YouTube, integradores (Bling, Tiny) e agências de ML |
| **Oferta** | **Auditoria gratuita dos últimos 60 dias do Full** (limite da API) com valor potencialmente recuperável por tipo |
| **Preço experimental** | 20% do recuperado **ou** R$ 199/mês + 15% |
| **Meta** | 10 auditorias concluídas → 3 pagantes |
| **Medições obrigatórias** | (a) R$ já compensado automaticamente pelo ML; (b) R$ recuperável detectado; (c) % de casos que o seller **efetivamente enviou**; (d) % aceita pelo ML; (e) valor pago por unidade × preço de venda (teto) |
| **GO** | Mediana de recuperável ≥ R$ 1.000/mês por seller, ≥ 50% dos casos enviados, ≥ 3 pagantes |
| **PIVOT** | Recuperável baixo, mas os sellers valorizam o razão do Full e a margem por SKU → assinatura de monitoramento sem êxito |
| **NO-GO** | O ML compensa automaticamente a maior parte, **ou** a mediana fica abaixo de R$ 300/mês, **ou** o seller não envia as reclamações |

---

## 7. Condições para o negócio funcionar e evidências que faltam

Não estimo "probabilidade de sucesso". As ideias funcionam **se** as condições abaixo forem confirmadas.

**Ideia 1:**
- As redes aceitam contestação documentada e a revertem com alguma frequência ❓.
- O indevido é ≥ 0,5% da receita com redes 🔢 ❓.
- Os avisos de crédito podem ser obtidos (portal, e-mail, EDI) sem integração fechada ❓.
- Não há BPO ou consultoria dominante por êxito ❓.

**Ideia 2:**
- O ML não compensa automaticamente a maior parte das perdas ❓.
- O valor pago por unidade é relevante (teto/valor declarado) ❓.
- O seller aceita o fluxo semimanual de envio, ou existe API de reclamação ❓.
- Hunter Hub e similares não fazem a reconstrução do Full ❓.

**Para fechar as lacunas:**
- busca nativa no LinkedIn (Sales Navigator) por "recuperação de verbas", "deduções", "auditoria Full";
- demonstração do Hunter Hub, do Koncili e do Arker;
- leitura da Central de Vendedores do ML (Full/Proteção) e dos manuais de fornecedor de 3 redes;
- as entrevistas do teste acima.

---

## 8. Fontes consultadas

- **Ideia 1:**
  - Guias de fornecedor (Antecipa Fácil): [Atacadão](https://antecipafacil.com.br/atacadao/prazos-e-pagamento), [Muffato](https://antecipafacil.com.br/muffato/contabilizacao), [Atacadão: contabilização](https://antecipafacil.com.br/atacadao/contabilizacao)
  - [CreditoeCobranca](https://www.creditoecobranca.com/artigos/grandes-redes-verbas-e-abatimentos) · [UNESP](https://repositorio.unesp.br/bitstreams/45ec6279-07ca-4f84-9e0c-1523f2fa61e5/download) · [Migalhas](https://www.migalhas.com.br/depeso/372846/bonus-e-descontos-entre-o-varejista-e-seus-fornecedores)
  - [Bluesoft](https://ajuda.bluesoft.com.br/modulo-de-compras/acordo-comercial/1243) · [Sults](https://www.sults.com.br/solucoes/gestao/4-melhores-sistemas-supermercado) · [Renov Retail](https://www.renovretail.com.br/produto/gestao-de-verbas/) · [Sankhya](https://www.sankhya.com.br/gestao-de-negocios/gestao-de-verbas-comerciais/)
  - [Neogrid/Arker](https://www.baguete.com.br/noticias/neogrid-compra-arker-por-r-26-milhoes) · [ABC da Comunicação](https://www.abcdacomunicacao.com.br/neogrid-anuncia-a-terceira-aquisicao-apos-seu-ipo/) · [Brazil Journal](https://braziljournal.com/?p=74816)
  - [HighRadius](https://www.highradius.com/resources/platform/deductions-management/) · [SPS Revenue Recovery](https://en.pine.gs1.de/solutions/revenue-recovery-von-sps-commerce) · [EDICOM](https://edicomgroup.com/br/blog/edi-varejo-mensagens-desadv-recadv)
  - [Glimpse (BevNET)](https://bevnet.com/pr/2026/03/25/glimpse-raises-35m-to-bring-ainative-infrastructure-to-cpg-and-retail) · [Salesbox](https://salesbox.ai/blog/top-deduction-management-platforms-2026) · [Stuut (PYMNTS)](https://www.pymnts.com/news/fintech-investments/2025/stuut-raises-29-million-dollars-ai-powered-accounts-receivable-automation-platform/)
- **Ideia 2:**
  - [ML Developers: Full](https://developers.mercadolivre.com.br/pt-br/envios-fulfillment) · [ML Developers: Fulfillment (EN)](https://developers.mercadolibre.cl/en_us/fulfillment) · [ML Developers: Devoluções](https://developers.mercadolivre.com.br/pt-br/gerenciar-devolucoes) · [ML Global Selling: Proteção Full](https://global-selling.mercadolibre.com/help/23703)
  - Reclame Aqui: [unidades perdidas](https://www.reclameaqui.com.br/mercado-livre/unidades-perdidas-no-full-e-falta-de-resposta-a-reclamacao-envio-52225082_rHqpVSAql6qPyo8-/), [envios ao CD](https://www.reclameaqui.com.br/mercado-livre/envios-ao-centro-de-distribuicao-full-nao-sao-confiaveis_Z_iNDCbvN-lYDH4i/), [reembolso parcial](https://www.reclameaqui.com.br/mercado-livre/contestacao-de-reembolso-parcial-indevido-em-venda-pelo-mercado-livre-full_SpNjj5WIKhiFjqBL/)
  - [Mercado Advogados](https://www.mercadoadvogados.com.br/conteudo/produto-sumiu-full-mercado-livre) · [GoBots](https://gobots.ai/blog/devolucao-full-mercado-livre-como-funciona-a-revisao-e-como-proteger-sua-margem/) · [SellSync](https://sellsync.ai/pt/blog/erros-mercado-livre-full-prejudicam-lucro/) · [Hunter Hub](https://hunterhub.com.br/blog/auditar-taxas-divergentes-2026-passo-a-passo/) · [Lupfy](https://www.lupfyapp.com/blog/estoque-full-mercado-livre-o-custo-de-cada-mes-parado) · [Jaguar Sheet](https://jaguarsheet.com/pt/blog/que-es-mercado-livre-full)
  - [Koncili](https://www.koncili.com/?p=4034) · [Anymarket](https://marketplace.anymarket.com.br/conciliacao-financeira-marketplace-comparativo/) · [UpSeller](https://upseller.com/pt/help-doc-article-532) · [SellerFiscal](https://www.producthunt.com/products/sellerfiscal/reviews) · [Gironews (CDs Full)](https://gironews.com/varejo-digital/mercado-livre-preve-chegar-a-72-centros-logisticos-no-brasil-em-2026/)
