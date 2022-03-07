# Aula TP - 08/Mar/2022

Cada grupo deve colocar a resposta às **perguntas** (note que pode colocar as respostas às **experiências**, mas estas não irão contar para avaliação) dos seguintes exercícios na área do seu grupo no Github até ao final do dia 22/Mar/22. Por cada dia de atraso será descontado 0,15 valores à nota desse trabalho.

## Exercícios

### Parte III: Segurança da informação

#### Experiência III.1

Durante a aula teórica desta semana, no âmbito das cifras simétricas, falámos de vários tipos de _stream ciphers_ e, vários modos de operação das _block ciphers_.

Identifique e explique quais das propriedades de segurança é que são fornecidas por essas cifras.


### Parte IV: Cifras simétricas

#### IV.1 _Stream cipher_

##### Experiência IV.1.1

O RC4 já foi uma cifra muito utilizada, nomeadamente no âmbito dos protocolos SSL/TLS e WEP, mas desde 2003 foram sendo encontradas várias vulnerabilidades pelo que na prática já é hoje pouco utilizado. 

1. Desenvolva, em python, uma aplicação linha de comando que utilize o RC4 para cifrar um ficheiro. No interface da linha de comando (CLI - _command line interface_) deve poder indicar o comprimento da chave (40, 56, 64, 80, 128, 192, ou 256 bits), a operação a efetuar (cifra/decifra), ficheiro de input e ficheiro de output.

2. Porque é que pode dizer que esta cifra não tem a propriedade de autenticidade?

##### Pergunta P.IV.1.1

O ChaCha20 é uma das duas cifras simétricas escolhidas para a encriptação dos novos protocolos de transporte, nomeadamente o TLS 1.3 (cf. [IETF RFC 8446](https://datatracker.ietf.org/doc/html/rfc8446)), embora a sua utilização seja opcional.

1. Desenvolva em python (utilizando a biblioteca [PyCryptodome](https://pycryptodome.readthedocs.io/en/latest/src/introduction.html)) uma aplicação linha de comando que utilize o Chacha20 para cifrar um ficheiro, em que o tamanho do nonce é de 12 bytes (conforme boas práticas definidas no [IETF RFC RFC 7539](https://datatracker.ietf.org/doc/html/rfc7539)).

   No interface da linha de comando (CLI - _command line interface_) deve poder indicar a chave (mas se o utilizador não a colocar, deve-lhe perguntar no inicio de execução do programa), a operação a efetuar (cifra/decifra), ficheiro de input e ficheiro de output.


#### IV.2 _Block cipher_

##### Pergunta P.IV.2.1

O AES é uma das duas cifras simétricas escolhidas para a encriptação dos novos protocolos de transporte, nomeadamente o TLS 1.3 (cf. [IETF RFC 8446](https://datatracker.ietf.org/doc/html/rfc8446)), sendo a sua utilização obrigatória, nomeadamente com tamanho de chave de 128 bits e no modo de operação GCM (i.e., AES-128-GCM).

O modo de operação GCM (_Galois Counter Mode_) é cada vez mais utilizado devido à sua performance, e combina o CTR (_Counter Mode_, visto na aula teórica) com a autenticação de Galois. O resultado do modo de operação GCM é uma sequência de bytes que contém o _IV_, _ciphertext_, e uma _authentication tag_ (utilizada para verificar a autenticação e integridade da restante sequência de bytes).

1. Desenvolva em java (utilizando os _providers_ da Sun fornecidos por omissão) uma aplicação linha de comando que utilize o AES-128-GCM (com IV de 12 bytes aleatório e diferente em cada utilização, e Tag de 128 bits) para cifrar um ficheiro.

   No interface da linha de comando (CLI - _command line interface_) deve poder indicar a chave (mas se o utilizador não a colocar, deve-lhe perguntar no inicio de execução do programa), a operação a efetuar (cifra/decifra), ficheiro de input e ficheiro de output.


##### Experiência IV.2.1

Utilizando o openssl indique qual é o comando linha que utiliza para cifrar e decifrar um ficheiro com AES-256-CBC.



