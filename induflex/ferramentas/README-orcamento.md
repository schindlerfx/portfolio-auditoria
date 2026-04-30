# Ferramenta de Orçamentação de Encomenda

**Contexto:** Controlo interno — Empresa manufatureira europeia em processo de insolvência  
**Referência RAI:** RAI-2026-003 — Ausência de KPIs (COSO — Monitoring Activities, Princípio 16)  
**Framework:** COSO — Control Activities + Monitoring Activities  
**Classificação:** Anonimizado em conformidade com LGPD/RGPD

---

## Contexto de Auditoria

O RAI-2026-003 identificou como deficiência de controlo interno a ausência de KPIs financeiros nos processos críticos da operação — em particular, a inexistência de margem real por encomenda calculada antes da aceitação comercial.

O pricing era realizado por intuição, sem suporte em dados estruturados, o que representava risco directo de aceitação de encomendas com margem negativa ou abaixo do mínimo operacional.

Esta ferramenta foi desenvolvida como resposta operacional a essa constatação de auditoria.

---

## O que a ferramenta faz

Dashboard de orçamentação de encomenda em HTML/JS puro — sem dependências externas, executável directamente no browser.

**Inputs por categoria de custo:**
- Cascos / Estruturas de tecido (€/m³ — por volume)
- Mecanismos — Fornecedor A (selecção por referência com preço de tabela)
- Espumas — Fornecedor B (€/m² por referência)
- MDF — Fornecedor C (€/m² com desconto comercial aplicado)
- Contraplacado — Fornecedor C (€/m² com desconto comercial aplicado)
- Mão de Obra (minutos × custo/hora)
- Materiais Diversos (quantidade × custo unitário)
- Embalagem (preço × quantidade)

**Outputs calculados em tempo real:**
- Custo total da encomenda
- Preço de venda sugerido (margem configurável)
- Lucro absoluto e margem percentual
- Breakdown de custos por categoria com barras visuais

---

## Ligação ao COSO

| Componente COSO | Aplicação nesta ferramenta |
|-----------------|---------------------------|
| Control Activities (P10) | Controlo preventivo — orçamento antes da aceitação |
| Monitoring Activities (P16) | KPI de margem real por encomenda |
| Information & Communication (P13) | Dados estruturados disponíveis para decisão do CFO |

---

## Nota técnica

- HTML/JS puro — sem frameworks, sem servidor, sem base de dados
- Preços de tabela dos fornecedores embutidos como referência (valores de mercado)
- Anonimizado: fornecedores identificados como Fornecedor A, B e C
- Valores financeiros específicos da operação não estão presentes

---

*Documento anonimizado em conformidade com LGPD/RGPD.*  
*Desenvolvido em contexto de auditoria interna — empresa manufatureira europeia, 2026.*
