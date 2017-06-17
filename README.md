Deadlock é um problema que temos em sistemas onde mais de um processo tenta executar um determinado evento, porém este evento somente aceita um processo por vez, assim formando gargalos e erros nos sistemas.
Um exemplo prático para um caso se Deadlock é quando mais de um processo de gravação em uma base de dados tenta utilizar uma mesma tabela, sendo assim caso o processo 1 demore para processar o processo 2 entra em conflito, assim acontecendo um Deadlock.

As condições para acontecer um Deadlock são:
- Quando todo recurso está alocado a um processo único, isso é chamado de Exclusão Mútua.
- Quando processos que já estão processando um evento e abrem uma nova chamada para mais eventos, isso é chamado de Posse e Espera.
- Quando um evento é previamente reservado para um processo, outro processo não pode forçar sua tomada, isso é chamado de Não Preempção.
- Quando vários processos do mesmo ciclo utilizam o mesmo fluxo de eventos, assim bloqueando a chamada seguinte, isso é chamado de Espera Circular.

Para correção de um Deadlock no caso de sistemas seria uma boa prática colocar as requisições em uma fila de processos, onde cada chamada tem sua vez, assim neutralizando o gargalo de chamadas que um evento único pode sofrer.
