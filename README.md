====================================================================
 ____  ____    _    ____ __  __    _  _____  _    
|  _ \|  _ \  / \  / ___|  \/  |  / \|_   _|/ \   
| |_) | |_) |/ _ \| |  _| |\/| | / _ \ | | / _ \  
|  __/|  _ </ ___ \ |_| | |  | |/ ___ \| |/ ___ \ 
|_|   |_| \_/_   \_\____|_|  |_/_/   \_\_/_   \_\
                                                  
====================================================================
DATASET EDUCACIONAL PARA LABORATÓRIOS E ANÁLISE DE DADOS
====================================================================

AVISO IMPORTANTE: DADOS 100% FICTÍCIOS
--------------------------------------------------------------------
Todos os dados contidos neste repositório são estritamente fictícios
e foram gerados de forma programática. Nomes de clientes, valores,
custos e transações não possuem nenhuma relação com empresas reais.

Eles foram desenvolvidos com o propósito exclusivo de servir como
material didático em ambientes de laboratório, testes e treinamento.
--------------------------------------------------------------------

APLICAÇÃO DIDÁTICA
------------------
Este conjunto de dados é ideal para cursos, workshops e disciplinas
práticas que ensinam ferramentas de Business Intelligence (BI) e
análise de dados, tais como:

* Microsoft Excel (Tabelas Dinâmicas, Fórmulas, Gráficos e Procv)
* Power Query (Processos de ETL - Extração, Transformação e Carga)
* Microsoft Power BI (Modelagem de Dados, Linguagem DAX e Dashboards)
* Microsoft Access (Introdução a Bancos de Dados Relacionais e SQL)


ESTRUTURA DOS ARQUIVOS (VERSÃO _v3)
-----------------------------------
Os dados estão fragmentados por meses para permitir exercícios de
consolidação de tabelas (Append/Acrescentar). A versão atual (_v3)
foi otimizada especificamente para o público brasileiro:

* Separador de colunas: Ponto e vírgula (;)
* Separador decimal: Vírgula (,) -> Evita erros de leitura no Excel PT-BR.
* Regra de negócio: O Custo_Unitario é sempre menor que o Valor_Unitario,
  garantindo que todas as operações gerem margem de lucro positiva.

Arquivos disponíveis no repositório:
- Pragmata_Vendas_Janeiro_v3.csv
- Pragmata_Vendas_Fevereiro_v3.csv
- Pragmata_Vendas_Marco_v3.csv
- Pragmata_Vendas_Abril_v3.csv (Sugerido para uso no MS Access)
- Pragmata_Vendas_Maio_v3.csv
- Pragmata_Vendas_Junho_v3.csv
- Pragmata_Vendas_Julho_v3.csv
- Pragmata_Vendas_Agosto_v3.csv
- Pragmata_Vendas_Setembro_v3.csv
- Pragmata_Vendas_Outubro_v3.csv
- Pragmata_Vendas_Novembro_v3.csv


DICIONÁRIO DE DADOS (COLUNAS)
-----------------------------
Coluna              Tipo      Descrição
--------------------------------------------------------------------
ID_Transacao        Texto     Identificador único da venda (Ex: PRG-202604-001)
Data                Data      Data da venda (Formato: DD/MM/AAAA)
Cliente             Texto     Nome da empresa compradora
Produto_Servico     Texto     Nome do software ou serviço vendido
Categoria           Texto     Segmentação do item ("Software" ou "Serviço")
Quantidade          Inteiro   Volume de itens vendidos na transação
Valor_Unitario      Decimal   Preço de venda de uma unidade do item
Custo_Unitario      Decimal   Custo de operação/produção de uma unidade
Qtd_Parcelas        Inteiro   Em quantas vezes o cliente parcelou (1 a 12)
Canal_Venda         Texto     Meio da venda (Direta, E-commerce, B2B)
Status              Texto     Situação (Pago, Pendente, Cancelado)
--------------------------------------------------------------------


SUGESTÕES DE EXERCÍCIOS PRÁTICOS EM AULA
----------------------------------------
1. Criação de Colunas Calculadas (Matemática no Power Query):
   Os arquivos propositalmente não trazem totais calculados. Desafie 
   os alunos a criarem as seguintes colunas personalizadas:
   * Faturamento Total = Quantidade * Valor_Unitario
   * Lucro Unitario = Valor_Unitario - Custo_Unitario
   * Valor da Parcela = Faturamento Total / Qtd_Parcelas

2. Combinação de Múltiplas Fontes (Cenário Híbrido):
   Coloque o arquivo de "Abril" dentro de uma tabela do MS Access e os
   outros meses no GitHub. Ensine os alunos a puxarem os dados de locais
   diferentes e unificarem tudo usando o "Acrescentar Consultas".

3. Atualização de Dados em Tempo Real (ETL Automatizado):
   Peça para criarem os relatórios contendo apenas de Janeiro a Outubro.
   Depois, adicione o arquivo de Novembro na pasta e mostre o poder do
   botão "Atualizar Tudo", que automatiza a expansão dos gráficos.
====================================================================****
