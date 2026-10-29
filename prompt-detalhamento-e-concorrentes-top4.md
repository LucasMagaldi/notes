# PROMPT — DETALHAMENTO OPERACIONAL E MAPEAMENTO DE CONCORRENTES BRASILEIROS
## As 4 primeiras oportunidades da pesquisa "Motor global de oportunidades" (out/2026)

> Cole este prompt num agente com acesso à web. Ele foi escrito para ser executado de ponta a ponta. A execução deve fazer pesquisa real, citar links e declarar o que não foi encontrado.

---

### 1. CONTEXTO

Uma pesquisa anterior identificou quatro oportunidades de SaaS B2B para o Brasil. As quatro seguem o mesmo padrão: **recuperar dinheiro perdido entre empresas**, em situações em que uma parte desconta, retém, cobra ou atrasa valores da outra e a parte prejudicada não tem dados, tempo nem processo para contestar.

| # | Oportunidade | Referência internacional | Classificação preliminar de concorrência no BR |
|---|---|---|---|
| 1 | Recuperação de deduções comerciais (indústria/distribuidor × varejo) | Glimpse, Confido, HighRadius Deductions | B (parcial) |
| 2 | Auditoria e recuperação de perdas em marketplaces (ML Full, Shopee, Amazon BR) | GETIDA, Carbon6/Seller Investigators | B (parcial) |
| 3 | Registro, prova e cobrança de estadia (tempo de espera) para transportadoras | GeoStamp + Motive (detention) | A/D (baixa ou não verificada) |
| 4 | Conciliação e contestação de delivery (iFood, 99Food, Keeta) para redes de restaurantes | Loop AI | B (parcial) |

**Perfil do fundador:**
- solo, desenvolvedor (TypeScript, React, Next.js, Node, NestJS, .NET, cloud);
- sem investimento externo;
- precisa chegar a R$ 30 mil de MRR operando sozinho no início.

**Sua missão tem duas partes:**

1. **Detalhar o funcionamento e o fluxo** de cada produto com profundidade suficiente para virar especificação de MVP.
2. **Mapear exaustivamente os concorrentes no mercado brasileiro**, usando LinkedIn e web, e classificar a sobreposição funcional **por problema específico**, não por categoria.

---

### 2. SUA FUNÇÃO

Atue como um comitê formado por:
- Product Manager de SaaS B2B;
- Arquiteto de software;
- Analista de inteligência competitiva especializado em LinkedIn e OSINT;
- Especialista no setor de cada ideia (trade marketing/CPG, e-commerce em marketplaces, transporte rodoviário de cargas, foodservice/delivery);
- Consultor jurídico (contratos B2B, Lei 11.442/2007, LGPD, termos de uso de plataformas).

---

### 3. PARTE A — DETALHAMENTO DO FUNCIONAMENTO E DO FLUXO

Para **cada uma das 4 ideias**, produza as seções A1 a A10. Use como ponto de partida os rascunhos de fluxo da seção 5. Valide e corrija esses rascunhos com pesquisa (documentação oficial das plataformas, manuais de fornecedor dos varejistas, legislação, fóruns e comunidades do setor) e acrescente o que estiver faltando.

**A1. Atores e papéis**
Quem usa, quem paga, quem aprova, quem é a contraparte (varejista, marketplace, embarcador, app de delivery) e qual é o interesse de cada um.

**A2. Anatomia do problema**
- Tipos de perda, divergência ou cobrança indevida, com exemplos reais.
- Frequência e valores típicos. Cite fontes e marque o que for estimativa.
- Em que ponto o processo atual falha.
- Prazos de contestação existentes (contratuais, da plataforma, legais).

**A3. Jornada atual (as-is)**
Passo a passo de como a empresa lida com o problema hoje: planilhas, e-mail, WhatsApp, portais, quem faz o trabalho e quanto tempo leva.

**A4. Fluxo do produto (to-be)**
Passo a passo numerado, do onboarding ao valor recuperado:
1. Conexão e importação de dados.
2. Normalização.
3. Detecção ou classificação.
4. Casamento com evidências.
5. Decisão (válido / inválido / sem evidência).
6. Geração de dossiê ou contestação.
7. Envio.
8. Acompanhamento.
9. Baixa financeira.
10. Relatório de valor.

