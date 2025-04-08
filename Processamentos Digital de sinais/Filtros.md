Filtros em imagens, interagem com pixels, uma grande variação da cor em poucos pixels, então seria equivalente a uma *frequência alta* 

Filtro anti-Aliasing: filtro de entrada para transformadas de Fourier, onde é um PB(Passa baixa) onde FC(Frequencia de corte) é Aproximadamente A frequência limite do sistema(Fs/2), lembrando que Fs é a frequência do sistema.
$$FC\approx Fs/2
$$
Filtro de reconstrução: é um filtro de saída PB onde a frequência de corte FC deve ser maior que Fs
$$ FC<Fs
$$

Uma forma de criar um filtro passa baixa pelo circuito é utilizando um resistor e um capacitor de forma que a frequência de corte desejada depende de uma escolher uma resistência, através da seguinte formula:
$$
Fc=1/{2\pi RC}
$$
Normalmente, indica-se a frequência desejada, e o Capacitor, e calcula a resistência necessária, por resistores terem mais variedade.