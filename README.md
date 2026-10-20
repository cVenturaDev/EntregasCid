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

*(vale 10% — Dimensão Procedimental \- Segue o modelo do arquivo 02-03g\_Exemplo\_Dicionario\_Dados.pdf)*

Para cada entidade identificada, liste:

| Atributo | Descrição | Regra de negócio associada |
| :---- | :---- | :---- |
| *nome do atributo* | *o que ele representa* | *se houver alguma regra (obrigatoriedade, valores possíveis, etc.)* |

*Mantenha o dicionário organizado e padronizado (mesmo formato de tabela para todas as entidades).*

**Atenção à privacidade:** se forem usados exemplos de valores para ilustrar os atributos, esses exemplos devem ser **fictícios** — não utilize dados reais de clientes, fiéis, beneficiários, doadores ou funcionários da organização (nomes, CPFs, contatos etc.), mesmo que tenham sido observados durante a pesquisa de campo. Os exemplos devem apenas ser **coerentes com as operações reais** observadas.

---

## 6\. Modelagem Conceitual (Entidades, Atributos, Relacionamentos)

*(vale 7,5% na dimensão conceitual)*

- **Entidades reconhecidas:** *liste e justifique brevemente cada uma.*  
- **Atributos e classificações:** *quais atributos pertencem a cada entidade.*  
- **Relacionamentos pertinentes:** *como as entidades se conectam.*  
- **Restrições e políticas organizacionais aplicadas ao modelo.**

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
