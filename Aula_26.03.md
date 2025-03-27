# Tópico 2.1 abordado em aula
Encontrar numericamente a raiz de uma equação requer duas etapas:

1. Isolar a raiz, ou seja, encontrar um intervalo $[a,b]$ contendo uma única raíz da equação $f(x)=0$ e;

2. Refinar o intervalo que contém a raíz até atingir a precisão desejada.
# Exemplo trabalhado em aula:
Podemos utilizar uma abordagem numérica para obter soluções aproximadas de equações, vejamos por exemplo a equação $f(d) = 1.047d^3-31.415d^2+2672.369$ do exemplo descrito anteriormente. 
Dos dados do problema, podemos inferir que a solução é um número entre 0 e 20, então, calculamos valores da função nesse intervalo e tentar encontrar uma aproximação. 
Buscamos o valor de $d$ que anula a função $f$, então, observando os resultados na tabera abaixo, podemos concluir que a solução é um número entre 11 e 12 cm pois é o intervalo onde a 
função muda de sinal.

## Para Calcular, usaremos o código:
  for d in range (0,21):
   y = 1.047*d**3 - 31.415*d**2 + 2672.369
   print(d, y)

## Refinando, usaremos o código:
 for i in range(0,11):
   d = 11 + (i/10)
   y = 1.047*d**3-31.415*d**2+2672.369
   print('f(',d,')=', round(y,3))

 for i in range(0,11):
     d = 11.86 + (i/1000)
     y = 1.047*d**3-31.415*d**2+2672.369
     print('f(',d,')=', round(y,3))

## Exemplo 2.1.5
