# Metodologia — Da Constatação de Auditoria à Ferramenta Operacional

**Referência:** RAI-2026-003 → Dashboard de Orçamentação  
**Framework:** COSO — Monitoring Activities (P16) + Control Activities (P10)  
**Contexto:** Empresa manufatureira europeia em processo de insolvência  
**Classificação:** Anonimizado em conformidade com LGPD/RGPD

---

## 1. O problema — O que o RAI-003 identificou

O RAI-2026-003 constatou a ausência total de KPIs nos processos críticos da operação. No processo comercial, a deficiência específica era:

> **O pricing era realizado por intuição** — sem cálculo estruturado de custo por encomenda, sem margem calculada antes da aceitação, sem dados que permitissem à gestão saber se uma encomenda era rentável antes de a confirmar.

Classificação COSO: deficiência no **Princípio 16 — Monitoring Activities** (ausência de mecanismo de avaliação contínua) e no **Princípio 10 — Control Activities** (ausência de controlo preventivo no processo de aceitação de encomenda).

---

## 2. A distinção entre auditor e controller

**O auditor** — identifica a deficiência, quantifica o risco e emite recomendação formal. Não implementa.

**O controller / consultor operacional** — recebe a recomendação e implementa a solução.

Em contexto de insolvência sem estrutura de auditoria prévia, foi exercido papel híbrido conforme os Standards do IIA — com separação clara documentada entre o trabalho de constatação (RAI-003) e o trabalho de implementação (ferramenta).

Esta distinção é fundamental para a integridade do trabalho de auditoria.

---

## 3. Do RAI à ferramenta — o processo

### Etapa 1 — Constatação formal (RAI-003)

Documentar a deficiência com precisão técnica:
- Qual o processo afectado
- Qual o princípio COSO violado
- Qual o risco concreto para a operação
- Qual a recomendação proposta

### Etapa 2 — Definir o requisito funcional

Traduzir a recomendação de auditoria em requisito operacional concreto:

| Constatação RAI | Requisito funcional |
|-----------------|---------------------|
| Pricing por intuição | Calcular custo total antes de aceitar encomenda |
| Sem margem calculada | Mostrar margem bruta e % em tempo real |
| Sem visibilidade de custos por categoria | Detalhar custo por fornecedor / tipo de material |
| Decisão sem dados | Output exportável para apresentar ao CFO |

### Etapa 3 — Mapear as fontes de custo

Identificar todas as categorias de custo que compõem uma encomenda:

```
Custo total da encomenda =
    Cascos / Estruturas (€/m³ × volume)
  + Mecanismos (preço de tabela por referência)
  + Espumas (€/m² × área)
  + Madeiras / MDF (€/m² × área × desconto)
  + Contraplacado (€/m² × área × desconto)
  + Mão de obra (minutos × custo/hora)
  + Materiais diversos (quantidade × custo unitário)
  + Embalagem (preço × quantidade)
```

### Etapa 4 — Construir a ferramenta

**Decisão técnica:** HTML/JS puro, sem servidor, sem base de dados, executável directamente no browser.

**Justificação:** Ambiente de insolvência sem infraestrutura IT. A ferramenta tem de funcionar em qualquer computador, offline, sem instalação.

**Estrutura da ferramenta:**
- Input por categoria de custo com preços de tabela embutidos
- Cálculo automático em tempo real
- Output: custo total, preço sugerido, margem bruta e %
- Breakdown visual por categoria

### Etapa 5 — Validar com dados reais

Testar a ferramenta com encomendas históricas cujo resultado já é conhecido. Confirmar que os cálculos coincidem com os custos reais registados no ERP.

### Etapa 6 — Documentar a ligação ao RAI

O README da ferramenta deve referenciar explicitamente o RAI que originou a necessidade:

```
"Ferramenta desenvolvida como resposta operacional à
constatação RAI-2026-003 — ausência de KPI de margem
real por encomenda (COSO P16)."
```

---

## 4. O que esta metodologia demonstra no perfil profissional

Um auditor que:
1. Identifica uma deficiência (RAI-003)
2. A documenta com referência COSO
3. Propõe recomendação formal
4. E depois implementa a ferramenta que resolve o gap

— está a demonstrar algo raro no mercado: **ponte entre auditoria e implementação prática**, com separação clara e documentada dos papéis conforme os Standards do IIA.

Esta capacidade é exactamente o que o Risk Advisory procura — não apenas diagnóstico, mas solução.

---

## 5. Ferramentas produzidas neste contexto

| Ferramenta | Tipo | RAI de origem |
|------------|------|--------------|
| Dashboard de Orçamentação | HTML/JS | RAI-2026-003 |
| Sistema de Controlo Financeiro de Encomendas | Excel | RAI-2026-003 |
| Dados de Auditoria de Conformidade de Preços | Excel | RAI-2026-004 |

---

## 6. Conexão ao framework COSO

| Princípio | Constatação | Resposta operacional |
|-----------|-------------|---------------------|
| P16 — Monitoring Activities | Ausência de KPI de margem | Dashboard com margem em tempo real |
| P10 — Control Activities | Sem controlo no pricing | Ferramenta obriga ao cálculo antes da decisão |
| P13 — Information & Communication | Dados não chegavam ao CFO | Output estruturado para reporting |

---

*Metodologia desenvolvida em contexto real — empresa manufatureira europeia, 2026.*  
*Anonimizado em conformidade com LGPD/RGPD.*
