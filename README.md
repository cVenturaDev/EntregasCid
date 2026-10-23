# Entrega 1 — Modelo Conceitual (DER)

### Donna Claudia Restaurante e Lanchonete

## Metadados

- Augusto - 48832588
- Felipe Rodrigues - 47868384
- Lucas Freitas de Oliveira - 48587885
- Matheus Faustino - 47854928
- Otavio Estevam Ventura Cristiano - 48763390

  ---

## 1 . Caracterização da Organização
**Nome e natureza da organização:** Donna Claudia Restaurante e Lanchonete, empresa privada do ramo alimentício (CNPJ 36.276.829/0001-69), que vende refeições e lanches.

**Contexto e porte:**
- Organização com fins lucrativos, em funcionamento há aproximadamente dois anos.
- Cinco funcionários.
- Cerca de 3.000 pessoas atendidas por mês.
- Pedidos recebidos por WhatsApp, aplicativos de delivery e atendimento no restaurante.

**Problemas e necessidades identificados:**
- O restaurante já usa o sistema online Bion Finance para controle de vendas, despesas e estoque (com aviso de estoque baixo), e ele continua atendendo bem.
- O ponto que mais exige atenção é o **delivery**: receber o pedido (WhatsApp ou aplicativo), conferir os dados do cliente, preparar e entregar.
- Há cancelamentos e reembolsos, principalmente nos aplicativos de delivery, que podem gerar confusão entre pedidos.
- Já ocorreram problemas por falta de controle, sem exemplo específico informado.
- O trabalho propõe um modelo de dados que organize essas informações (clientes, pedidos, produtos, pagamentos) de forma integrada.

**Justificativa da escolha:** Organização real, de porte adequado (pequena, mas com processos suficientes: venda, estoque, compras, pagamento, entrega) e com acesso garantido para a pesquisa de campo, o que permitiu levantar os processos reais por entrevista.

**Evidências da organização:**
- Endereço: Rua Maciel Monteiro, nº 264.
- Responsável: Antonia Claudia Freitas da Silva Oliveira
- Contatos (telefone, e-mail, site, Instagram): restaurante@donnaclaudia.com ; 1127439010 
- Fotos da visita / link do Google Maps: https://share.google/BqbmznFcOiSz4x2k4
---

## 2. Processos de Negócio

**Principais processos mapeados:**

1. **Abertura e fechamento do dia:** a proprietária costuma abrir o restaurante; os funcionários fazem o fechamento no fim do expediente.
2. **Cadastro de clientes:** coleta de nome, endereço e telefone, usados para identificar o cliente e realizar entregas.
3. **Venda e delivery:** o cliente pede por WhatsApp ou aplicativo, os dados são conferidos, o pedido vai para a cozinha e, quando pronto, é enviado para entrega.
4. **Controle de estoque:** feito no sistema online, que avisa quando um produto está acabando. No fim do dia, o gerente ou a proprietária confere e atualiza.
5. **Compras e fornecedores:** parte por aplicativos de fornecedores (com acompanhamento da entrega) e parte direto em mercados (conferência pela nota da compra).
6. **Pagamento:** dinheiro, Pix e cartão.
7. **Cancelamentos, trocas e reembolsos:** ocorrem principalmente nos aplicativos de delivery; conforme o caso, há reembolso ou preparo de um novo pedido.
8. **Fechamento de caixa e relatórios:** feito pelo gerente ou pela proprietária, conferindo as movimentações no Bion Finance.

A **cozinha** é a área que mais depende de trabalho em conjunto: o pedido precisa ser recebido, preparado e encaminhado corretamente. Não são realizados eventos nem campanhas.

## 3. Requisitos do Sistema

### 3.1 Requisitos Funcionais

- RF01 — O sistema deve permitir cadastrar clientes (nome, telefone e dados de contato).
- RF02 — O sistema deve permitir cadastrar produtos, com categoria, preço e quantidade em estoque.
- RF03 — O sistema deve permitir registrar pedidos com um ou mais produtos e acompanhar sua situação (recebido, em preparo, saiu para entrega, entregue ou cancelado).
- RF04 — O sistema deve permitir registrar pagamentos de um pedido (forma de pagamento, valor e situação).
- RF05 — O sistema deve permitir registrar cancelamentos e reembolsos.
- RF06 — O sistema deve alertar a proprietária quando um produto estiver com estoque baixo.
- RF07 — O sistema deve permitir consultar o total vendido no mês.
- RF08 — O sistema deve gerar relatórios de gastos e comparar vendas com despesas do período.
- RF09 — O sistema deve permitir cadastrar funcionários e seus cargos.

### 3.2 Requisitos Não Funcionais

