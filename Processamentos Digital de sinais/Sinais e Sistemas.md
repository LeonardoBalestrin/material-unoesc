### SINAIS
- são grandezas mensuradas em função de outra, 
Notação de [[sinais analógicos|sinais discretos ou digitais]], no *Matlab* é interessante utilizar a função *stem* para ver sinais discretos, já que o *plot* mascara deixando o gráfico mais ajeitadinho

$$
x[n],x \in \Bbb Z
$$
$$
x[n] = x_a[nT],n \in \Bbb Z
$$
- **Amostra unitária**
$$
\delta[n] = \begin{cases} 0, & n \neq 0 \\ 1, & n = 0 \end{cases}
$$
	são casos importantes onde posso desloca-los adiantando-os no tempo, ou nas amostras 
- **Sequências Básicas**
	1. cosseno e seno
$$
x(t)=A*cos(\omega t+\theta)
$$
onde  $$\omega t=2\pi F$$ e se for uma frequência discreta será rad/amostras e não pelos segundos, ou $$x(n) = A*cos(\omega n+\theta) $$ onde $$ \omega c = \omega d* Fs 
 $$
### SISTEMAS
- são amalgamas de componentes que tenham uma entrada, um processamento e uma saída
- onde os componentes processam/modificam *sinais*