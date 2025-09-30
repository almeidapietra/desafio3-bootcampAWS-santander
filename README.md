# AWS CloudFormation - Documentação do Desafio

## O que é AWS CloudFormation?

O AWS CloudFormation é um serviço de Infrastructure as Code (IaC) da AWS que permite criar, gerenciar e provisionar recursos de infraestrutura na nuvem usando templates declarativos. Em vez de configurar manualmente cada serviço pelo console da AWS, você define toda a infraestrutura em arquivos de template (YAML ou JSON) e o CloudFormation automaticamente provisiona e configura todos os recursos.

### Como funciona?

O CloudFormation funciona como um "orquestrador" de infraestrutura. Você fornece um template descrevendo o que deseja criar (servidores, bancos de dados, redes, etc.) e o serviço se encarrega de:
- Criar os recursos na ordem correta
- Gerenciar dependências entre serviços
- Validar configurações
- Fazer rollback em caso de erro
- Manter o estado atual da infraestrutura

## Conceitos Fundamentais

### Templates
São arquivos de texto (YAML ou JSON) que descrevem a infraestrutura desejada. Funcionam como uma "receita" que especifica quais recursos AWS criar, suas configurações e como se relacionam.

### Stacks
São o conjunto de recursos que o CloudFormation cria e gerencia como uma única unidade. Quando você executa um template, o CloudFormation cria uma stack contendo todos os recursos definidos. A stack permite gerenciar o ciclo de vida completo dos recursos.

### Resources
São os componentes individuais da AWS que você define no template, como instâncias EC2, buckets S3, bancos de dados RDS, security groups, etc. Cada recurso tem propriedades específicas que definem seu comportamento.

## Como Criar Stacks

### Métodos de Criação:

1. **Console de Gerenciamento AWS**: Interface gráfica para fazer upload de templates e configurar parâmetros visualmente.

2. **AWS CLI**: Linha de comando que permite automatizar a criação de stacks através de comandos como `create-stack`.

3. **AWS SDKs**: Integração programática com linguagens como Python, Java, JavaScript, etc.

4. **CloudFormation API**: Chamadas diretas à API REST do serviço.

### Fluxo de Criação:
1. Desenvolver o template com os recursos necessários
2. Validar o template (sintaxe e configurações)
3. Executar o comando de criação da stack
4. Monitorar o progresso da criação
5. Verificar os outputs gerados

## Stacks de Firewall no CloudFormation

### O que são Stacks de Firewall?
São stacks especializadas em criar e gerenciar recursos de segurança na AWS, principalmente Security Groups e Network ACLs. Esses recursos funcionam como firewalls virtuais que controlam o tráfego de rede para seus recursos AWS.

### Security Groups
Atuam como firewalls no nível da instância, controlando tráfego de entrada (ingress) e saída (egress) para recursos como EC2, RDS, Lambda. São stateful - se você permite tráfego de entrada, o retorno é automaticamente permitido.

### Network ACLs
Operam no nível da subnet, fornecendo uma camada adicional de segurança. São stateless - você precisa definir regras separadas para tráfego de entrada e saída.

### Para que servem?
- **Controle de Acesso**: Definir quais portas e protocolos estão abertos
- **Segmentação de Rede**: Isolar diferentes partes da infraestrutura
- **Conformidade**: Implementar políticas de segurança corporativas
- **Proteção**: Restringir acesso a serviços sensíveis

### Como são usados?
No CloudFormation, você define regras de firewall diretamente nos templates, especificando quais portas estão abertas, quais protocolos são permitidos e de quais endereços IP o tráfego é aceito. Isso permite versionar e replicar configurações de segurança entre ambientes.

## Vantagens e Benefícios

### Produtividade
- Provisionamento rápido de ambientes complexos
- Replicação de infraestrutura entre regiões
- Automação de processos manuais

### Confiabilidade
- Configurações consistentes entre ambientes
- Rollback automático em caso de falha
- Gestão de dependências entre recursos

### Governança
- Versionamento de infraestrutura
- Auditoria de mudanças
- Controle de custos através de tags
- Conformidade com políticas

### Segurança
- Configurações de segurança como código
- Revisão de templates antes da implantação
- Padronização de configurações seguras

O CloudFormation transforma a maneira como gerenciamos infraestrutura na nuvem, trazendo agilidade, confiabilidade e controle para operações de TI.

-----------------------------------------------------------------------------------------------------------------------------------------------------------

**Feito por**
**Pietra Almeida**

### Contatos
<div> 
    <a href = "mailto:costapietra@gmail.com"><img loading="lazy" src="https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white" target="_blank"></a>
    <a href="https://www.linkedin.com/in/almeidapietra" target="_blank"><img loading="lazy" src="https://img.shields.io/badge/-LinkedIn-%230077B5?style=for-the-badge&logo=linkedin&logoColor=white" target="_blank"></a>   
</div>
