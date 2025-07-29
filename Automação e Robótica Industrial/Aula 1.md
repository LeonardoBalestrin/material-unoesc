#Glossário
1. Controlador Lógico Programável
	Sistema rígido e flexível capaz de suportar os ambientes industriais, e capaz de ser reprogramável facilitando manutenções que outrora eram muito custosas.
2. Linguagem *Ladder*
	conhecida como linguagem de contatos, é facilmente associada a lógica de contatos elétricos, como era utilizado antes de surgirem os CLPs
3. *Word*
	conjunto de 2 bytes, ou 16 bits
4. *Double word*
	conjunto de 2 words, ou 32 bits
# Usando TIA Portal

- abre o TIA
- create new project
	- Nome do projeto de preferencia cada projeto novo com um nome exclusivo
	- De aula para outra importante salvar e compactar a PASTA toda, em .zip
- Configure device para configurar o dispositivo que sera usado
	- Add new device(tela destinada para selecionar o clp utilizado)
		- Vamos usar em aula Controllers > s7-1200 > CPU 1214 DC/DC/DC > VERSÃO_CLP
		- a versão é encontrada na carcaça levantando a tampa do CLP
	- Add no canto inferior direito
	- vai abrir uma tela com muita informação
	- nesta tela ao acessar a pasta do device criado > program blocks e clicar no OB1 inicia a programação em *Ladder*
	- clicando em devices and networks acessa tela para visualizar os devices e verificar como estão as configurações de rede

## Convenções de programação ladder
#### Entradas digitais
símbolo **I**
representada com linha central e duas linhas paralelas com espaço aberto para entradas **normalmente abertas**, e linha central com duas linhas paralelas ligadas por uma barra diagonal para entradas **normalmente Fechadas**
#### Saídas digitais
símbolo **Q**
representada como uma linha e parenteses 
#### Memórias digitais
símbolo **M**
pode ser representada em codigo como entrada ou como saida

## Programando em ladder no TIA 
I0.0 -> informa criação de entrada no bit 0 do byte 0
Q0.0 ->informa criação de saida no bit 0 do byte 0
M0.0 -> informa criação de memoria no bit 0 do byte 0
TP -> seta um temporizador
MB0 -> seta uma memoria no formato *double word*
