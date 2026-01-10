Olá, como vai? Sabe aquele momento em que a teoria finalmente encontra a prática? Decidi criar este projeto justamente para celebrar essa transição. Ele é o resultado do meu mergulho no primeiro módulo do MBA em Data Science and Analytics da USP/Esalq, onde explorei desde as bases da estatística descritiva e testes de hipóteses até o poder de automação e análise que o Python nos oferece. Meu objetivo aqui não foi apenas executar fórmulas ou scripts, mas sim construir um recurso prático onde cada análise conta uma parte da história escondida nos dados. Convido você a acompanhar como utilizei as ferramentas clássicas e modernas para resolver problemas reais no case abaixo:

# Case: Otimização de Campanha de Investimentos - Fintech "DataBank"

### Contexto

A **DataBank** é uma fintech que oferece produtos de investimento. Recentemente, eles realizaram uma grande campanha de telemarketing para oferecer um CDB.
O custo de manter uma central de vendas ativa é altíssimo, e os resultados da última campanha foram controversos. A diretoria de Marketing não quer mais ligar para "todo mundo". Eles precisam que você o analista de dados identifique o perfil ideal de cliente e valide se certas estratégias (como tempo de ligação ou segmentação por escolaridade) realmente trazem resultados estatisticamente significativos.

### 2. Objetivo de Negócio

**Reduzir o custo de aquisição de clientes (CAC)** e **aumentar a taxa de conversão**, gerando um relatório técnico que direcione a próxima campanha apenas para os leads com maior probabilidade de fechamento.

---

### 3. Roteiro de Execução (Seu "North Star")

Para atingir esse objetivo, você dividirá seu projeto em 4 perguntas fundamentais que utilizam todo o conteúdo do seu MBA:

### **Pergunta 1: Qual é o "retrato falado" do nosso cliente atual?**

- **Ação Python:** Use `pandas` (`describe`, `groupby`) para limpar os dados.
- **Ação Estatística:** Use **Medidas de Posição e Dispersão**.
- **Insight de Negócio:** "O cliente médio tem X anos e saldo de Y, mas a variância é alta, o que indica diferentes nichos."

### **Pergunta 2: O nível de escolaridade realmente afeta a decisão de investimento?**

- **Ação Python:** Crie tabelas de contingência com `pd.crosstab` e gráficos de barras no `plotly`.
- **Ação Estatística:** Aplique o **Teste Qui-Quadrado de Associação**.
- **Insight de Negócio:** "Confirmamos (ou não) que clientes com ensino superior têm Z% mais chance de investir. Devemos priorizar esse grupo?"

### **Pergunta 3: Existe uma relação entre o saldo bancário e a idade?**

- **Ação Python:** Gere um `sns.scatterplot` e um `sns.heatmap`.
- **Ação Estatística:** Calcule a **Correlação de Pearson**.
- **Insight de Negócio:** "Se houver correlação forte, podemos focar em produtos de maior valor para faixas etárias específicas."

### **Pergunta 4: O tempo de conversa ao telefone garante a venda?**

- **Ação Python:** Separe os dados em dois grupos (Quem comprou vs. Quem não comprou).
- **Ação Estatística:** Primeiro use o **Teste F para Variâncias** e, depois, o **Teste t para Amostras Independentes**.
- **Insight de Negócio:** "Provamos estatisticamente que ligações acima de X minutos têm uma média de conversão superior. Treinamento de retenção na linha é necessário."
