# Terraform
Start By Capgemini

## IAC

IaC ou infraestructure as a code (infraestrutura como código), consiste em escrever o que deseja implementar em código.
No lugar de processos manuais, de gerenciamento e provisionamento da infraestrutura, usamos trexos de códigos.
Os benefícios do Iac são: Código declarativo, redução de risco, rasteramento, colaboração, escalabilidade e velocidade.

## Terraform

O terraform é uma ferramenta de infraestrutura como código; criada pela HashiCorp, que permite gerenciar e provisionar recursos na Cloud ou Local usando arquivo onde podemos versionar, reutilizar e compartilhar.

Terraform <-> Terraform Provider <-> Target API

Write (escrever) -> Plan (verificação e validação) -> Apply (construção da infraestrutura)

## HCL

HCL ou HashiCorp Configuration Language é a linguagem utilizada nos arquivos de configuração de várias ferramentas criadas pela HashiCorp.

## BLOCK TYPE
**Resource**: Descreve um ou mais objetos de infraestrutura a ser provisionado;

**Data**: Permite que usemos informações de fora do terraform;

**Provider**: São plugins utilizados para interagir com o provedor de nuvem;

**Variable**: Usado para declarar variáveis que irão receber valores do usuário;

**Output**: Fornece informações da infraestrutura provisionada pelo terraform;

**Locals**: Atribui valor a uma expressão;

**Module**: Conjunto de multiplos resources;

**Terraform**: Configuração do terraform;

## PROVIDERS

O terraform conta com plugins chamados de "providers" usados para interagir com provedores de nuvem, provedores Saas e outras APIs.
Tipos: Oficial, Parceiros, Comunidade ou Próprio.
Usando o provider AWS podemos interagir com diversos resursos da Amazon Web Services (AWS).

**Métodos de autenticação**: 
+ Acesso direto usando credenciais do usuário
+ Acesso por assume role
+ Acesso usando IAM Instance Profile (EC2)


## Terraform Init

O comando terraform init é utilizado para inicializar o diretório.
A inicialização executa vária etapas e algumas verificações no arquivo do diretório preparando o mesmo para uso.

-upgrade: Atualiza módulos, provider e plugins.

-reconfigure: Reconfigura o backend.

-migrate-state: Reconfigura o backend e migra as informações para o state atual.

## Variáveis

Variável é o nome dado para definir um ou mais valores que são manipulados durante a execução do terraform.

Podendo ser usado para:

+ Aplicar uma personalização sem a necessidade de editar o código
+ Evitar a repetição de valores no código, minimizando o trabalho operacional.



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
