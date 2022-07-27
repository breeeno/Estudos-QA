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

-----------
### Personas
  - Persona é uma forma de tentar agir como uma outra pessoa, nesse caso, em prol de tentar testar outras maneiras de se usar a aplicação 
    - Dar um nome, um background, uma espécie de generalização, levantando as possíveis características e hábitos do personagem.
  

----------
### Soap Opera Scenarios 
  - Testes devem ser engraçados e agressivos, exagerados e condensados
  - Escrever cenários improváveis, mas possíveis
  - Possui fase design e execução separadas
  

-----------
### Tour 
  - Conceito dos testes que faz uma associação entre os testes e uma viagem a turismo, basicamente dividindo os testes em 5 áreas da cidade: 
  - Business District:
    - Guidebook Tour:
      - Atrações de bolso, nos testes, isso associa ao manual da aplicação, fazendo com que o testador siga normalmente o mesmo caminho do usuário, e problemas nessa rota normalmente tem prioridade alta na fila de resolução de problemas
    - Money Tour:
      - A razão principal porquê a aplicação existe, é uma forma de garantir que o coração da aplicação funcione corretamente.
    - Landmark Tour:
      - Associado dentro da cidade como os pontos turisticos, dentro do teste podemos dizer que seriam pontos de referencia para que você pudesse se guiar dentro do uso e de seus testes.
    - FedEX Tour:
      - Nos testes, considere ao invés de pacotes, os dados da aplicação, considere as entradas e confirme se elas estão corretas.
    - After-Hours Tour:
      - Nos horários fora do padrão da aplicação, vale-se testar essas funcionalidades e ver se ocorre o funcioamento correto delas.
    - Garbage Collector Tour:
      - Nos testes, quando verificamos interfaces, sempre procurando os menores caminhos a ela.
  - Historic District
    - Bad Neighborhood Tour:
      - Áreas que os turistas são recomendados a não entrarem, que estão infestadas de problemas, no ambiente de código, cheio de bugs, onde os testadores tem de explorar pra encontrar e nomear esses problemas
    - Museum Tour:
      - Códigos legados, dando atenção as funcionalidades que precisam de manunteção e observação
    - Pior Version:
      - Garantir que features e execuções das versões anteriores tenham sido mantidas com sucesso em refatorações.
  - Entertainment District
    - Supporting Actor Tour:
      - Testar se possíveis botões e atalhos tenham seu funcionamento correto.
    - Back Alley Tour:
      - No teste, isso é validar as funcionalidades que são menos usadas
    - All-Nighter Tour:
      - Manter a aplicação aberta e observar o comportamento dela após muito tempo. 
  - Tourism District
    - Collectors Tour:
      - Tentar mapear as funcionalidades e ir catalogando as funcionalidades.
    - Lonely Businesssman Tour:
      - Para conhecer as funcionalidades mais distantes do centro do app.
    - Supermodel Tour:
      - Testar e validar interfaces e suas responsividades.
  - Hotel District 
    - Rained-Out Tour:
      - Iniciar operações pesadas e cancela-las logo em seguida, basicamente um teste de estresse.
    - Couch Potato Tour:
      - Testar funcionalidades com os campos default e com o minimo de informações possíveis.

--------
### Outras estratégias
- Shoe test:
  - Estratégia incomum, a ideia é basicamente "espancar" o teclado com algum objeto e observar o comportamento da aplicação sobre essa ação
- Null, Zero e Vazio:
  - Passar dados nulos, vazios ou negativos para testar a validação de formulários da aplicação.
- Get one, take one:
  - Acessar a mesma instância da aplicação em dois lugares diferentes, pra ver e validar como a aplicação lida com esse comportamento.
- Bookmark:
  - A ideia aqui é testar as aplicações reutilizando as urls pra ver qual comportamento a aplicação vai ter
- Sabotagem:
  - Criar "problemas" para observar como a aplicação lida com essas ocorrências, tais como derrubar um banco, tentar realizar acessos ilegais e observar esses comportamentos.
- Ferramentas de desenvolvedor:
  - Modo desenvolvedor dos navegadores, tanto que é possível disparar eventos javascript direto no navegador, tais como:
    - ```alert:'qualquer coisa'```
  - É possível observar respostas recebidas e status code, além do html da página
  - Também é valido válidar a responsavidade do app, tanto em telas maiores quanto em telas menores
- Segurança:
  - Também é possível tentar realizar uma sql injection ao tentar passar informações no front end.