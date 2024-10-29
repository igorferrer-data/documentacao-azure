# Conceitos para Microsoft Entra ID e Segurança

## Objetivo

O objetivo é ajudar a fornecer uma visão geral das funcionalidades e benefícios do Microsoft Entra ID e da Segurança na plataforma do Azure. Essas ferramentas são essenciais para gerenciar identidades e controlar o acesso a recursos em ambientes de nuvem e locais, garantindo a segurança e a integridade dos dados da organização.

### Microsoft Entra ID

O Microsoft Entra ID é uma plataforma baseada na nuvem da Microsoft para gerenciamento de identidade e acesso a serviços. Dentre suas funcionalidades, temos:

- **Authentication (Autenticação)**: Verificação da identidade do usuário.
- **Single Sign-On (SSO)**: Uma vez feito o login, não é necessário fazer novamente para acessar outros serviços.
- **Application Management (Gerenciamento de Aplicações)**: Controle e gerenciamento de aplicativos.
- **Business to Business (B2B)**: Convidar pessoas de outras empresas (por exemplo, consultores em nuvem) para ajudar no seu tenant (ambiente de nuvem) através de um convite enviado diretamente para o e-mail dessa pessoa.
- **Business to Customer (B2C)**: Convidar seus clientes para acessar sua plataforma, criando automaticamente outro tenant para separar o ambiente dos colaboradores do ambiente dos clientes.
- **Device Management (Gerenciamento de Dispositivos)**: Controle e gerenciamento de dispositivos que acessam os serviços.
- **Role-Based Access Control (RBAC)**: Controle de acesso baseado em funções, permitindo a atribuição de permissões granulares aos usuários com base em suas funções dentro da organização.

#### Como utilizar o B2B ?

- Faça o login no Azure 
- Procure por Microsoft Entra ID
- Em Overview *"+ add" , "user" , "Invite External User"*

