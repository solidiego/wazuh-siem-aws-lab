## Acesso SSH à Instância EC2

O acesso à instância EC2 é realizado via SSH utilizando autenticação por chave.

### Sistema Local
- Windows
- PowerShell com OpenSSH Client

### Comando de acesso
```bash
ssh -i key-wazuh-lab.pem ubuntu@IP_PUBLICO
