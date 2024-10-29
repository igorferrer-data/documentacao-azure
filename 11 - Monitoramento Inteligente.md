# Monitoramento Inteligente

## Objetivo
 Fornecer uma visão clara e prática de como essa ferramenta pode ser utilizada para monitorar recursos no Azure de maneira eficiente

## Serviços de Monitoramento no Azure

### Azure Monitor

O "Azure Monitor" é uma solução abrangente para coletar, analisar e responder a dados de monitoramento de ambientes de nuvem e locais. Ele ajuda a maximizar a disponibilidade e o desempenho de aplicativos e serviços, fornecendo insights detalhados sobre a operação dos recursos.

![alt text](https://github.com/clouder-km/Challenge-Azure-Dio/blob/main/image/MONITOR.PNG)


### Activity Log
A aba *"Activity Log"* fornece um registro de todas as operações realizadas nos recursos do Azure. Ele ajuda a rastrear quem fez o quê e quando, permitindo auditorias e diagnósticos de problemas. Você pode visualizar eventos como criação, modificação e exclusão de recursos.

### Alerts
A aba *"Alerts"* permite configurar alertas para monitorar a integridade e o desempenho dos seus recursos. Você pode definir regras de alerta baseadas em métricas ou logs, e configurar ações a serem tomadas quando um alerta é disparado, como enviar notificações por email ou SMS.

### Metrics
A aba *"Metrics"* oferece uma visão detalhada das métricas de desempenho dos seus recursos. Você pode visualizar gráficos em tempo real e históricos, criar dashboards personalizados e configurar alertas baseados em métricas específicas, como uso de CPU, memória e latência.

### Change Analysis
A aba *"Change Analysis"* ajuda a identificar mudanças nos seus recursos que podem ter causado problemas. Ele fornece uma visão detalhada das alterações feitas, incluindo mudanças em propriedades de recursos e configurações. Isso é útil para diagnosticar e resolver problemas rapidamente.

### Insights
A aba *"Insights"* no Azure Monitor oferece visualizações personalizadas e detalhadas para monitorar diferentes tipos de recursos. Essas visualizações são projetadas para fornecer uma visão abrangente e específica do desempenho e da integridade dos seus recursos. Aqui estão alguns exemplos de Insights disponíveis:

- *"Azure VM Insights"*: Monitora o desempenho e a integridade das suas Máquinas Virtuais (VMs) e Conjuntos de Escala de Máquinas Virtuais no Azure. Ele analisa o desempenho dos VMs e monitora seus processos e dependências.
- *"Azure Container Insights"*: Monitora o desempenho das cargas de trabalho de contêineres implantadas em clusters Kubernetes gerenciados no Azure Kubernetes Service (AKS). Ele coleta métricas de controladores, nós e contêineres, além de logs de contêineres.
- *"Azure Network Insights"*: Fornece uma visão abrangente da integridade e das métricas de todos os seus recursos de rede. Isso inclui a capacidade de identificar dependências de recursos e resolver problemas de rede de forma eficiente.
- *"Azure Storage Insights"*: Oferece monitoramento abrangente das suas contas de armazenamento do Azure, fornecendo uma visão unificada do desempenho, capacidade e disponibilidade dos serviços de armazenamento.

## Azure Advisor

O "Azure Advisor" é um serviço que oferece recomendações personalizadas para otimizar suas implantações no Azure. Ele analisa a configuração e o uso dos recursos e sugere melhorias em áreas como alta disponibilidade, segurança, desempenho e custo.

![alt text](https://github.com/clouder-km/Challenge-Azure-Dio/blob/main/image/Advisor.PNG)

### Overview
A aba *"Overview"* fornece uma visão geral das recomendações do Azure Advisor.

### Getting Started
A aba *"Getting Started"* oferece orientações e recursos para ajudar você a começar a usar o Azure Advisor. Inclui tutoriais, documentação e exemplos de como configurar e utilizar as recomendações do Advisor para otimizar seus recursos no Azure.

### Advisor Score
A aba *"Advisor Score"* apresenta uma pontuação que reflete a eficácia das suas práticas de gerenciamento de recursos no Azure. A pontuação é baseada nas recomendações do Advisor e ajuda a medir o progresso na implementação de melhorias sugeridas.

### Recommendations
A aba *"Recommendations"* lista todas as recomendações personalizadas fornecidas pelo Azure Advisor. As recomendações são categorizadas em áreas como alta disponibilidade, segurança, desempenho e custo. Cada recomendação inclui detalhes sobre o impacto potencial e as ações sugeridas para melhoria.

### Monitoring
A aba *"Monitoring"* permite acompanhar o status das recomendações implementadas e monitorar o impacto das mudanças feitas com base nas sugestões do Advisor. Isso ajuda a garantir que as melhorias estejam sendo efetivamente aplicadas e mantidas.

### Settings
A aba *"Settings"* permite configurar as preferências do Azure Advisor, como a frequência das análises e as notificações de recomendações. Você pode personalizar as configurações para receber alertas e relatórios conforme suas necessidades.

### Support
A aba *"Support"* oferece acesso a recursos de suporte e ajuda relacionados ao Azure Advisor. Inclui links para documentação, tutoriais, fóruns de comunidade e opções de suporte técnico para resolver dúvidas e problemas específicos.

### Services Health

Os serviços de saúde no Azure incluem:

- "Azure Service Health": Fornece informações sobre a integridade dos serviços do Azure, notificando sobre problemas e manutenção planejada.
- "Resource Health": Monitora a integridade dos recursos individuais, ajudando a diagnosticar e resolver problemas rapidamente.
- "Azure Status": Exibe o status global dos serviços do Azure, informando sobre interrupções e problemas conhecidos.

Esses serviços ajudam a garantir que você esteja sempre informado sobre a integridade e o desempenho dos seus recursos no Azure.

## Conclusão

Os serviços de monitoramento no Azure, como o Azure Monitor, Azure Advisor e Services Health, são fundamentais para garantir a eficiência e a integridade dos seus recursos na nuvem. O Azure Monitor oferece uma visão abrangente e detalhada do desempenho e da operação dos seus recursos, enquanto o Azure Advisor fornece recomendações personalizadas para otimização. Já os serviços de saúde, como o Azure Service Health e o Resource Health, mantêm você informado sobre a integridade dos serviços e recursos, permitindo uma resposta rápida a problemas.

Essas ferramentas são essenciais para uma gestão proativa e eficiente da infraestrutura em nuvem, ajudando a maximizar a disponibilidade, segurança e desempenho dos seus aplicativos e serviços.

 ## Referências

- [Azure Monitor](https://learn.microsoft.com/pt-br/azure/azure-monitor/overview)
