# Época Especial

Na época especial poderá melhorar a sua nota de PD2. Para tal terá que se inscrever na época especial através do portal académico ou serviços académicos da Universidade do Minho.

Para a época especial, os grupos não poderão ter mais do que 3 elementos, pelo que serão criadas novas diretorias no github para esses grupos (ou mantêm-se as mesmas caso os grupos sejam iguais aos já existentes).

---
De seguida são apresentados os vários projetos para a época especial. O relatório final e o código fonte deverá ser colocado na área do Grupo no github até ao dia 24/07/2022, na subdiretoria "EpocaEspecial" (**Note que no relatório tem de indicar os passos necessários para se poder testar o código fonte, incluindo o ambiente (que se espera que seja preferencialmente Linux)**).

## Data e horário de apresentação do trabalho

Para além da apresentação oral do trabalho, também se vai querer ver o trabalho a funcionar, assim como aceder ao código fonte para que possam explicar algumas das alterações efetuadas.

Data e hora: Quarta-feira, dia 27 de Julho, no zoom utilizado para as aulas

+ Grupo 10 - 15h00
+ Grupo B - 15h40
+ Grupo C - 16h20
+ Grupo D - 16h40

## Avaliação

A avaliação do trabalho será efetuada entre 0 e 20 valores.

**Note** que o projeto de desenvolvimento, para além do desenvolvimento em si, inclui componentes de:

+ Identificação do “_Software Assurance Maturity Model_ (SAMM)” da equipa,
+ RGPD PIA, e
+ _Compliance_ com boas práticas de desenvolvimento.

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

1. Transponha as alterações que eles já tinham efetuado, para a nova versão da DSS Demo WebApp (versão 5.10 ou superior);
2. Adicione interface de autenticação inicial (com utilizador e password);
3. Adicione área de utilizador, onde o utilizador (após autenticação) possa definir qual o número de telemóvel que utiliza para a Chave Móvel Digital - sendo os dados do utilizador guardados em Base de Dados -;
4. Altere o código efetuado pelos seus colegas, de modo que seja utilizado o número de telemóvel guardado na área de utilizador, sempre que o utilizador efetue uma operação que utilize a Chave Móvel Digital.

Nota: Para testar a Chave Móvel Digital necessita de a ativar (componente de autenticação e assinatura) em <https://www.autenticacao.gov.pt/>.

Este trabalho será efetuado pelos Grupos:

+ Grupo 10, que em vez dos números 2., 3. e 4. acima, adiciona uma área de autenticação para o administrador do serviço, onde o administrador pode selecionar quais as Trusted Lists que são carregadas/utilizadas na DSS Demo WebApp, assim como adicionar novos certificados confiáveis de outros países ou organizações.
