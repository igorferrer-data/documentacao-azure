# Ferramentas de Implantação e Gerenciamento no Azure

## Objetivo
Apresentar as principais ferramentas de implantação e Gerenciamento no Azure, destacando o uso do Cloud Shell, a automação via Bash/PowerShell , linguagem Bicep e Azure Arc.

### Cloud Shell no Azure

O Azure Cloud Shell é uma ferramenta que você pode usar diretamente no navegador para gerenciar seus recursos no Azure.

- Acesso Fácil: Você pode acessar e gerenciar seus recursos do Azure de qualquer lugar, sem precisar instalar nada.
- Escolha de Shell: Pode usar comandos do Bash ou do PowerShell, conforme sua preferência.
- Ferramentas Prontas: Já vem com várias ferramentas e linguagens de programação instaladas.
- Armazenamento Seguro: Seus arquivos são salvos e mantidos seguros entre as sessões.
- Editor de Arquivos: Tem um editor de arquivos integrado para criar e editar arquivos diretamente.

### Para acessar o Cloud Shell
- No canto superior direito clique em "Cloud Shell" abrirá em Bash  
  ![alt text](https://github.com/clouder-km/Challenge-Azure-Dio/blob/main/image/cloud%20shell1.PNG)  
- Em *"Switch to Power Shell"* troca para o Power Shell  
  ![alt text](https://github.com/clouder-km/Challenge-Azure-Dio/blob/main/image/cloud%20shell2.PNG)  
- Em *"Manage Files"* pode fazer upload e download de arquivos.  
  ![alt text](https://github.com/clouder-km/Challenge-Azure-Dio/blob/main/image/cloud%20shell3.PNG)  

- Versão Bash - Interface Preta  
  ![alt text](https://github.com/clouder-km/Challenge-Azure-Dio/blob/main/image/cloud%20shell4.PNG)
- Versão Power Shell - Interface Azul
  ![alt text](https://github.com/clouder-km/Challenge-Azure-Dio/blob/main/image/cloud%20shell5.PNG)

*" Podemos acessar o azure via comando usando *"Bash ou PowerShell"* através da sua Maquina Local é possivel desde que esteja instalado os modulos do Azure nela.

### Automation (Automação)

#### Via Bash/PowerShell

"Implementar um recurso qualquer manualmente no azure" Ex: Virtual Machine | Vnet
- Na aba *"Automation"* em Vnet temos:
  - CLI/PS : Mostra alguns comandos de implementação de uma Vnet para serem executados via comando *"Bash ou PowerShell"*
   ![alt text](https://github.com/clouder-km/Challenge-Azure-Dio/blob/main/image/CLI.PNG)
   ![alt text](https://github.com/clouder-km/Challenge-Azure-Dio/blob/main/image/PS.PNG)
- Export Template :  Mostra o arquivo (Template) no formato JSON para salvar em nossa maquina local e re-utilizar no futuro o mesmo recurso configurado , quando necessário. Pode ser implementado via comando no **"Bash ou power shell"** no Cloud Shell
   ![alt text](https://github.com/clouder-km/Challenge-Azure-Dio/blob/main/image/EXPORT%20TEMPLATE.PNG)

    
- Ao salvar o arquivo na Maquina Local temos o arquivo Template.JSON e Parameters.JSON , o Template é o recurso em comando e o Parameters é usado para alterar o template.
    ![alt text](https://github.com/clouder-km/Challenge-Azure-Dio/blob/main/image/arquivos.PNG)

## Azure Arc

O **Azure Arc** é uma solução que estende a plataforma Azure para gerenciar recursos em datacenters, na borda e em ambientes multinuvem. Ele permite que você gerencie servidores, clusters de Kubernetes e serviços de dados como se estivessem no Azure, usando as mesmas ferramentas e práticas.

#### Abas do Azure Arc

  ![alt text](https://github.com/clouder-km/Challenge-Azure-Dio/blob/main/image/ARC.PNG)


- Azure Arc Resources - Esta aba permite que você gerencie recursos que não estão no Azure, como servidores físicos, máquinas virtuais e clusters Kubernetes, como se estivessem no Azure.

- Host Environments - Aqui, você pode gerenciar os ambientes de hospedagem, incluindo servidores e clusters Kubernetes, que são habilitados pelo Azure Arc.

- Data Services - Esta aba oferece serviços de dados habilitados pelo Azure Arc, como SQL Managed Instance e PostgreSQL. Esses serviços podem ser executados localmente, na borda ou em outras nuvens.

- IoT - Permite a integração e gerenciamento de dispositivos IoT usando o Azure Arc, facilitando a administração de dispositivos conectados em diferentes ambientes.

- Application Services - Esta aba é usada para gerenciar e implantar aplicativos em ambientes híbridos e multi-nuvem, utilizando o Azure Arc para garantir consistência e controle centralizado.

- Licenses - Aqui você pode gerenciar as licenças e assinaturas associadas aos recursos habilitados pelo Azure Arc.

- Management - Esta aba oferece ferramentas de gerenciamento centralizado para monitorar, atualizar e manter a integridade dos recursos habilitados pelo Azure Arc.

- Devops - Integração com ferramentas DevOps para automatizar a implantação e gerenciamento de aplicativos e serviços em ambientes híbridos e multi-nuvem.

O Azure Arc é usado para simplificar a governança e o gerenciamento de ambientes híbridos e multinuvem, proporcionando uma experiência consistente e centralizada.


## Conclusão

O Azure oferece uma gama robusta de ferramentas para implantação e gerenciamento de recursos, permitindo uma administração eficiente e centralizada. O Cloud Shell facilita o acesso e gerenciamento de recursos diretamente do navegador, enquanto a automação via Bash/PowerShell e a linguagem Bicep permitem a implementação e gerenciamento de recursos de forma programática e repetível.

O Azure Arc expande ainda mais essas capacidades, permitindo que você gerencie recursos em datacenters, na borda e em ambientes multinuvem como se estivessem no Azure

Essas ferramentas juntas proporcionam uma plataforma poderosa e flexível para atender às necessidades de gerenciamento e implantação em ambientes de TI modernos e complexos.

# Referência

- [Documentação de Aplicativo via ARM](https://learn.microsoft.com/pt-br/azure/app-service/quickstart-arm-template?pivots=platform-linux)
- [Documentação Azure Arc](https://learn.microsoft.com/pt-br/azure/azure-arc/overview)
