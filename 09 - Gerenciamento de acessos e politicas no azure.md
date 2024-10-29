# Gerenciamento de acessos e politicas no azure

## Objetivo
Conhecer o Portal Service Trust e como utilizar locks e políticas no Azure para proteger e gerenciar recursos, garantindo conformidade e segurança no ambiente de nuvem.

## Microsoft Service Trust Portal

O **Microsoft Service Trust Portal (STP)** é um ponto central para informações sobre segurança, conformidade regulatória e privacidade relacionadas aos serviços de nuvem da Microsoft. Ele fornece uma variedade de conteúdos, ferramentas e outros recursos que ajudam a entender como os serviços de nuvem da Microsoft protegem seus dados e como você pode gerenciar a segurança e conformidade dos dados na nuvem.

 ![alt text](https://github.com/clouder-km/Challenge-Azure-Dio/blob/main/image/servicetrust.PNG)

### Tipos de Lock 

#### Lock Delete
  - A nivel do Resource Group este lock não deleta o resource group mas pode fazer alterações nos recursos. 
  - A nivel do Resource o lock não deleta os recursos. Agora Se tivermos o lock em um recurso e outro recurso não tiver lock e for deletar o Resource Group não irá deletar nenhum recurso.
#### Lock Read-Only 
  - A nivel do Resource Group este lock somente deixará ler as informações não irá deixar deletar e nem alterar (atualizar) qualquer recurso. 
  - A nivel do Resource somente aquele recurso não irá deixar deletar e alterar porém se deletar o resource group não irá deixar deletar da mesma forma.

## Lock Delete no Resource Group 

- Acesse o [Portal Azure]()
- Vá para Resource Group 
- Em *"Settings"* : *"Locks"*
  ![alt text](https://github.com/clouder-km/Challenge-Azure-Dio/blob/main/image/LOCK.PNG)

- *"+ add"*
  - Lock name: Nome do Lock
  - Lock Type: Tipo do Lock (Delete)
  - Notes: Mensagem importante para o Lock 

  ![alt text](https://github.com/clouder-km/Challenge-Azure-Dio/blob/main/image/LOCK2.PNG)

- Por exemplo caso o usuário administrador do ambiente não saiba do que se trata esse *"resource group ou resource"* e o usuário for deletar,  o azure vai apresentar mensagem de erro e o motivo do erro e o usuário vai para "locks" e aparecerá o lock com a mensagem que configuramos em *"notes"*.

- Em *"Overview"* clique em *"Delete Resource Group"* 
- Forneça o nome do *"resource group"*
- Marque a caixa * "Apply force delete ..."*
- Clique em *"Delete"* e confirme o *"Delete"*
 ![alt text](https://github.com/clouder-km/Challenge-Azure-Dio/blob/main/image/LOCK5.PNG)

- Aparecerá mensagem de erro
 ![alt text](https://github.com/clouder-km/Challenge-Azure-Dio/blob/main/image/LOCK6.PNG)

- Volte em "Locks" e veja que tem um lock e uma mensagem que configuramos.

  ![alt text](https://github.com/clouder-km/Challenge-Azure-Dio/blob/main/image/LOCK3.PNG)


## Lock Read no Resource

- Vá para o recurso Ex: Virtual Machine
- Clique na Vm que deseja colocar o lock
- Clique em *"Settings" 
   - *"Locks"*
   - *"+ add"* e preencha as informações (Read)
   ![alt text](https://github.com/clouder-km/Challenge-Azure-Dio/blob/main/image/LOCKREAD.PNG)

- Em *"Availability + Scale"* clique em *"Size"*
  - Selecione a atualização de Vm que atenda a sua necessidade
  - Click em *"resize"* e confirme *"resize"*
  ![alt text](https://github.com/clouder-km/Challenge-Azure-Dio/blob/main/image/LOCKREAD2.PNG)

- Aparecerá mensagem de erro
  ![alt text](https://github.com/clouder-km/Challenge-Azure-Dio/blob/main/image/LOCKREAD3.PNG)

- Volte em "Locks" e veja que tem um lock e uma mensagem que configuramos.

## Mover recursos

- Vá para *"Resource Group*" que irá remover os resources
- Selecione os resources que quer mover
- Clique em Move
- Clique em Move to another resource group
  ![alt text](https://github.com/clouder-km/Challenge-Azure-Dio/blob/main/image/MOVE1.PNG)

- Selecione o outro resource group e clique em next

  ![alt text](https://github.com/clouder-km/Challenge-Azure-Dio/blob/main/image/MOVE2.PNG)

- Aguarde checar e clique em Next

  ![alt text](https://github.com/clouder-km/Challenge-Azure-Dio/blob/main/image/MOVE3.PNG)

- Marque a caixa *"I understand ... "*
  ![alt text](https://github.com/clouder-km/Challenge-Azure-Dio/blob/main/image/move4.PNG)
 
- Aguarde mover e aparecerá a mensagem de confirmação que foi movido

  ![alt text](https://github.com/clouder-km/Challenge-Azure-Dio/blob/main/image/move5.PNG)

## Atribuição de Politicas

- Procure por "Policy" 
- Vá para "Assignments"
- "Assign Policy"
- Em Scope " deixa a subscription"
- Em Policy Definition "Defina uma politica"

  ![alt text](https://github.com/clouder-km/Challenge-Azure-Dio/blob/main/image/policy1.PNG)

- Em parameters " defina uma tag *RH" 

  ![alt text](https://github.com/clouder-km/Challenge-Azure-Dio/blob/main/image/POLICY2.PNG)

- Review Create *"Save"*

- ** Neste caso defini uma politica no nivel da Assinatura para exigir a tag RH quando criar um grupo de recurso.**
- ** Para testar esta politica - Tentei criar um resource group sem tag e na ultima etapa quando clicar em create vai aparecer essa mensagem de erro. **

  ![alt text](https://github.com/clouder-km/Challenge-Azure-Dio/blob/main/image/POLICY3.PNG)

- ** Agora se atribuir a tag RH irá criar o resource group **

  ![alt text](https://github.com/clouder-km/Challenge-Azure-Dio/blob/main/image/pOLICY4.PNG)
  ![alt text](https://github.com/clouder-km/Challenge-Azure-Dio/blob/main/image/POLICY5.PNG) 

## Conclusão

Locks e políticas no Azure são ferramentas essenciais para garantir a segurança e conformidade dos recursos na nuvem. Os locks protegem contra exclusões e alterações acidentais, enquanto as políticas asseguram que os recursos estejam em conformidade com os padrões organizacionais. Implementar essas práticas ajuda a manter um ambiente de nuvem seguro e bem gerenciado.

## Referência

- [Microsoft Service Trust Portal](https://servicetrust.microsoft.com/)
- [Documentação Policy Azure](https://learn.microsoft.com/en-us/azure/governance/policy/)
