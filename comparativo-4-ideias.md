# Comparativo das 4 ideias (após detalhamento e mapeamento de concorrentes)

**Execução:** 29/10/2026. Os capítulos completos estão nestes arquivos:

| Ideia | Arquivo |
|---|---|
| 1 | `ideia-1-deducoes-comerciais.md` |
| 2 | `ideia-2-marketplaces-recuperacao.md` |
| 3 | `ideia-3-estadia-transportadoras.md` |
| 4 | `ideia-4-delivery-conciliacao-contestacao.md` |

> **Limitação comum às 4:** o LinkedIn não foi pesquisado (sem login, e o buscador ignora `site:linkedin.com`). A leitura direta de várias páginas oficiais foi bloqueada pela política de rede da sessão. As classificações têm **confiança média**, e startups pequenas que só existem no LinkedIn podem ter ficado de fora.

## 1. Tabela comparativa

| | **1. Deduções comerciais** | **2. Marketplaces (ML Full)** | **3. Estadia** | **4. Delivery** |
|---|---|---|---|---|
| Concorrência (antes → agora) | B → **B** | B → **B** | A/D → **B** | B → **B (mais forte)** |
| Concorrente mais próximo | Neogrid/Arker (planejamento de verbas, não contestação); HighRadius (global, enterprise) | Hunter Hub (auditoria de taxas 🟡); Koncili/TrackCash (repasse); Mercado Advogados | **TOTVS TMS** (cobrança automática de estadia ✅) | **F360** (auditoria de taxas de apps para franquias ✅); **iFood** dono de Saipos, Opdv, 3S Checkout e Anota AI |
| Lacuna confirmada | Contestação do lado do **fornecedor** médio | **Razão de unidades do Full** + reclamações | **Prova independente + dossiê** para transportadoras sem TOTVS | **Fila multi-app com prazos** (7 dias iFood, 72 h 99Food) + êxito |
| Complexidade do MVP | Média (PDFs heterogêneos por rede) | **Baixa** (API pública do ML: estoque e operações do Full) | Média (PWA offline + geofence) | Média (API Financial do iFood + uploads) |
| Dependência de integração | Baixa (upload e e-mail) | Média-alta (uma plataforma) | Baixa (XML de CT-e + PWA) | **Alta** (iFood, contraparte que controla os PDVs) |
| Risco jurídico | Baixo | Baixo-médio (termos do DevCenter) | Médio (LGPD de localização; tese do aviso prévio) | Médio (termos dos apps) |
| Risco de a contraparte resolver | **Baixo** | Médio-alto (o ML pode automatizar, como a Amazon fez) | Baixo (o embarcador não ajuda) | **Alto** (iFood) |
| Tempo até o 1º piloto pago | 45–75 dias | **15–30 dias** | 45–60 dias | 30–45 dias |
| Clientes para R$ 30 mil de MRR | **~8** | ~34 | ~25 | ~43 |
| **Nota (antes → agora)** | 7,7 → **7,7** | 7,5 → **7,4** | 7,3 → **7,0** | 7,1 → **6,6** |

## 2. Ordem de validação recomendada

1. **Ideia 1: deduções comerciais.** Validar primeiro. É a única em que a contraparte não tem incentivo para resolver, o ticket permite chegar a R$ 30 mil de MRR com cerca de 8 clientes, e não há player brasileiro do lado do fornecedor.
   - **Experimento:** 3 diagnósticos pagos de avisos de crédito (6 meses, 2–3 redes).
2. **Ideia 2: ML Full.** Em paralelo, como gerador de caixa rápido. A API documentada permite um MVP em 30 dias.
   - **Experimento:** 10 auditorias gratuitas de 60 dias → 3 pagantes.
   - **Antes de construir:** investigar o produto do Hunter Hub e os prazos oficiais do Programa de Proteção Full.
3. **Ideia 3: estadia.** Só se as entrevistas mostrarem disposição de cobrar ou de usar os dados para renegociar frete.
   - **Posicionamento:** transportadoras médias sem TOTVS, com foco em prova e dossiê.
4. **Ideia 4: delivery.** Rebaixada. A F360 já atende franquias, e o iFood controla os principais PDVs e a API.
   - **Só vale** para redes de 5–30 lojas e dark kitchens, ou como parceria com a F360.

## 3. Componentes técnicos reaproveitáveis

As 4 ideias compartilham o mesmo núcleo. Vale construí-lo uma vez, como módulos de um monorepo (NestJS + Postgres + Next.js):

| Componente | 1 | 2 | 3 | 4 |
|---|:-:|:-:|:-:|:-:|
| **Ingestão** (upload PDF/XLS/CSV, e-mail de entrada, XML NF-e/CT-e, OAuth/API) | ✅ | ✅ | ✅ | ✅ |
| **Extração por LLM** de documentos heterogêneos → schema validado | ✅ | ◐ | ◐ | ✅ |
| **Motor de regras** (esperado × realizado; regras versionadas por cliente) | ✅ | ✅ | ✅ | ✅ |
| **Caso / disputa** (máquina de estados, prazo-limite, SLA, alertas por WhatsApp/e-mail) | ✅ | ✅ | ✅ | ✅ |
| **Cofre de evidências** (arquivos, hash, linha do tempo) | ✅ | ✅ | ✅ | ✅ |
| **Gerador de dossiê** (PDF + texto de contestação) | ✅ | ✅ | ✅ | ✅ |
| **Conciliação do crédito** (casar o valor recuperado com o recebimento) | ✅ | ✅ | ✅ | ✅ |
| **Cobrança por êxito** (fatura sobre o recuperado + assinatura base) | ✅ | ✅ | ◐ | ✅ |
| **Painel** de perdas detectadas, contestadas e recuperadas | ✅ | ✅ | ✅ | ✅ |

**Conclusão:** a tese "**motor de recuperação de receita B2B**" se sustenta. Começar pela Ideia 1, com a Ideia 2 como fonte de caixa rápida, permite reaproveitar 70–80% do código (estimativa) se uma delas for descartada.
