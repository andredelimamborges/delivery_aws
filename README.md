# Assistente de Delivery com AWS

Este projeto implementa um Assistente de Delivery que utiliza diversos serviços da AWS para orquestrar e automatizar o fluxo de entrega. A arquitetura é serverless, altamente escalável e oferece resposta rápida aos usuários, possibilitando funcionalidades como rastreamento de pedidos, consultas sobre o status de entrega, e envio de notificações.

# Funcionalidades

-Recebimento de Pedidos: Automatiza o processo de recepção e confirmação de pedidos.

-Atualização de Estoque: Confere a disponibilidade dos itens em tempo real.

-Notificações em Tempo Real: Notifica clientes e entregadores sobre o status do pedido por meio de e-mail/SMS.

-Respostas Inteligentes: Utiliza Amazon Bedrock para oferecer respostas dinâmicas, como informações de tempo estimado de entrega e promoções.

# Arquitetura do Projeto

O projeto faz uso das seguintes tecnologias e serviços AWS:

-AWS Step Functions: Orquestra o fluxo de trabalho principal, conectando as diferentes etapas do processo de delivery.

-AWS Lambda: Executa funções específicas em cada etapa do processo, como confirmação de pedido, verificação de estoque e envio de notificações.

-Amazon DynamoDB: Banco de dados NoSQL usado para armazenar e consultar dados de pedidos e status de entrega em tempo real.

-API Gateway: Fornece uma interface RESTful para o front-end interagir com o sistema.

-Amazon Bedrock: Utilizado para fornecer respostas automáticas baseadas em IA generativa.

# Pré-requisitos

-Conta AWS com permissões para criar e gerenciar recursos.

-Ferramentas AWS CLI e SAM instaladas para implantação e configuração de recursos.

-Configuração das credenciais AWS em sua máquina local.

#Configuração e Implantação
Passo 1: Configurar o DynamoDB

Crie uma tabela no DynamoDB para armazenar os dados de pedidos, com:

Tabela: Pedidos

-Chave de Partição: PedidoID

-Índices: Adicione índices para consultas de status e tempo de entrega.

# Arquitetura do Projeto
O projeto faz uso das seguintes tecnologias e serviços AWS:

-AWS Step Functions: Orquestra o fluxo de trabalho principal, conectando as diferentes etapas do processo de delivery.

-AWS Lambda: Executa funções específicas em cada etapa do processo, como confirmação de pedido, verificação de estoque e envio de notificações.

-Amazon DynamoDB: Banco de dados NoSQL usado para armazenar e consultar dados de pedidos e status de entrega em tempo real.

-API Gateway: Fornece uma interface RESTful para o front-end interagir com o sistema.

-Amazon Bedrock: Utilizado para fornecer respostas automáticas baseadas em IA generativa.

# Configuração e Implantação

Passo 1: Configurar o DynamoDB

Crie uma tabela no DynamoDB para armazenar os dados de pedidos, com:

Tabela: Pedidos
Chave de Partição: PedidoID
Índices: Adicione índices para consultas de status e tempo de entrega.
Passo 2: Configurar Funções Lambda
Desenvolva as funções Lambda para cada etapa do processo:

Receber Pedido: Processa e valida pedidos.
VerificarEstoque: Confere disponibilidade e estoque.
NotificarEntrega: Envia notificações aos clientes.
Passo 3: Configurar o AWS Step Functions
Defina o fluxo de trabalho do Step Functions para conectar as funções Lambda em uma sequência lógica:

Receber Pedido
Verificar Estoque
Notificar Cliente
Rastrear e Atualizar Status de Entrega
Passo 4: Configurar Amazon Bedrock
Implemente o Amazon Bedrock para fornecer respostas inteligentes e personalizadas aos usuários.

Passo 5: Configurar API Gateway
Crie um endpoint RESTful usando o API Gateway para interações do front-end com o sistema.

Passo 6: Deploy
Para implantar o projeto, use o AWS SAM:
*Codigo*:
sam build
sam deploy --guided


# Contribuição
Contribuições são bem-vindas! Sinta-se à vontade para abrir uma issue ou enviar um pull request para melhorar este projeto.
