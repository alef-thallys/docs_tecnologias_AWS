# 📚 Documentação Detalhada: Tecnologias AWS e Conceitos de Nuvem

Esta documentação oferece um resumo detalhado dos principais conceitos e serviços da AWS, abrangendo desde a computação em nuvem até ferramentas de segurança, bancos de dados e gerenciamento.

---

## 🧭 Índice de Navegação

Clique em um tópico para ir diretamente à seção:

- [O que é Computação em Nuvem?](#o-que-é-computação-em-nuvem)
- [Vantagens da Computação em Nuvem](#vantagens-da-computação-em-nuvem)
- [O que é a AWS?](#o-que-é-a-aws)
- [Definição de Preços da AWS](#definição-de-preços-da-aws)
- [Visão Geral da Infraestrutura da AWS](#visão-geral-da-infraestrutura-da-aws)
- [Serviços e Categorias da AWS](#serviços-e-categorias-da-aws)
- [Modelo de Responsabilidade Compartilhada da AWS](#modelo-de-responsabilidade-compartilhada-da-aws)
- [Amazon S3 (Simple Storage Service)](#amazon-s3-simple-storage-service)
- [Elastic Compute da AWS (Amazon EC2)](#elastic-compute-da-aws-amazon-ec2)
- [Redes na Nuvem AWS](#redes-na-nuvem-aws)
- [Introdução à Segurança](#introdução-à-segurança)
- [Security Groups da AWS](#security-groups-da-aws)
- [AWS IAM (Identity and Access Management)](#aws-iam-identity-and-access-management)
- [AWS CloudTrail](#aws-cloudtrail)
- [AWS Config](#aws-config)
- [AWS Trusted Advisor](#aws-trusted-advisor)
- [Conformidade de Segurança da AWS](#conformidade-de-segurança-da-aws)
- [Recursos de Segurança da AWS](#recursos-de-segurança-da-aws)
- [Amazon RDS (Relational Database Service)](#amazon-rds-relational-database-service)
- [Amazon DynamoDB](#amazon-dynamodb)
- [AWS Cloud Adoption Framework (CAF)](#aws-cloud-adoption-framework-caf)
- [AWS Well-Architected Framework](#aws-well-architected-framework)
- [Design do Well-Architected](#design-do-well-architected)
- [Confiabilidade e Alta Disponibilidade](#confiabilidade-e-alta-disponibilidade)
- [Transição de um Data Center para a Nuvem](#transição-de-um-data-center-para-a-nuvem)
- [AWS Identity and Access Management (Revisão)](#aws-identity-and-access-management-revisão)
- [AWS Command Line Interface (CLI)](#aws-command-line-interface-cli)
- [AWS Systems Manager](#aws-systems-manager)
- [Ferramentas de Administração e Desenvolvimento](#ferramentas-de-administração-e-desenvolvimento)
- [Hospedar um Site Estático no S3 da AWS](#hospedar-um-site-estático-no-s3-da-aws)
- [Visão Geral da Computação (Servidores)](#visão-geral-da-computação-servidores)
- [Computação na AWS (Revisão)](#computação-na-aws-revisão)
- [Gerenciar Instâncias da AWS](#gerenciar-instâncias-da-aws)
- [Visão Geral do Laboratório: Instâncias do EC2](#visão-geral-do-laboratório-instâncias-do-ec2)
- [Demonstração do AWS IAM-2](#demonstração-do-aws-iam-2)
- [AWS Elastic Beanstalk](#aws-elastic-beanstalk)
- [Visão Geral de Escalabilidade e Resolução de Nomes](#visão-geral-de-escalabilidade-e-resolução-de-nomes)
- [Elastic Load Balancing (ELB)](#elastic-load-balancing-elb)
- [Listeners do Elastic Load Balancer](#listeners-do-elastic-load-balancer)
- [Auto Scaling do Amazon EC2](#auto-scaling-do-amazon-ec2)
- [Visão Geral do Laboratório: Auto Scaling do EC2](#visão-geral-do-laboratório-auto-scaling-do-ec2)
- [Desafio de Previsão de Auto Scaling](#desafio-de-previsão-de-auto-scaling)
- [Amazon Route 53](#amazon-route-53)
- [Demonstração do Amazon Route 53-2](#demonstração-do-amazon-route-53-2)
- [Amazon CloudFront](#amazon-cloudfront)
- [AWS Lambda](#aws-lambda)
- [APIs e REST da Amazon](#apis-e-rest-da-amazon)
- [Amazon API Gateway](#amazon-api-gateway)
- [Contêineres na AWS](#contêineres-na-aws)
- [Funções do AWS Step Functions](#funções-do-aws-step-functions)
- [Visão Geral dos Bancos de Dados](#visão-geral-dos-bancos-de-dados)
- [Amazon Redshift](#amazon-redshift)
- [Amazon Aurora](#amazon-aurora)
- [Migração de Banco de Dados da Amazon](#migração-de-banco-de-dados-da-amazon)
- [Visão Geral das Redes da AWS (Revisão)](#visão-geral-das-redes-da-aws-revisão)
- [Amazon VPC (Virtual Private Cloud)](#amazon-vpc-virtual-private-cloud)
- [Opções de Conectividade da Amazon VPC](#opções-de-conectividade-da-amazon-vpc)
- [Segurança e Solução de Problemas da Rede](#segurança-e-solução-de-problemas-da-rede)
- [Visão Geral do Laboratório: Configurar uma Amazon VPC](#visão-geral-do-laboratório-configurar-uma-amazon-vpc)
- [Visão Geral do Cloud Storage](#visão-geral-do-cloud-storage)
- [Amazon EBS (Elastic Block Store)](#amazon-ebs-elastic-block-store)
- [Demonstração do Amazon EBS-2](#demonstração-do-amazon-ebs-2)
- [O Armazenamento de Instâncias do EC2](#o-armazenamento-de-instâncias-do-ec2)
- [Elastic File System (EFS)](#elastic-file-system-efs)
- [Demonstração do Elastic File System-2](#demonstração-do-elastic-file-system-2)
- [Amazon Glacier](#amazon-glacier)
- [Demonstração do S3 Glacier-2](#demonstração-do-s3-glacier-2)
- [Amazon S3 e a CLI da AWS](#amazon-s3-e-a-cli-da-aws)
- [Amazon Storage Gateway](#amazon-storage-gateway)
- [Amazon CloudWatch](#amazon-cloudwatch)
- [Mergulhe Fundo: Amazon CloudWatch](#mergulhe-fundo-amazon-cloudwatch)
- [Integração do Serviço da AWS com o Athena](#integração-do-serviço-da-aws-com-o-athena)
- [AWS Organizations](#aws-organizations)
- [Marcação (Tagging)](#marcação-tagging)
- [Gerenciamento de Custos da AWS e Práticas Recomendadas](#gerenciamento-de-custos-da-aws-e-práticas-recomendadas)
- [Demonstração do Painel de Faturamento da AWS-2](#demonstração-do-painel-de-faturamento-da-aws-2)
- [Estratégia de Construção da AMI (Amazon Machine Image)](#estratégia-de-construção-da-ami-amazon-machine-image)
- [Modelos de Inicialização do Amazon EC2 (Launch Templates)](#modelos-de-inicialização-do-amazon-ec2-launch-templates)
- [Demonstração do Modelo de Lançamento EC2-2](#demonstração-do-modelo-de-lançamento-ec2-2)
- [Infraestrutura como Código (IaC)](#infraestrutura-como-código-iac)
- [Introdução ao JSON e ao YAML](#introdução-ao-json-e-ao-yaml)
- [AWS CloudFormation](#aws-cloudformation)

---

## O que é Computação em Nuvem?

A **Computação em Nuvem** é a entrega de recursos de computação, como servidores, armazenamento, bancos de dados, redes, software, análises e inteligência artificial, pela internet (“a nuvem”). Isso elimina a necessidade de comprar, possuir e manter sua própria infraestrutura física, permitindo que você acesse esses serviços sob demanda de um provedor de nuvem, como a AWS, pagando apenas pelo que usar.

Existem três modelos principais de serviços de nuvem:

* **Infraestrutura como Serviço (IaaS)**: Fornece recursos de computação e rede virtualizados. Você gerencia o sistema operacional, aplicações e dados, enquanto o provedor gerencia a infraestrutura subjacente. Exemplo: Amazon EC2.
* **Plataforma como Serviço (PaaS)**: Oferece um ambiente completo para desenvolvimento, execução e gerenciamento de aplicações. O provedor gerencia a infraestrutura, o sistema operacional e o middleware, e você foca apenas no código da sua aplicação. Exemplo: AWS Elastic Beanstalk.
* **Software como Serviço (SaaS)**: O provedor de nuvem gerencia todo o software e a infraestrutura, e você acessa a aplicação via navegador web ou aplicativo móvel. Exemplo: Gmail, Salesforce.

---

## Vantagens da Computação em Nuvem

Adotar a computação em nuvem traz benefícios significativos para organizações de todos os tamanhos:

* **Agilidade**: Lance e itere rapidamente. Em vez de semanas para provisionar hardware, você pode ter recursos de computação em minutos. Isso permite que você experimente e inove com maior velocidade.
* **Elasticidade**: Capacidade de escalar recursos para cima ou para baixo conforme a demanda, de forma automática. Evite o provisionamento excessivo para picos de uso e reduza o desperdício em períodos de baixa demanda.
* **Economia de Custos**: Mude de um modelo de Despesa de Capital (CAPEX) para uma Despesa Operacional (OPEX). Não há necessidade de grandes investimentos iniciais em hardware. Pague apenas pelos recursos que você realmente usa, convertendo custos fixos em variáveis.
* **Implantação Global**: Implante aplicações para usuários em todo o mundo com baixa latência e alta disponibilidade. A AWS possui infraestrutura global distribuída em várias regiões e zonas de disponibilidade.
* **Confiabilidade**: Provedores de nuvem projetam infraestruturas com alta disponibilidade e tolerância a falhas, utilizando redundância em múltiplos data centers.
* **Segurança**: Provedores de nuvem investem massivamente em segurança física e lógica, empregando equipes de segurança especializadas e implementando as melhores práticas e certificações. Isso geralmente oferece um nível de segurança superior ao que a maioria das empresas conseguiria implementar em seu próprio data center.

---

## O que é a AWS?

A **Amazon Web Services (AWS)** é a plataforma de nuvem mais abrangente e amplamente adotada do mundo, oferecendo mais de 200 serviços completos de data centers globais. Milhões de clientes — incluindo as startups que mais crescem, as maiores empresas e as principais agências governamentais — estão usando a AWS para reduzir custos, aumentar a agilidade e inovar mais rapidamente.

---

## Definição de Preços da AWS

O modelo de precificação da AWS é baseado no princípio de "**pague pelo que usar**", o que significa que não há custos iniciais, contratos de longo prazo ou taxas de cancelamento. Você paga apenas pelos serviços de computação, armazenamento e outros recursos que realmente consome.

Os preços podem variar conforme:

* **Tempo de uso**: Para serviços como EC2, você paga por segundo ou por hora de uso.
* **Quantidade de dados**: Para armazenamento S3, você paga pela quantidade de dados armazenados.
* **Número de requisições**: Para serviços como Lambda ou S3, você pode ser cobrado pelo número de invocações ou requisições.
* **Capacidade provisionada**: Em alguns serviços, você pode provisionar uma capacidade específica (ex: IOPS de um volume EBS) e ser cobrado por ela.
* **Transferência de dados**: Geralmente, dados que entram na AWS (inbound) são gratuitos, enquanto dados que saem da AWS (outbound) são cobrados. A transferência de dados entre serviços dentro da mesma região AWS pode ser gratuita ou ter um custo muito baixo.

A AWS oferece ferramentas como a [Calculadora de Preços da AWS](https://calculator.aws/) e o [AWS Cost Explorer](https://aws.amazon.com/aws-cost-management/aws-cost-explorer/) para ajudar os clientes a estimar e otimizar seus gastos.

---

## Visão Geral da Infraestrutura da AWS

A infraestrutura global da AWS é projetada para ser altamente disponível, escalável e tolerante a falhas, distribuída em diversas localizações geográficas:

* **Regiões**: Uma **Região** é uma localização geográfica física isolada onde a AWS hospeda seus data centers. Cada região é projetada para ser completamente independente das outras regiões, isolando falhas e garantindo resiliência. Exemplos incluem "us-east-1" (N. Virginia), "sa-east-1" (São Paulo).
* **Zonas de Disponibilidade (AZs)**: Dentro de cada região, existem duas ou mais **Zonas de Disponibilidade (AZs)**, que são data centers distintos e isolados, mas próximos o suficiente para ter conexões de rede de baixa latência e alta largura de banda. Cada AZ opera em uma infraestrutura de energia, refrigeração e rede independente, garantindo que falhas em uma AZ não afetem outras AZs na mesma região.
* **Edge Locations (Pontos de Presença)**: São data centers menores e mais distribuídos globalmente, usados pelo Amazon CloudFront (CDN) e Amazon Route 53 para armazenar conteúdo em cache e rotear o tráfego de usuários com a menor latência possível. Eles não são AZs nem Regiões.

Essa arquitetura permite que os clientes construam aplicações altamente disponíveis e tolerantes a falhas, distribuindo seus recursos entre diferentes AZs e regiões.

---

## Serviços e Categorias da AWS

A AWS oferece uma vasta gama de serviços, categorizados para facilitar o entendimento:

* **Computação**:
    * **Amazon EC2 (Elastic Compute Cloud)**: Máquinas virtuais redimensionáveis na nuvem.
    * **AWS Lambda**: Execução de código sem provisionamento ou gerenciamento de servidores (serverless).
    * **Amazon ECS (Elastic Container Service) / Amazon EKS (Elastic Kubernetes Service)**: Orquestração e gerenciamento de contêineres Docker e Kubernetes.
    * **AWS Elastic Beanstalk**: Plataforma como Serviço (PaaS) para implantação e escalonamento de aplicações web.
* **Armazenamento**:
    * **Amazon S3 (Simple Storage Service)**: Armazenamento de objetos escalável e durável.
    * **Amazon EBS (Elastic Block Store)**: Volumes de bloco persistentes para instâncias EC2.
    * **Amazon EFS (Elastic File System)**: Sistema de arquivos escalável e compartilhado para instâncias EC2.
    * **Amazon Glacier**: Armazenamento de arquivamento de baixo custo.
* **Banco de Dados**:
    * **Amazon RDS (Relational Database Service)**: Bancos de dados relacionais gerenciados (MySQL, PostgreSQL, Oracle, SQL Server, MariaDB, Aurora).
    * **Amazon DynamoDB**: Banco de dados NoSQL gerenciado, de alta performance e baixa latência.
    * **Amazon Redshift**: Data warehouse para análise de grandes volumes de dados.
    * **Amazon Aurora**: Banco de dados relacional compatível com MySQL/PostgreSQL, com alta performance e escalabilidade.
* **Redes e Entrega de Conteúdo**:
    * **Amazon VPC (Virtual Private Cloud)**: Crie redes virtuais isoladas na nuvem.
    * **Amazon Route 53**: Serviço DNS escalável e de alta disponibilidade.
    * **Amazon CloudFront**: Rede de entrega de conteúdo (CDN) para acelerar a entrega de conteúdo web.
    * **Elastic Load Balancing (ELB)**: Distribuição de tráfego entre múltiplos alvos para alta disponibilidade e escalabilidade.
* **Gerenciamento e Monitoramento**:
    * **Amazon CloudWatch**: Monitoramento de recursos e aplicações AWS.
    * **AWS CloudTrail**: Registro de atividades da conta AWS.
    * **AWS Config**: Avalia, audita e registra configurações de recursos AWS.
    * **AWS Systems Manager**: Gerenciamento de operações automatizadas e seguras.
    * **AWS Organizations**: Gerenciamento de múltiplas contas AWS.
* **Segurança, Identidade e Conformidade**:
    * **AWS IAM (Identity and Access Management)**: Gerenciamento de acesso a serviços e recursos AWS.
    * **AWS WAF (Web Application Firewall)**: Proteção contra ataques web comuns.
    * **AWS Shield**: Proteção contra ataques DDoS.
    * **Amazon GuardDuty**: Detecção de ameaças inteligente.
* **Análise**:
    * **Amazon Athena**: Serviço de consulta interativa para dados no S3 usando SQL.
    * **Amazon Kinesis**: Coleta, processamento e análise de dados de streaming em tempo real.
* **Machine Learning**:
    * **Amazon SageMaker**: Serviço para construir, treinar e implantar modelos de machine learning.
* **Integração de Aplicações**:
    * **Amazon SQS (Simple Queue Service)**: Serviço de fila de mensagens.
    * **Amazon SNS (Simple Notification Service)**: Serviço de notificação.
    * **AWS Step Functions**: Orquestração de fluxos de trabalho serverless.
* **Ferramentas de Desenvolvedor**:
    * **AWS CodeCommit**: Serviço de controle de versão de código.
    * **AWS CodePipeline**: Serviço de entrega contínua.
    * **AWS CloudFormation**: Infraestrutura como Código (IaC).

---

## Modelo de Responsabilidade Compartilhada da AWS

O **Modelo de Responsabilidade Compartilhada** define as responsabilidades da AWS e do cliente em relação à segurança na nuvem. É fundamental entender esse modelo para garantir a segurança dos seus recursos.

* **Responsabilidade da AWS - "Segurança *da* Nuvem"**: A AWS é responsável pela segurança da infraestrutura subjacente que executa os serviços de nuvem. Isso inclui:
    * Proteção física dos data centers.
    * Segurança da rede (hardware, software e instalações de rede).
    * Segurança do hardware de computação, armazenamento e bancos de dados.
    * Manutenção e gerenciamento da infraestrutura global da AWS.
* **Responsabilidade do Cliente - "Segurança *na* Nuvem"**: O cliente é responsável pela segurança na nuvem, ou seja, pela configuração e gerenciamento dos seus próprios recursos implantados na AWS. Isso inclui:
    * **Configuração de Segurança**: Gerenciar o AWS IAM (usuários, grupos, funções, políticas), Security Groups, Network ACLs, políticas de bucket S3, etc.
    * **Dados**: Proteção e criptografia dos seus dados (em trânsito e em repouso).
    * **Sistema Operacional**: Gerenciamento do sistema operacional (patching, configuração) em instâncias EC2.
    * **Aplicações**: Segurança e configuração das aplicações que você executa na AWS.
    * **Rede**: Definição de sub-redes, tabelas de rotas, gateways em sua VPC.

Em resumo, a AWS cuida do "chão" e das "paredes", e você cuida do "mobiliário" e da "segurança da sua casa" dentro da nuvem.

---

## Amazon S3 (Simple Storage Service)

O **Amazon S3** é um serviço de **armazenamento de objetos** altamente escalável, durável, disponível e seguro. Ele é ideal para uma vasta gama de casos de uso:

* Armazenamento de Backup e Restauração: Armazenar backups de dados de aplicações e sistemas.
* Hospedagem de Sites Estáticos: Hospedar arquivos HTML, CSS, JavaScript e imagens para sites estáticos.
* Armazenamento para Análise de Big Data: Servir como data lake para grandes volumes de dados que serão processados por serviços como Athena ou EMR.
* Distribuição de Conteúdo: Usado em conjunto com o CloudFront para cache de conteúdo.
* Armazenamento de Arquivos e Mídia: Imagens, vídeos, documentos.

**Características Principais:**

* **Armazenamento de Objetos**: Os dados são armazenados como objetos em buckets. Cada objeto possui uma chave (nome do arquivo) e metadados.
* **Durabilidade**: Projetado para 11 noves de durabilidade (99.999999999%), o que significa uma probabilidade extremamente baixa de perda de dados. Isso é alcançado replicando dados em múltiplos dispositivos em, no mínimo, três Zonas de Disponibilidade.
* **Disponibilidade**: Alta disponibilidade, geralmente 99.99% para S3 Standard.
* **Classes de Armazenamento**: Oferece diferentes classes para otimizar custo e performance:
    * **S3 Standard**: Para dados acessados com frequência.
    * **S3 Intelligent-Tiering**: Move automaticamente dados entre classes de acesso frequente e infrequente.
    * **S3 Standard-IA (Infrequent Access)**: Para dados acessados com pouca frequência, mas que precisam de acesso rápido quando necessário.
    * **S3 One Zone-IA**: Semelhante ao Standard-IA, mas armazenado em apenas uma AZ (menor custo, menor durabilidade).
    * **S3 Glacier / S3 Glacier Deep Archive**: Para arquivamento de dados de longo prazo com custos muito baixos e tempo de recuperação maior.
* **Segurança**: Suporta criptografia em repouso (SSE-S3, SSE-KMS, SSE-C) e em trânsito (SSL/TLS). As permissões são controladas por políticas de bucket e IAM.
* **Versionamento**: Mantém múltiplas versões de um objeto, protegendo contra exclusões acidentais e sobrescritas.
* **Transferência de Dados**: Suporta upload e download de grandes volumes de dados.

---

## Elastic Compute da AWS (Amazon EC2)

O **Amazon EC2 (Elastic Compute Cloud)** fornece capacidade de computação escalável na nuvem, permitindo que você lance e gerencie máquinas virtuais, chamadas **instâncias EC2**.

**Recursos e Benefícios:**

* **Máquinas Virtuais**: Você pode escolher entre uma variedade de tipos de instâncias com diferentes configurações de CPU, memória, armazenamento e capacidade de rede, otimizadas para diversas cargas de trabalho.
* **Sistemas Operacionais**: Suporta diversos sistemas operacionais, incluindo Linux, Windows Server e macOS.
* **Elasticidade**: Você pode escalar a capacidade de computação para cima ou para baixo em minutos ou segundos, usando o Auto Scaling, para lidar com picos de demanda.
* **Armazenamento**: Instâncias EC2 podem usar volumes Amazon EBS (armazenamento de bloco persistente) ou Armazenamento de Instância (armazenamento temporário, efêmero).
* **Rede**: Instâncias são lançadas dentro de uma Amazon VPC, com controle sobre sub-redes, IPs e Security Groups.
* **Modelos de Pagamento**:
    * **Sob Demanda (On-Demand)**: Pague por hora ou por segundo pelo uso da instância. Ideal para cargas de trabalho irregulares ou de curto prazo.
    * **Instâncias Reservadas (Reserved Instances - RIs)**: Comprometa-se com um período de 1 ou 3 anos para obter descontos significativos (até 75%). Ideal para cargas de trabalho estáveis e previsíveis.
    * **Savings Plans**: Comprometa-se com um determinado uso computacional (em USD/hora) por 1 ou 3 anos para obter descontos maiores do que as RIs para EC2, Fargate e Lambda. Mais flexível que as RIs.
    * **Spot Instances**: Solicite capacidade EC2 não utilizada com até 90% de desconto em relação aos preços sob demanda. Ideal para cargas de trabalho tolerantes a interrupções.
    * **Hosts Dedicados**: Servidores físicos EC2 dedicados ao seu uso, útil para requisitos de licenciamento de software.
* **Amazon Machine Image (AMI)**: Um template pré-configurado que inclui o sistema operacional, software e configurações para lançar uma instância EC2. Você pode usar AMIs fornecidas pela AWS, do AWS Marketplace ou criar suas próprias.

---

## Redes na Nuvem AWS

A AWS fornece uma infraestrutura de rede robusta e flexível para conectar seus recursos na nuvem:

* **Amazon VPC (Virtual Private Cloud)**: Permite que você crie uma rede virtual logicamente isolada na nuvem AWS, onde você pode lançar seus recursos AWS. Você tem controle total sobre seu ambiente de rede virtual, incluindo seleção de intervalos de endereços IP, criação de sub-redes, configuração de tabelas de rotas e gateways de rede.
    * **Sub-redes**: Uma VPC pode ser dividida em sub-redes, que podem ser públicas (com acesso à internet) ou privadas (sem acesso direto à internet). As sub-redes são associadas a Zonas de Disponibilidade para alta disponibilidade.
    * **Internet Gateway**: Componente que permite que as instâncias em uma sub-rede pública se conectem à internet.
    * **NAT Gateway / NAT Instance**: Permite que instâncias em uma sub-rede privada acessem a internet (para baixar atualizações, por exemplo), mas impede conexões de entrada da internet.
    * **Tabelas de Rotas**: Controlam o roteamento do tráfego de rede para sub-redes.
* **Elastic Load Balancing (ELB)**: Distribui o tráfego de entrada entre várias instâncias EC2 em várias Zonas de Disponibilidade, aumentando a tolerância a falhas e a escalabilidade da sua aplicação.
* **Amazon Route 53**: Um serviço de DNS (Domain Name System) altamente disponível e escalável. Permite registrar domínios, rotear o tráfego para recursos AWS e executar verificações de integridade.
* **AWS Direct Connect**: Uma conexão de rede dedicada de alta largura de banda entre seu data center on-premises e a AWS, bypassando a internet pública. Ideal para cargas de trabalho que exigem alta performance e baixa latência.
* **AWS Site-to-Site VPN**: Cria uma conexão criptografada (VPN) entre sua rede on-premises e sua VPC na AWS, usando a internet pública.

---

## Introdução à Segurança

A segurança na AWS é um pilar fundamental e é abordada em múltiplas camadas:

* **Segurança de Infraestrutura (Responsabilidade da AWS)**: A AWS investe pesadamente na segurança física de seus data centers, na segurança da rede (hardware, software, procedimentos) e na segurança dos serviços que oferece. Isso inclui monitoramento 24/7, controles de acesso rigorosos, proteção contra DDoS na camada da infraestrutura e certificações de conformidade.
* **Segurança de Serviços (Recursos Integrados da AWS)**: Muitos serviços da AWS já vêm com recursos de segurança embutidos, como criptografia por padrão, isolamento de recursos, logs de auditoria e integração com o IAM para controle de acesso granular.
* **Segurança do Cliente (Sua Responsabilidade)**: Você é responsável por configurar e gerenciar a segurança dos seus próprios recursos e dados na nuvem. Isso envolve:
    * Gerenciamento de identidades e acessos (IAM).
    * Proteção de rede (Security Groups, Network ACLs, VPCs).
    * Proteção de dados (criptografia em repouso e em trânsito).
    * Gerenciamento de patches e configuração de sistemas operacionais e aplicações.
    * Monitoramento e log de atividades.
    * Resposta a incidentes.

---

## Security Groups da AWS

**Security Groups** atuam como firewalls virtuais que controlam o tráfego de entrada e saída para uma ou mais instâncias EC2. Eles são configurados no nível da instância (ou da interface de rede) e são um dos principais mecanismos de segurança de rede na AWS.

**Características Principais:**

* **Stateful**: Isso significa que se você permitir uma conexão de entrada, o tráfego de resposta correspondente é automaticamente permitido de saída, sem precisar criar uma regra explícita para o tráfego de saída. O mesmo vale para o tráfego de saída.
* **Permissão Explícita**: Security Groups operam com um modelo de permissão explícita. Você só pode permitir o tráfego; não há regras de "negar". Se uma regra não for explicitamente permitida, o tráfego será bloqueado por padrão.
* **Regras de Entrada (Inbound Rules)**: Definem qual tráfego pode entrar nas instâncias associadas (protocolo, porta, origem).
* **Regras de Saída (Outbound Rules)**: Definem qual tráfego pode sair das instâncias associadas (protocolo, porta, destino). Por padrão, todo o tráfego de saída é permitido.
* **Associação**: Uma instância EC2 pode ter múltiplos Security Groups associados, e as regras de todos os Security Groups aplicados são combinadas.
* **Referências**: Você pode referenciar outros Security Groups em suas regras, o que é útil para permitir que instâncias em um Security Group se comuniquem com instâncias em outro Security Group.

**Exemplo**: Para permitir tráfego HTTP (porta 80) e SSH (porta 22) para uma instância EC2 a partir de qualquer lugar da internet, você criaria as seguintes regras de entrada:

* Tipo: HTTP, Protocolo: TCP, Porta: 80, Origem: 0.0.0.0/0
* Tipo: SSH, Protocolo: TCP, Porta: 22, Origem: 0.0.0.0/0

---

## AWS IAM (Identity and Access Management)

O **AWS IAM (Identity and Access Management)** é um serviço web que ajuda você a controlar com segurança o acesso aos seus recursos da AWS. Com o IAM, você pode gerenciar quem (usuários e serviços) pode acessar e como esses usuários ou serviços podem acessar seus recursos.

**Componentes Principais:**

* **Usuários (Users)**: Entidades no IAM que representam pessoas ou aplicações que precisam de acesso a recursos AWS. Podem ter credenciais de acesso (nome de usuário/senha para console e chaves de acesso para API/CLI).
* **Grupos (Groups)**: Coleções de usuários IAM. É uma prática recomendada anexar políticas a grupos e adicionar usuários a esses grupos, em vez de anexar políticas diretamente a usuários individuais.
* **Funções (Roles)**: Entidades do IAM que você pode assumir para conceder permissões temporárias a usuários, serviços ou aplicações que precisam acessar recursos da AWS. Funções são mais flexíveis e seguras que compartilhar credenciais de acesso.
* **Políticas (Policies)**: Documentos (em formato JSON) que definem as permissões de acesso. Elas especificam o que (ações), em quais recursos e sob quais condições uma entidade (usuário, grupo, função) pode executar.
    * **Política Gerenciada pela AWS**: Políticas pré-definidas pela AWS para casos de uso comuns.
    * **Política Gerenciada pelo Cliente**: Políticas personalizadas que você cria para atender às suas necessidades específicas.
    * **Política em Linha**: Políticas incorporadas diretamente a um usuário, grupo ou função.
* **Credenciais de Segurança**:
    * **Credenciais de Login** (Nome de Usuário e Senha): Para acesso ao Console de Gerenciamento da AWS.
    * **Chaves de Acesso** (Access Key ID e Secret Access Key): Para acesso programático via AWS CLI ou SDKs.
    * **Credenciais Temporárias**: Fornecidas por funções IAM, são mais seguras pois expiram após um tempo.

**Princípio do Privilégio Mínimo**: A melhor prática de segurança com IAM é conceder apenas as permissões necessárias para que uma tarefa seja realizada (princípio do privilégio mínimo).

---

## AWS CloudTrail

O **AWS CloudTrail** é um serviço que permite o registro e o monitoramento da atividade da conta AWS. Ele registra as chamadas de API feitas na sua conta, seja por usuários, funções ou serviços AWS.

**Funcionalidades:**

* **Log de Atividades**: Registra ações de gerenciamento (quem fez o quê, quando, onde e de qual IP) em sua conta AWS, como lançar uma instância EC2, criar um bucket S3, modificar uma política IAM, etc.
* **Conformidade e Auditoria**: Fornece um histórico de atividades que pode ser usado para auditoria de segurança, monitoramento de conformidade e solução de problemas.
* **Integração**: Os logs do CloudTrail podem ser entregues a um bucket S3, CloudWatch Logs e até mesmo ao Amazon Athena para análise e consulta.
* **Visibilidade**: Ajuda a ter uma visão clara de todas as ações que ocorrem em sua conta AWS, essencial para investigações de segurança.

---

## AWS Config

O **AWS Config** é um serviço que permite avaliar, auditar e registrar as configurações dos seus recursos da AWS. Ele monitora e registra continuamente as alterações de configuração dos seus recursos, permitindo que você verifique a conformidade com as políticas internas, padrões da indústria e regulamentações.

**Funcionalidades:**

* **Linha do Tempo de Configuração**: Mantém um histórico detalhado de todas as alterações de configuração de um recurso, facilitando a depuração e a auditoria.
* **Regras de Conformidade**: Permite definir regras (gerenciadas pela AWS ou personalizadas) para avaliar se seus recursos estão em conformidade com as melhores práticas de segurança e governança.
* **Detecção de Não Conformidade**: Notifica você quando um recurso entra em estado de não conformidade com as regras definidas.
* **Inventário de Recursos**: Fornece um inventário completo dos seus recursos AWS e suas configurações.
* **Solução de Problemas**: Ajuda a identificar a causa raiz de problemas operacionais ou de segurança, mostrando como as configurações mudaram ao longo do tempo.

---

## AWS Trusted Advisor

O **AWS Trusted Advisor** é uma ferramenta online que age como um "consultor" personalizado para sua conta AWS. Ele examina seu ambiente AWS e fornece recomendações automatizadas para otimizar seus custos, melhorar o desempenho, aumentar a segurança, garantir a tolerância a falhas e verificar limites de serviço.

**Categorias de Análise:**

* **Otimização de Custos**: Identifica oportunidades para economizar dinheiro, como instâncias EC2 ociosas, volumes EBS não utilizados, e recomendações de instâncias reservadas.
* **Performance**: Sugere melhorias para aumentar a velocidade e a capacidade das suas aplicações, como uso de instâncias EC2 otimizadas, configurações de rede.
* **Segurança**: Destaca vulnerabilidades de segurança e recomenda melhores práticas, como uso de IAM, Security Groups abertos, portas de acesso SSH ilimitado.
* **Tolerância a Falhas**: Ajuda a construir aplicações mais resilientes e disponíveis, verificando a distribuição de recursos entre AZs, backups e configurações de balanceamento de carga.
* **Limites de Serviço**: Alerta sobre o uso próximo dos limites de serviço da AWS, evitando interrupções operacionais.
* **Sustentabilidade**: Oferece recomendações para reduzir o impacto ambiental do seu uso da AWS.

O Trusted Advisor é um recurso valioso para manter seu ambiente AWS saudável, seguro e eficiente.

---

## Conformidade de Segurança da AWS

A AWS projeta seus serviços para serem altamente seguros e aderentes a diversos padrões e regulamentações globais e da indústria. Isso facilita para os clientes obterem e manterem sua própria conformidade.

**Exemplos de Conformidade Suportada pela AWS:**

* **ISO 27001, 27017, 27018**: Padrões internacionais para sistemas de gerenciamento de segurança da informação (SGSI).
* **SOC (Service Organization Control) 1, 2, 3**: Relatórios de auditoria sobre controles internos de serviços.
* **PCI DSS Nível 1**: Para empresas que processam, armazenam ou transmitem dados de cartão de crédito.
* **HIPAA (Health Insurance Portability and Accountability Act)**: Regulamentação para proteção de informações de saúde nos EUA.
* **GDPR (General Data Protection Regulation)**: Regulamentação europeia sobre proteção de dados.

A AWS mantém um programa de conformidade contínuo, com auditorias regulares e certificações de terceiros para garantir que seus serviços atendam aos requisitos de segurança e privacidade. Os clientes são responsáveis por garantir que suas aplicações e dados hospedados na AWS também estejam em conformidade com as regulamentações aplicáveis.

---

## Recursos de Segurança da AWS

Além do IAM, Security Groups e CloudTrail, a AWS oferece uma gama de serviços dedicados à segurança:

* **AWS WAF (Web Application Firewall)**: Protege suas aplicações web de exploits comuns na web (como injeção de SQL e cross-site scripting) que podem afetar a disponibilidade, comprometer a segurança ou consumir recursos excessivos.
* **AWS Shield**: Um serviço de proteção contra ataques DDoS (Distributed Denial of Service). Oferece dois níveis:
    * **Standard**: Proteção automática e gratuita para todos os clientes AWS.
    * **Advanced**: Proteção aprimorada para ataques DDoS mais sofisticados, com detecção e mitigação mais rápidas, e acesso à equipe de resposta a incidentes DDoS da AWS (DRT).
* **Amazon GuardDuty**: Um serviço de detecção de ameaças inteligente que monitora continuamente atividades maliciosas e comportamentos não autorizados em sua conta AWS. Ele usa machine learning e inteligência de ameaças para identificar ameaças como criptomineração, acesso incomum a portas e chamadas de API suspeitas.
* **Amazon Macie**: Serviço de segurança e privacidade de dados que usa machine learning para descobrir, classificar e proteger dados sensíveis no Amazon S3. Ele identifica automaticamente dados pessoais identificáveis (PII) e outras informações confidenciais.
* **AWS Key Management Service (KMS)**: Cria e gerencia chaves de criptografia e controla o uso da criptografia em uma ampla gama de serviços AWS.
* **AWS Secrets Manager**: Ajuda a proteger o acesso às suas aplicações, serviços e recursos de TI, permitindo que você gire, gerencie e recupere credenciais de banco de dados, chaves de API e outros segredos durante todo o seu ciclo de vida.

---

## Amazon RDS (Relational Database Service)

O **Amazon RDS (Relational Database Service)** é um serviço de banco de dados relacional gerenciado que facilita a configuração, operação e escalabilidade de bancos de dados relacionais na nuvem. A AWS automatiza tarefas administrativas demoradas, como provisionamento de hardware, aplicação de patches, backups e recuperação de desastres.

**Engines de Banco de Dados Suportados:**

* MySQL
* PostgreSQL
* Oracle
* Microsoft SQL Server
* MariaDB
* **Amazon Aurora**: Um banco de dados relacional compatível com MySQL e PostgreSQL, otimizado para a nuvem AWS, com performance e escalabilidade de nível comercial a um custo menor.

**Funcionalidades Chave:**

* **Gerenciamento**: A AWS gerencia a infraestrutura, o sistema operacional e a manutenção do banco de dados (patching, backups automáticos, replicação).
* **Escalabilidade**: Escala facilmente recursos de computação e armazenamento verticalmente (scaling up) ou horizontalmente (Read Replicas).
* **Alta Disponibilidade**: Configuração de Multi-AZ para failover automático para uma instância de standby em outra Zona de Disponibilidade em caso de falha da instância primária.
* **Backups Automatizados e Snapshots**: Backups diários automáticos e snapshots manuais que podem ser usados para restaurar o banco de dados para qualquer ponto no tempo dentro do período de retenção.
* **Read Replicas**: Crie réplicas somente leitura para escalar a leitura da base de dados e melhorar a performance de aplicações intensivas em leitura. Podem ser em outras regiões para recuperação de desastres.
* **Segurança**: Criptografia em repouso (com KMS) e em trânsito (SSL/TLS). Integração com Security Groups para controle de acesso de rede.

---

## Amazon DynamoDB

O **Amazon DynamoDB** é um serviço de banco de dados NoSQL totalmente gerenciado, sem servidor, que oferece alta performance e baixa latência em qualquer escala. É ideal para aplicações que exigem performance consistente com volumes massivos de dados.

**Características Principais:**

* **NoSQL**: Banco de dados de chave-valor e documento, flexível para dados não estruturados ou semi-estruturados.
* **Totalmente Gerenciado e Serverless**: Não há servidores para provisionar ou gerenciar. A AWS cuida da infraestrutura, escalabilidade, patches e backups.
* **Alta Performance**: Oferece latência de milissegundos de um dígito em qualquer escala, mesmo com petabytes de dados e milhões de requisições por segundo.
* **Escalabilidade Automática**: Escala automaticamente a capacidade de throughput e armazenamento para atender às demandas da sua aplicação.
* **Durabilidade e Alta Disponibilidade**: Dados são armazenados em três Zonas de Disponibilidade dentro de uma região para alta durabilidade e resiliência.
* **Consistência de Leitura**: Suporta consistência de leitura eventual (padrão) e consistência de leitura forte (garante que você sempre obterá a versão mais recente do dado).
* **Streams do DynamoDB**: Registra todas as modificações de dados em uma tabela, permitindo a replicação para outras tabelas ou a execução de funções Lambda em resposta a eventos.
* **Backup e Restauração**: Backups point-in-time e on-demand.
* **Segurança**: Criptografia em repouso por padrão, controle de acesso granular com IAM.

---

## AWS Cloud Adoption Framework (CAF)

O **AWS Cloud Adoption Framework (CAF)** é um guia da AWS para ajudar as organizações a planejar e executar uma transição bem-sucedida para a computação em nuvem. Ele estrutura as discussões e oferece orientações para desenvolver um plano abrangente de adoção da nuvem.

O CAF é dividido em seis perspectivas, cada uma abordando diferentes aspectos da organização:

* **Perspectiva de Negócios**: Foca em alinhar os objetivos de negócios com a estratégia de nuvem, demonstrando valor e gerenciando finanças.
* **Perspectiva de Pessoas**: Lida com o desenvolvimento de novas habilidades, treinamentos, adaptação de funções e cultura organizacional.
* **Perspectiva de Governança**: Estabelece a liderança, processos, controles e responsabilidades para gerenciar e otimizar o ambiente de nuvem.
* **Perspectiva de Plataforma**: Define a arquitetura e os serviços técnicos a serem usados na nuvem, incluindo a escolha de ferramentas e tecnologias.
* **Perspectiva de Segurança**: Garante a proteção de dados, sistemas e aplicações na nuvem, definindo políticas e implementando controles de segurança.
* **Perspectiva de Operações**: Foca em como operar, monitorar e otimizar a infraestrutura e as aplicações na nuvem, incluindo gerenciamento de incidentes e automação.

---

## AWS Well-Architected Framework

O **AWS Well-Architected Framework** é um conjunto de princípios e melhores práticas para arquitetar sistemas na nuvem que sejam confiáveis, seguros, eficientes, econômicos e sustentáveis. Ele fornece um guia para projetar, construir e operar aplicações e cargas de trabalho na AWS.

O Framework é baseado em seis pilares:

* **Excelência Operacional**: Capacidade de executar e monitorar sistemas para entregar valor de negócios e melhorar continuamente os processos e procedimentos de suporte.
* **Segurança**: Capacidade de proteger dados, sistemas e ativos para aproveitar as tecnologias de nuvem e aprimorar sua postura de segurança.
* **Confiabilidade**: Capacidade de um sistema de se recuperar de falhas, adquirir e recuperar recursos de computação para atender à demanda e mitigar interrupções.
* **Eficiência de Performance**: Capacidade de usar recursos de computação de forma eficiente para atender aos requisitos do sistema e manter essa eficiência à medida que a demanda muda.
* **Otimização de Custos**: Capacidade de evitar custos desnecessários.
* **Sustentabilidade**: Foco na redução do impacto ambiental das cargas de trabalho na nuvem.

A AWS oferece uma ferramenta, o [Well-Architected Tool](https://aws.amazon.com/well-architected/aws-well-architected-tool/), para ajudar os clientes a revisar suas arquiteturas em relação a esses pilares e identificar áreas para melhoria.

---

## Design do Well-Architected

O **Design do Well-Architected** é a aplicação prática dos princípios e pilares do AWS Well-Architected Framework no processo de criação de arquiteturas na nuvem. Envolve a tomada de decisões de design que levam a sistemas:

* **Resilientes**: Capazes de suportar falhas e se recuperar rapidamente.
* **Seguros**: Com controles de acesso e proteção de dados adequados.
* **Performáticos**: Que atendem aos requisitos de velocidade e capacidade.
* **Eficientes**: Utilizando os recursos de forma otimizada.
* **Econômicos**: Maximizando o valor pelo investimento.
* **Sustentáveis**: Com foco na redução do consumo de energia e recursos.

Ao projetar sistemas na AWS, é crucial considerar esses pilares desde as fases iniciais do projeto, não apenas como uma reflexão tardia. Isso leva a arquiteturas mais robustas e sustentáveis a longo prazo.

---

## Confiabilidade e Alta Disponibilidade

**Confiabilidade** e **Alta Disponibilidade** são conceitos críticos na arquitetura de nuvem:

* **Confiabilidade**: A capacidade de um sistema de funcionar corretamente e de forma consistente ao longo do tempo, mesmo diante de falhas. Isso envolve:
    * **Tolerância a Falhas**: Projetar o sistema para continuar operando mesmo quando componentes individuais falham.
    * **Resiliência**: A capacidade de um sistema de se recuperar rapidamente de falhas.
    * **Recuperação de Desastres**: Planos e estratégias para restaurar operações após um desastre maior (ex: falha de uma região inteira).
    * **Backup e Restauração**: Geração regular de cópias de segurança dos dados e capacidade de restaurá-los.
* **Alta Disponibilidade**: Garante que um sistema esteja acessível e operacional para os usuários por uma porcentagem muito alta do tempo. Isso é alcançado através de:
    * **Redundância**: Duplicação de componentes críticos para evitar um único ponto de falha.
    * **Múltiplas Zonas de Disponibilidade (AZs)**: Distribuir recursos entre várias AZs para proteção contra falhas em um único data center.
    * **Balanceamento de Carga (ELB)**: Distribuir o tráfego entre múltiplos recursos.
    * **Auto Scaling**: Ajustar automaticamente a capacidade para lidar com a demanda e substituir instâncias com problemas.
    * **Failover**: Mecanismos para redirecionar automaticamente o tráfego para componentes saudáveis em caso de falha.

Na AWS, serviços como ELB, Auto Scaling, RDS Multi-AZ e a distribuição de recursos em múltiplas AZs são fundamentais para construir arquiteturas confiáveis e altamente disponíveis.

---

## Transição de um Data Center para a Nuvem

A transição de um data center on-premises para a nuvem AWS é um processo estratégico que pode ser abordado de várias maneiras. A AWS sugere a estratégia dos "**6 R's**" de Estratégias de Migração:

* **Rehost (Lift-and-Shift)**: Mover aplicações como estão, sem grandes alterações de código, para a nuvem (ex: migrar VMs para instâncias EC2). É a abordagem mais rápida para começar.
* **Replatform (Lift-Tinker-and-Shift)**: Mover aplicações para a nuvem, mas fazendo algumas otimizações para aproveitar os recursos nativos da nuvem (ex: migrar para RDS em vez de gerenciar um banco de dados em EC2).
* **Refactor/Rearchitect**: Reprojetar e reescrever partes da aplicação para aproveitar totalmente os serviços nativos da nuvem (ex: migrar para microserviços e AWS Lambda). Oferece o maior potencial de otimização e inovação, mas é a mais demorada.
* **Repurchase (Drop-and-Shop)**: Migrar para um produto SaaS diferente. (ex: migrar de um CRM on-premises para Salesforce).
* **Retain (Revisitar)**: Manter algumas aplicações no ambiente on-premises, geralmente devido a requisitos de conformidade, dependências complexas ou baixo benefício de migração.
* **Retire**: Desativar aplicações e recursos que não são mais necessários após a migração.

A escolha da estratégia depende de fatores como custo, cronograma, complexidade da aplicação e objetivos de negócios.

---

## AWS Identity and Access Management (Revisão)

(Este tópico já foi coberto em detalhes acima, mas a revisão sugere que é um ponto de reforço na prova, indicando sua importância.)

**Revisão do IAM**: O IAM é o coração da segurança na AWS. Lembre-se que ele permite:

* Criar e gerenciar **Usuários**, **Grupos** e **Funções**.
* Aplicar **Políticas** para definir permissões granulares.
* Garantir o **Princípio do Privilégio Mínimo** (conceder apenas as permissões essenciais).
* Proporcionar **Credenciais Temporárias** via funções, que são mais seguras do que credenciais estáticas.
* Autenticar usuários no Console de Gerenciamento e para acesso programático via CLI/SDKs.

---

## AWS Command Line Interface (CLI)

A **AWS Command Line Interface (CLI)** é uma ferramenta unificada que permite interagir com os serviços da AWS a partir do seu terminal de comando ou scripts. Ela oferece uma alternativa programática e automatizada ao Console de Gerenciamento da AWS.

**Funcionalidades:**

* **Automação**: Permite automatizar tarefas repetitivas, como provisionamento de recursos, gerenciamento de instâncias, uploads para S3.
* **Scripting**: Integra-se facilmente com scripts Bash, PowerShell ou Python para construir fluxos de trabalho complexos.
* **Gerenciamento Completo**: A maioria dos serviços da AWS pode ser gerenciada através da CLI.
* **Configuração**: É necessário configurar a CLI com suas credenciais de acesso (Access Key ID e Secret Access Key, geralmente de um usuário IAM com as permissões apropriadas) e a região padrão.
* **Sintaxe Comum**: `aws [service] [command] [parameters]`. Ex: `aws s3 ls`, `aws ec2 run-instances`.

---

## AWS Systems Manager

O **AWS Systems Manager** é uma coleção de ferramentas que ajuda você a visualizar e controlar a sua infraestrutura na AWS e on-premises. Ele simplifica o gerenciamento de recursos, automatiza operações, e ajuda a garantir a conformidade e a segurança.

**Principais Recursos:**

* **Operations Dashboard**: Fornece uma visão unificada do status operacional de seus recursos AWS.
* **Patch Manager**: Automação do processo de aplicação de patches em instâncias.
* **Run Command**: Execute comandos remotamente em suas instâncias EC2 e servidores on-premises.
* **State Manager**: Define e mantém um estado consistente de suas instâncias.
* **Inventory**: Coleta e gerencia o inventário de software e configurações de suas instâncias.
* **Parameter Store**: Armazena e gerencia dados de configuração e segredos.
* **Session Manager**: Acesso seguro e auditável a suas instâncias sem a necessidade de abrir portas de entrada ou gerenciar chaves SSH.
* **Automation**: Automatiza tarefas operacionais comuns.

O Systems Manager é fundamental para a excelência operacional e o gerenciamento eficiente de grandes frotas de instâncias.

---

## Ferramentas de Administração e Desenvolvimento

A AWS oferece um conjunto de ferramentas para gerenciar e desenvolver soluções na nuvem:

* **AWS Management Console**: Interface gráfica baseada em navegador para gerenciar serviços AWS.
* **AWS Command Line Interface (CLI)**: Ferramenta de linha de comando para interação programática.
* **AWS SDKs (Software Development Kits)**: Kits de ferramentas para desenvolvedores em várias linguagens de programação (Java, Python, Node.js, .NET, Go, etc.) para interagir com os serviços AWS a partir do seu código.
* **AWS CloudFormation**: Serviço para Infraestrutura como Código (IaC), permitindo provisionar recursos AWS de forma declarativa usando templates.
* **AWS CodeSuite**: Conjunto de serviços para o ciclo de vida de desenvolvimento de software (DevOps):
    * **CodeCommit**: Serviço de controle de versão (Git gerenciado).
    * **CodeBuild**: Serviço de compilação de código.
    * **CodeDeploy**: Automatiza a implantação de código em instâncias.
    * **CodePipeline**: Orquestra pipelines de entrega contínua.
* **Amazon CloudWatch**: Monitoramento e observabilidade.
* **AWS X-Ray**: Analisa e depura aplicações distribuídas.
* **AWS CodeStar**: Ajuda a configurar rapidamente projetos de desenvolvimento na AWS com um pipeline de CI/CD.

---

## Hospedar um Site Estático no S3 da AWS

Hospedar um site estático no **Amazon S3** é uma solução econômica, escalável e altamente disponível para sites que não exigem processamento no lado do servidor (como HTML, CSS, JavaScript, imagens, vídeos).

**Passos Básicos:**

1.  **Crie um Bucket S3**: O nome do bucket deve ser o mesmo que o nome de domínio (ex: `meusite.com`).
2.  **Habilite a Hospedagem de Site Estático**: Nas propriedades do bucket S3, ative a opção "Static website hosting". Configure o documento de índice (ex: `index.html`) e, opcionalmente, o documento de erro (ex: `error.html`).
3.  **Faça Upload dos Arquivos**: Faça upload de todos os arquivos do seu site estático (HTML, CSS, JS, imagens) para o bucket S3.
4.  **Configure Permissões de Leitura Pública**: Edite as políticas de bucket para permitir que os objetos sejam lidos publicamente (normalmente, uma política de bucket que permita `s3:GetObject` para `*` para o principal `*` para o bucket e seus objetos).
5.  **Configure o DNS (Opcional, com Route 53)**: Para usar um domínio personalizado, você pode configurar um registro ALIAS ou CNAME no Amazon Route 53 que aponte para o endpoint de hospedagem de site estático do seu bucket S3.
6.  **Use CloudFront (Opcional)**: Para melhorar a performance e adicionar HTTPS, você pode usar o Amazon CloudFront como uma CDN na frente do seu bucket S3.

---

## Visão Geral da Computação (Servidores)

A AWS oferece uma variedade de serviços de computação para atender a diferentes necessidades e modelos operacionais:

* **Amazon EC2 (Elastic Compute Cloud)**: O serviço IaaS (Infraestrutura como Serviço) fundamental. Permite provisionar e gerenciar máquinas virtuais (servidores) com controle total sobre o sistema operacional e software. Ideal para cargas de trabalho que exigem personalização profunda do servidor.
* **AWS Lambda**: O serviço FaaS (Função como Serviço) ou "serverless". Você executa seu código em resposta a eventos sem precisar provisionar ou gerenciar servidores. Paga apenas pelo tempo de computação consumido. Ideal para funções de processamento de eventos, backends de API e tarefas assíncronas.
* **Amazon ECS (Elastic Container Service) / Amazon EKS (Elastic Kubernetes Service) / AWS Fargate**: Para aplicações conteinerizadas.
    * **ECS**: Serviço de orquestração de contêineres nativo da AWS.
    * **EKS**: Serviço Kubernetes gerenciado.
    * **Fargate**: Um mecanismo de computação serverless para ECS e EKS, eliminando a necessidade de provisionar e gerenciar servidores (instâncias EC2) para seus contêineres. Você só define os recursos (CPU, memória) que seus contêineres precisam.
* **AWS Elastic Beanstalk**: Um serviço PaaS (Plataforma como Serviço). Simplifica a implantação e o escalonamento de aplicações web, abstraindo a complexidade da infraestrutura subjacente (EC2, ELB, Auto Scaling). Você só precisa enviar seu código.

---

## Computação na AWS (Revisão)

(Este tópico já foi coberto em "Visão Geral da Computação (Servidores)", mas a revisão sugere que é um ponto de reforço na prova.)

**Resumo dos Serviços de Computação:**

* **IaaS (Infrastructure as a Service)**: EC2 - você gerencia a infraestrutura.
* **PaaS (Platform as a Service)**: Elastic Beanstalk - você gerencia a aplicação, a AWS a plataforma.
* **FaaS (Function as a Service) / Serverless**: Lambda - você gerencia o código, a AWS tudo o mais.
* **Containers**: ECS, EKS, Fargate - para cargas de trabalho baseadas em contêineres, com Fargate oferecendo uma opção serverless.

A escolha do serviço depende do nível de controle desejado, da granularidade de faturamento e da complexidade da sua aplicação.

---

## Gerenciar Instâncias da AWS

O gerenciamento de instâncias EC2 envolve diversas ações ao longo do seu ciclo de vida:

* **Lançar (Launch)**: Iniciar uma nova instância a partir de uma AMI, selecionando o tipo de instância, VPC, Security Group, chave SSH e outras configurações.
* **Iniciar (Start)**: Ligar uma instância que estava parada. A instância retém seu IP público elástico (se houver) e armazenamento de bloco (EBS). Você é cobrado pelo uso de computação.
* **Parar (Stop)**: Desligar uma instância. Os dados no armazenamento de instância são perdidos, mas os dados nos volumes EBS persistem. Você não é cobrado pela computação, apenas pelo armazenamento EBS.
* **Hibernar (Hibernate)**: Parar uma instância e manter o conteúdo da memória RAM e os volumes EBS. A instância reinicia mais rapidamente, mas é cobrado pelo armazenamento em disco da RAM.
* **Reiniciar (Reboot)**: Reiniciar a instância, como um reboot de um servidor físico. Os dados não são perdidos.
* **Encerrar (Terminate)**: Desligar e deletar permanentemente a instância. Todos os dados no armazenamento de instância são perdidos, e os volumes EBS podem ser configurados para serem deletados. A instância não pode ser recuperada.
* **Conectar**: Acessar a instância via SSH (Linux) ou RDP (Windows), geralmente usando um par de chaves ou o Session Manager.
* **Monitorar**: Usar o Amazon CloudWatch para monitorar métricas (CPU, rede, disco) e logs da instância.
* **Dimensionar (Scale)**: Alterar o tipo de instância (escalar verticalmente) ou usar Auto Scaling para adicionar/remover instâncias (escalar horizontalmente).

---

## Visão Geral do Laboratório: Instâncias do EC2

Um laboratório prático de EC2 tipicamente cobriria:

* **Lançar uma instância EC2**:
    * Escolher uma AMI (ex: Amazon Linux, Ubuntu).
    * Selecionar um tipo de instância (ex: t2.micro - camada gratuita).
    * Configurar detalhes da instância (VPC, sub-rede, atribuir IP público).
    * Adicionar armazenamento (volume EBS).
    * Adicionar tags.
    * Criar ou selecionar um Security Group (permitir SSH, HTTP).
    * Criar um par de chaves (key pair) para acesso SSH.
    * Revisar e lançar a instância.
* **Conectar-se à instância**:
    * Via SSH usando o par de chaves (Linux).
    * Via RDP (Windows).
    * Alternativamente, usar o AWS Systems Manager Session Manager.
* **Configurar um servidor web (opcional)**: Instalar Apache ou Nginx e servir uma página HTML simples.
* **Monitorar a instância**: Verificar métricas básicas no CloudWatch.
* **Gerenciar o ciclo de vida**: Parar, iniciar e encerrar a instância.

---

## Demonstração do AWS IAM-2

(Este é um reforço para uma demonstração prática. Já foi abordado em detalhes em "AWS IAM (Identity and Access Management)".)

Uma demonstração de IAM geralmente inclui:

* **Criação de um Usuário IAM**: Definindo um nome de usuário, tipo de acesso (console, programático) e senha.
* **Criação de um Grupo IAM**: Adicionando o usuário a um grupo.
* **Anexar Políticas a um Grupo**: Concedendo permissões a um grupo (ex: `AmazonS3ReadOnlyAccess`).
* **Testar Acesso**: Logar com o usuário recém-criado e verificar se ele pode acessar apenas os recursos permitidos pela política.
* **Criação de uma Função IAM**: Demonstrar como uma função pode ser usada para conceder permissões temporárias a um serviço (ex: uma função EC2 para acessar S3).
* **Acessar com CLI/SDK**: Configurar a AWS CLI com as chaves de acesso do usuário IAM e executar comandos.

---

## AWS Elastic Beanstalk

O **AWS Elastic Beanstalk** é um serviço PaaS (Plataforma como Serviço) fácil de usar para implantar e escalar aplicações web e serviços desenvolvidos com diversas linguagens de programação e servidores web (Java, .NET, PHP, Node.js, Python, Ruby, Go, Docker).

**Como Funciona:**

* Você carrega seu código.
* O Elastic Beanstalk automaticamente lida com o provisionamento de capacidade, balanceamento de carga, escalonamento automático e monitoramento de saúde da aplicação.
* Ele provisiona e gerencia a infraestrutura subjacente (instâncias EC2, Elastic Load Balancers, grupos de Auto Scaling, S3) sem que você precise configurá-los manualmente.
* Você tem controle sobre as configurações do ambiente e pode acessar os recursos subjacentes se precisar de maior controle.

**Benefícios:**

* **Simplicidade**: Simplifica a implantação de aplicações.
* **Produtividade**: Permite que os desenvolvedores se concentrem no código, não na infraestrutura.
* **Escalabilidade**: Escala automaticamente para atender à demanda.
* **Custo-benefício**: Paga apenas pelos recursos AWS subjacentes que o Beanstalk provisiona.

É uma ótima opção para equipes que desejam implantar aplicações rapidamente sem se aprofundar na complexidade da infraestrutura.

---

## Visão Geral de Escalabilidade e Resolução de Nomes

* **Escalabilidade**: A capacidade de um sistema de lidar com uma carga de trabalho crescente. Na AWS, é alcançada principalmente por:
    * **Escalabilidade Horizontal (Scale Out)**: Adicionar mais instâncias (ex: com Auto Scaling) para distribuir a carga. Preferível para a nuvem.
    * **Escalabilidade Vertical (Scale Up)**: Aumentar os recursos de uma única instância (ex: um tipo de instância EC2 maior). Tem limites.
    * **Elastic Load Balancing (ELB)**: Distribui o tráfego de entrada para múltiplos alvos, permitindo a escalabilidade horizontal e alta disponibilidade.
    * **Amazon EC2 Auto Scaling**: Ajusta automaticamente o número de instâncias EC2 com base na demanda definida por métricas (CPU, rede, requisições).
* **Resolução de Nomes (DNS)**: Traduz nomes de domínio legíveis por humanos (ex: `google.com`) em endereços IP (ex: `172.217.160.142`) que os computadores usam para se comunicar.
    * **Amazon Route 53**: Serviço DNS gerenciado e escalável da AWS, usado para registrar domínios e rotear o tráfego para os recursos da AWS e fora dela. Suporta vários tipos de registros (A, CNAME, MX, etc.) e políticas de roteamento avançadas (latência, geolocalização, failover).

---

## Elastic Load Balancing (ELB)

O **Elastic Load Balancing (ELB)** distribui automaticamente o tráfego de entrada entre vários alvos (como instâncias EC2, contêineres, funções Lambda) em várias Zonas de Disponibilidade. Isso aumenta a tolerância a falhas, a escalabilidade e a disponibilidade da sua aplicação.

**Tipos de Load Balancers:**

* **Application Load Balancer (ALB)**:
    * Opera na Camada 7 (HTTP/HTTPS).
    * Ideal para aplicações web e microserviços.
    * Suporta roteamento baseado em conteúdo (host, caminho, cabeçalhos HTTP), permitindo rotear requisições para diferentes grupos de destino com base no conteúdo da URL.
    * Suporta TLS/SSL Offloading (o ELB gerencia os certificados e a criptografia).
    * Suporta balanceamento de carga para contêineres e funções Lambda.
* **Network Load Balancer (NLB)**:
    * Opera na Camada 4 (TCP/UDP/TLS).
    * Projetado para lidar com milhões de requisições por segundo com latência ultrabaixa.
    * Ideal para cargas de trabalho que exigem alta performance e baixo overhead.
    * Suporta endereços IP estáticos.
    * Não inspeciona o conteúdo do tráfego (não tem roteamento baseado em conteúdo).
* **Gateway Load Balancer (GLB)**:
    * Opera na Camada 3 (IP).
    * Usado para implantar e dimensionar appliances virtuais de terceiros, como firewalls, sistemas de prevenção de intrusões (IPS) e outros dispositivos de rede.

---

## Listeners do Elastic Load Balancer

Um **Listener** em um Elastic Load Balancer é um processo que verifica solicitações de conexão de clientes, usando o protocolo e a porta que você configurar. Ele então encaminha as solicitações para um grupo de destino (target group), conforme as regras de roteamento.

**Configuração de um Listener:**

* **Protocolo e Porta do Front-end**: O protocolo (ex: HTTP, HTTPS, TCP, TLS) e a porta (ex: 80, 443) em que o load balancer ouve as conexões de entrada.
* **Grupo de Destino Padrão**: O grupo de destino para o qual o tráfego é roteado por padrão, se nenhuma outra regra for correspondida.
* **Regras (para ALB)**: Para Application Load Balancers, você pode definir regras baseadas em caminhos da URL, cabeçalhos HTTP, métodos HTTP ou parâmetros de consulta para rotear o tráfego para diferentes grupos de destino.

**Exemplo**: Um ALB pode ter um listener na porta 80 (HTTP) que encaminha todo o tráfego para um grupo de destino de instâncias EC2. Se você adicionar um certificado SSL/TLS, pode adicionar um listener na porta 443 (HTTPS) que também encaminha para o mesmo grupo de destino ou para um diferente, dependendo das regras.

---

## Auto Scaling do Amazon EC2

O **Auto Scaling do Amazon EC2** ajuda você a manter a disponibilidade da aplicação e permite que você dimensione a capacidade do EC2 automaticamente para cima ou para baixo de acordo com as condições que você definir. Ele garante que você tenha o número correto de instâncias EC2 para lidar com a demanda da sua aplicação.

**Componentes Principais:**

* **Grupos de Auto Scaling (Auto Scaling Groups - ASGs)**: São as coleções de instâncias EC2 que são gerenciadas pelo Auto Scaling. Você define o tamanho mínimo, máximo e desejado de instâncias no ASG.
* **Configuração de Lançamento / Modelo de Lançamento (Launch Configuration / Launch Template)**: Um template que o ASG usa para lançar novas instâncias. Define a AMI, tipo de instância, Security Group, par de chaves, dados do usuário (user data) e outras configurações. Launch Templates são a opção mais recente e flexível, permitindo várias versões.
* **Políticas de Escalamento (Scaling Policies)**: Regras que definem como o ASG deve escalar.
    * **Escalamento Simples**: Ajusta o número de instâncias com base em uma única métrica do CloudWatch (ex: aumentar em 2 instâncias se a CPU > 70%).
    * **Escalamento de Etapa**: Permite diferentes ajustes com base em diferentes limites de métricas.
    * **Escalamento de Rastreamento de Destino (Target Tracking)**: Mantém uma métrica em um valor alvo (ex: manter a utilização da CPU em 50%). É o mais fácil de configurar e o mais recomendado.
    * **Escalamento Agendado**: Escala com base em um cronograma (ex: aumentar instâncias às 9h e diminuir às 17h).
* **Verificações de Saúde (Health Checks)**: O Auto Scaling monitora a saúde das instâncias e substitui automaticamente instâncias que falham em suas verificações de saúde. Pode integrar-se com verificações de saúde do ELB.

---

## Visão Geral do Laboratório: Auto Scaling do EC2

Um laboratório prático de Auto Scaling envolveria:

* **Criação de um Load Balancer (ALB)**: Para distribuir o tráfego entre as instâncias do ASG.
* **Criação de um Modelo de Lançamento**: Definindo a AMI, tipo de instância, Security Group (permitindo tráfego do ELB), e um script user data para instalar um servidor web e criar uma página de teste.
* **Criação de um Grupo de Auto Scaling**:
    * Especificar o modelo de lançamento.
    * Definir o tamanho mínimo, máximo e desejado (ex: min 1, max 3, desired 1).
    * Associar o ASG ao ELB e sub-redes.
* **Configurar uma Política de Escalamento**:
    * Usar uma política de rastreamento de destino para a utilização da CPU (ex: manter CPU em 50%).
    * Verificar o escalamento aumentando a carga na instância (ex: usar um script para gerar CPU load).
* **Verificar a operação**: Observar as instâncias sendo lançadas/encerradas no console EC2 e a performance do ELB.

---

## Desafio de Previsão de Auto Scaling

Este desafio se refere a cenários onde a carga de trabalho é previsível e segue padrões conhecidos (ex: pico de tráfego de manhã e à noite). Nesses casos, em vez de depender apenas de métricas de CPU ou rede, que respondem depois que a demanda já aumentou, você pode usar o **escalamento agendado (Scheduled Scaling)** no Auto Scaling.

**Como funciona:**

* Você define horários específicos nos quais o grupo de Auto Scaling deve aumentar ou diminuir sua capacidade.
* Exemplo: Aumentar a capacidade para um mínimo de 5 instâncias às 8h da manhã e diminuir para 2 instâncias às 18h, todos os dias de semana.

Isso ajuda a pré-provisionar a capacidade antes do aumento da demanda, garantindo uma melhor experiência do usuário e evitando problemas de performance durante os picos.

---

## Amazon Route 53

O **Amazon Route 53** é um serviço DNS (Domain Name System) altamente disponível e escalável. Ele é usado para:

* **Registro de Domínio**: Você pode registrar novos nomes de domínio diretamente através do Route 53.
* **Roteamento de Tráfego**: Roteia o tráfego da internet para recursos hospedados na AWS (instâncias EC2, buckets S3, Load Balancers) e também para recursos fora da AWS.
* **Verificações de Integridade (Health Checks)**: Monitora a saúde dos seus recursos e pode rotear o tráfego para endpoints saudáveis em caso de falha.
* **Gerenciamento de Zonas Hospedadas (Hosted Zones)**: Contém os registros DNS (A, CNAME, MX, NS, SOA, TXT, etc.) para um domínio específico.
* **Políticas de Roteamento**: Suporta diferentes políticas para rotear o tráfego:
    * **Simple**: Roteia todo o tráfego para um único recurso.
    * **Weighted**: Distribui o tráfego entre múltiplos recursos com base em pesos definidos.
    * **Latency-based**: Roteia o tráfego para a região AWS com a menor latência.
    * **Geolocation**: Roteia o tráfego com base na localização geográfica do usuário.
    * **Failover**: Roteia o tráfego para um recurso primário e, em caso de falha, para um recurso secundário.
    * **Multivalue Answer**: Retorna múltiplos valores (IPs) para um único registro, permitindo que os clientes escolham um deles (usado para balanceamento de carga básico).

---

## Demonstração do Amazon Route 53-2

(Este é um reforço para uma demonstração prática. Já foi abordado em detalhes em "Amazon Route 53".)

Uma demonstração do Route 53 tipicamente inclui:

* **Criação de uma Zona Hospedada**: Para um domínio que você possui (ou um subdomínio).
* **Criação de Registros DNS**:
    * Criação de um registro A apontando para o IP público de uma instância EC2 ou um Elastic Load Balancer.
    * Criação de um registro CNAME para um alias.
    * Configuração de um registro ALIAS para um bucket S3 configurado para hospedagem de site estático ou um CloudFront distribution.
* **Configuração de Verificações de Integridade (opcional)**: Para monitorar a saúde de um endpoint e usar isso com uma política de failover.
* **Testar a Resolução de Nomes**: Usar ferramentas como `dig` ou `nslookup` para verificar se o DNS está resolvendo corretamente.

---

## Amazon CloudFront

O **Amazon CloudFront** é um serviço de **Rede de Entrega de Conteúdo (CDN - Content Delivery Network)** que acelera a entrega de conteúdo web estático e dinâmico aos usuários. Ele faz isso distribuindo o conteúdo para Edge Locations (pontos de presença) em todo o mundo.

**Como Funciona:**

* Quando um usuário solicita conteúdo (ex: imagem), o CloudFront direciona a requisição para o Edge Location mais próximo.
* Se o conteúdo estiver em cache no Edge Location, ele é entregue diretamente, reduzindo a latência.
* Se não estiver em cache, o Edge Location busca o conteúdo na origem (ex: bucket S3, ALB, EC2, ou qualquer servidor web).
* O conteúdo é então armazenado em cache no Edge Location e entregue ao usuário.

**Benefícios:**

* **Baixa Latência**: Entrega conteúdo mais rapidamente para usuários globais.
* **Redução de Carga no Servidor de Origem**: Diminui o número de requisições diretas ao seu servidor.
* **Segurança**: Integra-se com AWS WAF e AWS Shield para proteção adicional.
* **HTTPS**: Suporta HTTPS (SSL/TLS) em seus domínios personalizados.
* **Custo-benefício**: Reduz os custos de transferência de dados da sua origem, já que a maioria das requisições é atendida pelo cache do CloudFront.

---

## AWS Lambda

O **AWS Lambda** é um serviço de **computação serverless (sem servidor)** que permite executar código sem provisionar ou gerenciar servidores. Você só precisa carregar seu código, e o Lambda cuida de todo o resto: provisionamento de capacidade, escalonamento, patches, manutenção do sistema operacional e do hardware.

**Como Funciona:**

* Você escreve seu código (em várias linguagens: Node.js, Python, Java, C#, Go, Ruby).
* Você define um gatilho (trigger) para a função Lambda (ex: upload de um arquivo para S3, uma requisição HTTP via API Gateway, uma mensagem em uma fila SQS, um evento do CloudWatch).
* Quando o gatilho é acionado, o Lambda executa sua função.
* Você paga apenas pelo número de invocações e pelo tempo de execução do seu código (em milissegundos).

**Casos de Uso:**

* **Processamento de Eventos**: Redimensionamento de imagens após upload para S3, processamento de logs.
* **Backends de APIs**: Construir APIs RESTful com API Gateway.
* **Processamento de Dados em Tempo Real**: Responder a streams de dados do Kinesis ou DynamoDB.
* **Tarefas Agendadas (Cron Jobs)**: Executar tarefas em horários específicos.

**Benefícios:**

* **Serverless**: Não há servidores para gerenciar.
* **Escalabilidade Automática**: Escala automaticamente para milhões de requisições.
* **Custo-benefício**: Paga apenas pelo que usa, sem custo quando o código não está em execução.
* **Alta Disponibilidade Integrada**.

---

## APIs e REST da Amazon

* **API (Application Programming Interface)**: É um conjunto de definições e protocolos que permite que diferentes softwares se comuniquem uns com os outros. No contexto da AWS, as APIs da Amazon são as interfaces através das quais os desenvolvedores e serviços interagem programaticamente com os serviços da AWS (ex: a CLI e os SDKs usam as APIs da AWS).
* **REST (Representational State Transfer)**: É um estilo arquitetural para projetar APIs web. APIs RESTful usam o protocolo HTTP e seus métodos padrão (GET, POST, PUT, DELETE) para interagir com recursos.
    * **GET**: Recuperar dados.
    * **POST**: Criar novos dados.
    * **PUT**: Atualizar dados existentes.
    * **DELETE**: Excluir dados.

As APIs da AWS são em grande parte APIs RESTful.

---

## Amazon API Gateway

O **Amazon API Gateway** é um serviço totalmente gerenciado que facilita para os desenvolvedores a criação, publicação, manutenção, monitoramento e segurança de APIs RESTful ou WebSocket em qualquer escala. Ele atua como um "portão" de entrada para suas aplicações de backend.

**Funcionalidades:**

* **Criação de APIs**: Permite criar APIs para acessar dados, lógica de negócios ou funcionalidades de outros serviços AWS (Lambda, EC2) ou de aplicações on-premises.
* **Gerenciamento de Tráfego**: Lida com roteamento de requisições, controle de acesso e tratamento de erros.
* **Segurança**: Integra-se com o IAM, AWS WAF, Cognito e permite autenticação personalizada (Authorizers Lambda).
* **Cache**: Pode armazenar em cache as respostas da API para reduzir a latência.
* **Limitação de Requisições (Throttling)**: Protege seu backend contra excesso de requisições.
* **Monitoramento**: Integra-se com o CloudWatch para monitorar métricas de desempenho e logs.
* **Versões e Estágios**: Permite criar e gerenciar diferentes versões e estágios da sua API (ex: dev, test, prod).

O API Gateway é fundamental para a construção de arquiteturas serverless, atuando como o front-end para funções Lambda e outras lógicas de backend.

---

## Contêineres na AWS

Contêineres empacotam código e todas as suas dependências, permitindo que aplicações rodem de forma consistente em diferentes ambientes. A AWS oferece vários serviços para gerenciar e orquestrar contêineres:

* **Amazon Elastic Container Service (ECS)**: Um serviço de orquestração de contêineres totalmente gerenciado, nativo da AWS. É ideal para executar aplicações Docker em um ambiente escalável.
    * **Fargate**: Um modo de computação serverless para ECS (e EKS) que elimina a necessidade de gerenciar instâncias EC2 subjacentes. Você só precisa definir os recursos (CPU, memória) que seus contêineres precisam, e a AWS gerencia a infraestrutura.
    * **EC2**: Você também pode executar seus contêineres em instâncias EC2 que você gerencia (modo EC2 para ECS).
* **Amazon Elastic Kubernetes Service (EKS)**: Um serviço Kubernetes gerenciado que facilita a execução do Kubernetes na AWS sem a necessidade de instalar, operar e manter seu próprio plano de controle do Kubernetes.
    * Assim como o ECS, você pode usar o EKS com Fargate (serverless) ou com instâncias EC2 que você gerencia.
* **Amazon Elastic Container Registry (ECR)**: Um registro de contêineres Docker totalmente gerenciado que facilita o armazenamento, gerenciamento e implantação de suas imagens de contêiner.

---

## Funções do AWS Step Functions

O **AWS Step Functions** é um serviço de orquestração de fluxos de trabalho serverless que permite coordenar funções Lambda e outros serviços AWS em fluxos de trabalho visuais. Ele ajuda a construir aplicações distribuídas e microsserviços de forma fácil e robusta.

**Como Funciona:**

* Você define o seu fluxo de trabalho (estado-máquina) usando JSON.
* Cada "passo" no fluxo de trabalho pode ser uma função Lambda, um serviço ECS, ou outros serviços AWS.
* O Step Functions gerencia o estado entre os passos, lida com erros, repetições (retries) e timeouts, garantindo que o fluxo de trabalho seja concluído.
* Você pode visualizar o progresso de cada execução em tempo real.

**Casos de Uso:**

* Orquestração de microsserviços.
* Processamento de dados em lotes (ETL).
* Aplicações de longo prazo e multi-passos.
* Automação de tarefas de TI.

---

## Visão Geral dos Bancos de Dados

A AWS oferece uma variedade de opções de banco de dados, cada uma otimizada para diferentes casos de uso:

* **Bancos de Dados Relacionais**:
    * **Amazon RDS**: Serviço gerenciado para bancos de dados relacionais tradicionais (MySQL, PostgreSQL, Oracle, SQL Server, MariaDB). Ótimo para aplicações transacionais e sistemas legados.
    * **Amazon Aurora**: Banco de dados relacional compatível com MySQL e PostgreSQL, desenvolvido para a nuvem. Oferece performance e escalabilidade de nível comercial.
* **Bancos de Dados NoSQL**:
    * **Amazon DynamoDB**: Banco de dados de chave-valor e documento, gerenciado, serverless e de alta performance. Ideal para aplicações com requisitos de baixa latência em qualquer escala.
    * **Amazon DocumentDB (com compatibilidade com MongoDB)**: Banco de dados de documentos rápido, escalável e de alta disponibilidade, compatível com as APIs do MongoDB.
    * **Amazon ElastiCache**: Serviço de cache em memória (Redis, Memcached) para acelerar aplicações e reduzir a carga no banco de dados.
* **Data Warehouse**:
    * **Amazon Redshift**: Data warehouse totalmente gerenciado e escalável para análise de dados em larga escala e Business Intelligence (BI).
* **Bancos de Dados de Grafos**:
    * **Amazon Neptune**: Banco de dados de grafos rápido e totalmente gerenciado para construir e executar aplicações que trabalham com conjuntos de dados altamente conectados.
* **Bancos de Dados de Séries Temporais**:
    * **Amazon Timestream**: Banco de dados de séries temporais rápido, escalável e serverless.
* **Bancos de Dados de Ledger**:
    * **Amazon QLDB (Quantum Ledger Database)**: Banco de dados de ledger imutável, transparente e criptograficamente verificável, ideal para aplicações que precisam de um registro completo e verificável de dados.

---

## Amazon Redshift

O **Amazon Redshift** é um serviço de data warehouse totalmente gerenciado e otimizado para análise de grandes volumes de dados (petabytes). Ele é projetado para consultas complexas e agregações, sendo ideal para cargas de trabalho de Business Intelligence (BI), relatórios e análises.

**Características Principais:**

* **Colunar**: Armazena dados em colunas, o que é altamente eficiente para cargas de trabalho analíticas, pois permite que o banco de dados leia apenas as colunas relevantes para uma consulta.
* **Processamento Massivamente Paralelo (MPP)**: Distribui o processamento da consulta entre vários nós de computação para acelerar o desempenho.
* **Escalabilidade**: Escala facilmente de gigabytes a petabytes de dados.
* **Gerenciado**: A AWS lida com o provisionamento, aplicação de patches, backups e replicação.
* **Integração**: Integra-se bem com outras ferramentas de BI e serviços AWS como S3 (para ingestão de dados de data lakes), Kinesis (para streaming de dados) e EMR (para processamento de Big Data).

---

## Amazon Aurora

O **Amazon Aurora** é um banco de dados relacional compatível com MySQL e PostgreSQL, desenvolvido para a nuvem. Ele combina a velocidade e a disponibilidade de bancos de dados comerciais de ponta com a simplicidade e a economia dos bancos de dados de código aberto.

**Características Principais:**

* **Compatibilidade**: Totalmente compatível com MySQL e PostgreSQL, permitindo migração fácil de aplicações existentes.
* **Performance**: Até 5x mais rápido que MySQL padrão e 3x mais rápido que PostgreSQL padrão.
* **Escalabilidade**: Armazenamento auto-escalável até 128 TB e escalabilidade de leitura com até 15 réplicas de leitura.
* **Alta Disponibilidade e Durabilidade**: Armazenamento replicado automaticamente em 3 Zonas de Disponibilidade, com recuperação de falhas automática em segundos.
* **Gerenciado**: A AWS gerencia o provisionamento, aplicação de patches, backups e replicação.
* **Custo-benefício**: Preços significativamente mais baixos que bancos de dados comerciais.
* **Serverless (Aurora Serverless)**: Uma opção onde o Aurora é executado sob demanda e escala automaticamente a capacidade, cobrando apenas pelo uso, sem necessidade de provisionar instâncias.

---

## Migração de Banco de Dados da Amazon

A AWS oferece serviços e ferramentas para facilitar a migração de bancos de dados para a nuvem:

* **AWS Database Migration Service (DMS)**: Um serviço gerenciado que ajuda a migrar bancos de dados para a AWS de forma rápida e segura. Ele suporta migrações homogêneas (ex: Oracle para Oracle) e heterogêneas (ex: Oracle para PostgreSQL).
    * **Migração Homogênea**: Migração entre o mesmo tipo de banco de dados.
    * **Migração Heterogênea**: Migração entre diferentes tipos de banco de dados, geralmente exigindo a conversão do esquema.
    * Pode realizar migrações full load (migrar todos os dados de uma vez) ou Change Data Capture (CDC) para migração contínua de dados enquanto a aplicação permanece online.
* **AWS Schema Conversion Tool (SCT)**: Uma ferramenta que ajuda a converter o esquema do banco de dados e objetos de código (como stored procedures, funções, triggers) de uma plataforma de banco de dados para outra. É especialmente útil para migrações heterogêneas, pois automatiza grande parte da conversão de código.

---

## Visão Geral das Redes da AWS (Revisão)

(Este tópico já foi coberto em detalhes em "Redes na Nuvem AWS", mas a revisão sugere que é um ponto de reforço na prova.)

**Principais Componentes de Rede na AWS:**

* **Amazon VPC**: Sua rede virtual isolada.
* **Sub-redes**: Públicas ou privadas dentro da VPC.
* **Internet Gateway**: Para acesso à internet para sub-redes públicas.
* **NAT Gateway**: Para acesso à internet de saída para sub-redes privadas.
* **Security Groups**: Firewalls stateful no nível da instância.
* **Network ACLs (NACLs)**: Firewalls stateless no nível da sub-rede.
* **VPC Peering**: Conecta duas VPCs para comunicação privada.
* **AWS Direct Connect**: Conexão dedicada on-premises para AWS.
* **AWS Site-to-Site VPN**: Conexão VPN criptografada on-premises para AWS.
* **Elastic Load Balancing (ELB)**: Balanceamento de carga de tráfego.
* **Amazon Route 53**: Serviço DNS.
* **Amazon CloudFront**: CDN.

---

## Amazon VPC (Virtual Private Cloud)

A **Amazon VPC (Virtual Private Cloud)** é o serviço que permite que você provisione uma seção isolada da Nuvem AWS onde você pode lançar recursos AWS em uma rede virtual que você define. É como ter seu próprio data center virtual na AWS.

**Elementos Chave da VPC:**

* **CIDR Block**: Um intervalo de endereços IP que define o espaço de endereçamento da sua VPC (ex: `10.0.0.0/16`).
* **Sub-redes**: Uma VPC é dividida em sub-redes. Cada sub-rede reside em uma única Zona de Disponibilidade.
    * **Sub-rede Pública**: Possui uma tabela de rotas que encaminha o tráfego de saída para um Internet Gateway, permitindo acesso à internet.
    * **Sub-rede Privada**: Não tem uma rota direta para um Internet Gateway. O acesso à internet de saída geralmente é via NAT Gateway/Instance.
* **Tabelas de Rotas**: Controlam para onde o tráfego de rede é direcionado dentro de uma sub-rede.
* **Internet Gateway (IGW)**: Permite a comunicação entre as instâncias na sua VPC e a internet.
* **NAT Gateway / NAT Instance**: Permite que instâncias em sub-redes privadas iniciem conexões de saída para a internet, mas impede que a internet inicie conexões de entrada para essas instâncias.
* **Security Groups**: Firewalls virtuais para controle de tráfego em instâncias EC2.
* **Network Access Control Lists (Network ACLs - NACLs)**: Firewalls stateless no nível da sub-rede que controlam o tráfego de entrada e saída.

---

## Opções de Conectividade da Amazon VPC

Para conectar sua VPC a outros recursos ou redes, a AWS oferece diversas opções:

* **Internet Gateway (IGW)**: Permite acesso direto à internet para sub-redes públicas.
* **NAT Gateway / NAT Instance**: Permite que instâncias em sub-redes privadas acessem a internet para atualizações, downloads, etc., sem estarem publicamente acessíveis. NAT Gateway é gerenciado pela AWS e mais escalável e redundante que NAT Instance.
* **VPC Peering**: Conecta duas VPCs (suas ou de outras contas AWS) de forma privada, permitindo que as instâncias nessas VPCs se comuniquem como se estivessem na mesma rede. O tráfego permanece na rede AWS e não passa pela internet pública.
* **AWS Direct Connect**: Estabelece uma conexão de rede dedicada de alta largura de banda de seu data center on-premises para a AWS. Ideal para throughput alto, baixa latência e requisitos de segurança rigorosos.
* **AWS Site-to-Site VPN**: Cria uma conexão IPsec criptografada e segura através da internet pública entre sua rede on-premises e sua VPC.
* **AWS Transit Gateway**: Um hub de rede que permite conectar milhares de VPCs e redes on-premises em uma única região de forma simplificada e escalável.

---

## Segurança e Solução de Problemas da Rede

* **Security Groups**: (Revisão) Firewalls stateful no nível da instância, controlam o tráfego de entrada e saída para instâncias EC2. Regras de permissão explícita.
* **Network Access Control Lists (Network ACLs - NACLs)**: Firewalls stateless no nível da sub-rede.
    * **Stateless**: O tráfego de resposta deve ser explicitamente permitido por uma regra de saída, mesmo que o tráfego de entrada correspondente tenha sido permitido.
    * **Regras de Entrada e Saída**: Controlam o tráfego permitido de/para a sub-rede.
    * **Ordem das Regras**: As regras são avaliadas em ordem crescente de número (menor número = maior prioridade).
    * **Regra Deny**: NACLs permitem regras de "negar" explicitamente.
* **VPC Flow Logs**: Um recurso que captura informações sobre o tráfego IP de entrada e saída de interfaces de rede em sua VPC. Os dados de log podem ser publicados no Amazon CloudWatch Logs ou Amazon S3. Útil para:
    * **Monitoramento de Tráfego**: Entender o tráfego que entra e sai da sua VPC.
    * **Solução de Problemas**: Diagnosticar problemas de conectividade.
    * **Auditoria de Segurança**: Identificar padrões de tráfego incomuns ou acesso não autorizado.
* **Reachability Analyzer**: Uma ferramenta que ajuda a depurar problemas de conectividade de rede entre recursos na sua VPC, simulando o caminho da rede e identificando gargalos ou problemas de configuração.

---

## Visão Geral do Laboratório: Configurar uma Amazon VPC

Um laboratório de VPC tipicamente envolve:

* **Criação de uma VPC**: Definir um bloco CIDR.
* **Criação de Sub-redes**: Criar pelo menos uma sub-rede pública e uma privada em diferentes AZs.
* **Configuração de um Internet Gateway**: Anexar ao VPC.
* **Configuração de Tabelas de Rotas**:
    * Associar a sub-rede pública a uma tabela de rotas com uma rota para o Internet Gateway (`0.0.0.0/0` via IGW).
    * Associar a sub-rede privada a uma tabela de rotas sem rota direta para o Internet Gateway.
* **Configuração de um NAT Gateway**: Em uma sub-rede pública, para permitir que instâncias na sub-rede privada acessem a internet. Adicionar uma rota para o NAT Gateway na tabela de rotas da sub-rede privada.
* **Lançar Instâncias EC2**: Uma em cada sub-rede (pública e privada) para testar a conectividade.
* **Configurar Security Groups**: Para permitir SSH/HTTP nas instâncias.
* **Testar Conectividade**: Tentar pingar a internet de ambas as instâncias, acessar o servidor web na instância pública.

---

## Visão Geral do Cloud Storage

A AWS oferece uma gama diversificada de serviços de armazenamento para diferentes necessidades:

* **Armazenamento de Objetos**:
    * **Amazon S3**: Armazenamento de objetos escalável, durável e de alta disponibilidade. Ideal para dados não estruturados, backups, data lakes, hospedagem de sites estáticos.
    * **Amazon Glacier / S3 Glacier Deep Archive**: Classes de armazenamento do S3 para arquivamento de baixo custo de dados raramente acessados.
* **Armazenamento de Blocos**:
    * **Amazon EBS (Elastic Block Store)**: Volumes de armazenamento de blocos persistentes de alta performance que podem ser anexados a instâncias EC2. Ideal para sistemas de arquivos, bancos de dados e aplicações que exigem armazenamento persistente.
    * **Armazenamento de Instância**: Armazenamento de bloco temporário que reside fisicamente no servidor host de uma instância EC2. Os dados são perdidos quando a instância é parada ou encerrada.
* **Armazenamento de Arquivos**:
    * **Amazon EFS (Elastic File System)**: Sistema de arquivos escalável e compartilhado para instâncias EC2. Permite que várias instâncias acessem os mesmos dados simultaneamente. Ideal para cargas de trabalho de arquivos em escala, como análise de Big Data, desenvolvimento web, compartilhamento de conteúdo.
    * **Amazon FSx**: Oferece sistemas de arquivos nativos, como FSx for Windows File Server (SMB) e FSx for Lustre (para HPC).
* **Armazenamento Híbrido**:
    * **AWS Storage Gateway**: Conecta ambientes on-premises com o armazenamento em nuvem da AWS, oferecendo caches locais para acesso rápido. Permite que aplicações on-premises usem armazenamento em nuvem como volumes de bloco, compartilhamentos de arquivo ou fitas virtuais.

---

## Amazon EBS (Elastic Block Store)

O **Amazon EBS (Elastic Block Store)** fornece volumes de armazenamento de blocos persistentes para uso com instâncias EC2. É como um disco rígido virtual que você anexa à sua máquina virtual na nuvem.

**Características Principais:**

* **Volumes de Bloco**: Os volumes EBS funcionam como discos rígidos brutos. Você pode formatá-los com um sistema de arquivos e montá-los em sua instância EC2.
* **Persistência**: Os dados em um volume EBS persistem independentemente do ciclo de vida da instância EC2. Você pode parar ou encerrar a instância, e o volume EBS e seus dados permanecerão.
* **Zonal**: Um volume EBS só pode ser anexado a uma instância EC2 na mesma Zona de Disponibilidade.
* **Tipos de Volume**: A AWS oferece vários tipos de volumes EBS, otimizados para diferentes cargas de trabalho em termos de performance (IOPS e throughput) e custo:
    * **SSD de uso geral (gp2/gp3)**: Equilíbrio entre preço e performance, para a maioria das cargas de trabalho.
    * **SSD com IOPS provisionadas (io1/io2)**: Para cargas de trabalho com requisitos de IOPS muito altos e consistentes, como grandes bancos de dados.
    * **HDD otimizado para throughput (st1)**: Para cargas de trabalho que exigem alto throughput (ex: processamento de Big Data, data warehouses).
    * **HDD Cold (sc1)**: Para dados acessados com pouca frequência, com custo mais baixo.
* **Snapshots**: Você pode criar snapshots (cópias pontuais) de seus volumes EBS para backup. Snapshots são armazenados no Amazon S3 e são incrementais (apenas os blocos que mudaram são armazenados). Podem ser usados para restaurar um volume ou criar novos volumes.
* **Criptografia**: Suporta criptografia em repouso com AWS KMS.

---

## Demonstração do Amazon EBS-2

(Este é um reforço para uma demonstração prática.)

Uma demonstração de EBS tipicamente inclui:

* **Criação de um Volume EBS**: Selecionar tipo, tamanho, IOPS (se aplicável), e Zona de Disponibilidade.
* **Anexar o Volume a uma Instância EC2**: Selecionar a instância (na mesma AZ) e o ponto de montagem.
* **Formatar e Montar o Volume**: Conectar-se à instância EC2, formatar o novo disco e montá-lo em um diretório.
* **Criar um Snapshot do Volume**: Fazer um backup do volume.
* **Restaurar um Volume a partir de um Snapshot**: Criar um novo volume a partir do snapshot e anexá-lo a uma instância.
* **Desanexar e Excluir o Volume**: Remover o volume da instância e deletá-lo (se não for mais necessário).

---

## O Armazenamento de Instâncias do EC2

O **Armazenamento de Instâncias (Instance Store)**, também conhecido como armazenamento efêmero, é um armazenamento de bloco temporário que está fisicamente anexado ao servidor host onde sua instância EC2 é executada.

**Características Importantes:**

* **Temporário**: Os dados armazenados no armazenamento de instância são perdidos quando a instância é parada, hibernada ou encerrada (ou se o hardware subjacente falhar).
* **Alta Performance**: Oferece alta performance de E/S, pois é diretamente conectado ao hardware do host.
* **Casos de Uso**: Ideal para caches temporários, buffers, dados de scratch (rascunho) ou para instâncias Spot que podem ser interrompidas. Não é adequado para dados que precisam persistir.
* **Disponibilidade**: Nem todos os tipos de instância EC2 suportam o armazenamento de instância. Os volumes são incluídos no preço da instância.

Para dados persistentes, sempre use Amazon EBS.

---

## Elastic File System (EFS)

O **Amazon Elastic File System (EFS)** é um serviço de sistema de arquivos de rede (NFS) totalmente gerenciado e escalável para uso com instâncias EC2 e servidores on-premises (via Direct Connect ou VPN). Ele permite que várias instâncias acessem os mesmos dados simultaneamente.

**Características Principais:**

* **Compartilhado**: Múltiplas instâncias EC2 (em diferentes AZs na mesma região) e servidores on-premises podem montar e acessar o mesmo sistema de arquivos EFS.
* **Escalabilidade Elástica**: O EFS escala automaticamente para cima ou para baixo para atender às suas necessidades de armazenamento e throughput, sem provisionamento manual. Paga apenas pelo que armazena.
* **Durabilidade e Alta Disponibilidade**: Dados são armazenados de forma redundante em várias Zonas de Disponibilidade.
* **Protocolo NFSv4**: Baseado no protocolo Network File System (NFS) versão 4.
* **Casos de Uso**:
    * Compartilhamento de conteúdo web para farms de servidores.
    * Ambientes de desenvolvimento e teste.
    * Cargas de trabalho de análise de Big Data.
    * Repositórios de contêineres Docker.
    * Home directories para usuários.

---

## Demonstração do Elastic File System-2

(Este é um reforço para uma demonstração prática.)

Uma demonstração de EFS tipicamente inclui:

* **Criação de um Sistema de Arquivos EFS**: Escolher a VPC, sub-redes e grupos de segurança para os pontos de montagem.
* **Criação de Pontos de Montagem**: Em cada Zona de Disponibilidade onde você deseja que suas instâncias acessem o EFS.
* **Configurar Security Groups**: Garantir que o Security Group do EFS permita tráfego NFS da(s) instância(s) EC2, e o Security Group da instância permita saída para o EFS.
* **Montar o EFS em Instâncias EC2**: Conectar-se a duas ou mais instâncias EC2 e montar o sistema de arquivos EFS usando o utilitário `mount -t nfs4`.
* **Testar Acesso Compartilhado**: Criar um arquivo de uma instância e verificá-lo na outra instância.

---

## Amazon Glacier

O **Amazon Glacier** é uma classe de armazenamento do Amazon S3 (agora muitas vezes referida como S3 Glacier e S3 Glacier Deep Archive) projetada para arquivamento de dados de baixo custo e acesso infrequente ou para backups de longo prazo, onde o tempo de recuperação (retrieval time) pode ser de minutos a horas.

**Características Principais:**

* **Custo Extremamente Baixo**: É significativamente mais barato que o S3 Standard, ideal para dados que são acessados apenas uma ou duas vezes por ano.
* **Modelos de Recuperação Flexíveis**:
    * **Expedited**: Em 1-5 minutos (custo mais alto).
    * **Standard**: Em 3-5 horas.
    * **Bulk**: Em 5-12 horas (custo mais baixo, para grandes volumes).
* **Casos de Uso**:
    * Arquivamento de dados regulatórios.
    * Preservação de mídia digital (vídeos, áudios antigos).
    * Recuperação de desastres de longo prazo.
    * Dados de backup que raramente serão necessários.
* **Objetos S3 Glacier**: Você pode diretamente carregar objetos para o S3 Glacier ou configurar regras de ciclo de vida no S3 para mover objetos de outras classes para o Glacier após um determinado tempo.

---

## Demonstração do S3 Glacier-2

(Este é um reforço para uma demonstração prática.)

Uma demonstração do S3 Glacier geralmente envolve:

* **Configurar um Bucket S3**: Criar um bucket S3.
* **Configurar Regras de Ciclo de Vida do S3**: Criar uma regra para mover objetos (ex: após 30 dias) para a classe de armazenamento S3 Glacier.
* **Fazer Upload de um Objeto**: Carregar um arquivo para o bucket S3 e observar o status da classe de armazenamento.
* **Iniciar uma Recuperação (Restore) de Objeto Glacier**: Selecionar um objeto no Glacier e iniciar uma recuperação, escolhendo o tipo de recuperação (Expedited, Standard, Bulk).
* **Acessar o Objeto Recuperado**: Após o tempo de recuperação, acessar o objeto temporariamente restaurado no S3.

---

## Amazon S3 e a CLI da AWS

A **AWS CLI (Command Line Interface)** é uma ferramenta poderosa para interagir com o Amazon S3, permitindo automatizar tarefas e gerenciar buckets e objetos de forma eficiente.

**Comandos Comuns da CLI para S3:**

* `aws s3 ls`: Lista buckets ou o conteúdo de um bucket.
    * `aws s3 ls`
    * `aws s3 ls s3://meu-bucket`
* `aws s3 mb s3://meu-novo-bucket`: Cria um novo bucket (make bucket).
* `aws s3 rb s3://meu-bucket-a-remover`: Remove um bucket (remove bucket).
* `aws s3 cp [source] [destination]`: Copia objetos entre o sistema de arquivos local e S3, ou entre buckets S3.
    * `aws s3 cp meu_arquivo.txt s3://meu-bucket/pasta/`
    * `aws s3 cp s3://meu-bucket/arquivo.txt ./local_destino/`
* `aws s3 sync [source] [destination]`: Sincroniza um diretório local com um bucket S3, ou vice-versa, copiando apenas arquivos novos ou alterados.
    * `aws s3 sync ./meus_arquivos_locais/ s3://meu-bucket/backup/`
* `aws s3 rm s3://meu-bucket/arquivo_a_remover.txt`: Remove um objeto.
* `aws s3api`: Fornece acesso a operações de nível de API do S3, permitindo configurar mais detalhes, como políticas de bucket, ACLs, versionamento, etc.

---

## Amazon Storage Gateway

O **Amazon Storage Gateway** é um serviço híbrido de armazenamento em nuvem que conecta um ambiente de TI on-premises com o armazenamento em nuvem da AWS. Ele permite que as aplicações on-premises usem o armazenamento em nuvem de forma transparente, como se fosse armazenamento local.

**Tipos de Gateway:**

* **File Gateway**:
    * Oferece acesso a objetos S3 como compartilhamentos de arquivos NFS e SMB.
    * Armazena dados em cache localmente para acesso de baixa latência.
    * Ideal para backups, arquivos de usuários e compartilhamento de arquivos.
* **Volume Gateway**:
    * Oferece volumes de armazenamento de blocos baseados em iSCSI para servidores on-premises.
    * **Cached Volumes**: Armazena dados frequentemente acessados localmente e o restante na AWS.
    * **Stored Volumes**: Armazena todos os dados localmente e realiza backups (snapshots) assincronamente para S3.
    * Ideal para aplicações que exigem armazenamento de blocos e recuperação de desastres.
* **Tape Gateway**:
    * Oferece uma biblioteca de fitas virtuais (VTL) que permite substituir backups físicos em fita por backups na nuvem (Amazon S3 e Glacier).
    * Compatível com software de backup de terceiros.
    * Ideal para arquivamento de longo prazo.

---

## Amazon CloudWatch

O **Amazon CloudWatch** é um serviço de monitoramento e observabilidade para recursos e aplicações AWS e on-premises. Ele coleta e rastreia métricas, coleta e monitora arquivos de log, e configura alarmes que enviam notificações ou tomam ações automatizadas.

**Componentes Principais:**

* **Métricas**: Pontos de dados sobre o desempenho de seus recursos (ex: utilização da CPU do EC2, throughput do S3, latência do ELB). Podem ser visualizadas em gráficos no console.
* **Logs**: Coleta logs de diversas fontes (EC2, Lambda, VPC Flow Logs, CloudTrail) no CloudWatch Logs. Permite pesquisar, filtrar e analisar dados de log.
* **Alarmes**: Permite definir limites para métricas. Quando uma métrica excede o limite, um alarme é acionado e pode enviar notificações (via SNS) ou executar ações automáticas (ex: acionar um Auto Scaling, parar uma instância EC2).
* **Dashboards**: Crie dashboards personalizados para visualizar suas métricas e logs em um único painel.
* **Eventos (CloudWatch Events/EventBridge)**: Entregam um fluxo quase em tempo real de eventos do seu ambiente AWS, permitindo que você reaja a mudanças nos seus recursos.

O CloudWatch é essencial para a excelência operacional e para garantir que suas aplicações estejam funcionando conforme o esperado.

---

## Mergulhe Fundo: Amazon CloudWatch

Aprofundando no CloudWatch, podemos explorar:

* **Métricas Personalizadas**: Você pode publicar suas próprias métricas de aplicações no CloudWatch para monitorar aspectos específicos do seu software.
* **Logs Insights**: Uma ferramenta de consulta interativa no CloudWatch Logs que permite analisar grandes volumes de dados de log usando uma linguagem de consulta rica.
* **Detecção de Anomalias**: O CloudWatch pode usar machine learning para identificar padrões anormais em suas métricas, alertando sobre comportamentos inesperados que não seriam detectados por limites estáticos.
* **Contribuidores de Métricas**: Ajuda a identificar os principais contribuidores para uma métrica, útil para depuração de performance.
* **CloudWatch Agent**: Um agente que pode ser instalado em instâncias EC2 e servidores on-premises para coletar métricas de nível de sistema operacional e logs de aplicações.

---

## Integração do Serviço da AWS com o Athena

O **Amazon Athena** é um serviço de consulta interativa serverless que permite analisar dados diretamente no Amazon S3 usando SQL padrão.

**Como funciona:**

* Seus dados (ex: logs do CloudTrail, logs do VPC Flow, dados de aplicações) são armazenados no Amazon S3.
* Você define um esquema para seus dados no Athena (pode usar o AWS Glue Data Catalog para descoberta automática de esquema).
* Você escreve consultas SQL padrão, e o Athena executa essas consultas diretamente nos dados no S3.
* Você paga apenas pela quantidade de dados digitalizados por consulta.

**Integração com Outros Serviços AWS:**

* **S3**: A fonte principal de dados para o Athena.
* **CloudTrail**: Os logs do CloudTrail (armazenados no S3) podem ser facilmente consultados pelo Athena para auditoria e análise de segurança.
* **VPC Flow Logs**: Também armazenados no S3, podem ser analisados pelo Athena para entender padrões de tráfego de rede.
* **AWS Glue**: Um serviço de ETL (Extract, Transform, Load) e catálogo de dados que pode ser usado pelo Athena para descobrir e gerenciar os esquemas dos seus dados no S3.

O Athena é uma ferramenta poderosa para análise ad-hoc de grandes volumes de dados no S3 sem a necessidade de provisionar ou gerenciar infraestrutura de banco de dados.

---

## AWS Organizations

O **AWS Organizations** é um serviço de gerenciamento de contas que permite que você consolide e gerencie várias contas AWS em uma única organização. Ele ajuda a centralizar o faturamento, aplicar políticas de segurança e conformidade e gerenciar recursos em escala.

**Recursos Principais:**

* **Consolidated Billing (Faturamento Consolidado)**: Combina a fatura de todas as suas contas em uma única conta de pagamento, permitindo descontos por volume e simplificando o gerenciamento de custos.
* **Organizational Units (OUs)**: Permite organizar suas contas em uma estrutura hierárquica para facilitar o gerenciamento e a aplicação de políticas.
* **Service Control Policies (SCPs)**: Permitem definir permissões máximas para todas as contas em uma OU ou na organização. As SCPs são uma forma de "guardrail" de segurança, definindo o que os usuários e funções nessas contas não podem fazer.
* **Integração com outros serviços AWS**: Integra-se com serviços como AWS CloudTrail (para registro de atividades em várias contas) e AWS Config (para conformidade em várias contas).

O AWS Organizations é crucial para empresas que operam com várias contas AWS, oferecendo governança e controle centralizados.

---

## Marcação (Tagging)

A **marcação (tagging)** na AWS é o processo de atribuir metadados (pares de chave-valor) aos seus recursos AWS. As tags são uma forma de organizar e gerenciar seus recursos de forma lógica.

**Exemplos de Uso de Marcação:**

* **Gerenciamento de Custos**: Marcar recursos com tags como `Projeto: Financeiro`, `CentroDeCusto: 123`, `Ambiente: Producao`. Isso permite que você visualize os custos detalhados por projeto, departamento ou ambiente no AWS Cost Explorer.
* **Automação**: Usar tags em scripts de automação ou funções Lambda para identificar e operar em recursos específicos (ex: desligar todas as instâncias com a tag `Ambiente: Desenvolvimento` à noite).
* **Controle de Acesso**: Usar tags em políticas IAM para conceder permissões baseadas em tags (ex: permitir que um usuário inicie instâncias EC2 apenas se elas tiverem a tag `Proprietario: MeuNome`).
* **Organização**: Organizar recursos para facilitar a pesquisa e o gerenciamento (ex: `Aplicacao: WebApp`, `Componente: BancoDeDados`).
* **Auditoria e Conformidade**: Identificar a propriedade ou o propósito de recursos para fins de auditoria.

**Melhores Práticas:**

* **Consistência**: Use convenções de nomenclatura de tags consistentes em toda a sua organização.
* **Obrigatoriedade**: Considere a implementação de políticas que exijam a marcação de recursos.

---

## Gerenciamento de Custos da AWS e Práticas Recomendadas

Gerenciar e otimizar os custos na AWS é uma disciplina contínua.

**Ferramentas e Recursos:**

* **AWS Cost Explorer**: Uma ferramenta que permite visualizar, entender e gerenciar seus custos e uso da AWS ao longo do tempo. Você pode analisar padrões de gastos, identificar tendências e prever custos futuros.
* **AWS Budgets**: Permite definir orçamentos personalizados para seus custos e uso da AWS. Você recebe alertas quando seus custos ou uso excedem (ou estão projetados para exceder) os limites definidos.
* **AWS Cost and Usage Report (CUR)**: Um relatório detalhado que lista seus custos e uso da AWS em um nível granular, armazenado em um bucket S3.
* **AWS Trusted Advisor**: Oferece recomendações de otimização de custos (ver seção anterior).
* **AWS Organizations (Faturamento Consolidado)**: Simplifica o faturamento e permite descontos por volume.

**Práticas Recomendadas para Otimização de Custos:**

* **Dimensionamento Correto (Right-sizing)**: Use os tipos de instância EC2 e outros recursos que realmente atendam aos requisitos da sua carga de trabalho, evitando o superprovisionamento. Monitore o uso e ajuste conforme necessário.
* **Instâncias Reservadas (RIs) e Savings Plans**: Comprometa-se com o uso de recursos por 1 ou 3 anos para obter descontos significativos. Ideal para cargas de trabalho estáveis.
* **Instâncias Spot**: Para cargas de trabalho tolerantes a interrupções, use instâncias Spot para economizar até 90% em relação aos preços sob demanda.
* **Desligar Recursos Ociosos**: Pare ou encerre recursos que não estão em uso, especialmente em ambientes de desenvolvimento/teste.
* **Otimização de Armazenamento S3**: Use as classes de armazenamento S3 apropriadas (S3 Standard-IA, Glacier) e políticas de ciclo de vida para mover dados para classes mais baratas à medida que se tornam menos acessíveis.
* **Deletar Volumes EBS Não Anexados**: Identifique e remova volumes EBS que não estão mais anexados a instâncias.
* **Monitoramento e Automação**: Use CloudWatch e Lambda para monitorar o uso e automatizar ações de economia de custos.
* **Arquitetura Serverless**: Considere serviços serverless (Lambda, S3, DynamoDB, Fargate) onde você paga apenas pelo consumo real, eliminando o custo de recursos ociosos.

---

## Demonstração do Painel de Faturamento da AWS-2

(Este é um reforço para uma demonstração prática.)

Uma demonstração do painel de faturamento da AWS geralmente mostra:

* **Visão Geral do Faturamento**: Onde você pode ver o resumo do seu custo atual até a data.
* **Cost Explorer**: Como navegar no Cost Explorer para analisar custos por serviço, região, tags, tipo de instância, etc.
* **Orçamentos**: Como criar um novo orçamento (ex: para custos totais, custos de EC2) e configurar alertas.
* **Relatórios de Custos e Uso (CUR)**: Onde encontrar e como usar os relatórios detalhados exportados para o S3.
* **Otimização de Custos**: A seção que destaca as economias potenciais e as recomendações do Trusted Advisor.

---

## Estratégia de Construção da AMI (Amazon Machine Image)

A **Amazon Machine Image (AMI)** é um template que contém a configuração de software (sistema operacional, servidor de aplicações, aplicações e outras configurações) necessária para lançar uma instância EC2.

**Estratégias de Construção de AMI:**

* **Usar AMIs Fornecidas pela AWS**: A maneira mais simples de começar, usando AMIs pré-configuradas da Amazon (Amazon Linux, Ubuntu, Windows Server, etc.).
* **Usar AMIs do AWS Marketplace**: AMIs pré-configuradas e otimizadas por terceiros, muitas vezes com software licenciado.
* **Criar AMIs Personalizadas**: Recomendado para ambientes de produção.
    * **Vantagens**:
        * **Padronização**: Garante que todas as instâncias lançadas a partir da AMI tenham a mesma configuração.
        * **Velocidade de Lançamento**: As instâncias iniciam mais rapidamente, pois o software já está pré-instalado.
        * **Consistência**: Reduz erros de configuração e melhora a confiabilidade.
        * **Segurança**: Permite pré-instalar patches de segurança e endurecer a segurança.
        * **Automação**: Pode ser integrada em pipelines de CI/CD.
    * **Processo Básico**:
        * Lançar uma instância EC2 a partir de uma AMI base.
        * Configurar a instância (instalar software, aplicar patches, configurar aplicações).
        * Criar uma AMI a partir dessa instância configurada.
    * **Ferramentas para Automação**:
        * **Packer**: Uma ferramenta de código aberto da HashiCorp que automatiza o processo de criação de AMIs (e outras imagens de máquina) para várias plataformas de nuvem.
        * **AWS Systems Manager Automation**: Pode ser usado para automatizar partes do processo de construção de AMI.
        * **AWS Image Builder**: Um serviço gerenciado para automatizar a criação, gerenciamento e implantação de imagens de servidor seguras e atualizadas.

---

## Modelos de Inicialização do Amazon EC2 (Launch Templates)

Os **Modelos de Inicialização (Launch Templates)** são uma ferramenta mais moderna e flexível para armazenar as configurações de lançamento de instâncias EC2, substituindo as antigas Configurações de Lançamento.

**Vantagens dos Launch Templates:**

* **Versionamento**: Você pode criar várias versões de um modelo de lançamento, permitindo gerenciar alterações nas suas configurações ao longo do tempo.
* **Controle Granular**: Suportam mais opções de configuração do que as configurações de lançamento, incluindo tipos de instância Spot, volumes EBS otimizados e detalhes da rede mais específicos.
* **Integração Flexível**: Usados por Grupos de Auto Scaling, instâncias Spot, e outras automações de lançamento de EC2.
* **Parciais/Completos**: Você pode criar modelos parciais (com apenas algumas configurações) e usar dados do usuário ou parâmetros adicionais ao lançar instâncias.

Um Launch Template define: AMI, tipo de instância, par de chaves, Security Groups, volumes EBS, dados do usuário (user data), e outras configurações de rede e armazenamento.

---

## Demonstração do Modelo de Lançamento EC2-2

(Este é um reforço para uma demonstração prática.)

Uma demonstração de Launch Templates geralmente inclui:

* **Criação de um Novo Modelo de Lançamento**:
    * Definir um nome e uma descrição.
    * Escolher uma AMI.
    * Selecionar um tipo de instância.
    * Configurar Security Groups.
    * Adicionar um script user data para instalação de um servidor web ou outra configuração inicial.
    * Adicionar tags.
* **Lançar uma Instância EC2 a partir do Modelo de Lançamento**: Demonstrar como uma instância é provisionada usando o modelo.
* **Criar uma Nova Versão do Modelo de Lançamento**: Modificar uma configuração (ex: tipo de instância, user data) e criar uma nova versão.
* **Atualizar um Grupo de Auto Scaling para usar a Nova Versão**: Mostrar como um ASG pode ser atualizado para usar uma nova versão do template, permitindo uma atualização controlada das instâncias.

---

## Infraestrutura como Código (IaC)

**Infraestrutura como Código (IaC)** é a prática de gerenciar e provisionar a infraestrutura de computação (redes, máquinas virtuais, balanceadores de carga, bancos de dados, etc.) usando arquivos de definição legíveis por máquina, em vez de configuração manual ou ferramentas interativas.

**Benefícios da IaC:**

* **Automação**: Elimina a necessidade de provisionamento manual, reduzindo erros e acelerando o processo.
* **Versionamento**: A infraestrutura pode ser versionada em sistemas de controle de versão (Git), permitindo rastrear alterações, reverter para versões anteriores e colaborar.
* **Consistência**: Garante que os ambientes (desenvolvimento, teste, produção) sejam idênticos, reduzindo problemas de "funciona na minha máquina".
* **Reusabilidade**: Módulos de infraestrutura podem ser reutilizados em diferentes projetos.
* **Documentação Implícita**: Os arquivos de código servem como documentação do seu ambiente.
* **Desastres e Recuperação**: Permite recriar seu ambiente de forma rápida e confiável em caso de desastre.

**Ferramentas de IaC na AWS:**

* **AWS CloudFormation**: Serviço nativo da AWS.
* **Terraform**: Ferramenta de código aberto (multi-cloud).
* **AWS CDK (Cloud Development Kit)**: Permite definir infraestrutura usando linguagens de programação familiares (Python, Java, TypeScript).

---

## Introdução ao JSON e ao YAML

* **JSON (JavaScript Object Notation)**:
    * **Formato**: Um formato leve de intercâmbio de dados. É fácil para humanos lerem e escreverem, e fácil para máquinas analisarem e gerarem.
    * **Estrutura**: Baseado em pares de chave-valor e listas ordenadas de valores.
    * **Uso**: Amplamente utilizado para APIs web, arquivos de configuração e armazenamento de dados.
    * **Exemplo**:
        ```json
        {
          "Recurso": {
            "Tipo": "AWS::EC2::Instance",
            "Propriedades": {
              "ImageId": "ami-0abcdef1234567890",
              "InstanceType": "t2.micro"
            }
          }
        }
        ```
* **YAML (YAML Ain't Markup Language)**:
    * **Formato**: Um formato de serialização de dados legível por humanos. É mais legível para configurações complexas.
    * **Estrutura**: Usa indentação para representar a estrutura hierárquica, similar ao JSON em termos de dados representáveis.
    * **Uso**: Popular para arquivos de configuração (ex: Docker Compose, Kubernetes), e também amplamente utilizado no AWS CloudFormation.
    * **Exemplo**:
        ```yaml
        Recurso:
          Tipo: AWS::EC2::Instance
          Propriedades:
            ImageId: ami-0abcdef1234567890
            InstanceType: t2.micro
        ```

Ambos são linguagens de serialização de dados, não linguagens de programação. O YAML é frequentemente preferido para arquivos de configuração devido à sua maior legibilidade e sintaxe mais concisa em comparação com o JSON, especialmente para documentos mais longos e aninhados.

---

## AWS CloudFormation

O **AWS CloudFormation** é um serviço que permite que você modele e provisione seus recursos AWS e de terceiros de forma declarativa, usando a metodologia de Infraestrutura como Código (IaC). Você define seus recursos em um template (arquivo JSON ou YAML), e o CloudFormation se encarrega de provisioná-los e gerenciá-los na ordem correta, lidando com dependências.

**Como Funciona:**

* **Template**: Você escreve um template CloudFormation (JSON ou YAML) que descreve os recursos da AWS que você deseja provisionar (ex: instâncias EC2, buckets S3, bancos de dados RDS, Security Groups, VPCs).
* **Stack**: Você usa o template para criar uma stack. Uma stack é uma coleção de recursos AWS que são gerenciados como uma única unidade.
* **Provisionamento**: O CloudFormation lê o template, entende as dependências entre os recursos e provisiona-os na ordem correta.
* **Gerenciamento**: Ele monitora o estado dos recursos e permite atualizar ou excluir a stack facilmente, garantindo que todos os recursos associados sejam gerenciados juntos.
* **Rollback**: Se houver um erro durante o provisionamento ou atualização, o CloudFormation pode reverter automaticamente para o último estado estável da stack.

**Benefícios:**

* **Automação e Repetibilidade**: Crie ambientes complexos de forma consistente e repetível.
* **Controle de Versão**: Seus templates podem ser versionados no Git, permitindo rastrear alterações e colaborar.
* **Gerenciamento de Dependências**: O CloudFormation lida com a ordem de criação e exclusão de recursos.
* **Redução de Erros Manuais**: Diminui a chance de erros humanos na configuração da infraestrutura.
* **Custo**: Não há custo adicional pelo serviço CloudFormation, você paga apenas pelos recursos AWS provisionados.

O CloudFormation é uma ferramenta essencial para qualquer profissional que busca automação e governança no ambiente AWS.