- RNF01 — **Disponibilidade e acesso:** funcionar pela internet, em computador e celular.
- RNF02 — **Usabilidade:** interface simples, com informações fáceis de encontrar e poucas etapas por tarefa, pois há usuários com pouca familiaridade com tecnologia.
- RNF03 — **Desempenho:** suportar pelo menos 2 usuários simultâneos.
- RNF04 — **Segurança:** informações financeiras sob controle da proprietária; atualização de estoque permitida ao gerente (níveis de acesso).
- RNF05 — **Privacidade:** dados pessoais dos clientes acessíveis apenas a quem precisa deles, em conformidade com a LGPD.
- RNF06 — **Persistência:** armazenar o histórico de vendas, pedidos e gastos ao longo dos meses (prazo de guarda ainda a definir).
- RNF07 — **Contingência:** em caso de indisponibilidade, o controle pode ser manual, com atualização posterior dos registros.
---

## 4. Regras de Negócio

### Regras operacionais

- RN01 — Pedidos de delivery exigem cliente cadastrado com nome, telefone e endereço.
- RN02 — Vendas presenciais podem ocorrer sem cadastro de cliente (a confirmar com a proprietária).
- RN03 — O sistema deve considerar o estoque disponível antes de confirmar um pedido e avisar quando for insuficiente.
- RN04 — Um pedido pode conter vários produtos, e cada produto pertence a uma categoria.
- RN05 — Cada pedido deve ter ao menos um pagamento, registrado com forma de pagamento (dinheiro, Pix, cartão de crédito ou débito) e situação (pendente, pago ou reembolsado).
- RN06 — Situações do pedido: recebido, em preparo, saiu para entrega, entregue ou cancelado.
- RN07 — Em caso de problema, o pedido pode ser reembolsado ou refeito.
- RN08 — Cada cliente, produto, pedido e pagamento possui código único.
- RN09 — O histórico de vendas deve preservar o valor cobrado na época, mesmo que o preço do produto mude depois.
- RN10 — Cancelamentos, descontos e reembolsos devem seguir níveis de permissão (quem autoriza ainda deve ser definido).

### Restrições organizacionais

- **Normas sanitárias:** por ser do ramo alimentício, o restaurante segue as normas sanitárias aplicáveis.
- **Código de Defesa do Consumidor:** afeta cancelamentos, trocas e reembolsos.
- **LGPD:** nome, telefone e endereço dos clientes são dados pessoais e exigem acesso restrito.
- **Divisão de responsabilidades:** a proprietária abre o restaurante, e funcionários participam das atividades e do fechamento; a parte financeira fica com a proprietária e o gerente.
- **Guarda de registros:** o prazo ainda precisa ser definido conforme necessidades administrativas e obrigações legais.
- **Equipamentos:** o sistema deve rodar nos aparelhos já existentes (um computador e um celular), sem exigir novas compras.

---

## 5. Dicionário de Dados Conceitual (Preliminar)

O dicionário completo também está disponível em HTML (`dicionariodedados.html`)

###  Entidade: FORNECEDOR
| Atributo | Descrição | Regra de negócio associada |
|---|---|---|
| id_fornecedor | Identificador único do fornecedor | Obrigatório; não se repete |
| nome_empresa | Nome da empresa fornecedora | Obrigatório |
| contato | Forma de contato (telefone, e-mail ou responsável) | Opcional |

Um fornecedor pode ter nenhuma ou várias compras.

### Entidade: COMPRA
| Atributo | Descrição | Regra de negócio associada |
|---|---|---|
| id_compra | Identificador único da compra | Obrigatório; não se repete |
| data_compra | Data da compra de insumos/produtos | Obrigatório |
| valor_total | Valor total da compra em reais (atributo derivado) | Obrigatório; calculado pela soma de quantidade × custo_unitario dos itens |

Toda compra pertence a exatamente um fornecedor.

### Entidade: ITEM DE COMPRA
| Atributo | Descrição | Regra de negócio associada |
|---|---|---|
| quantidade | Quantidade do produto comprada | Obrigatório; maior que zero |
| custo_unitario | Custo de cada unidade na compra, em reais | Obrigatório; maior que zero |

Relacionamento “inclui” entre COMPRA e PRODUTO. Uma compra inclui de 1 a n produtos; um produto pode estar em nenhuma ou várias compras.

### Entidade: CATEGORIA
| Atributo | Descrição | Regra de negócio associada |
|---|---|---|
| id_categoria | Identificador único da categoria | Obrigatório; não se repete |
| nome_categoria | Nome da categoria (ex.: refeições, bebidas, lanches) | Obrigatório |

Uma categoria pode ter nenhum ou vários produtos.

