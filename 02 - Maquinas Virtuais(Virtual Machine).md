# Implementação de Máquina Virtual #

## Objetivo 
Criar uma máquina virtual no Azure para para fins de laboratório.

## Solução 
Para atender a essa necessidade , a solução envolve os seguintes passos:

1. #### Criar um *"Resource Group"* - para organizar todos os recursos do projeto.
     - Na barra de pesquisa digite *"Resource Group"* e selecione *"+ Create"* e siga as instruções a seguir na Aba *"Basics"*:
     
        | Subscription | Resource Group | Region |
        |----------|----------|------------------|
        | Subscription1| Nome Unico | (US) East Us|
     - Clique em *"Review Create"* + *"Create"* - Aguarde fazer o Deploy.

    ![alt text](https://github.com/clouder-km/Challenge-Azure-Dio/blob/main/image/2%20-%20Resource%20Group.PNG)

    ![alt text](https://github.com/clouder-km/Challenge-Azure-Dio/blob/main/image/2.1%20-%20Notifica%C3%A7%C3%A3o%20Implementado.PNG)

2. #### Criar e Configurar Virtual Machine
      - Pesquise por *"Virtual Machine"* , *"+ Create"* , selecione *"Azure Virtual Machine"* e siga as instruções a seguir na Aba *"Basics"*:
      
     ![alt text](https://github.com/clouder-km/Challenge-Azure-Dio/blob/main/image/2.2%20create%20vm.PNG)
      
     - Em *"Size"* Selecione a maquina virtual com base nas necessidades de CPU , Memória e Armazenamento
     - Em Administrator Account - defina o username e password para que o administrador possa se conectar a Vm

     ![alt text](https://github.com/clouder-km/Challenge-Azure-Dio/blob/main/image/2.3%20create%20vm.PNG)

     - Next: Disk - Deixe em Default (como está) *lembre-se quando fazer implementações o azure sempre trás as melhores configurações sempre revise para diminuir os custos.*

    ![alt text](https://github.com/clouder-km/Challenge-Azure-Dio/blob/main/image/2.4%20create%20vm.PNG)
     - *"Review Create"* + *"Create"* Aguarde o Deploy

     ![alt text](https://github.com/clouder-km/Challenge-Azure-Dio/blob/main/image/2.6%20create%20VM.PNG)

## Conclusão
  Seguindo os passos descritos, você conseguirá criar e configurar uma máquina virtual no Azure para fins de laboratório de forma eficiente. Este processo envolve a criação de um grupo de recursos para organizar todos os componentes do projeto e a configuração detalhada da máquina virtual conforme suas necessidades específicas de CPU, memória e armazenamento. Lembre-se de revisar as configurações padrão oferecidas pelo Azure para otimizar custos e garantir que a máquina virtual atenda aos requisitos do seu projeto.

## Referência

- [Documentação Virtual Machine](https://learn.microsoft.com/pt-br/azure/virtual-machines/)
