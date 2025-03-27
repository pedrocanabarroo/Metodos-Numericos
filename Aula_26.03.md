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
Encontrando a raiz de $A_S=\frac{1}{2}r^2(\theta-sen\theta)$ com $r=1$ e $A_s = 3.5$.

# Código #
from scipy.optimize import fsolve
import numpy as np

r = 1
As = lambda x: 0.5*r**2*(x-np.sin(x))-3.5

sol = fsolve(As, 1)
print (sol)

## Exemplo 2.1.6

A equação $f(x)=e^x-sen(x)-2=0$ pode ser escrita como $e^x=senx+2$ então, esboçando os gráficos de $f_1(x)=e^x$ e $f_2(x)=senx+2$, observamos que 
a raiz procurada está entre  $0.5$ e $1.5$, como pode ser visto no gráfico a seguir.

# Código #
import numpy as np
import matplotlib.pyplot as plt
x = np.linspace(0,2,51)
y1 = np.exp(x) 
y2 = np.sin(x) + 2
plt.plot(x,y1)
plt.plot(x,y2)