### Entidade: PRODUTO
| Atributo | Descrição | Regra de negócio associada |
|---|---|---|
| id_produto | Identificador único do produto | Obrigatório; não se repete |
| nome_produto | Nome do produto | Obrigatório |
| descricao | Descrição do produto | Opcional |
| preco | Preço de venda em reais | Obrigatório; maior que zero |
| quantidade_estoque | Quantidade disponível | Obrigatório; não pode ser negativa; baixo estoque gera aviso |

Todo produto pertence a exatamente uma categoria.

### Entidade: CLIENTE
| Atributo | Descrição | Regra de negócio associada |
|---|---|---|
| id_cliente | Identificador único do cliente (ex.: CLI-001) | Obrigatório; não se repete |
| nome | Nome do cliente | Obrigatório nos pedidos de delivery; opcional em vendas de balcão |
| telefone | Telefone principal | Obrigatório nos pedidos de delivery |
| telefone_2 | Telefone alternativo | Opcional |

Um cliente pode fazer nenhum ou vários pedidos. Um pedido tem no máximo um cliente (pode não ter, em vendas de balcão).

### Entidade: ENDEREÇO
| Atributo | Descrição | Regra de negócio associada |
|---|---|---|
| id_endereco | Identificador único do endereço | Obrigatório; não se repete |
| rua | Logradouro | Obrigatório |
| numero | Número do imóvel | Obrigatório |
| bairro | Bairro | Obrigatório |
| cep | Código postal | Formato 00000-000 |
| complemento | Complemento (apartamento, bloco, referência) | Opcional |

Um cliente possui nenhum ou vários endereços (clientes de balcão podem não ter endereço cadastrado; pedidos de delivery exigem ao menos um). Todo endereço pertence a exatamente um cliente. Um endereço pode receber nenhuma ou várias entregas.

### Entidade: FUNCIONÁRIO
| Atributo | Descrição | Regra de negócio associada |
|---|---|---|
| id_funcionario | Identificador único do funcionário | Obrigatório; não se repete |
| nome | Nome do funcionário | Obrigatório |
| cargo | Função exercida (ex.: proprietária, gerente, cozinha) | Obrigatório |
| nivel_acesso | Nível de permissão no sistema | Obrigatório; definido a partir do cargo |

Um funcionário pode atender nenhum ou vários pedidos e registrar nenhuma ou várias despesas.

### Entidade: PEDIDO
| Atributo | Descrição | Regra de negócio associada |
|---|---|---|
| id_pedido | Identificador único do pedido (ex.: PED-001) | Obrigatório; não se repete |
| data_hora | Data e hora do pedido | Obrigatório |
| canal_atendimento | Canal pelo qual o pedido foi feito | Obrigatório; valores como balcão, delivery, WhatsApp |
| status | Situação do pedido | Valores: recebido, em preparo, saiu para entrega, entregue, cancelado |
| valor_total | Valor total do pedido em reais (atributo derivado) | Obrigatório; calculado pela soma de quantidade × preco_unitario dos itens |
| observacao | Observações do pedido (ex.: sem cebola) | Opcional |

Todo pedido é atendido por exatamente um funcionário, o que garante rastreabilidade.

### Entidade: ITEM DE PEDIDO
| Atributo | Descrição | Regra de negócio associada |
|---|---|---|
| quantidade | Quantidade do produto no pedido | Obrigatório; maior que zero |
| preco_unitario | Preço cobrado por unidade no momento do pedido | Obrigatório; maior que zero; guarda o preço da época, mesmo que o preço do produto mude depois |

Relacionamento “contém” entre PEDIDO e PRODUTO. Um pedido contém de 1 a n produtos; um produto pode estar em nenhum ou vários pedidos.

### Entidade: PAGAMENTO
| Atributo | Descrição | Regra de negócio associada |
|---|---|---|
| id_pagamento | Identificador único do pagamento | Obrigatório; não se repete |
| forma_pagamento | Meio de pagamento | Valores: dinheiro, Pix, cartão de crédito, cartão de débito |
| valor | Valor pago em reais | Obrigatório; maior que zero |
| status_pagamento | Situação do pagamento | Valores: pendente, pago, reembolsado |
| data_hora | Data e hora do pagamento | Obrigatório |

Um pedido recebe de 1 a n pagamentos (permite dividir a conta em formas diferentes). Todo pagamento pertence a exatamente um pedido.

### Entidade: ENTREGA
| Atributo | Descrição | Regra de negócio associada |
|---|---|---|
| id_entrega | Identificador único da entrega | Obrigatório; não se repete |
| status_entrega | Situação da entrega | Valores: pendente, saiu para entrega, entregue |

A entrega só existe em pedidos de delivery: um pedido gera no máximo uma entrega, e toda entrega pertence a exatamente um pedido. O destino é dado pelo relacionamento “destina” com ENDEREÇO: toda entrega é destinada a exatamente um endereço do cliente.

