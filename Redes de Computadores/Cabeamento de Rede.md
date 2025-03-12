### Conectividade
- Entidade PAR, um lado da conexão deve ser compatível com o outro através de uma forma de conexão
- Formas de conexão
	- Interface serial ou paralela, onde serial transmite bit a bit num canal, enquanto paralela envia todos os bits por vez por diversos canais
	- rx -> tx, um "pino" transmissor e um "pino" receptor

### Canais de comunicação
oferecem veículos de comunicação de dados
	meio: cabo fibra optica, wifi etc
Oferecem largura de banda
	quantos Dados são transmitidos por segundo em bits(Mb,Gb), diferente do armazenamento(MB,GB)
tipos de canais
	Digital: utilizado na leitura de sinal binario, sinal digital de multiplexadores e etc
	Analógico: canais de rede eletrica principalmente
	Fluxo de dados: é como "andam" e por consequencia como chegam estes sinais para serem lidoos e entendidos

### Problemas
Interferências externas: Ruidos principalmente eletromagnéticos
cross talk: um cabo de rede gerando indução magnética, atenuando/anulando sinal

### Padronização de projeto
Órgãos internacionais publicam padrões para garantir performance e vida util, uma das tecnicas comuns é o aterramento
órgãos: IEEE, ISO, ANSI, EIA

### Cabeamento estruturado
estruturação física para evitar problemas, boas praticas e hábitos para aplicação de infraestrutura

### Meios físicos

Fibra ótica, imune a indução eletromagnética, tem, o limite de velocidade hoje é dado pelos equipamentos de comunicação, necessita de conectores ópticos precisos, muito frágil ao manuseio e existem dois métodos, multimodo e monomodo, onde não é possivel interagir com os 2 simultaneamente, portanto onde ja existe fibra óptica, deve-se tomar cuidado com qual método está utilizado naquele cabo.

Par trançado, pode ser blindado(STP) blindagem externa do cabo , ou não blindado(UTP) sem blindagem, categorias 1 a 8; Propriedades: Flexível, requer conector plástico, e vai até 40Gbps e é suscetível a interferência
