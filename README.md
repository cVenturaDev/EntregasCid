# Entrega 1 — Modelo Conceitual (DER)
## Donna Claudia Restaurante e Lanchonete


---

## Metadados

- Augusto - 48832588
- Felipe Rodrigues - 47868384
- Lucas Freitas de Oliveira - 48587885
- Matheus Faustino - 47854928
- Otavio Estevam Ventura Cristiano - 48763390

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
- Responsável: proprietária do restaurante, que acompanha a administração. [PREENCHER nome e confirmar autorização para uso do nome]
- Contatos (telefone, e-mail, site, Instagram): [PREENCHER]
- Fotos da visita / link do Google Maps: [PREENCHER]



---

## 2\. Processos de Negócio
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

---
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

## 4\. Regras de Negócio

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

## 5\. Dicionário de Dados Conceitual (Preliminar)

### Entidade: FORNECEDOR
| Atributo | Descrição | Regra de negócio associada |
|---|---|---|
| id_fornecedor | Identificador único do fornecedor | Obrigatório; não se repete |
| nome_empresa | Nome da empresa fornecedora | Obrigatório |
| contato | Forma de contato (telefone, e-mail ou responsável) | Opcional |

### Entidade: COMPRA
| Atributo | Descrição | Regra de negócio associada |
|---|---|---|
| id_compra | Identificador único da compra | Obrigatório; não se repete |
| data_compra | Data da compra de insumos/produtos | Obrigatório |
| valor_total | Valor total da compra em reais | Obrigatório; soma de quantidade × custo_unitario dos itens |

Toda compra pertence a exatamente um fornecedor. Um fornecedor pode ter nenhuma ou várias compras.

### Entidade: ITEM DE COMPRA (relacionamento "inclui" entre COMPRA e PRODUTO)
| Atributo | Descrição | Regra de negócio associada |
|---|---|---|
| quantidade | Quantidade do produto comprada | Obrigatório; maior que zero |
| custo_unitario | Custo de cada unidade na compra, em reais | Obrigatório; maior que zero |

Uma compra inclui de 1 a n produtos. Um produto pode estar em nenhuma ou várias compras.

###  Entidade: CATEGORIA
| Atributo | Descrição | Regra de negócio associada |
|---|---|---|
| id_categoria | Identificador único da categoria | Obrigatório; não se repete |
| nome_categoria | Nome da categoria (ex.: refeições, bebidas, lanches) | Obrigatório |

### Entidade: PRODUTO
| Atributo | Descrição | Regra de negócio associada |
|---|---|---|
| id_produto | Identificador único do produto | Obrigatório; não se repete |
| nome_produto | Nome do produto | Obrigatório |
| descricao | Descrição do produto | Opcional |
| preco | Preço de venda em reais | Obrigatório; maior que zero |
| quantidade_estoque | Quantidade disponível | Obrigatório; não pode ser negativa; baixo estoque gera aviso |

Todo produto pertence a exatamente uma categoria. Uma categoria pode ter nenhum ou vários produtos.

### Entidade: CLIENTE
| Atributo | Descrição | Regra de negócio associada |
|---|---|---|
| id_cliente | Identificador único do cliente (ex.: CLI-001) | Obrigatório; não se repete |
| nome | Nome do cliente | Obrigatório nos pedidos de delivery; opcional em vendas de balcão |
| telefone | Telefone principal | Obrigatório nos pedidos de delivery |
| telefone_2 | Telefone alternativo | Opcional |

Um cliente pode fazer nenhum ou vários pedidos. Um pedido tem no máximo um cliente (pode não ter, em vendas de balcão).

### Entidade: ENDERECO
| Atributo | Descrição | Regra de negócio associada |
|---|---|---|
| id_endereco | Identificador único do endereço | Obrigatório; não se repete |
| rua | Logradouro | Obrigatório |
| numero | Número do imóvel | Obrigatório |
| bairro | Bairro | Obrigatório |
| cep | Código postal | Formato 00000-000 |
| complemento | Complemento (apartamento, bloco, referência) | Opcional |

Todo cliente possui de 1 a n endereços. Todo endereço pertence a exatamente um cliente.

