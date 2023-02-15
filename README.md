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


## Terraform Init

O comando terraform init é utilizado para inicializar o diretório.
A inicialização executa vária etapas e algumas verificações no arquivo do diretório preparando o mesmo para uso.

-upgrade: Atualiza módulos, provider e plugins.
-reconfigure: Reconfigura o backend.
-migrate-state: Reconfigura o backend e migra as informações para o state atual.


### LAB01 - INSTALAÇÃO
Atividade 01 - Instalação do AWS CLI
Atividade 02 - Instalação do terraform
Atividade 03 - Instalação do VS Code 
Atividade 04 - Instalação de extensão no VS Code 
