# RAI-004 — Auditoria de Conformidade de Preços (Fornecedor)

**Referência:** RAI-[ANO]-004  
**Tipo:** Auditoria Operacional — Conformidade Comercial  
**Ambiente:** Empresa manufatureira europeia  
**Framework:** COSO — Control Activities + Monitoring Activities  
**Estado:** ✅ Concluído — Em fase de confrontação comercial

---

## Contexto

A empresa mantém relação comercial com um fornecedor de matéria-prima crítica (cascos e estruturas para mobiliário). O fornecedor disponibilizou uma tabela de preços manuscrita com critério de precificação por metro cúbico (€/m³) por tipologia de produto.

Perante um conflito de pagamento — o fornecedor reclamava valores que a empresa considerava incorrectos — foi solicitada uma auditoria formal de conformidade de preços.

---

## Objectivo

Verificar a conformidade entre os valores praticados pelo fornecedor nas facturas emitidas e os valores calculados com base na tabela de preços acordada, identificando e quantificando as divergências com impacto financeiro.

---

## Metodologia

### Passo 1 — Recolha documental
- Facturas emitidas pelo fornecedor no período em análise
- Tabela de preços manuscrita do fornecedor (único documento de referência)
- Fichas técnicas de cada modelo no ERP, com dimensões oficiais

### Passo 2 — Critério de cálculo
```
Volume (m³) = Largura × Altura × Profundidade
Valor correcto = Volume × Preço/m³ (conforme tabela)
```

| Tipologia | Preço acordado |
|-----------|---------------|
| Modelo recto | €60/m³ |
| Modelo curvo | €80/m³ |
| Rodapé separado | €70/m³ |
| Cadeira / Maple | €60/m³ |

### Passo 3 — Análise linha a linha
Para cada modelo facturado:
1. Calcular volume com base nas fichas técnicas do ERP
2. Aplicar preço da tabela conforme tipologia
3. Multiplicar pelo número de unidades efectivamente produzidas
4. Comparar com o valor facturado pelo fornecedor

### Passo 4 — Quantificação de desvios
Cálculo do desvio em valor absoluto (€) e percentual (%) — por unidade e no total do período.

---

## Resultados

| Indicador | Valor |
|-----------|-------|
| Modelos analisados | 51 |
| Modelos com sobrefacturação | 50 (98%) |
| Modelos com subfacturação | 1 (2%) |
| Valor correcto (tabela) | ~€10.300 |
| Valor facturado (fornecedor) | ~€28.300 |
| **Desvio total identificado** | **~€17.900 (+173%)** |

> Os valores acima foram anonimizados. O desvio percentual e a distribuição dos resultados são reais.

### Distribuição por categoria

| Categoria | Desvio médio |
|-----------|-------------|
| Modelos rectos | +171% |
| Cadeiras / Maples | +190% |
| Modelos curvos | +73% |

---

## Padrão Identificado

Foi detectado um padrão consistente em modelos de pequena dimensão (volume < 0,1 m³): os desvios percentuais eram significativamente superiores à média — chegando a +1.400% em alguns casos.

**Hipótese:** O fornecedor pode estar a aplicar um preço mínimo por unidade para peças de pequena dimensão — critério não documentado na tabela acordada.

Este padrão foi sinalizado à gestão como ponto prioritário de clarificação na reunião com o fornecedor.

---

## Limitações da Análise

1. A tabela de preços é manuscrita — não existe documento formal assinado por ambas as partes
2. Possível existência de critério de preço mínimo não documentado
3. A análise cobre apenas o período indicado

---

## Aprendizagens Técnicas

### Auditoria de fornecedor vs. Auditoria interna
A auditoria de fornecedor partilha a mesma metodologia da auditoria interna — recolha de evidência documental, comparação com critério acordado, quantificação de desvios — mas o destinatário das conclusões é externo. Isso exige ainda mais rigor na blindagem das evidências, porque o relatório pode ser usado numa disputa comercial ou judicial.

### A importância da evidência documental
Em qualquer disputa com fornecedor, o que conta é o que está escrito e assinado. Uma tabela manuscrita tem validade legal em Portugal, mas apresenta vulnerabilidades — pode ser contestada quanto à data, ao âmbito e à interpretação. Esta auditoria demonstrou a necessidade de formalizar todos os acordos comerciais em documentos bilaterais.

### Billing schemes — fraude em compras (ACFE)
O padrão identificado nesta auditoria é consistente com o que o ACFE classifica como *billing scheme* — esquema de facturação em que o fornecedor cobra valores superiores aos acordados de forma sistemática. A diferença para fraude intencional vs. erro de processo exige investigação adicional — que é exactamente o que a reunião de confrontação vai determinar.

---

## Templates Criados

→ Ver [templates/auditoria-precos-fornecedor.md](../../templates/auditoria-precos-fornecedor.md)

---

## Referências

- COSO Internal Control — Integrated Framework (2013), Princípios 10 e 16
- ACFE — Fraud Examiners Manual, Billing Schemes
- ISA 500 — Evidência de Auditoria

---

*Documento anonimizado em conformidade com LGPD/RGPD. Valores financeiros e identificação de empresa/fornecedor removidos.*