Inclua também um **diagrama em Mermaid** (`flowchart`) do fluxo principal e um diagrama de estados do "caso/disputa" (`stateDiagram`).

**A5. Fontes de dados e integrações**
Para cada fonte, informe:
- formato (API, CSV, XLSX, PDF, XML de NF-e/CT-e, portal web, e-mail);
- autenticação;
- disponibilidade pública da API, **com link para a documentação oficial**;
- limites conhecidos;
- plano B caso a integração esteja fechada (upload manual, leitura de e-mail, RPA).

Indique claramente o que dá para fazer **sem integração fechada** no MVP.

**A6. Regras de negócio e motor de decisão**
Liste as regras determinísticas, com exemplos de entrada e saída, e as partes em que a IA é realmente necessária: extração de PDFs, classificação de motivo, redação de contestação. Justifique cada uso de IA. Não use IA onde uma regra resolve.

**A7. Modelo de dados mínimo**
Entidades principais, campos-chave e relacionamentos (tabela ou ERD em Mermaid).

**A8. Telas do MVP**
No máximo 6 telas, com o objetivo de cada uma e o dado mais importante exibido.

**A9. Casos de borda e riscos**
- Técnicos: mudança de layout ou API, bloqueio de RPA, volume.
- Operacionais.
- Jurídicos: termos de uso das plataformas, uso de credenciais de terceiros, LGPD, risco de a contestação ser vista como prática abusiva, necessidade de advogado.
- Comerciais: medo do cliente de criar atrito com a contraparte.

**A10. Escopo do MVP em 30–60 dias e métricas de valor**
- O que entra e o que fica de fora.
- Métrica de valor primária (por exemplo, R$ recuperado/mês).
- Métricas de uso.
- Critério de sucesso do piloto.

---

### 4. PARTE B — MAPEAMENTO DE CONCORRENTES NO BRASIL (LinkedIn + web)

#### B1. Regras gerais
- Pesquise **o problema**, não só o nome da categoria. Um ERP com "conciliação" não é necessariamente concorrente de quem **contesta** um débito.
- Inclua startups, SaaS verticais, ERPs e TMS/WMS com módulos relevantes, consultorias que fazem o serviço manualmente (inclusive por taxa de êxito), BPOs financeiros, agências especializadas, recursos nativos das próprias plataformas e empresas estrangeiras que já atuam no Brasil.
- **Ausência de resultado não prova ausência de concorrente.** Registre cada busca feita e o resultado, inclusive os vazios.
- Para cada concorrente, **vá ao site e à documentação do produto** (central de ajuda, changelog, vídeos de demonstração no YouTube, página de preços) para confirmar se a funcionalidade **existe de fato**. Não basta citar um post de marketing.
- Não invente dados. Separe métricas declaradas pela empresa de dados verificados de forma independente.

#### B2. Protocolo de busca no LinkedIn

O LinkedIn exige login. Se você não tiver acesso autenticado, use buscas indexadas (Google ou Bing com `site:`) e diga isso explicitamente. Se tiver acesso (ou Sales Navigator), execute também as buscas nativas.

Para cada ideia, execute **no mínimo** estes 5 tipos de busca:

1. **Páginas de empresa:** `site:linkedin.com/company` + termos do problema.
2. **Posts e artigos:** `site:linkedin.com/posts` e `site:linkedin.com/pulse` + termos do problema. Posts de fundadores e de vendedores revelam startups pequenas que não aparecem no Google.
3. **Pessoas (fundadores e vendedores):** `site:linkedin.com/in` + ("founder" OR "fundador" OR "CEO" OR "co-founder") + termos do problema.
4. **Vagas:** `site:linkedin.com/jobs` + termos do problema. Vagas de "analista de deduções" ou "analista de estadia" revelam o tamanho da dor e as ferramentas usadas, e vagas de startups revelam concorrentes.
5. **Sinais indiretos:** buscas por pessoas com o cargo do comprador que mencionem ferramentas (por exemplo, "analista de contas a receber" + "débitos" + nome de software) e posts de reclamação do comprador.

