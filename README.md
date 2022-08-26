# POO---Trens
Trabalho dos trens, vagões, locomotivas e garagens 
ATIVIDADE PARA ENTREGAR – SISTEMA DE COMPOSIÇÃO DE TRENS
Uma empresa ferroviária possui uma garagem onde ficam estacionados os vagões que não
estão sendo usados e outra onde ficam estacionadas as locomotivas que estão paradas. Quando
precisa montar um trem para atender uma viagem específica os vagões e a locomotiva são
selecionados entre os que estão estacionados nestas garagens. O trem completo é então
estacionado no pátio de manobras aguardando o horário do início da viagem. A partir dessa
descrição inicial, a empresa necessita de um sistema que permita organizar os trens que irão
atender as diferentes demandas de carga da empresa. Um trem é composto por uma ou mais
locomotivas e pode ou não conter vagões de carga. Tanto as locomotivas como os vagões devem
ser selecionados na ordem em que serão engatados no trem, respeitando-se as seguintes regras:
• As locomotivas devem ser as primeiras a serem selecionadas. Não é possível “engatar”
uma locomotiva após um vagão;
• O total de vagões que podem ser engatados devem respeitar as limitações do conjunto
de locomotivas (peso máximo que conseguem puxar e número máximo de vagões que
conseguem tracionar). Para o cálculo do peso máximo, deve-se considerar o peso do
vagão com carga máxima;
o Observação: a partir da segunda locomotiva engatada, a capacidade total do
conjunto de locomotivas deve ser reduzida em 10% a cada nova locomotiva
engatada. Por exemplo, suponha que todas as locomotivas tenham capacidade para
tracionar 50 vagões. Uma composição com uma locomotiva consegue tracionar 50
vagões, com duas locomotivas 90 vagões e com 3 locomotivas 120 vagões.
• Só é possível engatar uma locomotiva ou vagão por vez e sempre no final do trem. A
locomotiva ou vagão engatados deixam de estar “livres” para serem usados em outro
trem;
• Só é possível desengatar uma locomotiva ou vagão por vez e sempre do final do trem. A
locomotiva ou vagão desengatado ficam livres para serem usados em outro trem.
As informações que são mantidas em relação as locomotivas, vagões e trens são as
descritas abaixo.
Locomotiva:
• Identificador da locomotiva (int)
• Peso máximo (em toneladas) que consegue puxar (double)
• Número máximo de vagões que consegue tracionar (int)
• Referência do trem que está integrando no momento ou null se está livre
PROGRAMAÇÃO ORIENTADA A OBJETOS – 4611F-04
Prof. Dr. Rafael Garibotti
2
Vagão:
• Identificador do vagão (int)
• Capacidade máxima de carga em toneladas (double)
• Referência do trem que está integrando no momento ou null se está livre
Trem:
• Identificador do trem
• Lista de locomotivas
• Lista de vagões
Com base nas informações apresentadas, deve ser desenvolvido um sistema em linguagem
de programação Java que permita montar e desmontar trens utilizando as locomotivas e vagões
pertencentes a empresa (no início do programa deve-se inserir, automaticamente, um conjunto
de vagões e locomotivas livres nas garagens). Note que a inicialização/inserção de vagões e
locomotivas se dará pela leitura de arquivos, o qual será visto na próxima aula. O sistema deve
apresentar as seguintes opções:
1. Criar um trem
• Esta operação exige que se indique o identificador do trem e a primeira locomotiva.
A primeira locomotiva nunca pode ser removida. Para liberar esta locomotiva é
necessário desfazer o trem.
2. Editar um trem
• Inicialmente deve-se indicar o identificador do trem a ser editado. A partir de então
ficam liberadas as seguintes operações:
o Inserir uma locomotiva (informar identificador) respeitando restrições
o Inserir um vagão (informar identificador) respeitando restrições
o Remover o último elemento do trem
o Listar locomotivas livres
o Listar vagões livres
o Encerrar a edição do trem
3. Listar todos os trens já criados, isto é, todos os trens que estão no pátio de manobras
4. Desfazer um trem
• Deve-se indicar o identificador do trem. A partir de então todos seus vagões e
locomotivas devem ser liberados e o trem removido do pátio de manobras.
5. Fim
• Encerra o programa.
