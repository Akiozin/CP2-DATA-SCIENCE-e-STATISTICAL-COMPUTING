# CP 2 - DATA SCIENCE e STATISTICAL COMPUTING
- Fabrício Saavedra - 97631
- Guilherme Akio - 98582
- Matheus Motta - 550352

# Gerador de Relatório HTML com Análise de Dados

Este projeto gera um relatório HTML com análise exploratória de um conjunto de dados utilizando `pandas` e `ydata-profiling`.

## Instalação

### 1. Instale as dependências necessárias

```bash
pip install vega_datasets pandas ydata-profiling
```

### 2. Teste o projeto

Você pode testar o projeto utilizando o dataset `cars` do `vega_datasets`. O código carregará os dados, criará uma análise exploratória e salvará o relatório como um arquivo HTML.

```python
# Importando bibliotecas necessárias
from vega_datasets import data  # Para carregar os datasets Vega
import pandas as pd
from pandas_profiling import ProfileReport  # Para gerar o relatório HTML

# Carregar o dataset 'cars' do vega_datasets
df = data.cars()

# Função para gerar o relatório HTML
def gerar_relatorio_html(df, nome_relatorio='relatorio_vegas.html'):
    # Gerando relatório de análise exploratória com pandas profiling
    profile = ProfileReport(df, title="Relatório de Análise - Vega Dataset", explorative=True)
    
    # Exportando o relatório gerado para um arquivo HTML
    profile.to_file(nome_relatorio)
    print(f"Relatório gerado: {nome_relatorio}")

# Testar a função gerando o relatório com o dataset de carros
gerar_relatorio_html(df)
```

### 3. Executar o código

Execute o código em seu ambiente para gerar o relatório HTML do dataset fornecido.

## Funcionalidade

- **Vega Dataset**: Um conjunto de dados de exemplo (neste caso, carros).
- **Pandas Profiling**: Gera relatórios de análise exploratória automatizados.

## Problemas comuns

Se encontrar erros de dependências, certifique-se de atualizar ou instalar as versões compatíveis de `pandas` e `pandas-profiling`:
```bash
pip install --upgrade pandas pandas-profiling
```
