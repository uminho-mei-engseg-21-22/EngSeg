# Avaliação prática 2 - Projeto de análise de um tema (PA)


De seguida são apresentados os vários projetos de análise de um tema. O relatório final deverá ser colocado na área do Grupo no github até ao dia 20/03/2021, na subdiretoria "AP2-PA".
A apresentação e discussão do trabalho será posteriormente marcada em data/hora a indicar.
## Data e horário de apresentação do trabalho

Data: A indicar

+ Grupo 1 - 14h00
+ Grupo 2 - 14h20
+ Grupo 3 - 14h40
+ Grupo 4 - 15h00
+ Grupo 5 - 15h20
+ Grupo 6 - 15h40
+ Grupo 7 - 16h00
+ Grupo 8 - 16h20
+ Grupo 9 - 16h40
+ Grupo 10 - 17h00
+ Grupo 11 - 17h20
+ Grupo 12 - 17h40


## Avaliação do PA

A avaliação do PA será efetuada entre 0 e 20 valores. Quem entregar antes da data limite tem uma valorização de 1% na sua nota por cada dia de antecipação.

Exemplificando:

+ o Grupo A entrega o PA no dia 10/03/2021 e tem uma avaliação de 15 valores. Como entregou 10 dias antes terá 10% de valorização, sendo a sua nota final de 16,5 valores. 
+ o Grupo B entrega o PA no dia 15/03/2021 e tem uma avaliação de 15 valores. Como entregou 5 dias antes terá 5% de valorização, sendo a sua nota final de 15,75 valores. 


## 1. Projetos de tipo 1 - Potencial de Ataque a tecnologia

O objetivo deste projeto é identificar o potencial de ataque estimado, necessário para efetuar ataque a determinada tecnologia, de acordo com a metodologia de avaliação do [Common Criteria](https://www.commoncriteriaportal.org/cc/) / ISO IEC 15408.

Não necessita de ter conhecimentos sobre o Common Criteria, mas se tiver curiosidade pode ver as seguintes apresentações:

+ <https://www.youtube.com/watch?v=ceg4hyrcHJc> - apresentação sucinta, menos técnica (recomendada);
+ <https://www.youtube.com/watch?v=PSAlyxhaf5c> - apresentação extensa, muito técnica.


O método de trabalho proposto é identificar vários cenários de ataque à tecnologia, baseado em riscos identificados, destacando a(s) vulnerabilidade(s) explorada(s) e a estimativa do potencial de ataque que é necessário para realizar os ataques.

Para estimar o potencial de ataque dos atacantes (i.e., o esforço necessário para criar o ataque), deve utilizar a metodologia identificada no anexo B.4 do documento _[Common Methodology for Information Technology Evaluation, Evaluation Methodology, Version 3.1, Revision 5, CCMB 2017-04-004](https://www.commoncriteriaportal.org/files/ccfiles/CEMV3.1R5.pdf)_ (também disponível [aqui](../Bibliografia/CEMV3.1R5.pdf)).

Esta metodologia determina quatro potenciais de ataque diferentes; Básico, Avançado-Básico, Moderado e Alto.
Para calcular o potencial de ataque necessário para explorar uma vulnerabilidade, os seguintes fatores devem ser levados em consideração:

+ a) Tempo gasto para identificar e concretizar o ataque,
+ b) Conhecimento técnico especializado necessário,
+ c) Conhecimento do _design_ e operação do alvo a atacar,
+ d) Janela de oportunidade,
+ e) Hardware / software ou outro equipamento necessário para a concretização do ataque.

Esses fatores são definidos no anexo B.4 do documento indicado acima, sendo fornecida tabela para calcular o potencial de ataque (tabela 3), assim como para classificar o potencial de ataque para explorar o cenário de ataque (tabela 4).

Notas: 

+ Para ajuda, é fornecido o ficheiro [PA.Potencial_ataque.doc](PA.Potencial_ataque.doc) com tabelas para cálculo e justificação do potencial de ataque (secção I). Não se esqueça de adicionar contextualização da tecnologia a analisar e seus riscos, assim como uma conclusão.
+ Grupos com mais de três elementos, deverão adicionalmente identificar contramedidas relevantes para cada um dos cenários de ataque, conforme secção II do ficheiro [PA.Potencial_ataque.doc](PA.Potencial_ataque.doc).


### 1.1 Tecnologia a determinar potencial de ataque

