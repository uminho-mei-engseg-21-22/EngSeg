
# Avaliação prática 2 - Projeto de desenvolvimento 2 (PD2)

De seguida são apresentados os vários projetos de desenvolvimento 2. O relatório final e o código fonte deverá ser colocado na área do Grupo no github até ao dia 20/06/2022, na subdiretoria "AP2-PD2" (**Note que no relatório tem de indicar os passos necessários para se poder testar o código fonte, incluindo o ambiente (que se espera que seja preferencialmente Linux)**).

Nota: Caso não consiga entregar até 20/06, pode entregar até 24/06, caso em que será descontado 0,5 valores na nota final do PD2.
## Data e horário de apresentação do trabalho

Para além da apresentação oral do trabalho, também se vai querer ver o trabalho a funcionar, assim como aceder ao código fonte para que possam explicar algumas das alterações efetuadas.

Data e hora: Terça-feira, dia 28 de Junho, no zoom utilizado para as aulas

+ Grupo 1 - 09h00
+ Grupo 2 - 09h40
+ Grupo 3 - 10h20
+ Grupo 5 - 11h40
+ Grupo 6 - 12h20

Data e hora: Quarta-feira, dia 29 de Junho, no zoom utilizado para as aulas

+ Grupo 7 - 14h00
+ Grupo 8 - 14h40
+ Grupo 9 - 15h20
+ Grupo 10 - 16h00
+ Grupo 11 - 16h40
+ Grupo 12 - 17h20
+ Grupo 13 - 18h00
+ Grupo 14 - 18h40
+ Grupo 4 - 19h00

## Avaliação do PD2

A avaliação do PD2 será efetuada entre 0 e 20 valores. Quem entregar antes da data limite tem uma valorização de 1% na sua nota por cada dia de antecipação.

**Note** que o projeto de desenvolvimento, para além do desenvolvimento em si, inclui componentes de:

+ Identificação do “_Software Assurance Maturity Model_ (SAMM)” da equipa,
+ RGPD PIA, e
+ _Compliance_ com boas práticas de desenvolvimento.

Para algumas destas componentes terão que entregar um relatório no âmbito das fichas de trabalho (avaliação prática 1), na sequência de aulas teóricas sobre o tema. Esses relatórios farão parte do relatório final do projeto de desenvolvimento.

## Objectivos

O objetivo destes projetos de desenvolvimento não é aprender a programar (esse poderia ser o objetivo se fosse um projeto no âmbito da licenciatura), mas