**Sales Navigator (se disponível):** filtros "Account" com setor, headcount de 1 a 200, sede no Brasil e as palavras-chave da tabela B3; filtros "Lead" com Função "Founder/Owner" + palavras-chave.

#### B3. Palavras-chave por ideia (use todas, em combinações)

**Ideia 1 — Deduções comerciais**
- **PT:** "deduções comerciais", "débitos de fornecedor", "descontos indevidos" varejo, "verbas comerciais", "acordos comerciais" fornecedor, "gestão de verbas", "conciliação de verbas", "abatimentos" duplicatas, "recuperação de verbas", "auditoria de acordos comerciais", "trade promotion management", "TPM", "contas a receber" + "redes varejistas", "glosa comercial", "débito de ruptura", "débito de avaria", "bonificação" + "conciliação".
- **EN (players estrangeiros no BR):** "deduction management" Brazil, "trade spend" Brazil, "chargeback" retail Brazil.
- **Players para checar obrigatoriamente:** Neogrid (Arker), Bluesoft, TOTVS (módulos de verbas), SAP (TPM/Deductions no BR), HighRadius no Brasil, Involves, Exato/consultorias de trade, BPOs financeiros com "recuperação de crédito comercial", Linx e Consinco (lado varejista).

**Ideia 2 — Marketplaces**
- **PT:** "reembolso Full", "Programa de Proteção Full", "estoque perdido Full", "auditoria Mercado Livre", "recuperação de valores marketplace", "tarifas indevidas Mercado Livre", "conciliação Mercado Livre", "conciliação Shopee", "divergência de frete Mercado Livre", "reclamações Mercado Livre seller", "devolução não reembolsada", "taxa de êxito" + "Mercado Livre".
- **EN:** "FBA reimbursement" Brasil, "Amazon reimbursement" Brasil.
- **Players para checar:** Koncili, TrackCash, Equals, GeFinance, Boa Vista View, Bling, Tiny/Olist, UpSeller, Base (ex-BaseLinker), Anymarket, Plugg.to, Hub2b, Nubimetrics, Real Trends, Jaguar Sheet, GoSmarter, Ideris, Magis5, agências certificadas pelo Mercado Livre, GETIDA e Carbon6 (atuam no BR?), Helium 10 (Amazon BR).

**Ideia 3 — Estadia**
- **PT:** "estadia" caminhão, "cobrança de estadia", "tempo de espera" descarga, "Lei 11.442" estadia, "indenização por estadia", "controle de estadia", "sobrestadia" rodoviário, "diária de caminhão", "tempo de pátio", "gestão de pátio", "agendamento de docas", "YMS", "check-in motorista", "geofence" transportadora, "comprovante de chegada".
- **EN:** "detention" trucking Brazil.
- **Players para checar:** Trizy, Senior (YMS/TMS), Reply LEA, ESL Sistemas, Bsoft, Rodopar, SSW, GKO Frete, Sascar, Omnilink, Onixsat, Autotrac, Cobli, Rota Exata, Frete.com (ex-FreteBras/CargoX), Truckpad, Buonny, Nstech (e suas aquisições), Veltec, Intelipost, Lincros, Qualp, apps de motorista com check-in.

**Ideia 4 — Delivery**
- **PT:** "conciliação iFood", "repasse iFood", "contestação iFood", "cancelamento iFood restaurante", "auditoria de delivery", "conciliação delivery", "taxas iFood" conferência, "99Food repasse", "Keeta repasse", "incentivos iFood desconto", "gestão de delivery multimarcas", "hub de delivery", "dark kitchen" gestão financeira.
- **Players para checar:** Saipos, Consumer, Goomer, Anota AI, Delivery Much (lado app), Cardápio Web, Ifood Gestor de Pedidos e Portal do Parceiro (recursos nativos), Reportei, Simetrik, Colibri/NCR, Linx (Degust), Totvs Chef, Bematech, Teknisa, Menew, Hubster/Otter no Brasil, Deliverect no Brasil, Apetit, consultorias de delivery (para ver se fazem conciliação manual), Concil e Equals (conciliação de cartões que podem ter estendido para apps).

