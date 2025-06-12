# Monte Carlo Drawdown Analysis 📈

Uma ferramenta Python para análise de risco de carteiras usando simulação Monte Carlo, focada na previsão de drawdowns futuros para diferentes estratégias de investimento.

## 🚀 Funcionalidades

- **Análise Histórica**: Calcula drawdowns históricos de ativos
- **Simulação Monte Carlo**: Prevê drawdowns futuros usando 10.000 simulações
- **Múltiplas Estratégias**: Suporte para Buy & Hold, Cruzamento de Médias Móveis e RSI Reversal
- **Visualizações Interativas**: Gráficos detalhados usando Plotly
- **Relatório de Risco**: Classificação automática de risco com métricas detalhadas

### Dependências Necessárias
```python
# pip install yfinance==0.2.58
```

## 📊 Outputs

### 1. Gráficos Gerados

#### Análise Monte Carlo - Drawdowns Futuros
![Monte Carlo Analysis](https://github.com/joaoal1998/Drawdown-previsto-com-Monte-Carlo/blob/main/drawdown_futuro.png)

- **Distribuição dos Drawdowns**: Histograma mostrando frequência dos drawdowns simulados
- **Box Plot**: Visualização dos quartis e outliers
- **Probabilidades Acumuladas**: Função de distribuição cumulativa (CDF)
- **Cenários de Risco**: Percentis P50, P75, P90, P95, P99

#### Análise Histórica - Evolução da Carteira
![Historical Analysis](https://github.com/joaoal1998/Drawdown-previsto-com-Monte-Carlo/blob/main/evolucao_carteira.png)

- **Curva de Equity**: Evolução do valor da carteira ao longo do tempo
- **Drawdown Histórico**: Períodos de perdas e recuperação
- **Drawdown Máximo**: Maior perda registrada no período analisado

### 2. Relatório de Risco

```
RELATÓRIO DE RISCO MONTE CARLO
Ativo: BOVA11.SA | Estratégia: ma_cross
================================================================================
ESTATÍSTICAS DOS DRAWDOWNS FUTUROS (3 anos):
   • Drawdown médio esperado: 18.45%
   • Drawdown mediano: 16.32%
   • Desvio padrão: 12.89%
   • Mínimo (melhor caso): 2.15%
   • Máximo (pior caso): 67.43%

CENÁRIOS DE RISCO (Probabilidade de EXCEDER):
   • 50% chance de DD > 16.32% (cenário médio)
   • 25% chance de DD > 26.78% (cenário conservador)
   • 10% chance de DD > 38.94% (cenário muito conservador)
   •  5% chance de DD > 45.12% (cenário extremamente conservador)
   •  1% chance de DD > 58.67% (cenário catastrófico)

CLASSIFICAÇÃO DE RISCO: MÉDIO
   • Drawdowns significativos possíveis
```

## 📈 Metodologia

### Monte Carlo
- **Bootstrap**: Reamostragem dos retornos históricos
- **10.000 Simulações**: Para garantir robustez estatística
- **3 Anos Futuros**: Horizonte de análise (ajustável)

### Métricas de Risco
- **Drawdown Máximo**: Maior perda peak-to-trough
- **Percentis de Risco**: P50, P75, P90, P95, P99
- **Classificação**: Baixo, Médio ou Alto risco


## ⚠️ Limitações

- Assume que retornos futuros seguem padrões históricos e uma distribuição normal
- Não considera custos de transação
- Simulação baseada em bootstrap dos dados históricos
- Estratégias são simplificadas para fins demonstrativos


**Disclaimer**: Esta ferramenta é apenas para fins educacionais e de pesquisa. Não constitui aconselhamento financeiro. Sempre consulte um profissional qualificado antes de tomar decisões de investimento.
