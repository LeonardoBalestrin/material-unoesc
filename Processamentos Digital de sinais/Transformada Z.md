- Ferramente de análise de filtros Digitais
	- FIR
	- IIR
Transformada de Fourier é um caso especifico dentro da Transformada Z 
na pratica é para transformar um sinal discreto em um sinal Continuo(de frequencia)

#### USO
usos analiticos tem mais facilidade de se observar pela transformada Z

#### Conceito
na pratica é bem parecido com a transformada de fourier, um somatório com uma exponencial complexa 
$$
X(z) = \sum^\infty_{n=0} X[n]z^{-z}
$$

No fim a transformada de um sinal discreto para frequencia se resume a uma PG(Progressão Geometrica)
$$
X(Z) = 1/({1-({a/z})})
$$
Podendo ser traduzido para 
$$
X(Z) = z/({z-({a})})
$$
Onde a é o Polo, ou seja define os zeros, porém para essa transformada não é o sinal do polo que define a estabilidade ou instabilidade
- o critério de estabilidade no plano Z é módulo de "a" se a for menor que 1, o sinal é estavel, em 1 é o limiar, e maior que 1, gera instabilidade.

#### Transformada Inversa
 com os termos 
$$
y[n] = a_1y[n-1]+a_2y[n-2] + b_0x[n]
$$
obtemos o diagrama de blocos [[Transformada Z aplicada.excalidraw]]
E podemos obter a transformada inversa
$$ 
\begin{align}
Y[Z] = a_1Y[Z] *z^{-1} +a_2Y[Z] *z^{-2} +b_0*X[Z] 
\\ 
Y[Z] (1-a_1Z^{-1}-a_2Z^{-2}) = b_0X[Z]
\end{align}
$$
Resultando na Função de Transferência
$$ 
H(Z) = {Y(Z)/X(Z)} = b_0/{1-a_1Z^{-1}-a_2Z^{-2}}
$$