#### B4. Outras fontes obrigatórias (além do LinkedIn)
- Google e Bing com operadores (`intitle:`, `inurl:`, `"termo exato"`).
- Catálogos: B2B Stack, Capterra Brasil, G2 (filtro Brasil), GetApp, Software Advice.
- Ecossistema: Distrito (dataminer e relatórios setoriais), StartupBase/ABStartups, Crunchbase, Dealroom, Sling Hub, Startups.com.br, Neofeed, Baguete, Brazil Journal, Pequenas Empresas & Grandes Negócios.
- Marketplaces de apps: **Central de Aplicativos/Parceiros do Mercado Livre**, Shopee Open Platform, **Portal do Desenvolvedor iFood (lista de parceiros homologados)**, Bling e Tiny App Stores, Google Play e App Store (apps de motorista, de seller, de restaurante).
- Comunidades: grupos e canais de sellers no YouTube, Reddit r/empreendedorismo, fóruns de transportadores, Abrasel, SETCESP/NTC, ABAD, ABIA, ABComm, eventos (Intermodal, Fispal, Fórum E-commerce Brasil, APAS Show), com listas de expositores.
- Reclame Aqui, que mostra se as próprias contrapartes já oferecem solução e onde está a dor.
- Licitações e editais privados (portais de compras de grandes indústrias e varejistas).
- GitHub (scripts open-source de conciliação de iFood ou ML, que indicam soluções caseiras).

#### B5. Ficha por concorrente encontrado

| Campo | Conteúdo |
|---|---|
| Nome / site / LinkedIn | links |
| Tipo | startup, SaaS vertical, ERP/TMS (módulo), consultoria, BPO, agência, recurso nativo da plataforma, player estrangeiro |
| Fundação / sede / nº de funcionários no LinkedIn | — |
| Funding (fonte) | ou "não divulgado" |
| Público-alvo | porte, setor |
| Funcionalidades **confirmadas** relacionadas ao problema | com link da evidência (doc, vídeo, help center) |
| Etapas do fluxo da Parte A cobertas | por exemplo, "1–4 sim; 5–8 não" |
| Modelo de preço / preço público | — |
| Sinais de tração | clientes citados, cases, vagas abertas, crescimento de headcount |
| O que **não** resolve | — |
| Como a verificação foi feita | busca, site, demonstração, documentação |
| Confiança | alta / média / baixa |

#### B6. Matriz de sobreposição funcional

Para cada ideia, monte uma matriz com as **etapas do fluxo da Parte A4 nas colunas** e **os concorrentes nas linhas**, usando ✅ (faz), ◐ (faz parcialmente), ❌ (não faz) e ❓ (não verificado). Destaque as etapas em que ninguém tem ✅: é ali que está o espaço do produto.

#### B7. Reclassificação de concorrência
Reclassifique cada ideia em A, B, C ou D, com:
- concorrentes que mais ameaçam;
- risco de a própria contraparte resolver o problema nativamente;
- grau de confiança;
- o que ainda não foi verificado.

---

### 5. RASCUNHOS DE FLUXO (ponto de partida a validar e expandir)

#### Ideia 1 — Recuperação de deduções comerciais
- **Cliente:** indústria ou distribuidor (R$ 30–500M/ano) que vende para redes de supermercado, atacarejos e farmácias.
- **Contraparte:** o varejista, que lança débitos no contas a pagar dele (verba de acordo, aniversário, inauguração, ruptura, avaria, devolução, multa logística, divergência de preço/quantidade) e abate da duplicata ou envia boleto de débito.

**Fluxo:**
1. **Onboarding:** cadastro das redes clientes, dos tipos de acordo e dos responsáveis.
2. **Importação:**
   - extratos de débitos (PDF/XLSX dos portais de fornecedor, e-mails de "aviso de débito");
   - contas a receber do ERP (títulos × valores pagos);
   - acordos comerciais (PDF/planilha);
   - XML de NF-e e CT-e;
   - comprovantes de entrega e canhotos.
3. **Normalização:** cada débito vira um registro (rede, loja, data, valor, código ou motivo, documento de referência).
4. **Classificação do motivo:** regras + LLM em textos livres.
5. **Casamento:**
   - débito de verba → existe acordo assinado com aquele valor e período?
   - débito de avaria ou falta → há canhoto sem ressalva ou NF-e de devolução?
   - débito de preço → NF-e × tabela acordada.