### Entidade: DESPESA
| Atributo | Descrição | Regra de negócio associada |
|---|---|---|
| id_despesa | Identificador único da despesa | Obrigatório; não se repete |
| descricao | Descrição da despesa | Obrigatório |
| categoria | Tipo da despesa (ex.: aluguel, energia, insumos) | Obrigatório |
| data_despesa | Data da despesa | Obrigatório |
| valor | Valor da despesa em reais | Obrigatório; maior que zero |

Toda despesa é registrada por exatamente um funcionário.
---


## 6. Modelagem Conceitual (Entidades, Atributos, Relacionamentos)


### Entidades reconhecidas

**FORNECEDOR** — representa as empresas que abastecem o restaurante, permitindo relacioná-las às compras de produtos e insumos.

**COMPRA** — representa uma aquisição feita junto a um fornecedor, concentrando data e valor total (derivado dos itens). Os produtos adquiridos são detalhados no relacionamento INCLUI.

**CATEGORIA** — criada para classificar os produtos (ex.: refeições, bebidas, lanches) e evitar repetir a informação de classificação em cada produto.

**PRODUTO** — representa os itens comercializados, com preço de venda e controle de quantidade em estoque. O baixo estoque gera aviso.

**CLIENTE** — representa as pessoas que fazem pedidos. O cliente é opcional no pedido porque o sistema precisa permitir vendas de balcão sem cadastro, mantendo a identificação quando necessária (como no delivery). Os endereços ficam em entidade própria (ver ENDEREÇO), e não como atributo direto de CLIENTE. O telefone_2 guarda um contato alternativo.

**ENDEREÇO** — separada de CLIENTE para permitir que um mesmo cliente tenha mais de um endereço (residencial, trabalho, entrega). Um cliente de balcão pode não ter endereço, mas pedidos de delivery exigem ao menos um. É também o destino das entregas.

**FUNCIONÁRIO** — representa os colaboradores. A associação ao pedido garante rastreabilidade de quem atendeu, e a associação à despesa mostra quem registrou o gasto. O atributo nivel_acesso define as permissões no sistema, a partir do cargo.

**PEDIDO** — representa uma operação de venda registrada, concentrando data/hora, canal de atendimento, status, valor total (derivado dos itens) e observações. É a entidade central do modelo, ligada a cliente, funcionário, produtos, pagamentos e entrega.

**PAGAMENTO** — representa cada recebimento vinculado a um pedido, permitindo mais de uma forma de pagamento para o mesmo pedido (divisão de conta). Todo pedido possui ao menos um pagamento, que fica com status “pendente” até a quitação.

**ENTREGA** — representa o envio de um pedido de delivery, com status próprio. Existe apenas nos pedidos que precisam ser entregues, e seu destino é um ENDEREÇO cadastrado, evitando texto solto e duplicação de dados.

**DESPESA** — representa os gastos do restaurante (ex.: aluguel, energia, insumos), sempre registrados por um funcionário.

## Atributos e classificações

Os atributos de cada entidade, com regras de negócio, estão detalhados no Dicionário de Dados. Em resumo:

| Entidade | Identificador | Atributos |
|---|---|---|
| FORNECEDOR | id_fornecedor | nome_empresa, contato |
| COMPRA | id_compra | data_compra, valor_total |
| CATEGORIA | id_categoria | nome_categoria |
| PRODUTO | id_produto | nome_produto, descricao, preco, quantidade_estoque |
| CLIENTE | id_cliente | nome, telefone, telefone_2 |
| ENDEREÇO | id_endereco | rua, numero, bairro, cep, complemento |
| FUNCIONÁRIO | id_funcionario | nome, cargo, nivel_acesso |
| PEDIDO | id_pedido | data_hora, canal_atendimento, status, valor_total, observacao |
| PAGAMENTO | id_pagamento | forma_pagamento, valor, status_pagamento, data_hora |
| ENTREGA | id_entrega | status_entrega |
| DESPESA | id_despesa | descricao, categoria, data_despesa, valor |

Os atributos **quantidade** e **custo_unitario** pertencem ao relacionamento INCLUI entre COMPRA e PRODUTO. Os atributos **quantidade** e **preco_unitario** pertencem ao relacionamento CONTÉM entre PEDIDO e PRODUTO. Eles não são atributos do produto, mas da sua participação em uma compra ou pedido específico.

Os atributos **valor_total** de COMPRA e de PEDIDO são **derivados**: resultam da soma dos itens (quantidade × custo_unitario e quantidade × preco_unitario, respectivamente). No DER aparecem com círculo tracejado.

## Relacionamentos pertinentes

