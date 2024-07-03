# Analisar-dados
import pandas as pd
df = pd.read_excel("vendas.xlsx")

print(df)

print(df['Valor Final'].sum())

valor_final_por_produto = df.groupby('Produto')['Valor Final'].sum().reset_index()


print(valor_final_por_produto)

valor_final_por_produto_loja = df.groupby(['Produto', 'ID Loja'])['Valor Final'].sum().reset_index()


print(valor_final_por_produto_loja)
