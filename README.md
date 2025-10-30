##  O que é o AWS CloudFormation?

O **AWS CloudFormation** é um serviço que permite **automatizar a criação e o gerenciamento de recursos AWS** através de arquivos de configuração, chamados **templates** (geralmente escritos em YAML ou JSON).  
Com ele, é possível definir toda a infraestrutura como código, garantindo **padronização, reprodutibilidade e controle de versão**.

**Vantagens principais:**
- Automação completa da infraestrutura.
- Evita erros manuais de configuração.
- Facilita o versionamento com Git e GitHub.
- Permite reproduzir o mesmo ambiente em minutos.
---

## Etapas do Laboratório

### 1. Criação do Bucket S3
Arquivo: `01-S3_Bucket.yaml`

- Configuração de um **bucket S3** para armazenamento de arquivos.
- Aprendizado sobre propriedades do recurso `AWS::S3::Bucket`.
- Introdução ao conceito de **recursos (Resources)** dentro de um template.

**Conceitos importantes:**
- Nomeação de buckets.
- Controle de acesso e permissões.
- Versionamento e gerenciamento de objetos.

---

### 2. Criação de uma Instância EC2
Arquivo: `02-EC2_Instance.yaml`

- Implantação de uma **instância EC2** configurável.
- Uso de parâmetros para definir **tipo de instância**, **AMI** e **chave SSH**.
- Demonstração da criação automatizada de servidores virtuais.

**Conceitos aplicados:**
- `Parameters`: entrada de dados personalizados no deploy.  
- `Mappings`: mapeamento de configurações regionais.  
- `Outputs`: exibição de informações após a criação da stack.

---

### 3. Criação de Usuário e Grupo IAM
Arquivo: `03-IAM_UserGroup.yaml`

- Implementação de um **usuário e grupo IAM** com permissões específicas.
- Aplicação de políticas (Policies) para controle de acesso.
- Associação do usuário ao grupo e configuração de permissões de segurança.

**Conceitos trabalhados:**
- `AWS::IAM::User`, `AWS::IAM::Group` e `AWS::IAM::Policy`.
- Princípio do **menor privilégio** (Least Privilege).
- Boas práticas de **segurança e governança** na nuvem.

---

### 4. Template — EC2 + S3 + IAM
Arquivo: `04-EC2_S3_UserGroup.yaml`

Template completo que **integra múltiplos serviços AWS** em uma única stack.

**Recursos implementados:**
- Criação de um **bucket S3**.
- Criação de **grupo e usuário IAM**.
- Criação de uma **instância EC2 parametrizada**.

**Principais conceitos:**
- **Parâmetros (`Parameters`)** para personalização de recursos.  
- **Referências entre recursos (`!Ref`)**, permitindo que serviços se conectem.  
- **Estrutura modular e reutilizável**, facilitando manutenção e expansão.  
- **Integração entre diferentes serviços AWS** dentro de um único template.

---

## 🧰 Ferramentas Utilizadas

- **AWS CloudFormation** — para criação e gerenciamento da infraestrutura.  
- **VS Code** — para edição e organização dos arquivos YAML.  
- **Git & GitHub** — para versionamento e entrega do desafio.  
- **AWS Console** — para acompanhamento das stacks criadas.  

---

## Conclusão

Com este desafio, foi possível compreender na prática o funcionamento do **AWS CloudFormation** e sua importância na automação da infraestrutura em nuvem.  
A experiência consolidou o entendimento de **Infraestrutura como Código (IaC)** e demonstrou como documentar e versionar ambientes de forma profissional.

---

## 🔗 Referências

- [Documentação Oficial do AWS CloudFormation](https://docs.aws.amazon.com/cloudformation)
- [Guia de Introdução Criar sua primeira pilha](https://docs.aws.amazon.com/pt_br/AWSCloudFormation/latest/UserGuide/gettingstarted.walkthrough.html)
- [Documentação AWS S3](https://docs.aws.amazon.com/s3)
- [Documentação AWS EC2](https://docs.aws.amazon.com/ec2)
- [Documentação AWS IAM](https://docs.aws.amazon.com/iam)

---



