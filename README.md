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

# Configuração do Load Balancer

# Configuração do RDS da AWS
