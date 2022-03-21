# Avaliação prática 2 - Projeto de desenvolvimento 1 (PD1)


De seguida são apresentados os vários projetos para consolidação dos conceitos básicos de criptografia. O relatório final deverá ser colocado na área do Grupo no github até ao dia 02/05/2022, na subdiretoria "AP2-PD1".
A apresentação e discussão do trabalho será posteriormente marcada em data/hora a indicar.

## Data e horário de apresentação do trabalho

Data e hora: A indicar

+ Grupo 1 - 
+ Grupo 2 - 
+ Grupo 3 - 
+ Grupo 4 - 
+ Grupo 5 - 
+ Grupo 6 - 
+ Grupo 7 - 
+ Grupo 8 - 
+ Grupo 9 - 
+ Grupo 10 - 
+ Grupo 11 - 
+ Grupo 12 - 
+ Grupo 13 - 
+ Grupo 14 - 


## Avaliação do PD1

A avaliação do PD1 será efetuada entre 0 e 20 valores. Quem entregar antes da data limite tem uma valorização de 1% na sua nota por cada dia de antecipação.

----

## 1. Projetos do tipo 1 - Encriptação homomórfica

A encriptação homomórfica é uma forma de encriptação que permite efetuar operações sobre os dados cifrados, sem que seja necessário decifrá-los primeiro, garantindo a privacidade desses dados. 

É um conceito que pode parecer uma paradoxo (ou, por vezes, mágico), já que o que temos visto nas aulas até agora, é que para fazer operações sobre dados cifrados, tem de os decifrar primeiro. Mas assim que decifrou os dados, a sua privacidade está comprometida.

A encriptação homomórfica começa a ter algumas aplicações, mas a que nos interessa é a potencial aplicação que pode ter num sistema de voto eletrónico, de forma a garantir aceder a resultados provisórios (através da encriptação homomórfica) antes de decifrar todos os boletins de voto.

Vamos tomar por exemplo um sistema muito simples de votação eletrónica em que:

+ Existem boletins de voto com diferentes opções de votação, sendo possível votar entre zero e o número máximo de opções que forem permitidas nesse boletim;
+ Todos os votos são cifrados com a chave pública do sistema de voto;
+ A operação de votação tem como input o número de votos que o votante representa, o boletim de voto, assim como as opções em que vota. No resultado da operação de votação, o boletim de voto já vem cifrado.
+ No final da votação todos os votos são decifrados com a chave privada do sistema de voto, e é apresentado o resultado da votação, com o número de votos por cada opção, assim como o número total de eleitores que participaram na votação e o número total de votos que representam.

Na primeira parte do seu trabalho pretende-se que implemente em python (versão 3) este sistema de votação muito simples, e onde se espera que explique as várias decisões tomadas em termos de estruturas de dados, operações existentes e bibliotecas utilizadas.

Adicionalmente, para tornar mais simples o exemplo de uma votação com dezenas/centenas de milhar de eleitores, pretende-se que disponibilize uma operação que vote automáticamente e de modo aleatório nas várias opções do boletim de voto. Esta operação deverá ter como input, o boletim de voto, o número de votantes e o máximo de votos que cada um representa (entre outros que ache necessários), e a partir daí votar aleatóriamente por cada votante (gerando também aleatoriamente o número de votos que cada votante representa, assim como o número de opções em que vota).

Numa segunda parte do seu trabalho pretende-se que **adicione** (note que é adicionar e não substituir) encriptação homomórfica ao sistema de votação, e para tal pode utilizar a biblioteca indicada mais abaixo, consoante o número do seu grupo.

O que se pretende com a adição da encriptação homomórfica, é que o sistema de votação passe a ter as seguintes funcionalidades adicionais:

+ Operação de validação do voto, que sem decifrar o voto permite que o sistema de votação verifique que o boletim de voto não tem mais opções assinaladas do que o número máximo de opções que forem permitidas nesse boletim. Esta operação será efetuada após a operação de votação, sendo independente da mesma;
+ Operação de obtenção dos resultados provisórios da votação, que será obtida no final da votação antes de decifrar todos os boletins de voto. O que se pretende é que através da encriptação homomórfica, que é muito mais rápida do que a decifra do boletim, obter os resultados provisórios, que se espera que sejam corroborados pela decifra dos boletins.

Note que se for necessário, deve alterar a operação de voto automático (ou fazer outra operação) de modo a englobar a adição da encriptação homomórfica.

Numa terceira parte do seu trabalho pretende-se que calcule e compare o tempo necessário para obter os resultados provisórios (por encriptação homomórfica) e os resultados definitivos (por decifra dos boletins de voto). No relatório deve fazer a comparação para 1 voto, 100 votos, 1.000 votos, 5.000 votos, ... (até que tenha resultados que permita conseguir estabelecer uma relação entre o tempo necessário para obter resultados provisórios e definitivos).

