# Documentação de uma arquitetura na AWS utilizando Docker
Este repositório tem como objetivo conter uma documentação necessária para configurar uma arquitetura na AWS e a utilização de docker, de acordo com os requisitos citados abaixo.

## Arquitetura a ser implementada:
![arquitetura](https://github.com/PinheiroChequin/TrabalhoDocker/assets/117855728/a739dc36-9159-4b95-8ed6-e633545a202f)

Começaremos pela instalação e configuração das duas instâncias que serão utilizadas para a aplicação do WordPress, além disso será criada uma instância para ser nosso Bastion Host como uma medida de segurança extra. 

# Configuração das Instâncias:
-Instâncias "comuns"-
- _**SO: Amazon Linux 2**_
- _**Família: t3.small**_
- _**Volume: 1x8GB gp2**_

**Observação**: Na criação das instâncias acima, em detalhes avançados encontraremos o campo "userdata" (Dados do usuário) e colocaremos o script `userdata` o qual encontra-se presente neste repositório e logo abaixo com sua explicação:
  ```
#!/bin/bash

yum update -y
yum install -y nfs-utils
mkdir /efs
echo [fs-XXXXXXXX.efs.REGION.amazonaws.com]:/ /efs nfs4 defaults,_netdev 0 0 >> /etc/fstab
yum install docker -y
systemctl enable docker
systemctl start docker
usermod -aG docker ec2-user
  ```
O script fará:
1. Atualiza pacotes do sistema operacional
2. Instala o utilitário NFS para o sistema de arquivos que será usado
3. Cria um diretório
4. Configura montagem de sistema de arquivos NFS, sendo que "[fs-XXXXXXXX.efs.REGION.amazonaws.com]" é o DNS do sistema de arquivos criado na AWS
5. Instala e configura o Docker 
6. Modifica o grupo do usuário para permitir a execução de comandos Docker.
Esse script proporciona maior eficiência e praticidade. Por isso sua utilização.

-Bastion Host-
- _**SO: Amazon Linux 2**_
- _**Família: t2.micro**_
- _**Volume: 1x8GB gp2**_

# Configuarção da VPC(Virtual Private Cloud)

# Configuração do Loud Balancer

# Configuração do RDS da AWS
