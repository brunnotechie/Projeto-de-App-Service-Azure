## Visão Geral do Projeto
Este projeto tem como objetivo implementar uma plataforma wiki baseada na nuvem, utilizando os serviços da Microsoft Azure. A solução permite que uma equipe crie, edite e gerencie documentos, runbooks e bases de conhecimento de forma colaborativa, centralizada e com controle de versão.

## Principais Recursos
- **Plataforma Wiki Colaborativa**: A equipe utiliza a aplicação de código aberto Wiki.js para criar e atualizar a documentação.
- **Armazenamento de Dados Seguro**: O conteúdo da wiki é armazenado em um Banco de Dados Azure for PostgreSQL, proporcionando gerenciamento de dados confiável e escalável.
- **Controle de Versão**: O conteúdo da wiki é integrado ao Azure Repos, permitindo o rastreamento de versões e o histórico de alterações de todos os documentos.
- **Implantação Containerizada**: A aplicação Wiki.js é empacotada e implantada usando contêineres Docker, para garantir consistência e escalabilidade.
- **Monitoramento e Manutenção**: A solução inclui mecanismos de monitoramento, alertas, backups e atualizações automatizadas, para garantir a confiabilidade e a longevidade da wiki.

## Visão Geral da Arquitetura
A arquitetura do projeto consiste nos seguintes componentes principais:

1. **Microsoft Azure**: A plataforma de nuvem que hospeda todos os serviços necessários.
2. **Azure Database for PostgreSQL**: O serviço de banco de dados gerenciado que armazena o conteúdo da wiki.
3. **Azure Repos**: O sistema de controle de versão que acompanha as alterações nos documentos da wiki.
4. **Docker**: A plataforma de containerização utilizada para empacotar e implantar a aplicação Wiki.js.
5. **Wiki.js**: A plataforma wiki de código aberto que serve como interface para a colaboração da equipe.

![Diagrama da Arquitetura do Projeto](architecture-diagram.png)

## Guia de Implementação
Instruções detalhadas passo a passo para implantar a solução estão disponíveis no [Guia de Implementação](implementation-guide.md).

## Downloads
- [Guia de Implementação](implementation-guide.md)
- [Script Terraform](terraform-script.tf)
- [Playbook Ansible](ansible-playbook.yml)