![alt text](https://github.com/clouder-km/Challenge-Azure-Dio/blob/main/image/B2B.PNG)

- Em *"basics"* somente o *"Email"* é obrigatório preencher, o restante é opcional.

![alt text](https://github.com/clouder-km/Challenge-Azure-Dio/blob/main/image/B2B1.PNG)

- Em *"Properties"* confira a imagem abaixo:

![alt text](https://github.com/clouder-km/Challenge-Azure-Dio/blob/main/image/B2B2.PNG)

*"Aqui é tudo opcional , mas para melhores práticas sempre é bom colocar as informações importantes"*

- Em "*Assigments"* vai em *"add role"* (adicione uma role (papel), para que este usuário possa exercer uma role dentro do seu ambiente) neste exemplo adicionei a *"role de Global Administrator"* para fins de laboratório mas para melhores práticas de acordo com o *"job title"* definido no inicio *"System Administrator"* seria *"role de Owner (Proprietário) ou Contributor (colaborador)"*.

Proprietário: Concede acesso total para gerenciar todos os recursos, incluindo a capacidade de atribuir funções a outros usuários.

Colaborador: Permite gerenciar todos os recursos, mas não permite atribuir funções a outros usuários.

![alt text](https://github.com/clouder-km/Challenge-Azure-Dio/blob/main/image/B2B3.PNG)

- Clique em *"Select"*
- Clique em *"Review + Invite"* (revise todas as informações)

![alt text](https://github.com/clouder-km/Challenge-Azure-Dio/blob/main/image/B2B4.PNG)
![alt text](https://github.com/clouder-km/Challenge-Azure-Dio/blob/main/image/B2B5.PNG)

- Clique em *"Invite"*

- O email chegará a este usuário dessa forma abaixo e este usuário poderá acessar o seu ambiente para exercer a função que lhe foi concedida.

![alt text](https://github.com/clouder-km/Challenge-Azure-Dio/blob/main/image/EMAIL%20RECEBE.PNG)

#### Como utilizar o B2C ?

- No menu do portal do Azure ou na Página Inicial, selecione *"Create resource"*

![alt text](https://github.com/clouder-km/Challenge-Azure-Dio/blob/main/image/B2C1.PNG)

- Pesquise e selecione *"Azure Active Directory B2C"* e selecione *"Create"*

![alt text](https://github.com/clouder-km/Challenge-Azure-Dio/blob/main/image/B2C2.PNG)

- Organization name: insira um nome para o seu Azure AD B2C.
- Initial domain name: insira um nome de domínio para o seu Azure AD B2C.
- Location, selecione seu país/região na lista. Se o país/região selecionado tiver uma opção de complemento Go-Local, como Japão ou Austrália, e você quiser armazenar seus dados exclusivamente nesse país/região, marque a caixa de seleção Armazenar dados do Microsoft Entra Core Store e componentes e dados de serviço do Microsoft Entra no local selecionado. O complemento Go-Local é um complemento pago cuja cobrança é adicionada às cobranças de licenças do Azure AD B2C Premium P1 ou P2. Não é possível alterar a região de residência de dados depois de criar seu Azure AD B2C.
- Subscription, selecione sua subscription na lista.
- Resource Group, selecione ou pesquise pelo grupo de recursos que conterá no Tenant (Azure AD B2C)

![alt text](https://github.com/clouder-km/Challenge-Azure-Dio/blob/main/image/B2C3.PNG)

- Clique em *"Review + Create"* (revise as informações) e Clique *"Create"*

- Para começar a usar seu novo Tenant do Azure AD B2C, você precisa alternar para o diretório que contém o novo Tenant:

  - Clique no canto superior direito onde esta escrito Diretório Padrão e clique em *"Switch Directory"* Clique em "Switch"
  
![alt text](https://github.com/clouder-km/Challenge-Azure-Dio/blob/main/image/B2C4.PNG)


  ### Segurança

- **Multi-factor Authentication (MFA)**: Fornece segurança adicional para suas identidades exigindo dois ou mais elementos para autenticação completa.

  Por exemplo:
  - Algo que você sabe: Pode ser seu login e senha para entrar no Azure.
  - Algo que você possui: Pode ser um token para acessar um determinado site ou app.
  - Algo que você é: Pode ser a digital do seu dedo.

- #### Como Ativar o MFA?
    - Faça login no [Portal Azure](https://portal.azure.com)
    - Na barra procure por *"Microsoft Entra ID"*
    - No canto esquerdo vá para *"Security"* e clique em *"Manage" e "Multifactor Authentication"*  
    - Clique em "Users" e Clique em "Start" para ativar o MFA.  

    - Para usar o MFA precisa garantir uma Subscription Premium conforme mostra a imagem abaixo.

![alt text](https://github.com/clouder-km/Challenge-Azure-Dio/blob/main/image/MFA1.PNG)
![alt text](https://github.com/clouder-km/Challenge-Azure-Dio/blob/main/image/MFA2.PNG)

![alt text](https://github.com/clouder-km/Challenge-Azure-Dio/blob/main/image/MFA3.PNG)

[Documentação MFA](https://learn.microsoft.com/pt-br/entra/identity/authentication/tutorial-enable-azure-mfa)



- **Conditional Access (Acesso Condicional)**: Usado no Entra ID para tomar decisões através de sinais, por exemplo, *"IP Location"*. Se um funcionário tentar acessar a plataforma do Azure de um local diferente da empresa, o acesso condicional pode negar o acesso ou solicitar um MFA para autenticação, garantindo maior segurança para a empresa. Outros sinais que podem ser usados incluem:
  
  - User (Usuário)
  - Device (Dispositivo)
  - Application (Aplicação)
  - Detection Risk (Detecção de Risco) 

![alt text](https://github.com/clouder-km/Challenge-Azure-Dio/blob/main/image/Conditional%20Access.PNG)

### Microsoft Defender for Cloud

O Microsoft Defender for Cloud é uma ferramenta de gerenciamento de postura de segurança e proteção contra ameaças para cargas de trabalho em nuvem e locais. Ele oferece:

- **Avaliação contínua de segurança**: Monitora continuamente a segurança de suas cargas de trabalho e fornece recomendações para melhorar a postura de segurança.
- **Proteção contra ameaças**: Detecta ameaças em tempo real e fornece alertas e insights para ajudar a mitigar riscos com o Azure Security Benchmark.
- **Gerenciamento de conformidade**: Ajuda a garantir que suas cargas de trabalho estejam em conformidade com padrões de segurança e regulamentações.

![alt text](https://github.com/clouder-km/Challenge-Azure-Dio/blob/main/image/Defender.PNG)


### Conclusão

O Microsoft Entra ID e as soluções de segurança associadas, como o Multi-factor Authentication (MFA), Conditional Access, Role-Based Access Control (RBAC) e Microsoft Defender for Cloud, fornecem uma abordagem robusta e integrada para gerenciar identidades e proteger acessos em ambientes de nuvem e locais. Essas ferramentas ajudam a garantir que apenas usuários autorizados possam acessar recursos críticos, protegendo assim a integridade e a segurança dos dados da organização.

## Referência

- [Documentação Microsoft Entra ID](https://learn.microsoft.com/en-us/entra/identity/)
- [Documentação Security Azure](https://learn.microsoft.com/en-us/azure/security/)
