
# Sistema tradicional vs Sistema reativo

## Sistema tradicional

![alt text](image.png)

## Sistema reativo

è um sitema projetado para ser altamente responsivo, resiliente e elástico lidando de forma eficaz com solicitações e falhas, garantindo um desempenho consistente.

Sistema reativos tem uma visão de escalabilidade e resiliência aonde os componentes podem facilmente se eslaveis é ter resiliencia com serviços. No geral uma form de executar é por meio de uma arquitetura orientada a eventos.

![alt text](image-1.png)

## Manifesto reativo

- **Responsivo**:  O sistema deve responder rapidamente a todas as solicitações, mesmo sob carga.
- **Elástico**: O sistema deve ser capaz de se adaptar a variações na carga, aumentando ou diminuindo os recursos conforme necessário.
- **Resiliente**:  O sistema permance responsivo mesmo diante de falhas, garantindo que os serviços continuem disponíveis.
- **Orientado a eventos**: O sistema deve ser projetado para lidar com eventos de forma assíncrona, permitindo uma comunicação eficiente entre os componentes.

## Programação reativa

### Foco em desenvolvimento assíncrono e não bloqueante

No java para resolver o problema é utilizado um conceito semelhante ao do node do event loop. A biblioteca do java que implementa esse conceito é o [Project Reactor](https://projectreactor.io/).

Uma thread está sempre é executada no event loop, e atribuir uma tarefa a uma outra thread que está no poll de threads. Assim o event loop não fica bloqueado e pode continuar a processar outras tarefas.

![alt text](image-2.png)

### Programação funcional

A programação utilizada é a programação funcional, que é um paradigma declartivo, utilizando streams e lambdas.

### Propagação de mundaças data streams

Cada etapa gerar eventos que são processados de forma assíncrona.

### Controle de backpressure

O controle de backpressure é um mecanismo que permite que os sistemas reativos gerenciem a pressão de dados entre produtores e consumidores. Ele garante que os consumidores não sejam sobrecarregados com mais dados do que podem processar, evitando assim problemas de desempenho e falhas.

Esse conceito pode ser visualizado em serviços de mensagerias como o kafka, onde kafka tem o sistema balaceamento entre partições e consumidores.

![alt text](image-3.png)

### Programação reativa

è uma abordagem no desenvolvimento de software que se concentra em lidar a **propagação de mudanças**  em **fluxos de dados** de **forma assíncrona e não bloqueante com mecanismo de bakcpressure**, permitindo que sistema reajam automaticamente a esssas mudanças.

## Resumo

- **Sistema reativo**: Sistemas construídos de forma responsiva, resiliente, escaláveis e orientados a mensagens.

- **Programação reativa**: Paradigma de programação que reage a eventos de forma assíncrona e não bloqueante com backpressure.

- **Fluxo síncrono**: Execução sequencial de tarefas, aguardando a conclusão de cada uma antes de continuar para a próxima.

- **Fluxo assíncrono**: Execução simultânea de tarefas, permitindo paralelismo.

- **Não bloqueante**: Capacidade de um programa continuar a execução sem ser bloqueado por uma outra tarefa. No Project Reactor, o mecanismo conhecido como Event Loop otimiza o uso das threads.

- **Backpressure**: Mecanismo de controle para lidar com a discrepância de velocidade entre a produção e consumo de dados.
