aplicada somente em sinais periódicos, que se repetem em períodos fixos
$$
x(t) = x(t+T_0)
$$
sinais periódicos podem ser reescritos como um somatório de coeficientes e senóides.
a Série de Fourier objetiva encontrar uma forma de criar outras formas de onda através da senóide
### Representação Matlab da série de Fourier
```
%% Série de Fourier  
clear  
close  
clc  
  
%Período fundamental  
T0 = 2;  
f0 = 1/T0;  
w0 = 2*pi*f0;  
%Primeiro termo da série de Fourier  
%Expressa o valor médio do sinal periódico  
syms t  
a0 = 1/T0*(int(-2,t,0,1)+int(2,t,1,2));  
  
total_coef = 20;  
for n=1:total_coef  
   a(n) = 2/T0*(int(-2*cos(n*w0*t),t,0,1)+int(2*cos(n*w0*t),t,1,2));  
    b(n)= 2/T0*(int(-2*sin(n*w0*t),t,0,1)+int(2*sin(n*w0*t),t,1,2));  
end
```
### Representação Matemática da Série de Fourier
$$
\begin{align}
a_n = {2/T_0} * \int_{T_0} * x(t)*cos(n*\omega_0*t)dt \newline
a_n = {2/T_0} * \int_{T_0} * x(t)*sin(n*\omega_0*t)dt \newline
\end{align}
$$


> [!NOTE] Simetrias:
> Simetria impar X(t) = -X(-t) Simetria Par      X(t) = X(-t)

Espectro de Amplitude e fase