+ Integrar/utilizar/alterar frameworks, APIs, código de terceiros, ..., que sejam relevantes para o seu projeto, de modo a simplificarem o desenvolvimento e/ou aumentarem a segurança;
+ Utilizar metodologia de desenvolvimento de software seguro, realçando-se a [_Fundamental Practices for Secure Software Development_](https://safecode.org/uncategorized/fundamental-practices-secure-software-development/), o [_Mitigating the Risk of Software Vulnerabilities by Adopting a Secure Software Development Framework_ (SSDF)](https://csrc.nist.gov/publications/detail/sp/800-218/final), e o [Microsoft _Security Development Lifecycle_ (SDL)](https://www.microsoft.com/en-us/securityengineering/sdl);
+ Identificar e melhorar as capacidades do grupo de trabalho no desenvolvimento de software seguro, através do modelo de maturidade [OWASP _Software Assurance Maturity Model_ (SAMM)](https://owasp.org/www-project-samm/);
+ Seguir o standard de verificação de segurança de aplicações ([OWASP _Application Security Verification Standard_](https://github.com/OWASP/ASVS)), no desenvolvimento do projeto;
+ Utilizar [ferramentas de análise de impacto da proteção de dados](https://www.cnil.fr/en/privacy-impact-assessment-pia) (PIA - _Privacy Impact Assessment_), de modo a demonstrar compliance com o RGPD (Regulamento Geral de Proteção de Dados).

----

## Utilização/integração de ferramentas disponibilizadas no âmbito do Digital Signature Services (DSS)

A União Europeia disponibiliza uma biblioteca de software _open-source_ ([_Digital Signature Services_ - DSS](https://ec.europa.eu/cefdigital/wiki/display/CEFDIGITAL/Start+using+Digital+Signature+Services+-+DSS)) para a criação e validação de assinaturas eletrónicas, em linha com o Regulamento eIDAS e standards relacionados.

O código fonte do DSS encontra-se disponível no [repositório Bitbucket do DSS](https://ec.europa.eu/cefdigital/code/projects/ESIG/repos/dss/browse) (conforme indicado em <https://ec.europa.eu/cefdigital/wiki/display/CEFDIGITAL/Start+using+Digital+Signature+Services+%28DSS%29+-+Releases+and+Bitbucket>) e, no github em <https://github.com/esig/dss>.

Também são disponibilizadas várias aplicações de demonstração da utilização do DSS, que pode encontrar no [repositório Bitbucket do DSS](https://ec.europa.eu/cefdigital/code/projects/ESIG/repos/dss-demos/browse) e, no github em <https://github.com/esig/dss-demonstrations>.

### DSS Demo WebApp

Como aplicação de demonstração, o DSS disponibiliza a [DSS Demo WebApp](https://ec.europa.eu/cefdigital/DSS/webapp-demo/home) que pode fazer download e instalar a partir de <https://ec.europa.eu/cefdigital/wiki/display/CEFDIGITAL/DSS>.

Os seus colegas do ano passado alteraram a DSS Demo WebApp - versão 5.8.2 - (pode ver no [projeto dos seus colegas do ano passado](https://github.com/uminho-miei-engseg-20-21/Grupo3/tree/main/AP2-PD)), de modo a poder ser utilizada com:

+ Cartão de Cidadão,
+ Chave Móvel Digital, e
+ a fonte de _timestmap_ do Cartão de Cidadão, de modo a não se utilizar a _dummy timestamp source_ que é utilizada nas várias opções da Demo WebApp que utilizam _timestamp_.

Pretende-se que pegue no trabalho dos seus colegas, e:

1. Transponha as alterações que eles já tinham efetuado, para a nova versão da DSS Demo WebApp (versão 5.10.1 ou superior);
2. Adicione interface de autenticação inicial (com utilizador e password);
3. Adicione área de utilizador, onde o utilizador (após autenticação) possa definir qual o número de telemóvel que utiliza para a Chave Móvel Digital - sendo os dados do utilizador guardados em Base de Dados -;
4. Altere o código efetuado pelos seus colegas, de modo que seja utilizado o número de telemóvel guardado na área de utilizador, sempre que o utilizador efetue uma operação que utilize a Chave Móvel Digital.

Nota: Para testar a Chave Móvel Digital necessita de a ativar (componente de autenticação e assinatura) em <https://www.autenticacao.gov.pt/>.

Este trabalho será efetuado pelos Grupos:

+ Grupo 1, que para além do que é pedido acima, adiciona a possibilidade de assinar com chaves privadas (e respetivos certificados, em hierarquia até à Entidade de Certificação raiz) em ficheiro (formato PEM e/ou DER), nas opções de assinatura: _Sign a document_.
+ Grupo 2, que para além do que é pedido acima, retirará da interface existente, as componentes de "_Documentation_" e "_Useful Links_";
+ Grupo 3, que para além do que é pedido acima, adiciona a possibilidade de assinar com chaves privadas (e respetivos certificados na hierarquia até à Entidade de Certificação raiz) em ficheiro (formato PEM e/ou DER),  nas opções de assinatura: _Sign a PDF_.
+ Grupo 4, que para além do que é pedido acima, adiciona a possibilidade de assinar com chaves privadas (e respetivos certificados na hierarquia até à Entidade de Certificação raiz) em ficheiro (formato PEM e/ou DER),  nas opções de assinatura: _Sign a digest_.
+ Grupo 5, que para além do que é pedido acima, adiciona a possibilidade de assinar com chaves privadas (e respetivos certificados na hierarquia até à Entidade de Certificação raiz) em ficheiro (formato PEM e/ou DER),  nas opções de assinatura: _Sign with JAdES_.
+ Grupo 6, que para além do que é pedido acima, adicionará à interface existente, uma nova componente de "Chave Móvel Digital", a que adicionará várias sub-componentes com a informação que lhe parecer mais conveniente;
+ Grupo 7, que para além do que é pedido acima, adiciona a possibilidade de assinar com chaves privadas (e respetivos certificados na hierarquia até à Entidade de Certificação na raiz) em ficheiro (formato PEM e/ou DER),  nas opções de assinatura: _Sign multiple documents_.
+ Grupo 8, que para além do que é pedido acima, adiciona a possibilidade de assinar com chaves privadas (e respetivos certificados na hierarquia até à Entidade de Certificação na raiz) em ficheiro (formato PEM e/ou DER),  nas opções de assinatura: _Counter sign a signature_.
+ Grupo 9, que para além do que é pedido acima, adicionará à interface existente, uma nova componente de "Cartão de Cidadão", a que adicionará várias sub-componentes com a informação que lhe parecer mais conveniente;
+ Grupo 10, que em vez dos números 3. e 4. acima, adiciona uma área de administração, onde o administrador pode definir quais as Trusted Lists que são carregadas, assim como adicionar novas Trusted Lists de outros países ou organizações;
+ Grupo 11, que para além do que é pedido acima, permite que o utilizador indique na sua área de utilizador, qual a fonte de _timestamp_ que pretende utilizar (por omissão será a fonte de _timestmap_ do Cartão de Cidadão), utilizando sempre essa fonte de timestamp na assinatura desse utilizador;
+ Grupo 12, que para além do que é pedido acima, adicionará à interface existente, uma nova componente de "Ajuda", a que disponibilizará texto de ajuda para a utilização das várias opções na componente _e-Signature_, nomeadamente para _Sign a document_, _Sign a digest_, _Sign a PDF_, _Sign with JAdES_, _Sign multiple documents_, _Counter sign a signature_;
+ Grupo 13, que para além do que é pedido acima, adicionará à interface existente, uma nova componente de "Ajuda", a que disponibilizará texto de ajuda para a utilização das várias opções na componente _Server side_, nomeadamente para _Extend a signature_, _Timestamp document(s)_, _Validate a signature_, _Validate a certificate_, _SSL-certificate validation_, _Replay Diagnostic Data_.