### 1.1 Grupos (e bibliotecas a utilizar)

+ Grupo 6 - [Esquema de encriptação homomórfica de Pallier](https://en.wikipedia.org/wiki/Paillier_cryptosystem) (biblioteca [phe](https://coderzcolumn.com/tutorials/python/paillier-homomorphic-encryption-phe) do python);
+ Grupo 7 - Biblioteca [Pyfhel](https://github.com/ibarrond/Pyfhel) (PYthon For Homomorphic Encryption Libraries). Recomenda-se que para perceber o seu funcionamento genérico, veja os vários exemplos, entre os quais o [HelloWorld](https://github.com/ibarrond/Pyfhel/blob/master/examples/Demo_HelloWorld.py).
+ Grupo 9 - Biblioteca [TenSEAL](https://github.com/OpenMined/TenSEAL). As operações são sobre vetores, o que poderá ser interessante no caso de ver um boletim de voto como um vetor.

-----

## 2. Projetos do tipo 2 - Cofre digital

O objetivo deste projeto é disponibilizar um serviço de cofre digital, garantindo que os documentos lá depositados só são acedidos pelos seus titulares.

O cofre digital tem as seguintes operações para o exterior:

+ depositar documento (qualquer tipo de documento), sendo que o depositante tem que identificar quem lhe pode aceder. Como resultado é devolvido ao depositante o hash do documento depositado e a chave de decifra do mesmo, cifrada com a chave pública do depositante. Caso o depositante identifique que o documento só pode ser acedido por várias pessoas em conjunto (n pessoas de um conjunto de m pessoas, com n <= m), essa chave de decifra é partida pelas m pessoas (utilize o esquema de Shamir para partilha de segredo que iremos ver numa das próximas aulas teóricas) e fornecida a cada uma, cifrada com a chave pública de cada uma.
+ fornecer documento, desde que seja pedido pelo(s) depositante(s) que lhe podem aceder, e fornecida a chave correta de decifra (já decifrada pela chave privada do depositante).

Internamente, e como atua como fiel depositário do que lhe é confiado, o cofre digital gera a hash do documento e cifra-o, guardando apenas o par (hash, documento cifrado). A chave de cifra é única para cada documento e não é guardada, mas é devolvida ao(s) depositante(s), conforme descrito na operação de depositar.
Para fornecer o documento, o cofre digital tem que receber a chave de decifra (ou as várias componentes da mesma, caso só seja possível aceder por vários depositantes em conjunto), e só devolve o documento original caso o consiga decifrar. No caso de receber várias componentes da mesma, deve existir um mecanismo que permita que os vários depositantes forneçam a sua componente da chave sem necessitarem de a mostrar aos restantes depositantes.

### 2.1 Grupos (e linguagens a utilizar)

Este projeto deve ser realizado pelos seguintes grupos:

+ Grupo 11, em Java, utilizando o _provider_ da BouncyCastle;
+ Grupo 3, em Java, utilizando o _provider_ da Sun, por omissão;
+ Grupo 1, em Python (versão 3);
+ Grupo 8, em Javascript (ou outra linguagem à escolha, que não Java ou Python).

No relatório espera-se que explique as várias decisões tomadas em termos de estruturas de dados, operações existentes e bibliotecas utilizadas. Indique também de que modo é possível instalar e utilizar o código que desenvolveu.



-----

## 3. Projetos do tipo 3 - JSON Web

JOSE (JSON Object Signing and Encryption), JWT (JSON Web Token), JWS (JSON Web Signature), JWE (JSON Web Encryption), JWK (JSON Web Key) e JWA (JSON Web Algorithms) são especificações cada vez mais utilizadas no âmbito das técnicas criptográficas. Mas afinal o que são e o que se pode fazer com elas?

É a esta pergunta que cada conjunto de dois grupos, indicados abaixo, vão ter que responder, incluindo a sua estrutura e exemplos da sua utilização. 

O resulado deste projeto é:

+ um relatório técnico que permita a qualquer um dos vossos colegas ficar a conhecer estas especificações, saber quando devem ser utilizadas e para que fins, para além de indicar bibliotecas e incluir código que permita iniciar rapidamente a sua utilização;
+ uma apresentação de 40 minutos, efetuada por cada conjunto de dois grupos.

### 3.1 Grupos (e linguagens)

Este projeto deve ser realizado pelos seguintes grupos, em conjunto:

+ Grupo 2 e Grupo 4 - Java;
+ Grupo 5 e Grupo 10 - Javascript/Node.js;
+ Grupo 12 e Grupo 13 - Python (versão 3);
 
