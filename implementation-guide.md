## Visão Geral
Este guia detalha as etapas necessárias para implantar a solução wiki baseada na nuvem Azure, conforme descrita na arquitetura anterior. Inclui a criação dos recursos principais, a configuração da aplicação Wiki.js, a integração com o banco de dados e controle de versão, além de práticas de monitoramento e manutenção.

## Pré-requisitos
- Assinatura ativa do Microsoft Azure
- Familiaridade com conceitos de nuvem e serviços do Azure

## Etapas de Implementação

### 1. Criar o Resource Group
1. Acesse o portal do Azure e navegue até a seção de Resource Groups.
2. Clique em "Adicionar" para criar um novo Resource Group.
3. Forneça um nome significativo para o Resource Group, como "rg-projeto-wiki".
4. Selecione a região desejada para a implantação.
5. Clique em "Revisar + Criar" para concluir a criação do Resource Group.

### 2. Provisionar o Azure Database for PostgreSQL
1. Acesse o serviço Azure Database for PostgreSQL no portal.
2. Clique em "Adicionar" para criar um novo servidor PostgreSQL.
3. Configure as propriedades do servidor, como nome, região, método de conectividade e credenciais de acesso.
4. Crie um novo banco de dados com um nome significativo, como "db-wiki".
5. Anote as informações de conexão, incluindo o nome do servidor, nome do banco de dados, usuário e senha.

### 3. Configurar o Azure Repos
1. Acesse o serviço Azure Repos no portal.
2. Crie um novo repositório de código, com um nome como "repo-wiki".
3. Conceda permissões de acesso à equipe, conforme necessário.
4. Opcionalmente, configure integração com ferramentas de CI/CD.

### 4. Implantar a Wiki.js
1. Acesse o serviço Azure App Service no portal.
2. Crie um novo App Service, selecionando o Runtime como "Node.js".
3. Vincule o App Service ao banco de dados PostgreSQL criado anteriormente.
4. Configure as variáveis de ambiente necessárias para a Wiki.js, como credenciais de banco de dados.
5. Implemente o código-fonte da Wiki.js no App Service, usando o Azure Repos.

### 5. Configurar o Docker
1. Crie um Dockerfile na raiz do repositório da Wiki.js.
2. Construa a imagem Docker localmente e teste-a.
3. Crie um Azure Container Registry no portal.
4. Faça o push da imagem Docker para o Azure Container Registry.
5. Atualize o App Service para utilizar a imagem Docker implantada.

### 6. Testar e Validar
1. Acesse a Wiki.js implantada no Azure App Service.
2. Crie, edite e visualize documentos na plataforma.
3. Verifique o histórico de alterações no Azure Repos.
4. Teste a integridade da conexão com o banco de dados PostgreSQL.

### 7. Monitorar e Manter
1. Configure alertas e monitoramento no Azure para a infraestrutura.
2. Automatize atualizações e implantações da Wiki.js, integrando com ferramentas de CI/CD.
3. Defina um plano de backups regulares do banco de dados PostgreSQL.
4. Revise periodicamente a configuração e o desempenho da solução.

## Downloads
- [Terraform Script](terraform-script.tf)
- [Ansible Playbook](ansible-playbook.yml)