### Entidade: FUNCIONARIO
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
| valor_total | Valor total do pedido em reais | Obrigatório; soma de quantidade × preco_unitario dos itens |
| observacao | Observações do pedido (ex.: sem cebola) | Opcional |

Um pedido é atendido por no máximo um funcionário.

### Entidade: ITEM DE PEDIDO (relacionamento "contém" entre PEDIDO e PRODUTO)
| Atributo | Descrição | Regra de negócio associada |
|---|---|---|
| quantidade | Quantidade do produto no pedido | Obrigatório; maior que zero |
| preco_unitario | Preço cobrado por unidade no momento do pedido | Obrigatório; maior que zero; guarda o preço da época, mesmo que o preço do produto mude depois |

Um pedido contém de 1 a n produtos. Um produto pode estar em nenhum ou vários pedidos.

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
| endereco_entrega | Endereço de destino da entrega | Obrigatório |
| status_entrega | Situação da entrega | Valores: pendente, saiu para entrega, entregue |

A entrega só existe em pedidos de delivery: um pedido gera no máximo uma entrega, e toda entrega pertence a exatamente um pedido.

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


## 6\. Modelagem Conceitual (Entidades, Atributos, Relacionamentos)
## Entidades reconhecidas

**CLIENTE** — representa as pessoas que fazem pedidos. O cliente é opcional no pedido porque o sistema precisa permitir vendas de balcão sem cadastro, mantendo a identificação quando necessária (como no delivery). Os endereços ficam em entidade própria (ver ENDERECO), e não como atributo direto de CLIENTE. O telefone_2 permite guardar um contato alternativo.

**ENDERECO** — separada de CLIENTE para permitir que um mesmo cliente tenha mais de um endereço (residencial, trabalho, entrega). Todo cliente possui pelo menos um endereço cadastrado.

**FUNCIONARIO** — representa os colaboradores. A associação ao pedido garante rastreabilidade de quem atendeu, e a associação à despesa mostra quem registrou o gasto. O atributo nivel_acesso define as permissões no sistema, a partir do cargo.

**FORNECEDOR** — representa as empresas que abastecem o restaurante, permitindo relacioná-las às compras de produtos e insumos.

**COMPRA** — representa uma aquisição feita junto a um fornecedor, concentrando data e valor total. Os produtos adquiridos são detalhados no relacionamento INCLUI.

**CATEGORIA** — criada para classificar os produtos (ex.: refeições, bebidas, lanches) e evitar repetir a informação de classificação em cada produto.

**PRODUTO** — representa os itens comercializados, com preço de venda e controle de quantidade em estoque. O baixo estoque gera aviso.

**PEDIDO** — representa uma operação de venda registrada, concentrando data/hora, canal de atendimento, status, valor total e observações. É a entidade central do modelo, ligada a cliente, funcionário, produtos, pagamentos e entrega.

**PAGAMENTO** — representa cada recebimento vinculado a um pedido, permitindo mais de uma forma de pagamento para o mesmo pedido (divisão de conta). Todo pedido possui ao menos um pagamento, que fica com status "pendente" até a quitação.

**ENTREGA** — representa o envio de um pedido de delivery, com endereço de destino e status. Existe apenas nos pedidos que precisam ser entregues.

**DESPESA** — representa os gastos do restaurante (ex.: aluguel, energia, insumos), sempre registrados por um funcionário.

## Atributos e classificações

Os atributos de cada entidade, com chave primária e regras de negócio, estão detalhados no Dicionário de Dados. Em resumo:

| Entidade | Identificador | Atributos |
|---|---|---|
| FORNECEDOR | id_fornecedor | nome_empresa, contato |
| COMPRA | id_compra | data_compra, valor_total |
| CATEGORIA | id_categoria | nome_categoria |
| PRODUTO | id_produto | nome_produto, descricao, preco, quantidade_estoque |
| CLIENTE | id_cliente | nome, telefone, telefone_2 |
| ENDERECO | id_endereco | rua, numero, bairro, cep, complemento |
| FUNCIONARIO | id_funcionario | nome, cargo, nivel_acesso |
| PEDIDO | id_pedido | data_hora, canal_atendimento, status, valor_total, observacao |
| PAGAMENTO | id_pagamento | forma_pagamento, valor, status_pagamento, data_hora |
| ENTREGA | id_entrega | endereco_entrega, status_entrega |
| DESPESA | id_despesa | descricao, categoria, data_despesa, valor |

