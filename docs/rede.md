# Configuração de Rede

## Região
- us-east-1 (N. Virginia)

## VPC
- CIDR: 10.0.0.0/16
- VPC dedicada para o laboratório

## Subnet
- Subnet pública: 10.0.1.0/24
- Atribuição automática de IPv4 público habilitada

## Internet Gateway
- Associado à VPC
- Permite acesso controlado à internet

## Tabela de Rotas
- Rota padrão (0.0.0.0/0) apontando para o Internet Gateway
- Associada à subnet pública

## Security Groups

### Servidor Wazuh
- SSH (22): permitido apenas a partir do IP administrativo
- HTTPS (443): permitido apenas a partir do IP administrativo
- Portas Wazuh (1514/1515): permitidas apenas dentro da VPC

### Agentes
- Nenhuma porta de entrada exposta
- Comunicação somente de saída
