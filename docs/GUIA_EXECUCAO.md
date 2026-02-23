# 🚀 Guia de Execução do Notebook

## 📋 Pré-requisitos

1. **Python 3.13** instalado
2. **Jupyter Notebook** instalado
3. **Dependências** instaladas

---

## ⚙️ Instalação

### 1. Instalar Dependências

```bash
pip install -r requirements.txt
```

Ou, se preferir usar o ambiente virtual:

```bash
# Ativar ambiente virtual
.venv\Scripts\activate

# Instalar dependências
pip install -r requirements.txt
```

---

## 📓 Executar o Notebook

### Opção 1: Jupyter Notebook (Recomendado)

```bash
# Navegar para a pasta do projeto
cd c:\dev\data-test

# Iniciar Jupyter
jupyter notebook notebooks/analise_csat_dezembro_2025.ipynb
```

### Opção 2: Jupyter Lab

```bash
jupyter lab notebooks/analise_csat_dezembro_2025.ipynb
```

### Opção 3: VS Code

1. Abrir VS Code
2. Abrir o arquivo `notebooks/analise_csat_dezembro_2025.ipynb`
3. Selecionar kernel Python 3.13
4. Executar células com `Shift + Enter`

---

## ▶️ Executar Todas as Células

No Jupyter:
- **Menu:** `Kernel` → `Restart & Run All`
- **Atalho:** `Ctrl + Shift + F9` (pode variar)

No VS Code:
- **Botão:** `Run All` no topo do notebook

---

## 📁 Estrutura de Arquivos Necessária

```
data-test/
├── notebooks/
│   └── analise_csat_dezembro_2025.ipynb  ← Notebook principal
│
├── dados/                                 ← CSVs aqui
│   ├── base_1_tickets.csv
│   ├── base_2_historico.csv
│   └── base_3_metas.csv
│
├── outputs/                               ← Outputs gerados aqui
│   └── (arquivos serão criados)
│
└── requirements.txt
```

---

## 🎯 O que o Notebook Faz

### Seções:

1. **Carregamento de Dados** - Lê os 3 CSVs
2. **Diagnóstico Atual** - Calcula CSAT geral e identifica ofensores
3. **Análise de Meta** - Calcula meta ponderada e GAP
4. **Plano de Ação (NLP)** - Análise semântica dos comentários
5. **Visualizações Adicionais** - Gera 3 gráficos
6. **Resumo Executivo** - Síntese final

### Outputs Gerados:

```
outputs/
├── grafico_distribuicao_notas.png
├── grafico_reincidencia_satisfacao.png
├── grafico_matriz_priorizacao.png
├── grafico_gap_performance.png
└── relatorio_semantico.txt
```

---

## ⚠️ Troubleshooting

### Erro: "No module named 'pandas'"
```bash
pip install pandas numpy scipy matplotlib seaborn keybert sentence-transformers
```

### Erro: "File not found: base_1_tickets.csv"
- Verifique se os CSVs estão em `dados/`
- Execute o notebook a partir da pasta raiz do projeto

### Erro: "Permission denied" ao salvar outputs
- Verifique se a pasta `outputs/` existe
- Crie manualmente: `mkdir outputs`

### Kernel não inicia
```bash
# Reinstalar ipykernel
pip install --upgrade ipykernel
python -m ipykernel install --user
```

---

## ⏱️ Tempo de Execução

- **Carregamento de dados:** ~5 segundos
- **Análise e cálculos:** ~10 segundos
- **NLP (análise semântica):** ~2-3 minutos (primeira vez, carrega modelos)
- **Visualizações:** ~30 segundos
- **Total:** ~4-5 minutos

---

## ✅ Verificação de Sucesso

Após executar todas as células, você deve ter:

- ✅ CSAT geral calculado: **54.6%**
- ✅ Meta projetada: **57.66%**
- ✅ 7 ofensores identificados
- ✅ 4 gráficos PNG em `outputs/`
- ✅ Relatório semântico TXT em `outputs/`
- ✅ Nenhum erro nas células

---

## 🔄 Re-executar

Para re-executar o notebook:

1. **Limpar outputs anteriores** (opcional):
   ```bash
   del outputs\*.png
   del outputs\relatorio_semantico.txt
   ```

2. **Reiniciar kernel:** `Kernel` → `Restart & Clear Output`

3. **Executar tudo:** `Kernel` → `Restart & Run All`

---

## 📞 Suporte

Se encontrar problemas:

1. Verifique a estrutura de pastas
2. Confirme que todas as dependências estão instaladas
3. Verifique a versão do Python (3.13 recomendado)
4. Revise os caminhos dos arquivos no notebook

---

**Última atualização:** 03/02/2026