Os atributos **quantidade** e **custo_unitario** pertencem ao relacionamento INCLUI entre COMPRA e PRODUTO. Os atributos **quantidade** e **preco_unitario** pertencem ao relacionamento CONTEM entre PEDIDO e PRODUTO. Eles não são atributos do produto, mas da sua participação em uma compra ou pedido específico.

Os atributos **valor_total** de COMPRA e de PEDIDO são derivados: resultam da soma dos itens (quantidade × custo_unitario e quantidade × preco_unitario, respectivamente).

## Relacionamentos pertinentes

| Relacionamento | Origem | Destino | Tipo de Conexão |
|---|---|---|---|
| FORNECEDOR ↔ COMPRA (fornece) | (1,1) | (0,N) | Um para Muitos (1:N) |
| COMPRA ↔ PRODUTO (inclui) | (0,N) | (1,N) | Muitos para Muitos (N:M), com atributos no relacionamento |
| CATEGORIA ↔ PRODUTO (classifica) | (1,1) | (0,N) | Um para Muitos (1:N) |
| PEDIDO ↔ PRODUTO (contem) | (0,N) | (1,N) | Muitos para Muitos (N:M), com atributos no relacionamento |
| CLIENTE ↔ PEDIDO (realiza) | (0,1) | (0,N) | Um para Muitos (1:N) Opcional |
| FUNCIONARIO ↔ PEDIDO (atende) | (0,1) | (0,N) | Um para Muitos (1:N) Opcional |
| CLIENTE ↔ ENDERECO (possui) | (1,1) | (1,N) | Um para Muitos (1:N) |
| PEDIDO ↔ PAGAMENTO (recebe) | (1,1) | (1,N) | Um para Muitos (1:N) |
| PEDIDO ↔ ENTREGA (gera) | (1,1) | (0,1) | Um para Um (1:1) Opcional |
| FUNCIONARIO ↔ DESPESA (registra) | (1,1) | (0,N) | Um para Muitos (1:N) |

**FORNECEDOR ↔ COMPRA (1:N):** um fornecedor pode ter nenhuma ou várias compras; cada compra pertence a um único fornecedor.

**COMPRA ↔ PRODUTO (N:M, relacionamento INCLUI):** uma compra inclui de um a vários produtos e um produto pode estar em várias compras. A quantidade comprada e o custo unitário não são atributos do produto, mas daquela compra específica.

**CATEGORIA ↔ PRODUTO (1:N):** cada produto pertence a uma categoria, evitando repetição de dados de classificação; uma categoria pode ter vários produtos.

**PEDIDO ↔ PRODUTO (N:M, relacionamento CONTEM):** um pedido contém vários produtos e um produto pode estar em vários pedidos. A quantidade e o preço unitário pertencem à participação do produto no pedido, e o preço guarda o valor da época, mesmo que o preço do produto mude depois.

**CLIENTE ↔ PEDIDO (1:N opcional):** cada pedido pode ou não estar associado a um cliente, respeitando a regra de venda de balcão sem cadastro.

**FUNCIONARIO ↔ PEDIDO (1:N opcional):** cada pedido é atendido por no máximo um funcionário, dando rastreabilidade ao atendimento; um funcionário pode atender vários pedidos.

**CLIENTE ↔ ENDERECO (1:N):** um cliente possui um ou mais endereços; cada endereço pertence a um único cliente.

**PEDIDO ↔ PAGAMENTO (1:N):** permite que um mesmo pedido seja quitado com mais de uma forma de pagamento; todo pedido possui ao menos um registro de pagamento.

**PEDIDO ↔ ENTREGA (1:1 opcional):** apenas pedidos de delivery geram entrega; cada pedido gera no máximo uma entrega e cada entrega pertence a um único pedido.

**FUNCIONARIO ↔ DESPESA (1:N):** toda despesa é registrada por exatamente um funcionário, que pode registrar várias despesas.

## Restrições e políticas organizacionais aplicadas ao modelo

