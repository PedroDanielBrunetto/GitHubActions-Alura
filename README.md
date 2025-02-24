### **Resumo sobre GitHub Actions e CI/CD**  

GitHub Actions é uma ferramenta de automação para workflows dentro do GitHub, permitindo a implementação de **CI/CD (Continuous Integration e Continuous Deployment)**.  

- **CI (Continuous Integration)**: Automatiza testes e builds a cada novo commit ou pull request, garantindo qualidade e integridade do código.  
- **CD (Continuous Deployment/Delivery)**: Automatiza a entrega e o deploy da aplicação em ambientes de produção ou staging.  

🔹 **Principais conceitos:**  
- **Workflows**: Definem processos automatizados e são descritos em arquivos YAML dentro do repositório (`.github/workflows/`).  
- **Jobs**: Conjunto de etapas (steps) executadas em paralelo ou sequência.  
- **Steps**: Comandos individuais dentro de um job.  
- **Actions**: Scripts reutilizáveis para automação, como testes, builds e deploys.  
- **Triggers**: Definem quando o workflow será executado (ex: `push`, `pull_request`, `schedule`).  

### **Exemplo de Workflow Simples**  
```yaml
name: CI/CD Pipeline

on: [push, pull_request]

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout código
        uses: actions/checkout@v3
      - name: Instalar dependências
        run: npm install
      - name: Rodar testes
        run: npm test
```
Esse workflow roda automaticamente ao fazer um `push` ou `pull request`, garantindo integração contínua no projeto. 🚀
