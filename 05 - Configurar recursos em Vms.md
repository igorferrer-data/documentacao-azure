# Implementação de uma Solução Escalável no Azure | VMs 

## Objetivo
Criar e configurar uma infraestrutura escalável e de alta disponibilidade no Azure para suportar por exemplo: aplicativo web, utilizando grupos de recursos, máquinas virtuais, conjuntos de dimensionamento automático (scale sets) e conjuntos de disponibilidade (availability sets).

### Instruções: 

- Criar um Resource Group:
No portal do Azure, crie um novo grupo de recursos para organizar todos os recursos relacionados ao projeto.

#### Configurar Virtual Machine , Scale Set , Avalability Set:

- No portal do Azure, vá para *“Virtual Machines”* e clique em *“+ Create”*.
Preencha os campos na aba *“Basics”*:

   - Subscription: *Selecione sua assinatura*.
   - Resource Group: *Selecione o grupo de recursos*.
   - Virtual Machine Name: Insira um nome único para a VM.
   - Region: *"Escolha a mesma região do grupo de recursos*".
   - Availability Options: *"Availability Set"*

![alt text](https://github.com/clouder-km/Challenge-Azure-Dio/blob/main/image/4%20-%20RECURSO%20VMS.PNG)

![alt text](https://github.com/clouder-km/Challenge-Azure-Dio/blob/main/image/4%20-%20RECURSO%20VMS%202.PNG)


- Em Availability Sets clique em *"Create New"*
  - Name : Defina o nome do availability sets
   - Defina Fault Domains e Update Domains (Ao distribuir VMs em diferentes Fault Domain, o Azure garante que uma falha de hardware em um rack não afete todas as VMs) e (O Azure distribui VMs em diferentes Update Domains para garantir que apenas uma parte das VMs seja reiniciada de cada vez durante as atualizações, minimizando o impacto no serviço.)

 
![alt text](https://github.com/clouder-km/Challenge-Azure-Dio/blob/main/image/4%20-%20CREATE%20AVAIBILITY%20SET.PNG)

   - Clique em *"OK"*

   - Image: *"Selecione a imagem do sistema operacional"*.
   - Size: *"Escolha o tamanho da VM."*
    
![alt text](https://github.com/clouder-km/Challenge-Azure-Dio/blob/main/image/4%20-%20RECURSO%20VMS%202.PNG)

- Administrator Account: Defina o username e password do administrador.

![alt text](https://github.com/clouder-km/Challenge-Azure-Dio/blob/main/image/4%20-%20ADMIN.PNG)

- Clique em “Next: Review Create"
- Revise todas as configurações e crie a VM.
- Aguarde o Deploy

#### Implementar Scale Set

- No portal do Azure, vá para “Virtual Machine Scale Sets” e clique em “+ Create”.
- Preencha os campos na aba “Basics”:
*"Subscription"*: Selecione sua assinatura.
*"Resource Group*": Selecione o grupo de recursos criado anteriormente.
*"Scale Set Name*": Insira um nome único para o Scale Set.
Availability Zone: None
Region: Escolha a mesma região do grupo de recursos.

![alt text](https://github.com/clouder-km/Challenge-Azure-Dio/blob/main/image/4%20-%20Scale%20Set%201.PNG)

- Em Scaling Mode clique em "Autoscaling" (Baseado em metricas do CPU)
  - Defina as regras de dimensionamento para que novas VMs sejam provisionadas automaticamente quando a demanda aumentar e desprovisionadas quando a demanda diminuir. 
  - Configurar Regras de Dimensionamento:
Defina as métricas de desempenho (como uso de CPU ou memória) que acionarão o provisionamento ou desprovisionamento de VMs adicionais.
Configure o número mínimo e máximo de VMs no scale set para garantir que haja capacidade suficiente durante os picos de demanda.

![alt text](https://github.com/clouder-km/Challenge-Azure-Dio/blob/main/image/4%20-%20Scale%20Set%202.PNG)


Image: Selecione a imagem do sistema operacional.
Size: Escolha o tamanho das VMs.

Clique em “Review + Create” e depois em “Create”.

![alt text](https://github.com/clouder-km/Challenge-Azure-Dio/blob/main/image/4%20-%20Scale%20Set%203.PNG)
![alt text](https://github.com/clouder-km/Challenge-Azure-Dio/blob/main/image/4%20-%20Scale%20set%204.PNG)
![alt text](https://github.com/clouder-km/Challenge-Azure-Dio/blob/main/image/4%20-%20Scale%20Set%205.PNG)


Scale Set : O Azure provisiona e desprovisiona VMs automaticamente com base na demanda, garantindo que o aplicativo web possa lidar com picos de tráfego sem interrupções.
Custo-Efetivo: O cliente paga apenas pelo uso efetivo das VMs, otimizando os custos durante os períodos de baixa demanda.
Alta Disponibilidade: A solução garante alta disponibilidade do aplicativo web, proporcionando uma experiência de usuário consistente e confiável.

## Conclusão

Essa abordagem garante que você esteja bem preparado para lidar com o aumento de tráfego, oferecendo uma solução escalável, custo-efetiva e de alta disponibilidade. Utilizando grupos de recursos, máquinas virtuais com Availability Sets e Scale Sets, você pode garantir que seu aplicativo web possa lidar com picos de tráfego sem interrupções, pagando apenas pelo uso efetivo das VMs e proporcionando uma experiência de usuário consistente e confiável.

## Referência
- [Documentação Scale Set](https://learn.microsoft.com/en-us/azure/virtual-machine-scale-sets/overview)
- [Documentação Availability Set](https://learn.microsoft.com/en-us/azure/virtual-machines/availability)
