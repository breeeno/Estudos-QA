### Automação de testes
- O que é testar?
  - É verificar se o comportamento de determinado objeto está de acordo com o esperado.
- Testes de unidade?
  - Seu objetivo é encontrar falhas de funcionamento dentro de uma pequena parte do sistema, teste normalmente feito por programadores 
  - Normalmente são feitos usando ferramentas e libs de diferentes linguagens, é variável a cada sistema
- Testes de integração:
  - Normalmente são feitos pelos programadores e a intenção dele é testar a comunicação entre os componentes 
- Testes de sistema:
  - Executar e testar o sistema sob o ponto de vista do usuário 
  - Testes dessa natureza normalmente seguem um documento de especificações da aplicação
- Testes de aceitação:
  - Executar o sistema sob o ponto de vista de um usuário final, varrendo as funcionalidades em busca de possíveis falhas em relação aos objetivos originais.
- Testes Alfa:
  - Executar o sistema de forma não planejada, apenas por um pequeno grupo de pessoas
- Testes Beta:
  - Executar o sistema de forma não planejada, a diferença entre esse teste e o teste alfa são as proporcões. Um sistema beta tem um acesso maior e o as pessoas são pessoas normalmente desconhecidas que não participarar de nenhuma forma do desenvolvimento.
- Testes de regressão:
  - Reexecutar testes após alterações serem realizadas no sistema.

-------------
### Caixa branca e caixa preta
- Caixa branca: 
  - Na hora de testar, você testa avaliando o código em sí
- Caixa preta:
  - Você não observa o código, e sim entradas e saídas, um teste "aberto"
- Teste estático:
  - Analisar o código sem executá-lo e verificar se as boas práticas adotadas estão sendo obedecidas
- Teste dinâmico:
  - Validar o sistema através da sua execução.

-----------
### O que testar 
- Teste de funcionalidade:
  - Validar que as funções estão funcionando como o planejado 
- Testes de desempenho:
  - Validar o desempenho do sistema no que diz a respeito ao seu tempo de resposta para determinadas operações 
    - Ferramenta útil: .JMETER
- Teste de usabilidade:
  - Valida aspectos que envolvem a experiência de um usuário utilizando um sistema.
- Teste de segurança:
  - Validam a proteção do sistema contra invasões ou acesso não autorizado a informações
- Teste de portabilidade:
  - Valida o sistema em diferenças plataformas e dispositivos
- Teste de stress:
  - Validam o comportamento do sistema em condições extremas.