6. **Decisão:** válido (baixa contábil sugerida), inválido (contestável) ou sem evidência (pendência interna).
7. **Dossiê de contestação:** PDF com o débito, a evidência e a cláusula, mais e-mail ou texto para o portal, endereçado ao comprador ou ao financeiro da rede.
8. **Acompanhamento:** status por disputa, SLA, lembretes, prazo contratual de contestação.
9. **Recuperação:** crédito em nota de débito reversa ou boleto; conciliação com o recebimento.
10. **Painel:** R$ contestado, recuperado e perdido por rede, por motivo e por vendedor; insumo para renegociar o próximo acordo.

**Pontos a pesquisar:** como cada grande rede (Carrefour/Atacadão, GPA, Assaí, Grupo Mateus, Cencosud, Muffato, Savegnago, Raia Drogasil etc.) disponibiliza débitos ao fornecedor (portal, EDI, e-mail); se há prazos contratuais de contestação; se Neogrid ou EDI transportam esses débitos.

#### Ideia 2 — Auditoria e recuperação em marketplaces
- **Cliente:** seller profissional (R$ 100 mil a R$ 5M/mês), especialmente quem usa Mercado Livre Full.
- **Contraparte:** o marketplace.

**Fluxo:**
1. **Conexão:** OAuth na API do Mercado Livre (e na Shopee Open Platform e na Amazon SP-API).
2. **Importação contínua:** pedidos, pagamentos e liberações, tarifas, fretes, inbounds do Full (envios ao CD), movimentações e saldo de estoque do Full, reclamações, devoluções e mediações, dimensões e peso cadastrados.
3. **Regras de detecção:**
   - (a) unidades enviadas ao Full × recebidas × saldo × vendidas: diferença = possível perda;
   - (b) devolução com reembolso ao comprador sem retorno ao estoque ou com produto avariado no CD;
   - (c) tarifa de venda acima da tabela vigente da categoria ou tipo de anúncio;
   - (d) frete cobrado acima do peso e dimensão corretos;
   - (e) mediação perdida com evidência a favor do seller;
   - (f) liberação de dinheiro atrasada além do prazo.
4. **Fila de casos:** cada um com valor estimado, prazo-limite para reclamar e evidência montada.
5. **Contestação:** texto pronto e anexos. O envio é automático onde a API permitir; nos demais casos, o seller envia com 1 clique e um guia.
6. **Acompanhamento** até o crédito.
7. **Faturamento** da taxa de êxito sobre o valor efetivamente creditado.
8. **Relatório mensal** de valor recuperado e de margem real por SKU.

**Pontos a pesquisar:** documentação oficial da API do ML para estoque do Full e para reclamações; regras e prazos do Programa de Proteção Full no Brasil; se o próprio ML já reembolsa automaticamente parte das perdas; termos de uso sobre ferramentas de terceiros.

#### Ideia 3 — Estadia para transportadoras
- **Cliente:** transportadora de lotação, granel agrícola, porto ou químicos com 20 a 300 veículos (e embarcadores com frota própria).
- **Contraparte:** embarcador ou destinatário.
- **Base legal:** Lei 11.442/2007 (tolerância de 5 h, art. 11; responsabilidade solidária, art. 5º-A; dever de registrar a chegada).

**Fluxo:**
1. **Cadastro:** clientes, endereços de coleta e entrega com geofence, regra de estadia (contratual ou legal), capacidade dos veículos.
2. **Viagem:** criada a partir do CT-e/MDF-e (XML) ou do TMS.
3. **Chegada:** geofence pelo app/PWA do motorista ou pelo rastreador (API Sascar, Omnilink etc.) registra a hora; o motorista tira foto da portaria ou da senha e coleta assinatura ou QR do conferente (opcional).
4. **Saída:** registro de liberação.
5. **Cálculo automático:** tempo excedente acima de 5 h (ou do contrato) × regra (R$/t·h × capacidade).
6. **Dossiê por viagem:** linha do tempo, mapa, fotos, CT-e, base legal.
7. **Faturamento:** fatura ou nota de débito de estadia vinculada ao CT-e, envio ao cliente e régua de cobrança.
8. **Repasse ao motorista** ou agregado (quando aplicável).
9. **Painel:** horas de espera por cliente e por local, estadia gerada × faturada × recebida, ranking de embarcadores mais lentos. Serve de insumo para renegociar o frete mesmo quando o cliente decide não cobrar.