| Relacionamento | Origem | Destino | Tipo de Conexão |
|---|---|---|---|
| FORNECEDOR ↔ COMPRA (fornece) | (1,1) | (0,N) | Um para Muitos (1:N) |
| COMPRA ↔ PRODUTO (inclui) | (0,N) | (1,N) | Muitos para Muitos (N:M), com atributos no relacionamento |
| CATEGORIA ↔ PRODUTO (classifica) | (1,1) | (0,N) | Um para Muitos (1:N) |
| PEDIDO ↔ PRODUTO (contém) | (0,N) | (1,N) | Muitos para Muitos (N:M), com atributos no relacionamento |
| CLIENTE ↔ PEDIDO (realiza) | (0,1) | (0,N) | Um para Muitos (1:N) Opcional |
| FUNCIONÁRIO ↔ PEDIDO (atende) | (1,1) | (0,N) | Um para Muitos (1:N) |
| CLIENTE ↔ ENDEREÇO (possui) | (1,1) | (0,N) | Um para Muitos (1:N) |
| ENDEREÇO ↔ ENTREGA (destina) | (1,1) | (0,N) | Um para Muitos (1:N) |
| PEDIDO ↔ PAGAMENTO (recebe) | (1,1) | (1,N) | Um para Muitos (1:N) |
| PEDIDO ↔ ENTREGA (gera) | (1,1) | (0,1) | Um para Um (1:1) Opcional |
| FUNCIONÁRIO ↔ DESPESA (registra) | (1,1) | (0,N) | Um para Muitos (1:N) |

A cardinalidade escrita junto a uma entidade indica quantas ocorrências dela se associam a **uma** ocorrência da outra entidade.

**FORNECEDOR ↔ COMPRA (1:N):** um fornecedor pode ter nenhuma ou várias compras; cada compra pertence a um único fornecedor.

**COMPRA ↔ PRODUTO (N:M, relacionamento INCLUI):** uma compra inclui de um a vários produtos e um produto pode estar em várias compras. A quantidade comprada e o custo unitário pertencem àquela compra específica.

**CATEGORIA ↔ PRODUTO (1:N):** cada produto pertence a uma categoria, evitando repetição de dados de classificação; uma categoria pode ter vários produtos.

**PEDIDO ↔ PRODUTO (N:M, relacionamento CONTÉM):** um pedido contém vários produtos e um produto pode estar em vários pedidos. A quantidade e o preço unitário pertencem à participação do produto no pedido, e o preço guarda o valor da época, mesmo que o preço do produto mude depois.

**CLIENTE ↔ PEDIDO (1:N opcional):** cada pedido pode ou não estar associado a um cliente, respeitando a regra de venda de balcão sem cadastro.

**FUNCIONÁRIO ↔ PEDIDO (1:N):** todo pedido é atendido por exatamente um funcionário, dando rastreabilidade ao atendimento; um funcionário pode atender vários pedidos.

**CLIENTE ↔ ENDEREÇO (1:N):** um cliente possui nenhum ou vários endereços (clientes de balcão podem não ter endereço); cada endereço pertence a um único cliente.

**ENDEREÇO ↔ ENTREGA (1:N):** toda entrega é destinada a exatamente um endereço cadastrado; um endereço pode receber nenhuma ou várias entregas.

**PEDIDO ↔ PAGAMENTO (1:N):** permite que um mesmo pedido seja quitado com mais de uma forma de pagamento; todo pedido possui ao menos um registro de pagamento.

**PEDIDO ↔ ENTREGA (1:1 opcional):** apenas pedidos de delivery geram entrega; cada pedido gera no máximo uma entrega e cada entrega pertence a um único pedido.

**FUNCIONÁRIO ↔ DESPESA (1:N):** toda despesa é registrada por exatamente um funcionário, que pode registrar várias despesas.

## Restrições e políticas organizacionais aplicadas ao modelo
O cliente é opcional no pedido para permitir vendas de balcão sem cadastro, mas nome, telefone e ao menos um endereço passam a ser obrigatórios nos pedidos de delivery. A entidade ENTREGA existe somente para pedidos de delivery e aponta para um ENDEREÇO cadastrado, o que mantém o modelo enxuto para pedidos de balcão. Todo pedido tem um funcionário responsável, e o controle de acesso (nivel_acesso, definido pelo cargo) é tratado como regra de negócio desde o nível conceitual. O preço unitário é gravado no item do pedido para preservar o histórico de vendas. A separação de CLIENTE e ENDEREÇO também ajuda a isolar os dados pessoais dos dados operacionais

---


## 7. Diagrama Entidade-Relacionamento (DER)
[Diagrama Entidade-Relacionamento](DER/DER%20conceitual.png)

📁 [Abrir a pasta do DER](DER)

---

## 8. Justificativa Técnica

