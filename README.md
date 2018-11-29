# NetMap

Trabalho de estrutura de dados

NetMap é uma rede que permite a passagem de dados entre terminais distribuídos.
Assim como a internet, NetMap é composta por roteadores que se conectam através de enlaces
que habilitam a passagem de dados pela rede.
Conectados a roteadores, estão os terminais. Cada terminal pode estar conectado a somente um roteador.
Já um roteador pode estar conectado a vários terminais.

O NetMap pode ser implementado usando um conjunto de listas encadeadas:
basicamente, implementa-se uma lista de Roteadores, onde cada célula contém os dados do roteador (nome e operadora).
Além disso, cada célula desta lista de roteadores contém uma lista encadeada indicando quais
são os roteadores conectados a ele, ou seja, representando os enlaces. Para implementar os terminais,
pode-se implementar uma lista de terminais, na qual cada terminal possui um ponteiro para o seu roteador.

Um NetMap não precisa ter todos os roteadores interligados, ou seja, a listas encadeadas que indicam quais
são os roteadores ligados a eles podem ser nulas.


# Detalhes do trabalho

Nesse trabalho, você deverá implementar estruturas com listas.
Considere que cada roteador é uma estrutura contendo os campos nome (ex.: roteador1)
e operadora do roteador (e.x., Telemar, GVT , NET, etc.), e que não há roteadores ou terminais com os mesmos nomes.
De maneira similar, considere também que os terminais são estruturas contendo os campos nome (ex.: ter1)
e localização do terminal(ex.: Vitória). O NetMap não aceita nomes compostos..

# As seguintes operações devem ser implementadas:
 CadastraRoteador(Roteador): Cadastra um novo roteador ao NetMap;

 CadastraTerminal(Terminal): Cadastra um novo terminal ao NetMap (já deve conectar o terminal a um roteador);

 RemoveRoteador(Roteador): Remover o roteador do NetMap (Note que todas as relações deste roteador com outros devem ser excluídas.);

 RemoveTerminal(Terminal): Remove o terminal do NetMap;

 ConectaRoteadores(Roteador1, Roteador2): Cria um enlace entre dois roteadores já cadastrados;

 DesconectaRoteadores(Roteador1, Roteador2): Remove o enlace entre dois roteadores já cadastrados;

 FrequenciaOperadora(operadora): Imprime o número de roteadores cadastrados de uma determinada operadora;

 EnviarPacotesDados(Terminal1, Terminal2): Verifica se é possível enviar dados, por exemplo do Terminal1 para o Terminal2. Retorna SIM se for possível e NAO caso contrário;

 MostrarTerminais(): mostrar todos os terminais e o roteador qu está conectado;

 MostrarRoteadores(): Mostrar roteadores e para cada roteador os enlaces que possui.
