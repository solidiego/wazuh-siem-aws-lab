# Arquitetura do Laboratório

O laboratório foi implantado na AWS utilizando uma VPC dedicada para garantir isolamento e controle de acesso.

## Componentes
- 1 Servidor Wazuh (Ubuntu EC2)
- 1 Agente Linux (Ubuntu EC2)
- 1 Agente Windows (Windows Server EC2)
- 1 Subnet pública
- Security Groups com regras restritivas

## Diagrama lógico

Internet
   |
[Security Group]
   |
[Servidor Wazuh]
      |
      |-- Comunicação interna (VPC)
      |
[Agente Linux]   [Agente Windows]

## Princípios adotados
- Menor privilégio
- Isolamento de rede
- Exposição mínima à internet
