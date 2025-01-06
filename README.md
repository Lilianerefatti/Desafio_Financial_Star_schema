Modelo Star Schema - Análise de Vendas
Este projeto utiliza o modelo Star Schema para organizar e analisar dados de vendas no Power BI. O modelo consiste em uma tabela de fatos centralizada conectada a diversas tabelas dimensionais. A tabela de fatos contém dados quantitativos, enquanto as tabelas dimensionais armazenam informações descritivas.

Estrutura do Modelo
Tabelas:
F_Vendas (Fato): Contém métricas de vendas como unidades vendidas, preço de venda, lucro, etc.
D_Produtos (Dimensão): Detalha informações sobre os produtos, como média de unidades vendidas, preço, valor máximo e mínimo de vendas.
D_Descontos (Dimensão): Informações sobre faixas de desconto aplicadas aos produtos.
D_Detalhes (Dimensão): Contém dados detalhados sobre vendas, como lucro, vendas brutas e preço.
D_Calendário (Dimensão de Data): Armazena informações temporais como ano, mês, trimestre e dia da semana.
Relacionamentos:
F_Vendas[ID_Produto] → D_Produtos[ID_Produto]
F_Vendas[Discount Band] → D_Descontos[Discount Band]
F_Vendas[Date] → D_Calendário[Date]
Construção do Modelo
Tabelas de Dimensão: Criadas a partir de dados de produtos, descontos, detalhes e datas.
Tabela de Fato: Centralizada com as métricas de vendas e conectada às tabelas dimensionais.
Relacionamentos: Estabelecidos entre a tabela de fatos e as tabelas dimensionais usando chaves como ID_Produto e Discount Band.
Conclusão
O modelo Star Schema facilita a análise de dados de vendas, permitindo insights detalhados sobre produtos, descontos e performance ao longo do tempo, proporcionando uma visualização eficiente no Power BI.
