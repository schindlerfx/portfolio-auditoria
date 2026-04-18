# CONTRIBUTING — Como manter este repositório

> Guia de uso pessoal. Como adicionar, actualizar e versionar os documentos.

---

## Regra de Ouro — LGPD/RGPD

Antes de fazer qualquer commit, verificar:

- [ ] Nenhum nome de empresa real está presente
- [ ] Nenhum nome de pessoa (colaboradores, fornecedores, gestão) está presente
- [ ] Nenhum valor financeiro específico e identificável está presente
- [ ] Nenhuma referência geográfica que permita identificar a empresa está presente

**Substituições padrão:**

| Original | No repositório |
|----------|----------------|
| Nome da empresa | "empresa manufatureira europeia" |
| Nome do fornecedor | "fornecedor [categoria]" |
| Nome do CFO | "CFO" ou "gestão" |
| Valor financeiro exacto | "~€[magnitude]" ou percentagem |
| Localização específica | "empresa europeia" |

---

## Estrutura de commits

Usar mensagens de commit descritivas:

```bash
# Adicionar novo RAI
git add induflex/relatorios/RAI-005-novo.md
git commit -m "feat: adicionar RAI-005 auditoria de inventário físico"

# Actualizar roadmap
git add carreira/roadmap-2026-2029.md
git commit -m "update: marcar CFI módulo 1 como concluído"

# Adicionar template
git add templates/novo-template.md
git commit -m "feat: template para checklist de auditoria de inventário"
```

---

## Cadência de actualização

| Quando | O que fazer |
|--------|-------------|
| Ao concluir um projecto | Criar novo RAI anonimizado |
| Ao concluir um módulo do bacharel/pós | Actualizar formacao/ |
| Ao obter uma certificação | Actualizar README e carreira/ |
| Ao aprender uma metodologia nova | Adicionar em induflex/metodologias/ |
| Domingo (revisão semanal) | Commit das notas da semana |

---

## Como criar um novo RAI

```bash
# 1. Copiar o template
cp templates/template-RAI.md induflex/relatorios/RAI-005-descricao.md

# 2. Preencher o template
# 3. Verificar checklist LGPD
# 4. Commit
git add induflex/relatorios/RAI-005-descricao.md
git commit -m "feat: RAI-005 [descrição breve]"
git push
```

---

## Estrutura de ficheiros — convenções

```
RAI-[NNN]-[descricao-kebab-case].md     # Relatórios
metodologia-[nome].md                    # Metodologias
framework-[nome].md                      # Frameworks
template-[tipo].md                       # Templates
```
