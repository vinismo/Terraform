# Terraform
Start By Capgemini

## IaC
IaC ou infraestructure as a code (infraestrutura como código), consiste em escrever o que deseja implementar em código.
No lugar de processos manuais, de gerenciamento e provisionamento da infraestrutura, usamos trexos de códigos.
Os benefícios do IaC são: Código declarativo, redução de risco, rastreamento, colaboração, escalabilidade e velocidade.

## Terraform
O terraform é uma ferramenta de infraestrutura como código; criada pela HashiCorp, que permite gerenciar e provisionar recursos na Cloud ou Local usando arquivo onde podemos versionar, reutilizar e compartilhar.

Terraform <-> Terraform Provider <-> Target API

Write (escrever) -> Plan (verificação e validação) -> Apply (construção da infraestrutura)

## HCL
HCL ou HashiCorp Configuration Language é a linguagem utilizada nos arquivos de configuração de várias ferramentas criadas pela HashiCorp.

## Block Type
**Resource**: Descreve um ou mais objetos de infraestrutura a ser provisionado;

**Data**: Permite que usemos informações de fora do terraform;

**Provider**: São plugins utilizados para interagir com o provedor de nuvem;

**Variable**: Usado para declarar variáveis que irão receber valores do usuário;

**Output**: Fornece informações da infraestrutura provisionada pelo terraform;

**Locals**: Atribui valor a uma expressão;

**Module**: Conjunto de múltiplos resources;

**Terraform**: Configuração do terraform;

## Providers
O terraform conta com plugins chamados de "providers" usados para interagir com provedores de nuvem, provedores SaaS e outras APIs.
Tipos: Oficial, Parceiros, Comunidade ou Próprio.
Usando o provider AWS podemos interagir com diversos recursos da Amazon Web Services (AWS).

**Métodos de autenticação**: 
+ Acesso direto usando credenciais do usuário
+ Acesso por assume role
+ Acesso usando IAM Instance Profile (EC2)

## Terraform Init
O comando terraform init é utilizado para inicializar o diretório.
A inicialização executa várias etapas e algumas verificações no arquivo do diretório preparando o mesmo para uso.

-upgrade: Atualiza módulos, provider e plugins.

-reconfigure: Reconfigura o backend.

-migrate-state: Reconfigura o backend e migra as informações para o state atual.

## Variáveis
Variável é o nome dado para definir um ou mais valores que são manipulados durante a execução do terraform.

Podendo ser usado para:

+ Aplicar uma personalização sem a necessidade de editar o código
+ Evitar a repetição de valores no código, minimizando o trabalho operacional.

Depois de declaradas as variáveis podem ser definidas das seguintes formas: 

+ No workspace
+ Linha de comando, usando o -var
+ Arquivo com a extensão .tfvars
+ Como variável de ambiente

## Output
O output pode nos disponibilizar informações sobre a infraestrutura provisionada via linha de comando ou expor informações para outras configurações do terraform.

## State
O state é o local onde o terraform armazena o estado e configurações da infraestrutura gerenciada.
O terraform usa essas informações para mapear o mundo real, acompanhar metadados e melhorar o desempenho de grandes infraestruturas.
Por padrão esse estado é armazenado em um arquivo chamado terraform.state dentro do diretório de trabalho.

## Remote State
Com o remote state temos o nosso arquivo de estado em um local remoto onde vários colaboradores possam usar de forma centralizada.

## State Locking
Se suportado pelo backend, o terraform poderá bloquear o uso do state caso alguma operação esteja em andamento.

## Count
Por padrão o resource block cria somente um recurso.
Com o count podemos aproveitar o mesmo bloco de configuração para criar mais de um recurso.

## For_each
O for_each tem a mesma função do count, porém podemos utilizar valores de uma lista.

## Locals
O locals é a forma que temos para atribuir um nome e uma expressão (se refere ou calcula valores dentro de uma configuração) e usá-la várias vezes sem precisar repeti-la.

## Dynamic Blocks
Algumas vezes precisamos repetir sub-blocos dentro do bloco de resources, e isso deixa nosso código enorme.
O dynamic blocks nos ajuda a ter vários sub-blocos configurados de forma dinâmica e com menos código.

## Módulos
Módulos são conjuntos de arquivos .tf criados para serem usados juntos. Dessa forma facilita a reutilização do código.

## Workspaces
Com o workspaces podemos ter um state ou mais utilizando o mesmo diretório de trabalho.
Cada workspace possui suas próprias configurações como se fosse diretórios diferentes, simplificando o desenvolvimento e manutenção do código.

## Validação de Entrada
O parâmetro validation dento do bloco de variável pe usado para analisar se o valor fornecido para a variável atende os requisitos.

## Precondition e Postcondition
O precondition e o postcondition podem ser utilizados para criar regras de validação nos blocos resources, datasource e outputs.
O precondition é executado antes da avaliação do objeto em que foi configurado.
O postcondition é executado depois da avaliação do objeto em que foi configurado.

Processo de validação: input validation -> precondition -> plan -> postcondition

## Projeto
Provisionamento de infra-estrutura para uma aplicação em multiplas camadas.

+ Network: Base para conexão entre os serviços.
+ Frontend: Instâncias em auto-scaling onde irá rodar a aplicação Web.
+ Backend: API Rest rodando com API Gateway e Lambdas.
+ Database: Base de dados para armazenar os dados da aplicação.


-----------------------------------------------------------------------------------------------------------------------------------------------------------------------

### LAB01 - INSTALAÇÃO
Atividade 01 - Instalação do AWS CLI

Atividade 02 - Instalação do terraform

Atividade 03 - Instalação do VS Code 

Atividade 04 - Instalação de extensão no VS Code 

### LAB02 - PROVIDERS
Atividade 01 - Desvendando a documentação do provider

### LAB03 - AUTENTICAÇÃO DA AWS
Atividade 01: Criar usuário

Atividade 02: Liberar acesso ao usuário

Atividade 03: Configurar variáveis

Atividade 04: Criar arquivo terraform.tf

Atividade 05: Criar arquivo provider.tf

Atividade 06: Criar role (opcional)

Atividade 07: Reconfigurar o provider (opcional)

### LAB04 - INICIALIZAÇÃO
Atividade 01: Executando o Init

### LAB05 - MEU PRIMEIRO RECURSO
Atividade 01: Criar um bucket S3 na AWS

Atividade 02: Apagar um bucket S3 na AWS

### LAB06 - VARIÁVEIS
Atividade 01: Usar variáveis

### LAB07 - OUTPUTS
Atividade 01: Usar output

### LAB08 - STATE
Atividade 01: Criar o S3

Atividade 02: Criar o DynamoDB

Atividade 03: Configurar o remote state

Atividade 04: Validar o uso do remote state

### LAB09 - IMPORT
Atividade 01: Criar o S3

Atividade 02: Importar S3

### LAB10 - MOVENDO RECURSOS
Atividade 01: Criar o S3

Atividade 02: Renomear bloco

Atividade 03: Mover para outro state

### LAB11 - COUNT
Atividade 01: Usar o count

### LAB12 - FOR_EACH
Atividade 01: Usar o for_each

### LAB13 - LOCALS
Atividade 01: Usar o locals

### LAB14 - DYNAMIC BLOCKS
Atividade 01: Usar o dynamic blocks

### LAB15 - MÓDULOS
Atividade 01: Usar módulos

### LAB16 - WORKSPACES 
Atividade 01: Usar workspaces

### LAB17 - VALIDAÇÃO
Atividade 01: Usar validação de entrada

Atividade 02: Usar precondition

Atividade 03: Usar postcondition

