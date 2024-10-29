# Calculadoras de Custos do Azure
## Objetivo 
Demonstrar como utilizar as calculadoras de preços do Azure para estimar e gerenciar os custos dos serviços na nuvem.

## Introdução

O Microsoft Azure oferece uma variedade de serviços em nuvem que podem ser utilizados para diferentes finalidades, desde armazenamento até inteligência artificial. No entanto, é crucial entender e gerenciar os custos associados a esses serviços para garantir uma operação eficiente e econômica.

## Ferramentas Utilizadas

### Calculadora de Preços do Azure

A Calculadora de Preços do Azure permite que você estime os custos dos serviços do Azure com base no uso antecipado. É uma ferramenta essencial para planejamento e orçamento. 
- **A calculadora serve para ter uma ideia do valor de custo por mês. Porém, este custo é estimado, pois ainda se aplicam impostos.**

### Calculadora de Custo Total de Propriedade (TCO)

A Calculadora de TCO ajuda a estimar a economia de custos ao migrar suas cargas de trabalho para o Azure. Ela considera os custos de infraestrutura, licenciamento e outros fatores.

- **A TCO faz a comparação do ambiente on-premises com o ambiente de nuvem, estimando valores aproximados em anos.**

## Como Utilizar as Calculadoras

### Acessar a Calculadora de Preços

1. Vá para [Calculadora de Preços do Azure](https://azure.microsoft.com/pt-br/pricing/calculator/)

![alt text](https://github.com/clouder-km/Challenge-Azure-Dio/blob/main/image/princing%20calculator%20azure.PNG)

### Criar uma Estimativa

1. Selecione os serviços que desejam implementar no azure.
2. Configure as opções de cada serviço para calcular a estimativa de custo.
3. Revise o resumo da estimativa para ver os custos totais.
5. Salve ou exporte a estimativa para referência futura.

![alt text](https://github.com/clouder-km/Challenge-Azure-Dio/blob/main/image/princing%20calculator%20azure%201.PNG)

### Passo 3: Utilizar a Calculadora de TCO

1. Acesse a [Calculadora TCO do Azure](https://azure.microsoft.com/pt-br/pricing/tco/calculator/)
2. Insira os detalhes da sua infraestrutura atual.

![alt text](https://github.com/clouder-km/Challenge-Azure-Dio/blob/main/image/TCO1.PNG)

3. Preencha as informações de acordo com os gastos da empresa com seu Datacenter.

![alt text](https://github.com/clouder-km/Challenge-Azure-Dio/blob/main/image/TCO2.PNG)

3. Compare os custos atuais com os custos estimados no Azure.

![alt text](https://github.com/clouder-km/Challenge-Azure-Dio/blob/main/image/tco3.PNG)

## Exemplos Utilizados

### Exemplo 1: Estimativa de Custos para um Aplicativo Web (Calculadora de Preços do Azure)

- **Serviços Utilizados**: App Service, SQL Database, Storage Account
- **Configuração**:
  - App Service: Plano Standard, 2 instâncias
  - SQL Database: 100 DTUs, 250 GB
  - Storage Account: 1 TB, LRS


### Exemplo 2: Migração do On-Premise para o Azure (Calculadora TCO do Azure)

- **Serviços Utilizados**: Virtual Machines, Azure Backup
- **Configuração**:
  - Virtual Machines: 10 VMs, Standard_D2s_v3
  - Azure Backup: 1 TB

## Conclusão

Utilizar as calculadoras de preços do Azure é fundamental para planejar e gerenciar os custos dos serviços em nuvem. Com essas ferramentas, você pode tomar decisões e otimizar seus custos.

## Referências

- [Documentação Custos Azure](https://learn.microsoft.com/pt-br/azure/cost-management-billing/costs/pricing-calculator)