A modelagem conceitual foi desenvolvida para representar, de forma estruturada, os principais processos operacionais do Donna Claudia Restaurante e Lanchonete, incluindo o cadastro de clientes, produtos, categorias, fornecedores, compras, pedidos, pagamentos, entregas, funcionários e despesas. A definição das entidades, atributos e relacionamentos foi baseada nas informações levantadas durante a pesquisa de campo, considerando as necessidades reais da organização, especialmente o controle dos pedidos de delivery, o acompanhamento do estoque, a rastreabilidade das vendas e o registro de cancelamentos e reembolsos. O modelo busca organizar as informações de maneira integrada, reduzir redundâncias e facilitar a futura implementação de um banco de dados.

Algumas decisões de modelagem merecem destaque:

- **Relacionamento N:M CONTÉM entre PEDIDO e PRODUTO, em vez de armazenar os produtos diretamente no PEDIDO:** um pedido pode conter vários produtos, e um mesmo produto pode estar presente em diversos pedidos. Armazenar os produtos em uma lista dentro de PEDIDO dificultaria as consultas e o controle individual dos itens. Por isso, o relacionamento CONTÉM possui os atributos `quantidade` e `preco_unitario`, que representam a participação de cada produto em um pedido específico. Essa decisão permite calcular os subtotais e o valor total da venda, além de facilitar consultas como os produtos mais vendidos e a quantidade comercializada em determinado período. Na modelagem lógica, esse relacionamento será convertido em uma tabela associativa.

- **Relacionamento N:M INCLUI entre COMPRA e PRODUTO, em vez de vincular cada compra a apenas um produto:** uma compra realizada com um fornecedor pode incluir diferentes produtos e insumos, enquanto um mesmo produto pode ser adquirido em várias compras. Os atributos `quantidade` e `custo_unitario` foram associados ao relacionamento, pois representam as condições de aquisição de cada produto em uma compra específica. Essa estrutura permite registrar os custos de aquisição e calcular o valor total da compra sem limitar a operação a um único item.

- **Separação da entidade CATEGORIA em relação a PRODUTO:** a criação de uma entidade específica para categorias permite classificar os produtos em grupos, como refeições, bebidas e lanches, sem repetir o nome da categoria em cada registro de produto. Cada produto pertence a exatamente uma categoria, enquanto uma categoria pode estar associada a vários produtos. Essa decisão facilita a organização do catálogo e permite futuras consultas e relatórios por categoria.

- **Entidade ENDEREÇO separada de CLIENTE:** a separação permite que um cliente possua vários endereços, como residencial, comercial ou de entrega, sem duplicar os dados cadastrais do cliente. Além disso, a entidade ENTREGA pode ser vinculada diretamente a um endereço cadastrado, garantindo maior consistência das informações utilizadas no delivery. Essa decisão é especialmente relevante para o restaurante, que recebe pedidos por WhatsApp e aplicativos de entrega. Para pedidos de delivery, devem ser informados os dados necessários à identificação do cliente e ao destino da entrega, enquanto clientes de balcão podem não possuir endereço cadastrado.

- **Relacionamento opcional entre CLIENTE e PEDIDO (0,1 para 0,N):** o cliente foi definido como opcional no pedido para permitir vendas presenciais sem a necessidade de realizar um cadastro. Essa decisão considera a regra de negócio RN02, segundo a qual vendas de balcão podem ocorrer sem identificação do cliente, enquanto pedidos de delivery exigem os dados cadastrais necessários ao atendimento. Dessa forma, o modelo atende aos diferentes canais de venda sem exigir informações desnecessárias em todas as operações.

- **Relacionamento 1:N entre PEDIDO e PAGAMENTO, com pelo menos um pagamento por pedido:** cada pedido possui ao menos um registro de pagamento, inicialmente podendo apresentar a situação Pendente e posteriormente ser atualizado para Pago ou Reembolsado. A possibilidade de registrar vários pagamentos para um mesmo pedido permite dividir o valor entre diferentes formas de pagamento, como dinheiro, Pix e cartão. Essa estrutura também facilita o acompanhamento dos valores recebidos e a identificação de pedidos ainda não quitados. O registro de pagamentos e seus respectivos status contribui para o controle financeiro e para a organização dos casos de cancelamento e reembolso.

- **Atributo `preco_unitario` no relacionamento CONTÉM, em vez de utilizar exclusivamente o preço atual de PRODUTO:** o preço de venda de um produto pode mudar ao longo do tempo. Caso o sistema utilizasse apenas o preço cadastrado atualmente, pedidos antigos poderiam apresentar valores incorretos em consultas e relatórios históricos. Por isso, o preço unitário é registrado no relacionamento entre PEDIDO e PRODUTO, preservando o valor efetivamente cobrado no momento da venda. O mesmo princípio é aplicado ao `custo_unitario` no relacionamento INCLUI, permitindo manter o custo praticado em cada compra.

