# Metodologia — Auditoria de Conformidade de Preços (Fornecedor)

**Referência:** RAI-2026-004  
**Framework:** COSO — Control Activities (P10) + Monitoring Activities (P16)  
**Norma:** ISA 500 — Evidência de Auditoria  
**Contexto:** Empresa manufatureira europeia em processo de insolvência  
**Classificação:** Anonimizado em conformidade com LGPD/RGPD

---

## 1. Quando aplicar esta metodologia

Esta metodologia aplica-se sempre que:

- Existe conflito de pagamento com um fornecedor sobre valores facturados
- Há suspeita de desvio sistemático entre preços acordados e preços praticados
- A gestão necessita de suporte documental para confrontação comercial
- O auditor identifica ausência de controlo de conformidade de preços no processo de compras

---

## 2. Pré-requisitos documentais

Antes de iniciar a análise, recolher obrigatoriamente:

| Documento | Fonte | Observação |
|-----------|-------|-----------|
| Tabela de preços acordada | Fornecedor | Manuscrita ou formal — qualquer formato tem validade |
| Facturas emitidas no período | Contabilidade / ERP | Todas as facturas do período em análise |
| Fichas técnicas dos produtos | ERP (BOM) | Dimensões oficiais de cada modelo |
| Ordens de produção | ERP | Para confirmar quantidades efectivamente produzidas |

> **Nota crítica:** A ausência de contrato formal não invalida a auditoria. Uma tabela manuscrita tem validade legal em Portugal. Documentar a fonte e a data de cada documento recolhido.

---

## 3. Metodologia passo a passo

### Passo 1 — Definir o critério de cálculo

Identificar e documentar a fórmula de precificação acordada com o fornecedor.

**Exemplo aplicado (RAI-2026-004):**
```
Critério por volume:
Volume (m³) = Largura × Altura × Profundidade
Valor correcto = Volume × Preço/m³ (conforme tabela por tipologia)
```

Registar a tabela de preços de referência:

| Tipologia | Preço acordado |
|-----------|---------------|
| Modelo recto | €60/m³ |
| Modelo curvo | €80/m³ |
| Rodapé separado | €70/m³ |
| Cadeira / Maple | €60/m³ |

### Passo 2 — Construir a matriz de análise

Criar folha de cálculo com as seguintes colunas obrigatórias:

| Campo | Descrição |
|-------|-----------|
| Nº linha | Sequencial |
| Ref. / Modelo | Identificação do produto |
| Nº Factura | Referência documental |
| Tipo | Categoria de precificação |
| Dimensões (L × A × P) | Extraídas da ficha técnica do ERP |
| Volume m³ | Calculado automaticamente |
| €/m³ | Conforme tabela por tipologia |
| Valor calculado unitário | Fórmula: Volume × €/m³ |
| Valor facturado unitário | Extraído da factura |
| Unidades | Quantidade produzida (não encomendada) |
| Valor facturado total | Fórmula: Val. fact. unit. × Unidades |
| Desvio unitário | Fórmula: Val. fact. - Val. calc. |
| Desvio total | Fórmula: Desvio unit. × Unidades |
| Desvio % | Fórmula: Desvio / Val. calc. |

> **Distinção importante:** Usar as **quantidades efectivamente produzidas** (ordens de produção), não as quantidades da encomenda original. A sobrefacturação calcula-se sobre o que foi entregue.

### Passo 3 — Análise linha a linha

Para cada modelo facturado:

1. Extrair dimensões da ficha técnica do ERP
2. Calcular volume com a fórmula acordada
3. Identificar tipologia e aplicar preço da tabela
4. Comparar com o valor facturado pelo fornecedor
5. Registar desvio em € absolutos e percentagem

### Passo 4 — Identificar padrões

Após concluir a análise linha a linha, procurar padrões nos desvios:

- Desvios concentrados numa tipologia específica?
- Desvios maiores em produtos de pequena dimensão?
- Desvios sistemáticos acima de determinado limiar?

**Padrão identificado no RAI-2026-004:**  
Modelos com volume < 0,1 m³ apresentavam desvios percentuais muito superiores à média — chegando a +1.400% em casos extremos. Hipótese: aplicação de preço mínimo por unidade não documentado na tabela acordada.

### Passo 5 — Resumo executivo

Calcular e documentar:

| Indicador | Como calcular |
|-----------|--------------|
| Modelos analisados | Contagem total de linhas |
| Modelos com sobrefacturação | Linhas com desvio > 0 |
| Modelos com subfacturação | Linhas com desvio < 0 |
| Valor correcto total | SOMA(Val. calc. unit. × Unidades) |
| Valor facturado total | SOMA(Val. fact. total) |
| Desvio total | Valor facturado - Valor correcto |
| Desvio % médio | Desvio total / Valor correcto |

---

## 4. Limitações a documentar sempre

1. **Documento de referência não formalizado** — tabela manuscrita sem assinatura bilateral apresenta vulnerabilidade em disputa judicial
2. **Critérios não documentados** — preço mínimo por unidade, acréscimos por componente, etc.
3. **Período de análise** — a auditoria cobre apenas o período indicado; desvios anteriores requerem análise separada

---

## 5. Output — Relatório formal (RAI)

O resultado desta análise deve ser formalizado num RAI com:

- Sumário executivo com os indicadores do Passo 5
- Tabela completa de análise linha a linha como anexo
- Padrões identificados e hipóteses explicativas
- Recomendações priorizadas:
  - **Urgente:** confrontação comercial com o fornecedor
  - **Curto prazo:** formalização do acordo em documento bilateral assinado
  - **Médio prazo:** implementação de controlo periódico de conformidade de preços

---

## 6. Conexão ao framework COSO

| Princípio | Aplicação |
|-----------|-----------|
| P10 — Control Activities | Esta auditoria é o controlo que detecta o desvio |
| P16 — Monitoring Activities | A repetição periódica desta análise constitui monitorização contínua |
| P7 — Risk Assessment | Fornecedores sem contrato formal = risco de billing scheme (ACFE) |

---

## 7. Nota sobre billing schemes (ACFE)

O padrão de sobrefacturação sistemática identificado nesta auditoria é consistente com o que o ACFE classifica como *billing scheme* — esquema em que o fornecedor cobra valores superiores aos acordados de forma recorrente.

A distinção entre **erro de processo** e **fraude intencional** requer investigação adicional — nomeadamente a confrontação directa com o fornecedor e análise de padrão histórico. O auditor documenta e reporta; a decisão sobre acções subsequentes pertence à gestão.

---

*Metodologia desenvolvida em contexto real — empresa manufatureira europeia, 2026.*  
*Anonimizado em conformidade com LGPD/RGPD.*
