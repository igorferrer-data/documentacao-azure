# Deploy de uma Instância de Banco de Dados no Azure | Redundância LRS
## Objetivo
O objetivo deste guia é demonstrar como criar e configurar uma instância de banco de dados no Azure 

1. #### Criar Resource Group
    - Clique *"+Create"*
    - Selecione *"Subscription"* e *"Region"*
    - Crie um nome único para o Resource Group

2. #### Criar Database 
    *(O Banco de Dados SQL do Azure é um serviço de banco de dados relacional gerenciado, baseado no mecanismo do Microsoft SQL Server)* 

    - Na barra de pesquisa do Azure, digite *“SQL Database”* e selecione *“+ Create”*.

    [![alt text](https://github.com/clouder-km/Challenge-Azure-Dio/blob/main/image/DBA%20CREATE.PNG)

    - Na aba “Basics”, preencha os campos:
      - Subscription: Selecione sua assinatura
      - Resource Group: Selecione o grupo de recursos criado anteriormente.
      - Database Name: Insira um nome único para o banco de dados

       - Server: Crie um novo servidor , clique em *"Create new”.*

    - Preencha os campos:
      - Server name: *“Nome único para o servidor*“
      - Location: *“Mesma Região do Resource Group*“
      - Authetication method: *“Selecione um metodo de autenticação ou Ambos metodos de autenticação para o administrador do DBA possa ter acesso ao Database:*“
        - Microsoft Entra - Entrar usando as credenciais do Azure
        - SQL Authentication - Entrar definindo credenciais "Server Admin" e "password"

    ![alt text](https://github.com/clouder-km/Challenge-Azure-Dio/blob/main/image/DBA%20CREATE%20SERVER.PNG)
        
    - Clique em *“OK*“
        
    - Compute + storage: Selecione a configuração de desempenho e armazenamento conforme suas necessidades. 
      - Service tier : *“Selecionar a camada de serviço*“
      - Compute tier : *“Provisioned*“ - Custo fixo e Computação de alto desempenho -> Indicado para ambiente em produção ou *“Serverless*“ - Custo variavel , baseado no uso e permite auto-pause (pausa automaticamente o banco de dados quando estiver inativo pelo periodo especificado e retoma atividade quando estiver em uso)-> Indicado para ambiente de desenvolvimento

    ![alt text](https://github.com/clouder-km/Challenge-Azure-Dio/blob/main/image/CONFIGURE%20DBA.PNG)
    ![alt text](https://github.com/clouder-km/Challenge-Azure-Dio/blob/main/image/AUTO%20PAUSE.PNG)

   - Backup Storage redundancy 
     -*“LRS*“ - Grava os dados em 1 zona na mesma região - Ideal para ambientes menos críticos.
     -*“ZRS*“ - Grava os dados em 3 zonas diferentes na mesma região - Ideal para app que necessitam de alto disponibilidade e resiliência contra falhas de zona
     -*“GRS*“ - Grava os dados em 1 zona na mesma região e faz replicação para outra região gravando em 1 zona - Ideal para proteção contra desastres regionais.
     -*“GZRS*“ - Grava os dados em 3 zonas diferentes na mesma região e faz replicação para outra região em 1 zona.

    ![alt text](https://github.com/clouder-km/Challenge-Azure-Dio/blob/main/image/DBA%20PRONTO.PNG)

    - Clique em *“Review + Create”* e depois em *“Create”* e aguarde o Deploy

3. #### Configurar o Banco de Dados
    Após a criação da instância, é necessário configurar o banco de dados para garantir segurança e desempenho.

      - Firewall e redes virtuais: Configure as regras de firewall para permitir o acesso ao banco de dados.
      - Auditoria e ameaças: Ative a auditoria e a detecção de ameaças para monitorar atividades suspeitas.
      - Backups: Configure políticas de backup para garantir a recuperação de dados em caso de falhas.


## Conclusão
Seguindo estes passos, você conseguirá criar e configurar uma instância de banco de dados no Azure. Este processo envolve a criação de um grupo de recursos, a configuração detalhada da instância de banco de dados e a implementação de medidas de segurança e desempenho.

## Referência

- [Documentação Database Azure](https://azure.microsoft.com/pt-br/products/azure-sql/database/)
