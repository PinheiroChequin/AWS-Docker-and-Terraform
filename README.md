# Documentação de uma arquitetura na AWS utilizando Docker
Este repositório tem como objetivo conter uma documentação necessária para configurar uma arquitetura na AWS e a utilização de docker, de acordo com os requisitos citados abaixo.

## Arquitetura a ser implementada:
<p align="center">
  <img src="https://github.com/PinheiroChequin/TrabalhoDocker/assets/117855728/a739dc36-9159-4b95-8ed6-e633545a202f">
</p>

Na implementação da arquitetura acima, foi utilizado o Terraform visando aplicabilidade e eficiência. Todos os arquivos utilizados estão disponíveis no seguinte repositório: [diretório do Terraform](https://github.com/PinheiroChequin/TrabalhoDocker/tree/main/proj-compass).

A configuração das instâncias utilizadas encontra-se abaixo:

# Configuração das Instâncias:
-Instâncias principais-
- _**SO: Amazon Linux 2**_
- _**Família: t3.small**_
- _**Volume: 1x16GB gp2**_

-Bastion Host-
- _**SO: Amazon Linux 2**_
- _**Família: t2.micro**_
- _**Volume: 1x8GB gp2**_

# Configuração da VPC(Virtual Private Cloud)
Com a Amazon Virtual Private Cloud (Amazon VPC), é possível iniciar recursos da AWS em uma rede virtual definida pelo usuário. Essa rede virtual é bem parecida com uma rede tradicional, com a vantagem de usar a infraestrutura da AWS.

<p align="center">
  <img src="https://github.com/PinheiroChequin/TrabalhoDocker/assets/129349503/f4e098f6-8918-4ba0-a9b7-b06f8c441832">
</p>

## **Criação de uma VPC**


# Configuração do Load Balancer

# Configuração do RDS da AWS

# Configuração do Terraform