- **Entidade ENTREGA separada de PEDIDO, com relacionamento 1:1 opcional:** nem toda venda realizada pelo restaurante exige entrega, pois também existem pedidos atendidos presencialmente no balcão. Por esse motivo, a entidade ENTREGA foi criada separadamente, permitindo registrar o status da entrega apenas quando necessário. Cada pedido pode gerar, no máximo, uma entrega, e cada entrega está vinculada a exatamente um pedido. Essa decisão evita a criação de informações de entrega desnecessárias para vendas presenciais e permite acompanhar etapas como pendente, saiu para entrega e entregue.

- **Entidade FUNCIONÁRIO relacionada a PEDIDO e DESPESA:** todo pedido é associado a um funcionário responsável pelo atendimento, enquanto toda despesa é registrada por um funcionário. Essa estrutura permite identificar quem realizou o atendimento e quem registrou determinado gasto, contribuindo para a rastreabilidade das operações. O atributo `cargo`, em conjunto com `nivel_acesso`, também permite representar as responsabilidades e as permissões de cada usuário, considerando que as informações financeiras devem permanecer sob controle da proprietária e do gerente, conforme as regras organizacionais levantadas.

- **Entidade DESPESA separada das demais operações financeiras:** as despesas, como aluguel, energia e aquisição de insumos, foram representadas em uma entidade própria, com descrição, categoria, data e valor. Essa decisão permite registrar os gastos independentemente das vendas e possibilita comparar as receitas e despesas de um período. Assim, o modelo oferece suporte aos requisitos RF07 e RF08, relacionados à consulta do total vendido no mês e à geração de relatórios financeiros.

- **Entidade FORNECEDOR relacionada a COMPRA:** cada compra pertence a exatamente um fornecedor, enquanto um fornecedor pode estar associado a nenhuma ou várias compras. Essa estrutura permite identificar a origem dos produtos e insumos adquiridos, organizar o histórico de compras e apoiar o acompanhamento dos custos de abastecimento do restaurante.

- **Atributos derivados `valor_total` em PEDIDO e COMPRA:** os valores totais foram definidos como derivados porque podem ser calculados a partir dos respectivos itens. No pedido, o total resulta da soma das quantidades multiplicadas pelos preços unitários praticados; na compra, resulta da soma das quantidades multiplicadas pelos custos unitários. Essa decisão estabelece uma regra clara de cálculo e reduz o risco de inconsistências entre os valores individuais e os totais registrados. Na implementação física, deverá ser definida uma estratégia para calcular ou armazenar esses valores de maneira consistente.

- **Controle de estoque representado em PRODUTO:** o atributo `quantidade_estoque` permite registrar a quantidade disponível de cada produto, respeitando a regra de que o saldo não pode ser negativo. Essa escolha atende à necessidade de acompanhar a disponibilidade dos itens e de emitir alertas quando o estoque estiver baixo. Como o restaurante já utiliza um sistema de gestão que oferece esse recurso, a modelagem considera essa necessidade operacional sem pressupor a substituição imediata da solução atualmente utilizada.

- **Registro de status de PEDIDO e PAGAMENTO para apoiar cancelamentos e reembolsos:** os atributos `status` e `status_pagamento` permitem distinguir as etapas do atendimento e a situação financeira de cada operação. Essa separação é importante porque um pedido pode ser cancelado e exigir um reembolso ou o preparo de um novo pedido, situações identificadas durante o levantamento dos processos. O modelo prevê o registro dessas informações, enquanto as regras de autorização para cancelamentos, descontos e reembolsos deverão ser detalhadas nas próximas etapas do projeto.

- **Separação entre dados operacionais e informações pessoais dos clientes:** os dados de identificação e contato são mantidos em CLIENTE, enquanto os endereços são armazenados em ENDEREÇO. Essa organização favorece a consistência cadastral e facilita a aplicação de controles de acesso, em conformidade com o requisito de privacidade e com a Lei Geral de Proteção de Dados Pessoais (LGPD). Na implementação, deverão ser definidos mecanismos de autenticação, autorização e proteção dos dados, limitando o acesso às informações pessoais e financeiras conforme a responsabilidade de cada usuário.

O modelo conceitual foi estruturado considerando o porte do Donna Claudia Restaurante e Lanchonete, seus canais de atendimento e as necessidades identificadas na pesquisa de campo. As decisões adotadas procuram equilibrar simplicidade, organização e capacidade de evolução, sem introduzir entidades ou relacionamentos que não apresentem justificativa operacional. A estrutura também permite atender aos requisitos funcionais relacionados ao cadastro, às vendas, aos pagamentos, às entregas, ao estoque e às despesas.

Por fim, o DER constitui a base para o desenvolvimento das próximas etapas do projeto. Na modelagem lógica, serão definidas as tabelas, as chaves primárias e estrangeiras e as restrições de integridade. Na modelagem física, serão especificados os tipos de dados, as validações, os índices e os demais mecanismos necessários à implementação do banco de dados. Também deverão ser detalhadas as regras de permissão, a política de armazenamento dos registros e os procedimentos para tratar cancelamentos, reembolsos e indisponibilidade do sistema.

