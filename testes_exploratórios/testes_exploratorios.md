## Testes manuais x automatizados 

Primeiro de tudo: testes manuais são lentos e propensos a falha.
- Ao início de um processo de desenvolvimento de uma nova funcionalidade, apesar de o tempo de desenvolvimento da funcionalidade ser linear e não cumulativo, os testes sim.
  - Ao principio que você tem mais coisas a testar, mais testes você acumula, trazendo assim mais tempo de entrega a sua demanda.
- Indo na contramão dos testes manuais, os testes automatizados apesar de custarem mais caros inicialmente, não são descartados em uma segunda rodada de testes, apenas executados novamente.
- Testes exploratórios são como testes sem roteiro, abrindo possibilidade de encontrarem possíveis problemas em meio aos testes.
- Com testes baseados em roteiro, é possível realizar a automatização desses testes atrávez dos testes dentro do código da aplicação 
- O ideal, é testar e explorar a aplicação, tendo como confiabilidade a parte da escrita do código e problemas que podem surgir durante um uso de um usuário na aplicação

--------------
Quando parar de testar?
- Deadline
- Fim dos recursos 
- Cobertura de testes atingir a meta
- Taxa de erros reduzir até um determinado patamar 
- Alpha / Beta / RC

E não existe meio de campo, entre qualidade, tempo e dinheiro, as pessoas responsáveis tem de escolher dois dos três, uma aplicação com entrega rápida porém cara, uma aplicação boa e barata porém com uma entrega maior ou então uma aplicação barata e rápida, com um padrão de qualidade baixo, muitas vezes sem a cobertura de testes o suficiente

'A meta é chegar ao ponto em que tudo que não foi feito é menos importante do que as coisas que foram feitas'

------------- 
### Planejamento de testes
  - Planeje antecipadamente
    - Caso de testes > Aqui > ?????
    - O que, como, porque? 
  - Crie sessões com tempo pré-determinado
  - Evite distrações 
  --------
  - Explorar uma funcionalidade / componente / módulo 
  - Com alguma estratégia / recurso / condição
  - Para descobrir alguma informação
    - Exemplo:
      - Explorar a regra de datas de cadastro de empregos
      - Com classes de equivalência e valores limite 
      - Para descobrir como o sistema se comportará em caso de concomitâncias de emprego

----------
### Técnicas
  - Avaliar expectativas
    - Talvez o problema seja um possível desalinhamento entre cliente e produção, uma modelagem errado ou um erro de requisito.
    - A ideia é reduzir um conjunto infinito de possibilidades a um número finito e palpável para que possam ser tratados possíveis erros.
    - Concomitância: Não se pode ser realizado mais que um processo ao mesmo tempo.
    - Classe de equivalência, por exemplo:
      - Um programa de ordenar cervejas:
        - Pedir uma cerveja
        - Pedir 0 cervejas
        - Pedir -1 cerveja
        - Pedir um lagarto
        - Pedir xzyhsdah
    - Valores limites:
      - Testar entre os valores válidos, utilizando os valores mínimos e máximos desses intervalos por exemplo:
        - Intervalo: 5000 a 10000
          - Testar: 4999, 5000 ; 10000, 10001
    - Transição de estados:
      - Que seja impossível de realizar uma ação sem a transição, um exemplo:
        - Não deveria ser possível empurrar um interruptor pra baixo após já tê-lo empurrado, sua unica ação possível deveria ser empurra-lo para cima.
    - Array Ortogonal:
      - Site para testar combinações de variáveis de teste:
        - 'https://pairwise.teremokgames.com/4s8/'