+ Grupo 1 - Potencial de ataque à tecnologia de OTP (_One Time Password_) por _Push Notification_ e por SMS.
+ Grupo 5 - Potencial de ataque à tecnologia de autenticação com Cartão de Cidadão.
+ Grupo 8 - Potencial de ataque à tecnologia de autenticação com Chave Móvel Digital.
+ Grupo 10 - Potencial de ataque à tecnologia de identificação de pessoas físicas, através de procedimentos de identificação à distância com recurso a videoconferência - para contextualização pode ler o [Despacho 154/2017 da Entidade Supervisora nacional, de 5 de dezembro](https://www.gns.gov.pt/media/10442/Despacho-154-2017-ID-Videoconferencia.pdf).
+ Grupo 12 - Potencial de ataque à tecnologia de criação de assinaturas eletrónicas à distância, com gestão por um prestador qualificado de serviços de confiança em nome do signatário - para contextualização pode ler o [ETSI TS 119 432 V1.2.1 (2020-10)](https://www.etsi.org/deliver/etsi_ts/119400_119499/119432/01.02.01_60/ts_119432v010201p.pdf), em especial as secções 4 e 5.
+ Grupo 14 - Potencial de ataque à tecnologia de identificação de pessoas físicas, através de procedimentos de identificação à distância com recurso a sistemas biométricos automáticos de reconhecimento facial - para contextualização pode ler o [Despacho n.º 2705/2021 da Entidade Supervisora nacional, de 11 de março](https://www.gns.gov.pt/media/14878/despacho-2705-2021-sb-pt.pdf).


## 2. Projetos de tipo 2 - Sistema Gestão de Segurança de Informação

A [família de standards ISO/IEC 27000](https://en.wikipedia.org/wiki/ISO/IEC_27000-series) (ou ISO27K) é constituída por standards de segurança de informação publicados conjuntamente pela _International Organization for Standardization_ (ISO) e pela _International Electrotechnical Commission_ (IEC). 

Esta família de standards fornece recomendações de melhores práticas para gestão de segurança de informação, no contexto integrado de um Sistema de Gestão de Segurança de Informação (SGSI) - _Information security management system_ (ISMS) -. O seu âmbito é vasto, sendo aplicável a todo o tipo de entidades, independentemente do seu tamanho. 

Caso tenha curiosidade sobre esta família de standards, recomenda-se que veja:

+ os vários episódios da série da Clearsec, que começam em <https://www.youtube.com/watch?v=0gzjTD1tdOw> (em francês, com legendas em inglês);
+ <https://www.youtube.com/watch?v=ltEEZLOUP90> (em inglês).

### 2.1 Regulamento eIDAS

A [Comissão Técnica _Electronic Signatures and Infrastructures_ (ESI) do ETSI](https://www.etsi.org/committee/esi) publica standards europeus no âmbito das assinaturas digitais e serviços de confiança relacionados (em especial, no contexto do [Regulamento eIDAS](https://eur-lex.europa.eu/legal-content/PT/TXT/PDF/?uri=CELEX:32014R0910&from=ga) - Regulamento (UE) n.o 910/2014 do Parlamento Europeu e do Conselho
de 23 de julho de 2014
relativo à identificação eletrónica e aos serviços de confiança para as transações eletrónicas no
mercado interno e que revoga a Diretiva 1999/93/CE), para fornecer confiança e segurança às transações eletrónicas.

O objetivo deste projeto é analisar e relacionar os requisitos nos standards ETSI sobre um determinado tema, com as recomendações de melhores práticas  efetuada por um standard da família ISO/IEC 27000.

Notas: 

+ Não se esqueça de adicionar contextualização do(s) tema(s) a analisar, assim como uma conclusão onde reflete sobre a adequação dos requisitos do ETSI face às recomendações do ISO.
+ Grupos com mais de três elementos, deverão adicionalmente identificar (e justificar) qual dos requisitos do ETSI e boas práticas do ISO analisados, deverão ser vistas como requisitos a serem seguidos no âmbito de votações eletrónicas _online_.

#### 2.1.1 Temas a analisar e relacionar 

Os temas a analisar e relacionar serão entre o [ETSI EN 319 411-2 V2.4.1 (2021-11) - Electronic Signatures and Infrastructures (ESI);
Policy and security requirements for Trust Service Providers issuing certificates; Part 2: Requirements for trust service providers issuing EU qualified certificates](https://www.etsi.org/deliver/etsi_en/319400_319499/31941102/02.04.01_60/en_31941102v020401p.pdf) e o [ISO/IEC 27002:2013 - Information technology — Security techniques — Code of practice for information security controls](https://trofisecurity.com/assets/img/ISO-IEC_27002-.pdf). Se o link para o ISO 27002 não esiver ativo, podem encontrar o documento [aqui](ISO27002_2013.pdf).

Temas a analisar por grupo:

+ Grupo 2 - Política de segurança de informação (_Information Security Policy_), Recursos humanos (_Human resources_), Gestão de incidentes (_Incident management_)
+ Grupo 6 - Controlo de acessos (_Access control_)
+ Grupo 9 - Segurança ambiental e física (_Physical and environmental security_), Controlos criptográficos (_Cryptographic controls_) 
+ Grupo 11 - Segurança de operações (_Operation security_) - para grupo com 5 elementos, se existir
+ Grupo 13 - Gestão de ativos (_Asset Management_), Gestão de continuidade de negócio (_Business continuity management_) 


### 2.2 Novo Cartão de Identidade europeu

O [Regulamento (UE) 2019/1157 do Parlamento Europeu e do Conselho de 20 de junho de 2019 que visa reforçar a segurança dos bilhetes de identidade dos cidadãos da União e dos títulos de residência emitidos aos cidadãos da União e seus familiares que exercem o direito à livre circulação](https://eur-lex.europa.eu/eli/reg/2019/1157/oj):

+ É aplicável a partir de 2 de agosto de 2021;
+ Identifica as  normas de segurança aplicáveis aos bilhetes de identidade de cidadão nacional emitidos pelos Estados-Membros e aos títulos de residência emitidos pelos Estados-Membros aos cidadãos da União e seus familiares que exercem o direito à livre circulação na União.


#### 2.2.1 Temas a analisar e relacionar 

Os temas a analisar e relacionar serão entre o Regulamento (UE) 2019/1157 (e documentos técnicos conexos) e o [ISO/IEC 27002:2013 - Information technology — Security techniques — Code of practice for information security controls](https://trofisecurity.com/assets/img/ISO-IEC_27002-.pdf). Se o link para o ISO 27002 não esiver ativo, podem encontrar o documento [aqui](ISO27002_2013.pdf).

Cada um dos grupos deverá analisar os controlos de segurança do ISO/IEC 27002:2013 referidos de seguida e justificar quais é que se aplicam na emissão/utilização do novo cartão de identidade (indicando as componentes em que se aplicam, se relevante):

+ Grupo 7 - Política de segurança de informação (_Information Security Policy_), Recursos humanos (_Human resources_), Gestão de incidentes (_Incident management_)
+ Grupo 15 - Controlo de acessos (_Access control_)
+ Grupo 16 - Segurança ambiental e física (_Physical and environmental security_), Controlos criptográficos (_Cryptographic controls_) 
+ Grupo 17 - Segurança de operações (_Operation security_) - para grupo com 5 elementos, se existir
+ Grupo 18 - Gestão de ativos (_Asset Management_), Gestão de continuidade de negócio (_Business continuity management_) 


Notas: 

+ Não se esqueça de adicionar contextualização do(s) tema(s) a analisar, assim como uma conclusão onde reflete sobre a adequação dos controlos do ISO/IEC 27002:2013 face à emissão/utilização do novo cartão de identidade.
+ Grupos com mais de três elementos, deverão adicionalmente identificar (e justificar) qual das boas práticas do ISO analisados, deverão ser vistas como requisitos a serem seguidos no âmbito de uma _wallet_ de identificação em dispositivo móvel (como por exemplo a id.gov.pt).




## 3. Projetos de tipo 3 - Sistema de identificação eletrónica

O [Regulamento eIDAS](https://eur-lex.europa.eu/legal-content/PT/TXT/PDF/?uri=CELEX:32014R0910&from=ga) (Regulamento (UE) n.o 910/2014 do Parlamento Europeu e do Conselho
de 23 de julho de 2014
relativo à identificação eletrónica e aos serviços de confiança para as transações eletrónicas no
mercado interno e que revoga a Diretiva 1999/93/CE), no seu Capítulo II (Identificação Eletrónica), define os critérios de elegibilidade para notificação dos sistemas de identificação eletrónica, assim como os níveis de garantia dos mesmos ("reduzido", "substancial" e "elevado"). Nesse âmbito, Portugal já tem dois sistemas de identificação eletrónica aprovados, pela [_Cooperation Network_](https://ec.europa.eu/cefdigital/wiki/display/EIDCOMMUNITY/Cooperation+Network+Resources), com nível de garantia "elevado", de acordo com os requisitos da [COMMISSION IMPLEMENTING REGULATION (CIR) (EU) 2015/1502
of 8 September 2015
on setting out minimum technical specifications and procedures for assurance levels for electronic identification means pursuant to Article 8(3) of Regulation (EU) No 910/2014 of the European Parliament and of the Council on electronic identification and trust services for electronic transactions in the internal market](https://eur-lex.europa.eu/legal-content/EN/TXT/PDF/?uri=CELEX:32015R1502):

+ Cartão de Cidadão, [publicado a 28/02/2019](https://eur-lex.europa.eu/legal-content/EN/TXT/?uri=CELEX:52019XC0228(01));
+ Chave Móvel Digital, [publicado a 08/04/2020](https://eur-lex.europa.eu/legal-content/EN/TXT/?uri=OJ:JOC_2020_116_R_0005).


### 3.1 Tema a analisar 

Várias entidades portuguesas querem que o seu sistema de autenticação seja aprovada como sistema de identificação eletrónica, e cabe-lhe a si justificar, o nível de garantia para cada uma das especificações técnicas e procedimentos elencadas no anexo do CIR 2015/1502, assim como o nível de garantia máximo que a autenticação no homebanking poderia obter.

Nota: Utilize [este guia](Guidance_on_Levels_of_Assurance.docx) para o ajudar a perceber melhor cada um dos requisitos elencadas no anexo do CIR 2015/1502.


Tema a analisar por:

+ Grupo 3 - entidade é um Banco (escolha o que preferir), e o sistema de autenticação é a app mobile do Banco;
+ Grupo 4 - entidade é a Universidade do Minho, e o sistema de autenticação é o uilizado no site da UM.
