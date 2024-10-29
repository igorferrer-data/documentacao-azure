# Storage - Configuração | Redundancy GRS | Cenario de Backup

### Criar uma Conta de Armazenamento

Lembre-se é importante sempre criar um Resource Group para organizar seus resources no Azure.

A conta de armazenamento é usada para armazenar dados de diferentes tipos, como blobs, arquivos, filas e tabelas.

### Instruções:

1. No portal do Azure, vá para *"Storage Accounts"* e clique em *"+ Create"*.
   - Preencha os campos na aba *"Basics"*:
   - Subscription: *"Selecione sua assinatura"*
   - Resource Group: *"Selecione o grupo de recursos"*
   - Storage Account Name: Insira um nome único para a conta de armazenamento.
   - Region: Escolha a mesma região do grupo de recursos.
   - Performance: Selecione “Standard” para armazenamento geral ou “Premium” para desempenho mais alto.
   - Replication: Escolha o tipo de replicação (por exemplo, GRS - Geo Redundant Storage).
   - Clique em “Review + Create” e depois em   “Create”.
   - *"Next : *"Review Create "* (Revise todas as configurações)
   - *"+ Create"*

  ![alt text](https://github.com/clouder-km/Challenge-Azure-Dio/blob/main/image/1%20-%20Storage.PNG)
  ![alt text](https://github.com/clouder-km/Challenge-Azure-Dio/blob/main/image/2%20-%20storage%20deploy.PNG)

2. Criar um Contêiner de Blob
Descrição: Um contêiner de blob é usado para armazenar grandes quantidades de dados não estruturados.

- Na conta de armazenamento, vá *"Data Storage"* “Containers” e clique em “+ Container”.
   - Insira um nome para o contêiner e defina o nível de acesso private
   - Clique em “Create”.

![alt text](https://github.com/clouder-km/Challenge-Azure-Dio/blob/main/image/2%20-%20BLOB.PNG)

## Migração de dados

  - A migração de dados é o processo de transferir dados de um sistema ou ambiente de armazenamento para outro. Esse processo pode ser complexo e requer planejamento cuidadoso para garantir que os dados sejam transferidos de forma segura e eficiente. Aqui estão os passos principais para realizar uma migração de dados:

## Planejamento e Avaliação
  - Revisar os Dados de Origem: Examine e descreva os dados existentes. Identifique a estrutura e os atributos dos dados que serão migrados.
  - Determinar o Destino: Escolha a solução de armazenamento de dados de destino com base na estrutura e nos requisitos dos dados de origem1.
  - Definir a Estratégia de Migração: Decida se a migração será feita de uma só vez (big bang) ou em etapas (trickle-feed). O método big bang envolve mover todos os dados de uma vez, enquanto o trickle-feed migra os dados em pequenas partes ao longo do tempo.

## Preparação dos Dados
  - Mapeamento de Dados: Identifique a estrutura do sistema de destino e mapeie as tabelas e campos correspondentes do sistema de origem.
  - Perfil de Dados: Verifique a qualidade e a consistência dos dados de origem. Identifique problemas de dados e regras de conversão necessárias.
  - Transformação de Dados: Aplique as regras de conversão e transforme os dados do sistema de origem para o formato do sistema de destino3.

## Execução da Migração

  - Extração de Dados: Remova os dados do sistema atual para começar a trabalhar neles1.
  - Carregamento de Dados: Transfira os dados transformados para o sistema de destino.
  - Reconciliamento de Dados: Verifique se os dados foram migrados corretamente e completamente. Acompanhe o progresso da migração e os pontos de reversão.
## Teste e Validação

  - Testar a Solução: Realize testes para garantir que os dados foram migrados corretamente e que o sistema de destino está funcionando conforme esperado.
  - Auditoria de Dados: Realize uma auditoria final para garantir que todos os dados foram migrados e que não há perda ou corrupção de dados.
## Monitoramento e Ajustes
  - Monitorar o Desempenho: Utilize ferramentas de monitoramento para acompanhar o desempenho do sistema de destino e fazer ajustes conforme necessário.
  - Ajustar Regras de Migração: Se necessário, ajuste as regras de migração para otimizar o desempenho e a eficiência.
## Conclusão
- Seguindo esses passos, você pode configurar uma conta de armazenamento no Azure com redundância GRS e criar um contêiner de blob para armazenar grandes quantidades de dados não estruturados. A migração de dados, quando bem planejada e executada, garante que os dados sejam transferidos de forma segura e eficiente para o novo ambiente de armazenamento.

- Ao monitorar e ajustar continuamente o desempenho, você pode otimizar a eficiência e garantir que os dados estejam sempre disponíveis e protegidos. Essa abordagem não só melhora a resiliência e a disponibilidade dos seus dados, mas também proporciona uma solução de backup robusta e confiável. 

# Referência

- [Documentação Storage Account Azure](https://learn.microsoft.com/en-us/azure/storage/)
- [Documentação Migrate Azure](https://learn.microsoft.com/en-us/azure/migrate/)
