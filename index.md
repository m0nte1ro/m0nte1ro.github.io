# Desenvolvimento de Jogos

Esta página web irá servir como Caderno Digital para registar e acompanhar os projetos realizados, bem como dar a conhecer o processo de realização e o estado dos mesmos.
## Introdução do Primeiro Projeto

O primeiro projeto desta unidade curricular, circula à volta da criação de um ou mais níveis de jogo originais partindo de um GameKit à nossa escolha. 
Como tal, o GameKit escolhido foi o Karting MiniGame devido à sua modularidade, flexibilidade e devido a ser o jogo mais acentuado na realidade o que facilita a criação de novos níveis. 

## Fases de Desenvolvimento
### Primeira Fase

- O primeiro passo a tomar foi escolher um layout para a pista. Inicialmente decidi tentar improvisar um layout aleatório, mas o design simplesmente não funcionava, tanto visualmente, como na prática. 
![Design Falhado](https://raw.githubusercontent.com/m0nte1ro/m0nte1ro.github.io/main/assets/primeiroProjeto/2.%20Tentativa.PNG)

- Após perceber que o design não funcionava decidi tentar recriar a pista de Montalegre.
![Fase Inicial](https://raw.githubusercontent.com/m0nte1ro/m0nte1ro.github.io/main/assets/primeiroProjeto/3.%20Plano.png)

- De forma a ter uma de referência de escala, decidi criar uma reta no Unity que achei que fosse de uma dimensão apropriada, resultando num total de 17 'track pieces'. Uma vez obtido um valor de referência foi só fazer uma regra de 3 simples. Se a reta mede 170 px (valor exemplificativo) cada 'track piece' são 10px. Abaixo podemos ver um exemplo da escala em funcionamento.
![Escala](https://raw.githubusercontent.com/m0nte1ro/m0nte1ro.github.io/main/assets/primeiroProjeto/4.%20Estrutura.png)

### Segunda Fase
- Após a fase de planeamento estar terminada, bastou apenas recriar a pista no Unity.
![Pista](https://raw.githubusercontent.com/m0nte1ro/m0nte1ro.github.io/main/assets/primeiroProjeto/5.%20Pista.PNG)

- Uma vez recriada a pista é necessário adicionar os objetivos, de forma a adicionar dificuldade ao jogo. Neste caso decidi optar por implementar um objetivo de voltas, bem como um objetivo adicional de 3 checkpoints que dão ao jogador 5 segundos a mais. De notar ainda a adição das lombas que para além de reduzir a velocidade do jogador, dificulta a fazer as curvas.
![Pista com Meta](https://raw.githubusercontent.com/m0nte1ro/m0nte1ro.github.io/main/assets/primeiroProjeto/6.%20Checkpoints%20-%20Meta%20-%20Lombas.PNG)

- De forma a concluir esta fase foi necessário terminar o design do nível. Tal como a pista de Montalegre, parte da pista tem um cenário mais urbano (edifícios de apoio) e a outra parte um cenário mais rural.
![Pista com Decoração](https://raw.githubusercontent.com/m0nte1ro/m0nte1ro.github.io/main/assets/primeiroProjeto/7.%20Level%20Design.PNG)

### Terceira Fase
- Dando como concluído o design do nível foi necessário fazer algumas alterações ao código. Neste caso só alterei o 'Game Flow Manager' do Game Manager.
![Game Manager](https://raw.githubusercontent.com/m0nte1ro/m0nte1ro.github.io/main/assets/primeiroProjeto/8.%20Game%20Manager.PNG)

- O objetivo das alterações foi poder adicionar condições de fim de jogo: se o utilizador abandonar a pista, o mesmo perde; se o utilizar pressionar uma tecla à escolha, este dá restart à corrida.
![Enumerator](https://raw.githubusercontent.com/m0nte1ro/m0nte1ro.github.io/main/assets/primeiroProjeto/8.1.%20Enum.PNG)
![Condicoes](https://raw.githubusercontent.com/m0nte1ro/m0nte1ro.github.io/main/assets/primeiroProjeto/8.2.%20Condicoes.PNG)
![Game End](https://raw.githubusercontent.com/m0nte1ro/m0nte1ro.github.io/main/assets/primeiroProjeto/8.3.%20Game%20End.PNG)

- Por fim, foi necessário alterar os valores de referência dos controlos do carro. Abaixo podemos ver os valores iniciais e os valores finais.
![Valores Iniciais](https://raw.githubusercontent.com/m0nte1ro/m0nte1ro.github.io/main/assets/primeiroProjeto/9.%20Valores%20Refer%C3%AAncia%20do%20Kart.PNG)
![Valores Finais](https://raw.githubusercontent.com/m0nte1ro/m0nte1ro.github.io/main/assets/primeiroProjeto/9.1.%20Valores%20Finais%20do%20Kart.PNG)


## Segundo projeto da cadeira

O segundo projeto da cadeira baseia-se à volta da criação de um jogo de fantasia 2D, inspirado por jogos como Zelda e Pokémon, chamado 'The Legend of Talion'. Este jogo foi desenvolvido de raíz por mim e pelo Bruno Dias, sendo que eu fiquei responsável pela implementação das ideias do Bruno. 

### Sinopse

Talion, um escravo e rato de laboratório de uma família de magos nobres, escapa e embarca numa aventura para parar Argonath, que tenta trazer o mundo para uma nova era
de trevas.

### Narrativa

Antes de começar a codificar o jogo, primeiro foi decidido o mundo e história que irão levar à contextualização dos eventos no jogo. Criar o mundo foi simples pois um dos membros do grupo, Bruno Dias, já tinha várias ideias em mente. Esse mundo seria um de fantasia, com magia, armas místicas e bestas fantasmagóricas. Mas este mundo na realidade passa-se milhares de anos no passado, quando todos os continentes estavam unidos na Pangeia. No entanto, um evento apocalíptico ocorre que leva à separação dos continentes e a morte da magia no mundo, que leva à nossa realidade no presente. Apesar destes detalhes não afetarem a história, torna o mundo onde a história acontece possivelmente mais interessante e traria a chance de criar sequelas e spinoffs no mesmo mundo, mas com personagens diferentes. 
A história que planeamos para o jogo, segue Talion, um escravo e rato de laboratório para uma família de magos nobres liderada pelo patriarca Argonath para testarem experiências mágicas. Graças às experiências feitas, Argonath “renasceu” como um novo ser todo poderoso. Nesse mesmo dia, Talion consegue escapar graças à espada lendária Mithrandir que Argonath tinha obtido há muito tempo atrás. Mesmo com os anos de desuso e ferrugem na espada, Talion consegue manter-se na luta. Não é o suficiente e ele é quase morto, mas milagrosamente consegue sobreviver e fugir. 
O jogo em si começa após a fuga do Talion, quando ele chega a Gondolin, uma pequena aldeia. Talion recebe um pedido de ajuda de um dos aldeões após o ver com a espada, que leva ao início da história do jogo. Este descobre que tem de explorar o mundo à procura de artefactos que sejam capazes de restaurar a espada, matar bestas a aterrorizar aldeões e vingar-se dos magos que o torturaram. O jogo em si serve como uma demo para o que seria o jogo completo, sendo que não foi considerado planear mais para além do básico para servir de base para o jogo. 
Uma das ideias que não foi implementada no projeto é que as ações do Talion levariam ao apocalipse mencionado anteriormente, mas foi decidido optar por uma história mais tradicional inspirada pelo mundo de Senhor dos Anéis e os jogos da SNES que serviram de inspiração. 

