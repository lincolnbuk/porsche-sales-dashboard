# Porsche Sales Dashboard

Dashboard responsiva de vendas Porsche em **um único arquivo HTML**, com filtros e visualizações interativas, sem dependências externas.

## Acesse o projeto

- **Dashboard publicada:** [Abrir a dashboard no GitHub Pages](https://lincolnbuk.github.io/porsche-sales-dashboard/)
- **Repositório e código-fonte:** [lincolnbuk/porsche-sales-dashboard](https://github.com/lincolnbuk/porsche-sales-dashboard)

## Perguntas de negócio

1. **Quais modelos geram mais receita?** Compara a contribuição de cada modelo e destaca os dez maiores no recorte.
2. **Como a receita evolui por ano?** Acompanha a receita anual usando apenas datas sanitizadas válidas. As linhas com `INVALID` continuam nos indicadores e nas demais análises, mas não são atribuídas a um ano.
3. **Quais métodos concentram mais vendas?** Compara a quantidade de vendas por forma de pagamento.

Os indicadores de topo mostram vendas, receita, ticket médio e quantidade de datas válidas. Os filtros de modelo, ano da venda, estado e pagamento atualizam todos os indicadores e gráficos.

## Identidade visual

Interface escura com vermelho como cor de destaque, dourado discreto, tipografia sem serifa e componentes responsivos. A página foi pensada para leitura em desktop e celular; os gráficos são barras CSS renderizadas em JavaScript.

## Dados e tratamento

A dashboard incorpora os 100 registros fornecidos no desafio usando somente os campos sanitizados necessários: data da venda, modelo, ano do modelo, preço, forma de pagamento e cidade. Nomes de clientes e vendedores, além de identificadores da venda, foram descartados e não estão no HTML.

O preço e o ano do modelo são valores numéricos sanitizados. Datas `INVALID` são representadas sem data válida para fins de agrupamento temporal; os registros permanecem nos totais e nas outras visualizações. O estado foi derivado da cidade para oferecer o filtro estadual.

## Prompt e refinamentos

**Prompt de referência:** “Crie uma dashboard em um único arquivo HTML, em português, usando somente as colunas sanitizadas da base de vendas Porsche. Inclua indicadores de vendas, receita e ticket médio; filtros por modelo, ano, estado e método de pagamento; e três análises para responder quais modelos geram mais receita, como a receita evolui por ano e quais métodos de pagamento concentram mais vendas. Use uma identidade visual automotiva premium, escura, com vermelho Porsche como destaque. Não inclua dados pessoais. Datas inválidas não devem ser incluídas na análise temporal, mas seus registros devem continuar nos totais.”

**Refinamentos incluídos:** filtro de cidade trocado por estado; acrescentado indicador de datas válidas; layout responsivo com identidade premium; datas inválidas mantidas fora do agrupamento temporal; remoção de identificadores e dados pessoais. A primeira data da base também foi corrigida para ser tratada como inválida (`2024-02-30` não é uma data válida).

## Ferramenta

Implementação em HTML, CSS e JavaScript, sem Canvas ou agente com skill e sem bibliotecas externas. A estrutura mantém o conjunto de dados necessário no próprio `index.html` para funcionar como arquivo único.

## Arquivos

- `index.html` — dashboard e dados sanitizados mínimos usados nos gráficos.
- `README.md` — perguntas, decisões de tratamento, prompt e instruções de publicação.

## Publicação

O site está publicado pelo GitHub Pages. Para verificar ou alterar as configurações, abra **Settings → Pages**, com origem **Deploy from a branch**, branch `main` e pasta `/(root)`. O deploy pode levar alguns minutos após alterações.