---

## 9. Uso de Inteligência Artificial


| **Item** | **Registro** |
|---|---|
| **Ferramenta e etapa** | ChatGPT — apoio à organização dos requisitos, estruturação do Dicionário de Dados Conceitual, descrição das entidades e relacionamentos e elaboração da Justificativa Técnica do DER do Donna Claudia Restaurante e Lanchonete. |
| **Motivação** | Auxiliar na organização das informações coletadas durante a pesquisa de campo, transformar as necessidades operacionais do restaurante em uma estrutura técnica adequada ao modelo conceitual e melhorar a clareza e a consistência da documentação acadêmica. |
| **Prompt(s) utilizados** | "Com base nas informações coletadas sobre o Donna Claudia Restaurante e Lanchonete, organize os requisitos funcionais e não funcionais, as regras de negócio, o Dicionário de Dados Conceitual e os relacionamentos do DER." Outro prompt utilizado foi: "Faça uma Justificativa Técnica para o modelo conceitual do Donna Claudia Restaurante e Lanchonete, seguindo a estrutura de um exemplo fornecido e considerando as entidades, os atributos, as cardinalidades e as regras de negócio levantadas na pesquisa de campo." |
| **Resposta recebida** | A IA auxiliou na organização dos requisitos e das entidades, na descrição dos relacionamentos entre clientes, pedidos, produtos, pagamentos, fornecedores, compras, endereços, entregas, funcionários e despesas, além de elaborar justificativas para decisões de modelagem, como o relacionamento N:M entre PEDIDO e PRODUTO, a separação de CLIENTE e ENDEREÇO, a preservação do preço praticado na venda e a utilização de atributos derivados para os valores totais. Também auxiliou na redação da Justificativa Técnica, relacionando as decisões de modelagem às necessidades operacionais do restaurante. |
| **Fontes consultadas e verificadas** | A elaboração foi baseada nas informações fornecidas sobre a organização, nos resultados da entrevista e da pesquisa de campo, nos requisitos funcionais e não funcionais, nas regras de negócio, no Dicionário de Dados Conceitual e nas descrições do DER. A IA não apresentou fontes externas específicas para a elaboração desses textos. As informações devem ser conferidas pelo grupo com os registros da pesquisa de campo e com os documentos finais da entrega. |
| **Trechos rejeitados ou corrigidos** | As sugestões da IA foram utilizadas como apoio à documentação, sem substituir as decisões do grupo. As cardinalidades, os atributos e os relacionamentos devem permanecer alinhados ao DER definitivo. Merecem atenção especial a opcionalidade do cliente em pedidos de balcão, a obrigatoriedade dos dados cadastrais nos pedidos de delivery, o relacionamento N:M entre PEDIDO e PRODUTO, os atributos `quantidade` e `preco_unitario` associados ao relacionamento CONTÉM e a existência da entidade ENTREGA apenas para pedidos de delivery. Também é necessário confirmar com a proprietária as regras ainda pendentes, como a possibilidade de vendas de balcão sem cadastro, as permissões para autorizar cancelamentos e reembolsos e o prazo de armazenamento dos registros. |
| **Justificativa da escolha final** | O grupo considerou as características reais do Donna Claudia Restaurante e Lanchonete, seus diferentes canais de atendimento e os processos identificados na pesquisa de campo para orientar as decisões de modelagem. A identificação do cliente foi tratada de forma condicional conforme o canal de venda, enquanto as entidades e os relacionamentos foram definidos para organizar as operações de venda, compra, pagamento, entrega, estoque e controle de despesas. A versão final deve refletir as regras de negócio confirmadas pelo grupo e manter a consistência entre o DER, o README e o Dicionário de Dados. |
| **Reflexão crítica** | A inteligência artificial contribuiu para agilizar a organização das informações e melhorar a redação técnica, mas suas sugestões não substituem a análise dos processos reais da organização. Algumas decisões dependem de regras operacionais que ainda precisam ser confirmadas, como a identificação de clientes nas vendas presenciais, os níveis de autorização para reembolsos e o tratamento dos pagamentos pendentes. Além disso, a coerência entre cardinalidades, atributos e relacionamentos precisa ser verificada no DER e nos demais documentos. Por isso, o grupo deve utilizar a IA como ferramenta de apoio, validando as respostas com os dados da pesquisa de campo, os requisitos da atividade e os critérios definidos pelo professor. |

---

## Referências Bibliográficas

ELMASRI, Ramez; NAVATHE, Shamkant B. **Sistemas de Banco de Dados**. 7. ed. São Paulo: Pearson, 2011.




