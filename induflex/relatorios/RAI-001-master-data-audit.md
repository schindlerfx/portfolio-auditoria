# RAI-001 — Auditoria de Dados Mestres (Master Data Audit)

**Referência:** RAI-[ANO]-001  
**Tipo:** Auditoria Operacional — Integridade de Dados  
**Ambiente:** Empresa manufatureira europeia · ERP AS/400  
**Framework:** COSO — Control Activities (Princípio 10) + IAS 2  
**Estado:** ✅ Concluído

---

## Contexto

Empresa de capital aberto do sector do mobiliário, em processo de insolvência, com produção baseada em encomendas personalizadas (make-to-order). O processo produtivo é inteiramente dependente das Fichas Técnicas (BOM — Bill of Materials) registadas no ERP AS/400, que determinam:

- A necessidade de compra de matérias-primas
- O custo de produção por produto
- A margem de contribuição calculada para decisão de pricing
- A valorização do inventário (IAS 2)

---

## Problema Identificado

Durante revisão de rotina, foram detectadas discrepâncias sistemáticas entre:

- **Os dados registados nas Fichas Técnicas (BOM)** no ERP
- **O consumo real de materiais** verificado na produção

As divergências não eram aleatórias — apresentavam um padrão consistente que indicava que as fichas técnicas não tinham sido actualizadas para reflectir alterações nos modelos de produto.

### Impacto directo

```
Ficha técnica incorrecta
        ↓
Cálculo de necessidade de compra distorcido
        ↓
Custo de produção calculado incorrectamente
        ↓
Margem de contribuição não reflecte a realidade
        ↓
Decisões de pricing baseadas em dados incorrectos
        ↓
Valorização do inventário não conforme IAS 2
```

---

## Metodologia

### Passo 1 — Levantamento da amostra
Selecção das fichas técnicas activas com maior volume de produção no período.

### Passo 2 — Cruzamento de dados
Comparação linha a linha entre:
- Componentes registados na BOM
- Consumo real registado nas ordens de produção

### Passo 3 — Categorização de discrepâncias

| Tipo de Discrepância | Descrição |
|----------------------|-----------|
| Componente em falta | Material consumido não consta na BOM |
| Quantidade incorrecta | BOM regista quantidade diferente do consumo real |
| Referência errada | Material com referência incorrecta no sistema |
| Componente obsoleto | BOM inclui material que deixou de ser usado |

### Passo 4 — Quantificação do impacto
Para cada discrepância identificada, cálculo do impacto em:
- Custo unitário de produção (€)
- Margem de contribuição (%)
- Valor de inventário afectado (€)

### Passo 5 — Correcção e validação
Correcção das fichas técnicas no ERP em coordenação com o CFO e responsável de planeamento. Validação pós-correcção antes do fechamento mensal.

---

## Resultados

- ✅ Discrepâncias críticas identificadas e corrigidas
- ✅ Integridade dos dados mestres restaurada
- ✅ Fechamento mensal suportado por dados fiáveis
- ✅ Valorização do inventário alinhada com IAS 2
- ✅ Base de dados limpa para cálculo de margens

---

## Aprendizagens Técnicas

### IAS 2 — Inventários
A norma internacional exige que os inventários sejam mensurados pelo menor valor entre o custo e o valor realizável líquido. Dados mestres incorrectos distorcem directamente o custo de produção e podem resultar em incumprimento desta norma.

### COSO — Control Activities (Princípio 10)
> *"A organização selecciona e desenvolve actividades de controlo que contribuem para a mitigação de riscos para a consecução dos objectivos em níveis aceitáveis."*

A ausência de um processo de revisão periódica das fichas técnicas representava uma falha neste princípio — o controlo existia (o ERP) mas não havia processo que garantisse a sua actualização contínua.

### Lição principal
**Dados mestres são a fundação de todo o sistema financeiro.** Um erro na BOM propaga-se silenciosamente por todos os relatórios derivados — custos, margens, inventário, pricing — sem que qualquer alarme dispare. A auditoria de dados mestres deve ser um processo recorrente, não pontual.

---

## Template de Trabalho Criado

→ Ver [templates/checklist-bom-validation.md](../../templates/checklist-bom-validation.md)

---

## Referências

- IAS 2 — Inventários (IASB)
- COSO Internal Control — Integrated Framework (2013), Princípio 10
- COSO Internal Control — Integrated Framework (2013), Princípio 16

---

*Documento anonimizado em conformidade com LGPD/RGPD. Dados financeiros e identificativos específicos foram removidos.*
