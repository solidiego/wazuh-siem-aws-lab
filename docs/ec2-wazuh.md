# Servidor Wazuh – EC2

## Instância
- Nome: ec2-wazuh-server
- Tipo: t2.micro (Free Tier legado)
- Sistema Operacional: Ubuntu Server 22.04 LTS

## Rede
- VPC: vpc-wazuh-lab
- Subnet: subnet-public-wazuh
- Security Group: sg-wazuh-server
- IP público dinâmico

## Armazenamento
- Volume root: 30 GB (gp3)

## Instalação do Wazuh
O Wazuh foi instalado utilizando o script oficial em modo all-in-one, incluindo:
- Wazuh Manager
- Indexer
- Dashboard

## Observações
- Instância dimensionada apenas para laboratório
- Dashboard acessível somente via IP administrativo
