# Porsche Sales Dashboard

Dashboard interativa em HTML único, publicada com GitHub Pages.

## Perguntas de negócio

1. **Quais modelos geram mais receita?** Ajuda a identificar o mix de produtos que mais contribui para o faturamento.
2. **Como a receita evolui por ano?** Mostra tendências temporais para apoiar comparação de desempenho. Datas sanitizadas como `INVALID` não entram neste gráfico.
3. **Quais métodos de pagamento concentram mais vendas?** Ajuda a entender a composição das vendas por forma de pagamento.

Os indicadores do topo mostram número de vendas, receita total e ticket médio. Os filtros de modelo, ano da venda, cidade e método de pagamento atualizam os indicadores e gráficos em conjunto.

## Base e tratamento

A dashboard usa os 100 registros fornecidos no desafio, embutidos em `index.html` somente com campos sanitizados necessários: data de venda, modelo, ano do modelo, preço, forma de pagamento e cidade. Nomes de clientes e vendedores, além de identificadores, não foram incluídos. Preço e ano do modelo são valores numéricos. Datas `INVALID` são mantidas para os indicadores gerais, mas excluídas do gráfico temporal porque não permitem atribuição confiável de ano.

A base fornecida no chat continha valores sanitizados e valores crus lado a lado, além de colunas com dados pessoais. Foram selecionadas somente as colunas sanitizadas para análise e os dados pessoais foram descartados antes de embutir a base no HTML.

## Prompt e refinamentos

**Prompt inicial:** “Crie uma dashboard em um único arquivo HTML, em português, usando somente as colunas sanitizadas da base de vendas Porsche. Inclua indicadores de vendas e receita, filtros por modelo, ano e cidade, e três visões que respondam: quais modelos geram mais receita, como a receita muda ao longo do tempo e quais métodos de pagamento concentram mais vendas. Use uma identidade visual automotiva premium, escura, com vermelho Porsche como destaque. Não inclua dados pessoais.”

**Ajustes até a versão final:** foi esclarecido que datas `INVALID` não devem distorcer a análise temporal; os registros continuam nos totais e nas demais análises. Também foram adicionados filtro por pagamento, ticket médio, layout responsivo e a exclusão explícita de nomes e identificadores pessoais.

## Ferramenta

A implementação foi montada diretamente em HTML/JavaScript, sem Canvas ou agente com skill. Os gráficos são gerados no próprio arquivo, sem bibliotecas externas.

## Publicação

- Repositório: https://github.com/lincolnbuk/porsche-sales-dashboard
- Dashboard: https://lincolnbuk.github.io/porsche-sales-dashboard/

Para publicar, habilite **Settings → Pages** no repositório, selecionando a branch `main` e a pasta `/ (root)`. O endereço acima ficará disponível após o primeiro deploy do GitHub Pages.
