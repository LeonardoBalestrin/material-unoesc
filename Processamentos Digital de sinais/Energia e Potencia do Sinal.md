### Energia 
Integração do sinal num período de tempo equações relacionadas

$$
 F(t)=A*sen(2*\pi*Ft+\theta)
$$
##### Codigo Matlab exemplificando
```
A = 311;

f = 60;

theta=0;

t=0:1e-3:1/f;

f_t = A*sin(2*pi*f*t+theta);

stem(f_t)
plot(f_t)
```
$$
P = {1/T} \int_T F(t)^2 => 1/{1/60} \int_0^{1/60} 311 sen(2\pi*60*t)^2dt
$$
##### Codigo Matlab exemplificando
```
A = 311;

f = 60;

theta=0;

syms t;

T = 1/f;

f_t = A*sin(2*pi*f*t+theta);

P = 1/T*int(f_t^2,t,0,T);

Prms = double(sqrt(P))

```
onde:
A = amplitude
Ft = Frequência {hz}
o = Fase{rad}


### Potencia
É para casos onde o sinal é periódico e se repete infinitamente, fazendo com que a integração tenda ao infinito, portanto é necessário buscar um "Valor médio quadrático" através do período de um CICLO

$$
Px = \lim_{T\to0} 1/T \int^{T/2}_{-T/2} x(t)^2 dt
$$

