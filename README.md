# 📑 Relatório de Análise de Evasão de Clientes (Churn)

## 1. Introdução
O objetivo desta análise é compreender os fatores que influenciam a evasão de clientes (Churn) em uma empresa de telecomunicações.
A evasão representa um desafio estratégico, pois impacta diretamente na receita e na sustentabilidade do negócio.
Através da exploração dos dados, buscamos identificar padrões e variáveis que possam explicar por que alguns clientes cancelam seus contratos, enquanto outros permanecem.

## 2. Limpeza e Tratamento de Dados
- Importação dos dados a partir do arquivo TelecomX_Data.json.
- Normalização de colunas aninhadas (customer, phone, internet, account).
- Conversão de variáveis numéricas que estavam como texto (TotalCharges → float).
- Tratamento de valores nulos em TotalCharges (substituídos por 0).
- Remoção de espaços em branco em colunas categóricas.
- Padronização de categorias (No internet service → No).
- Conversão da variável alvo Churn para binária (Yes=1, No=0).
- Criação da coluna Contas_Diarias (valor diário baseado no faturamento mensal).

### 3. Análise Exploratória de Dados
- **Distribuição da variável Churn:** gráficos de barras e pizza mostraram que a maioria dos clientes permanece, mas há uma proporção significativa de evasão.
- **Variáveis categóricas:**
  - Contratos mensais apresentam maior taxa de evasão.
  - O método de pagamento influencia: clientes com cobrança eletrônica têm maior tendência a cancelar.
  - Gênero não mostrou diferença significativa.
- **Variáveis numéricas:**
  - Clientes com menor tempo de contrato (tenure) e menor gasto acumulado (TotalCharges) tendem a evadir mais.
  - O faturamento mensal (MonthlyCharges) também mostrou associação com evasão, especialmente em valores mais altos.
 
### 4. Conclusões e Insights
- Tempo de contrato é um dos fatores mais relevantes: clientes novos têm maior risco de evasão.
- Tipo de contrato influencia fortemente: contratos mensais são mais vulneráveis.
- Valor gasto: clientes com baixo gasto acumulado tendem a evadir, indicando que a fidelização ainda não ocorreu.
- Método de pagamento: pode ser um indicador de perfil de cliente mais propenso ao cancelamento.

### 5. Recomendações
- **Incentivar contratos de longo prazo**: oferecer descontos ou benefícios para clientes que migram de contratos mensais para anuais/bienais.
- **Programas de fidelização**: criar ações específicas para clientes novos (primeiros meses de contrato), reduzindo o risco de evasão inicial.
- **Monitorar clientes com alto custo mensal**: oferecer pacotes personalizados ou suporte adicional para evitar insatisfação.
- **Revisar métodos de pagamento**: analisar se clientes com determinados métodos (ex: cobrança eletrônica) precisam de comunicação diferenciada ou suporte extra.