O cliente é opcional no pedido para permitir vendas de balcão sem cadastro, mas nome e telefone passam a ser obrigatórios nos pedidos de delivery. A entidade ENTREGA existe somente para pedidos de delivery, o que mantém o modelo enxuto para pedidos de balcão. O preço unitário é gravado no item do pedido para preservar o histórico de vendas, e o controle de acesso (nivel_acesso, definido pelo cargo do funcionário) é tratado como regra de negócio desde o nível conceitual. A separação de CLIENTE e ENDERECO também ajuda a isolar os dados pessoais dos dados operacionais.




---







## 7\. Diagrama Entidade-Relacionamento (DER)

*(vale 20% — é o item de maior peso da entrega)*

- Anexe o DER (em imagem).  
- O diagrama deve representar corretamente:  
  - Entidades  
  - Atributos  
  - Relacionamentos  
  - **Cardinalidades**  
- O modelo deve ser **consistente** e já demonstrar potencial de **escalabilidade e integração** (pensando nas próximas etapas do projeto).

---

## 8\. Justificativa Técnica

*(vale 7,5% — sozinho, é o subcritério de maior peso dentro da Dimensão Conceitual)*

*Explique e defenda as decisões de abstração e modelagem tomadas: por que essas entidades, esses atributos, esses relacionamentos e essas cardinalidades — e não outras alternativas possíveis?*

---

## 9\. Uso de Inteligência Artificial

*(documentação obrigatória — não é opcional se o grupo usou IA em qualquer etapa: pesquisa, escrita, organização de ideias ou revisão de texto)*

Se o grupo usou alguma ferramenta de IA (ChatGPT, Claude, Gemini, Perplexity etc.) em qualquer parte do trabalho, registre **para cada uso relevante**:

| Item | O que registrar |
| :---- | :---- |
| **Ferramenta e etapa** | Qual IA foi usada e em qual parte do trabalho (ex.: pesquisa sobre o setor da organização, redação do README, organização dos requisitos, revisão ortográfica/gramatical). |
| **Motivação** | Por que o grupo recorreu à IA nesse ponto específico. |
| **Prompt(s) utilizados** | Texto exato (ou muito próximo) do que foi perguntado/pedido à IA. |
| **Resposta recebida** | Resumo ou trecho relevante da resposta da IA. |
| **Fontes consultadas e verificadas** | Se a IA citou fontes/dados, quais foram checadas pelo grupo e como (ex.: comparação com o que foi observado na visita de campo). |
| **Trechos rejeitados ou corrigidos** | O que da resposta da IA foi descartado, editado ou corrigido manualmente, e por quê. |
| **Justificativa da escolha final** | Por que o grupo manteve, adaptou ou rejeitou o que a IA sugeriu. |
| **Reflexão crítica** | Limites, vieses ou erros identificados no uso da IA nessa etapa (ex.: informação desatualizada, alucinação, generalização incorreta sobre o tipo de organização). |

*Se o grupo não usou nenhuma ferramenta de IA, declare isso explicitamente nesta seção.*

---

## Critérios Atitudinais (20%)

**Estes critérios NÃO constam explicitamente como item de entrega no README.** Eles são avaliados por meio de **Avaliação 360º entre os integrantes do grupo** (cada membro avalia os colegas de equipe) e, no caso da Colaboração, também pela **colaboração equilibrada no histórico de commits** do repositório GitHub — não pela leitura do restante do repositório nem pela apresentação:

- **Participação (5%):** envolvimento nas discussões técnicas e nas decisões do grupo.  
- **Comprometimento (5%):** cumprimento de prazos e responsabilidades assumidas.  
- **Colaboração (5%):** respeito às contribuições dos colegas, cooperação na construção do projeto e colaboração equilibrada no histórico de commits do repositório GitHub.  
- **Autonomia (5%):** busca independente de soluções e proposta de melhorias.

---

## Resumo dos Pesos

| Dimensão | Peso total |
| :---- | :---- |
| Conceitual (contexto, requisitos/regras, modelagem, justificativa técnica) | 30% |
| Procedimental (requisitos, fluxogramas, dicionário de dados, DER) | 50% |
| Atitudinal (participação, comprometimento, colaboração, autonomia) | 20% |

**Entrega final:** README.md completo \+ DER \+ Dicionário de Dados em HTML (com exceção dos cursos GTI) anexado no repositório GitHub do grupo.

&nbsp;
