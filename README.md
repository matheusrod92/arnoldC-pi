# Desafio NoBox Robotics
O desafio da 3ª fase deste processo seletivo consiste em escolher uma linguagem nunca antes programada por mim e fazer um algoritmo para calcular até o 3º decimal de PI (i.e. até 3,141). Tendo em vista a similaridade entre as linguagens de programações atuais foi dificil escolher uma que fugisse deste aspecto.. Até que encontrei um artigo com as [linguagens mais bizarras](http://www.hongkiat.com/blog/bizarre-insane-programming-languages/) e nela encontrei a **ArnoldC** que foi a escolhida realizar este desafio. Implementar o código em **ArnoldC** teve suas complicações porque é uma linguagem completamente imperativa e só possui um tipo de variavel *(16bits signed integer)*, como pi é um numero real ele teve que ser alterado para um inteiro de 4 casas.

## Com qual método calcularemos PI?
Eu escolhi o método de série infinita desenvolvido por Leibniz em 1682, que utiliza da série de Taylor na função arctan(x). Para executar tomamos x=1 e, consequentemente, temos arctan(1)=pi/4.

![Série infinita de Leibniz](https://upload.wikimedia.org/math/9/1/7/917b7776c680e8a181a59ec05913f735.png)

## E o algoritmo?
Utilizaremos de um algoritmo em javascript para mostrar como foi pensado na solução usando da série de Leibniz.

```javascript
function calculaPI(){
	//inicializa variavel de contagem de loops, quanto maior mais precisao no numero de PI
	var loops = 10000;
	//variavel que irá guardar o valor de pi
	var pi = 0;
	//variavel para manipular o divisor
	var divisor = 1;
	//loop para calcular PI
	while(loops > 0){
		pi += 1/divisor;
		//inverte o sinal de pi
		pi *= -1;
		//incremento de 2 para o divisor
		divisor+=2;
		//decremento de 1 para o loop
		loops--;
	}
	//o valor encontrado na somatória é de pi/4. por isso multiplicamos por 4
	pi *= 4;
	//imprimimos pi
	console.log(pi);
}
```
## IT'S SHOW TIME
Abaixo podemos verificar alguns exemplos sucintos das funções básicas da linguagem que foram utilizadas no algoritmo. Devemos nos atentar que toda variável quando declarada deve ser inicializada.

#### HelloWolrd.arnoldc
```
IT'S SHOWTIME
TALK TO THE HAND "Olá mundo"
YOU HAVE BEEN TERMINATED
```

#### Declarando variáveis
```
HEY CHRISTMAS TREE variavel
YOU SET US UP valorInicial
```

#### Atribuindo valor às variáveis (variavel = 10)
```
GET TO THE CHOPPER variavel
HERE IS MY INVITATION 10
ENOUGH TALK
```

#### Operações (a = b + c)
```
GET TO THE CHOPPER a
HERE IS MY INVITATION b
GET UP c
ENOUGH TALK
```

#### Estrutura de condição (if/else)
```
BECAUSE I'M GOING TO SAY PLEASE variavelBooleana
[executa se variavelBooleana for true]
BULLSHIT
[executa se variavelBooleana for false]
YOU HAVE NO RESPECT FOR LOGIC
```

#### Laço de repetição (while)
```
STICK AROUND variavelBooleana
[executa enquanto variavelBooleana for true]
CHILL
```

#### Operadores
```
+ = GET UP
- = GET DOWN
* = YOU'RE FIRED
/ = HE HAD TO SPLIT
== = YOU ARE NOT YOU YOU ARE ME
> = LET OF SOME STEAM BENNET
|| = CONSIDER THAT A DIVORCE
&& = KNOCK KNOCK
```

**YOU HAVE BEEN TERMINATED** 

## Compilando e rodando
Para compilar e executar faça o [download do ArnoldC.jar](http://lhartikk.github.io/ArnoldC.jar) e coloque na mesma pasta do código, depois execute:
```
java -jar ArnoldC.jar seucodigo.arnoldc
java seucodigo
```

## Referências
[1] PI [https://pt.wikipedia.org/wiki/Pi](https://pt.wikipedia.org/wiki/Pi)
[2] ArnoldC [https://github.com/lhartikk/ArnoldC](https://github.com/lhartikk/ArnoldC)
[3] Wiki ArnoldC [https://github.com/lhartikk/ArnoldC/wiki/ArnoldC](https://github.com/lhartikk/ArnoldC/wiki/ArnoldC)
[4] Weirdest Programming Languages [http://www.hongkiat.com/blog/bizarre-insane-programming-languages/](http://www.hongkiat.com/blog/bizarre-insane-programming-languages/)
[5] [HASTA LA VISTA, BABY :sunglasses:](https://www.youtube.com/watch?v=Hhm7aWp8gvc)