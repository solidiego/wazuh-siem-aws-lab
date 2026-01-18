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

## Acesso à Instância
- Sistema local: Windows
- Acesso realizado via PowerShell (SSH nativo)
- Autenticação por chave (.pem)

## Ambiente Local
- Sistema operacional: Windows
- Cliente SSH: OpenSSH Client (Windows Optional Feature)
- Acesso realizado via PowerShell

## Atualização do Sistema

Antes da instalação do Wazuh, o sistema foi atualizado para garantir
correções de segurança e compatibilidade.

"```bash
sudo apt update && sudo apt upgrade -y"

## Problemas Encontrados

Durante a instalação do Wazuh em instância Free Tier,
o processo falhou devido à limitação de memória.

### Solução aplicada
Foi criado um arquivo de swap de 2 GB para permitir
a conclusão da instalação.
"

```bash
sudo fallocate -l 2G /swapfile
sudo chmod 600 /swapfile
sudo mkswap /swapfile
sudo swapon /swapfile"

## Instalação do Wazuh
O Wazuh foi instalado utilizando o script oficial em modo all-in-one, incluindo:
- Wazuh Manager
- Indexer
- Dashboard

## Observações
- Instância dimensionada apenas para laboratório
- Dashboard acessível somente via IP administrativo
