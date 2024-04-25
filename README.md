# Machine-Learning-Churn-Project
O modelo deve prever se o cliente irá cancelar ou não o serviço, vamos usar 5 modelos e comparar as métricas de cada um para estabelecermos o melhor. Os modelos usados serão **CatBoostClassifier**, **Regressão Logística**, **Redes Neurais**, **SVM** e **Árvore de Decisão**.

## Sobre a base:

- **genero**: gênero biológico do cliente (female, male)
- **idoso**: Verifica se o cliente é considerado idoso. (1 para sim e 0 para não)
- **parceiro**: Verifica se o cliente possui conjuge. (Sim, Não)
- **dependentes**: Verifica se o cliente possui dependentes. (Sim, Não)
- **tempoDeServico**: Número de meses que o cliente utiliza os serviços da Telecom.
- **ServicoTelefone**: Verifica se o cliente possui um serviço de telefone. (Sim, Não)
- **MultiLinhas**: Verifica se o cliente possui mais de uma linha em um contrato de telefone. (Sim, Não, Sem serviço de telefone)
- **ServicoInternet**: Verifica se o cliente possui um serviço de internet. (DSL, Fibra Óptica, Não)
- **ServicoSegurancaCyber**: Verifica se o cliente possui um serviço de segurança na internet. (Sim, Não, Sem serviço de internet)
- **ServicoBackup**: Verifica se o cliente possui um serviço de segurança de backup de arquivos. (Sim, Não, Sem serviço de internet)
- **SeguroDispositivos**: Verifica se o cliente possui um serviço de proteção de dispositvos. (Sim, Não, Sem serviço de internet)
- **ServicoSuporteTecnico**: Verifica se o cliente possui um serviço de suporte técnico. (Sim, Não, Sem serviço de internet)
- **StreamingTV**: Verfica se o cliente possui serviço de Streaming de canais de TV. (Sim, Não, Sem serviço de internet)
- **StreamingFilmes**: Verfica se o cliente possui serviço de Streaming de Filmes. (Sim, Não, Sem serviço de internet)
- **Contrato**: Tipo de contrato do cliente. (Mensal, 1 Ano, 2 Anos)
- **BillingDigital**: Verifica se o cliente recebe a fatura de forma digital. (Sim, Não)
- **MetodoPagamento**: Tipo de pagamento da fatura do cliente (Cheque Eletrônico, Cheque por carta, Transferência Bancária (Automática), Cartão de Crédito (Automático))
- **FaturaMensal**: Total cobrado ao cliente mensalmente.
- **FaturaTotal**: Total cobrado ao cliente.
- **NumTickets**: Número de Protocolos de Serviço (Ticket) abertos pelo cliente.
- **NumTicketsTecnico**: Número de Protocolos de Serviço de TI (Ticket) abertos pelo cliente.
- **Churn**: Verifica se o cliente cancelou o contrato de serviço e saiu da empresa de telecom. (Sim, Não)

## Sobre o CatBoostClassifier
O CatBoostClassifier funciona usando técnicas de árvores de decisão. Cat vem de categorical, pois ele consegue trabalhar com dados categóricos (sem precisar de pré-processamento) e Boost vem de Gradient Boosting, num processo em que várias árvores de decisão são construidas em sequência, com cada árvore subsequente sendo melhor que a anterior.


![catboost](https://miro.medium.com/v2/resize:fit:1400/1*W6Nn0qgu5q4QKjpAeSBXGQ.png)

## Sobre a Regressão Logística

A regressão logística funciona como uma regressão linear, porém nela queremos prever valores discretos, enquanto na linear prevemos valores contínuos. Ou seja, na regressão logística queremos fazer uma classificação, na regressão linear queremos fazer uma regressão mesmo.

![regressão logística](https://brains.dev/wp-content/uploads/2023/01/log_reg8.png)

## Sobre as Redes Neurais

As redes neurais são modelos que tentam simular o aprendizado humano. De forma simples, elas são divididas em camadas com neurônios, com todos ligados entre si. Temos a camada de entrada, as camadas ocultas e a camada de saída, o dado passa por essas camadas e vai ativando alguns dos neurônios, que no final vão passando suas saídas e na última camada retornam o resultado da rede neural.

![redes neurais](https://sites.icmc.usp.br/andre/research/neural/image/camadas_an.gif)

## Sobre o SVM

O **Support Vector Machine** é um algoritmo que pode ser usado tanto para classificação quanto para regressão. Ele busca encontrar um hiperplano que possa separar melhor os dados em diferentes classes.

![SVM](https://miro.medium.com/v2/resize:fit:786/format:webp/1*kRfvm_eGkkpRKrsUTPYYQQ.png)

## Sobre a Árvore de Decisão

A árvore de decisão é como um mapa dos possíveis resultados de uma série de escolhas relacionadas. Nesse sentido, ela começa com um único nó e vai se dividindo em possíveis resultados, estes que também se ramificam, chegando até a possível solução.

![arvore decisão](https://www.hashtagtreinamentos.com/wp-content/uploads/2022/11/Arvore-de-Decisao-1.png)

