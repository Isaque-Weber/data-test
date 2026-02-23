# 📊 Análise de CSAT - Customer Experience

**Case Técnico:** Data Science & Customer Experience  
**Período:** Dezembro/2025  
**Autor:** Isaque

---

## 📋 Descrição do Projeto

Este projeto contém uma análise completa do desempenho de atendimento ao cliente (CSAT) de uma empresa de E-commerce durante dezembro de 2025, com projeção de metas para janeiro de 2026.

### Objetivos

1. **Diagnosticar** a situação atual do CSAT
2. **Avaliar** a viabilidade da meta projetada
3. **Propor** ações baseadas em dados para melhoria do indicador

---

## 🗂️ Estrutura do Projeto

```
data-test/
│
├── 📓 notebooks/
│   └── analise_csat_dezembro_2025.ipynb    ← NOTEBOOK PRINCIPAL
│
├── 📊 dados/
│   ├── base_1_tickets.csv                  ← Avaliações de CSAT
│   ├── base_2_historico.csv                ← Volumetria total
│   └── base_3_metas.csv                    ← Metas por motivo
│
├── 📈 outputs/
│   ├── relatorio_semantico.txt             ← Análise NLP
│   ├── grafico_distribuicao_notas.png      ← Distribuição CSAT
│   ├── grafico_gap_performance.png         ← Visualização GAP vs Meta
│   ├── grafico_ranking_csat.png            ← Ranking de Ofensores
│   └── grafico_reincidencia_satisfacao.png ← Impacto da Reincidência
│
├── 📚 docs/
│   ├── GUIA_EXECUCAO.md                    ← Guia detalhado de execução
│   ├── RELATORIO_EXECUTIVO.md              ← Relatório completo e análise
│   └── SUMARIO_EXECUTIVO.md                ← Resumo de 1 página
│
└── requirements.txt                        ← Dependências do projeto
```

---

## 🚀 Como Executar

### 1. Instalar Dependências

```bash
pip install -r requirements.txt
```

### 2. Abrir o Notebook Principal

```bash
jupyter notebook notebooks/analise_csat_dezembro_2025.ipynb
```

### 3. Executar Todas as Células

No Jupyter: `Kernel` → `Restart & Run All`

---

## 📊 Principais Resultados

### CSAT Geral (Dezembro/2025)
- **54.6%** (Top 2 Box - notas 4 e 5)
- 5,460 avaliações positivas de 10,000 total

### Meta Projetada (Janeiro/2026)
- **57.66%** (ponderada pelo mix de motivos)
- **GAP:** +3.06 pontos percentuais (+5.6% de crescimento)

### Principais Ofensores (7 motivos)
1. **Confirmação de Pagamento** - 51.6% CSAT
2. **Cupom de Desconto Inválido** - 50.6% CSAT
3. **Dúvida sobre Frete** - 53.5% CSAT
4. **Rastreamento não Atualiza** - 54.4% CSAT
5. **Estorno não Realizado** - 52.6% CSAT
6. **Reclamação sobre Transportadora** - 53.4% CSAT
7. **Alteração de Dados Cadastrais** - 53.8% CSAT

### Causas Raízes (Análise NLP)
1. **Quebra de Confiança** (21%) - Risco de churn e judicialização
2. **Falha Logística** (22%) - Problemas com parceiros externos
3. **Fricção em Autoatendimento** (16%) - UX complexa

---

## 🛠️ Tecnologias Utilizadas

- **Python 3.13**
- **Pandas** - Manipulação de dados
- **NumPy** - Computação numérica
- **SciPy** - Análise estatística (Spearman)
- **Matplotlib / Seaborn** - Visualizações
- **KeyBERT** - Extração de palavras-chave
- **Sentence-Transformers** - Análise semântica (NLP)
- **AdjustText** - Ajuste de rótulos em gráficos

---

## 📈 Metodologia

### CSAT (Top 2 Box)
```
CSAT% = (Notas 4 e 5) / Total de Respostas
```

### Meta Ponderada
```
Meta Geral = Σ(Volume_Motivo × Meta_Motivo) / Σ(Volume_Total)
```

### Análise de Reincidência
- **Correlação de Spearman** entre número de contatos e CSAT
- Evidência de falha na resolução de primeira chamada (FCR)

### NLP (Processamento de Linguagem Natural)
- **KeyBERT** para extração de conceitos
- **Sentence-BERT** para classificação semântica
- Análise de 80 comentários por motivo ofensor

---

## 💡 Principais Recomendações

### ⚡ Prioridade Crítica (30 dias)
1. Revisar régua de comunicação financeira
2. Auditoria de processos com percepção de fraude

### 📅 Médio Prazo (60 dias)
3. Simplificar UX de fluxos críticos
4. Implementar comunicação preventiva

### 🏗️ Estrutural (90+ dias)
5. Renegociar SLAs com parceiros logísticos

---

## 📝 Arquivos Importantes

### Notebook Principal
- **`notebooks/analise_csat_dezembro_2025.ipynb`** - Análise completa com todas as seções

### Outputs
- **`outputs/relatorio_semantico.txt`** - Análise NLP detalhada por motivo
- **`outputs/*.png`** - Gráficos gerados para o relatório

### Documentação
| Arquivo | Propósito | Público-Alvo |
| :--- | :--- | :--- |
| **`GUIA_EXECUCAO.md`** | Passo a passo técnico detalhado para rodar o código, configurar ambiente e reproduzir a análise. Inclui troubleshooting. | Desenvolvedores, Data Scientists |
| **`RELATORIO_EXECUTIVO.md`** | *Deep dive* nos resultados. Contém todas as descobertas, gráficos, metodologia estatística, diagnóstico de NLP e plano de ação detalhado. | Gerentes de CX, Analistas Sêniores |
| **`SUMARIO_EXECUTIVO.md`** | "One-pager" com os highlights essenciais: números macro, principais ofensores e top 3 ações recomendadas. Leitura rápida (< 2 min). | Diretores, C-Level |

---

## ✅ Validação

Todos os dados e cálculos foram validados:
- ✅ Integridade dos dados confirmada
- ✅ Cálculos verificados manualmente
- ✅ Zero valores nulos em colunas críticas
- ✅ Range de CSAT correto [1-5]

---

## 👤 Autor

**Isaque**  
Data Science & Analytics  

---

## 📄 Licença

Este projeto foi desenvolvido como parte de um case técnico.