**Pontos a pesquisar:** se TMSs nacionais (ESL, Bsoft, SSW, Rodopar, Senior) já têm cálculo e faturamento de estadia; se rastreadores oferecem relatórios de estadia; o valor de referência atual por tonelada/hora (ANTT); jurisprudência recente sobre a prova.

#### Ideia 4 — Conciliação e contestação de delivery
- **Cliente:** redes, franquias e dark kitchens com 5 a 100 lojas em iFood, 99Food e Keeta.
- **Contraparte:** os apps de delivery.

**Fluxo:**
1. **Conexão:** API de merchant do iFood (pedidos, cancelamentos, financeiro e repasses), exportações e relatórios da 99Food e da Keeta (verificar se existem APIs) e o PDV (Saipos, Consumer etc.) como fonte de verdade.
2. **Cadastro das condições contratadas por loja e app:** comissão, taxa de pagamento, plano de entrega, incentivos e promoções aceitas.
3. **Conciliação** pedido a pedido: valor do pedido × comissão aplicada × taxa × incentivo × repasse efetivo.
4. **Detecção:**
   - (a) cancelamento após preparo com estorno ao restaurante;
   - (b) comissão ou taxa acima do contratado;
   - (c) incentivo ou promoção descontada que deveria ser bancada pelo app;
   - (d) pedido entregue e não repassado;
   - (e) atraso de repasse;
   - (f) item faltante ou reclamação com reembolso indevido.
5. **Contestação:** fila com prazo e evidência (status do pedido, horário de despacho, código de entrega).
6. **Acompanhamento** até o crédito.
7. **Painel por loja, por app e por marca:** margem real por canal, perdas recuperadas e lojas com mais cancelamentos.

**Pontos a pesquisar:** documentação do Portal do Desenvolvedor iFood (endpoints financeiros e de cancelamento, homologação de parceiros, restrições a "software de conciliação"); prazos de contestação de cada app; se o próprio iFood oferece relatório de conciliação ou contestação no Portal do Parceiro.

---

### 6. FORMATO FINAL DA RESPOSTA

Organize a resposta em **quatro capítulos (um por ideia)**, cada um com:

1. **Resumo em 5 linhas:** problema, cliente, como funciona, onde está o espaço e veredito.
2. **Parte A completa (A1–A10)**, com os diagramas Mermaid.
3. **Parte B completa:**
   - log das buscas executadas (consulta → resultado relevante ou "vazio");
   - fichas dos concorrentes;
   - matriz de sobreposição;
   - reclassificação A, B, C ou D.
4. **Riscos principais e perguntas para as entrevistas de validação** (10 perguntas por ideia, focadas em dinheiro perdido e disposição a pagar).

Feche com um **capítulo comparativo** contendo:
- tabela das 4 ideias (concorrência reclassificada, complexidade do MVP, dependência de integração, risco jurídico, tempo até o primeiro piloto pago);
- recomendação de ordem de validação;
- componentes técnicos reaproveitáveis entre as 4 (motor de evidência → dossiê → acompanhamento → cobrança por êxito).

### 7. REGRAS DE EXECUÇÃO
- **Execute a pesquisa real agora.** Não devolva um plano de pesquisa.
- Todo concorrente deve ter **link verificável** (site e, quando houver, LinkedIn).
- Marque cada afirmação como **✅ verificado** (com link), **🟡 declarado pela empresa** ou **❓ não verificado**.
- Não invente funding, preços, número de clientes, endpoints de API ou funcionalidades.
- Se o LinkedIn não estiver acessível, diga isso e compense com buscas `site:linkedin.com` e com as demais fontes da B4.
- Ao confirmar que uma funcionalidade **existe**, cite a evidência mais forte disponível: documentação > vídeo de demonstração > case > post de marketing.
- Se um concorrente cobrir o fluxo inteiro de uma ideia para o mesmo cliente, diga isso claramente e rebaixe a ideia.
