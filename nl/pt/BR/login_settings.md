---

copyright:
  years: 2018, 2019
lastupdated: "2019-06-19"

keywords: account security, login security, TOTP, MFA, password expiration

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:tip: .tip}
{:note: .note}


# Configurando a segurança de login
{: #login-settings}

Com o acesso autorizado, é possível configurar a segurança extra para seu login do {{site.data.keyword.cloud}}. É possível configurar perguntas e respostas, selecionar uma expiração de senha, configurar uma senha descartável baseada em tempo (TOTP), a autenticação de diversos fatores (MFA) e configurar opções de autenticação externa.  
{:shortdesc}

Um proprietário da conta pode requerer a MFA do IBMid em uma conta da qual você é um membro. A MFA do IBMid substitui qualquer outra configuração de MFA. Por exemplo, quando a MFA do IBMid está configurada, você recebe uma solicitação para fornecer uma MFA do TOTP associada a seu IBMid em vez de perguntas de segurança ou um dos métodos de autenticação externa.
{: note}

Será possível visualizar as opções de segurança a seguir e ativar ou desativá-las somente se seu administrador conceder acesso a você. Acesse **Ícone do {{site.data.keyword.avatar}}**![Ícone do Avatar](../icons/i-avatar-icon.svg) > **Perfil e configurações** e selecione **Configurações de login**.

## Configurando perguntas de segurança
{: #security-questions}

Para configurar suas perguntas de segurança:
1. No console, acesse **Ícone do {{site.data.keyword.avatar}}**![Ícone do Avatar](../icons/i-avatar-icon.svg) > **Perfil e configurações** e selecione **Configurações de login**.
2. Clique em **Editar**.
3. Selecione as perguntas que você deseja ter e respondê-las. Deve-se usar três opções de pergunta de segurança.
4. Clique em **Salvar** quando tiver concluído.  
5. Certificar-se de que a caixa `Yes` esteja marcada para que as perguntas de segurança sejam ativadas. Marcar a caixa `Yes` pode solicitar que você se conecte à sua conta novamente.  

É possível configurar respostas para três perguntas de segurança para autenticação extra no login. Deve-se configurar suas perguntas e respostas de segurança antes que seu administrador possa ativar esse requisito da MFA para você.

Deve-se ser o proprietário da conta ou ter a configuração Login gerenciado pelo usuário ativada para você por seu administrador de conta para ativar e desativar perguntas de segurança.
{: note}

## Configurando uma expiração de senha
{: #password-expiration}

Para configurar o período de tempo que você gostaria de usar sua senha atual, selecione uma opção para que sua senha expire na seção **Expiração de senha**.

A expiração de senha é configurada para nunca por padrão. Quando você se inscreve para uma conta, nunca é necessário mudar sua senha. Ao configurar um período de expiração da senha, você é notificado sobre a expiração de senha por e-mail 14 dias antes, 7 dias antes e no dia em que a senha está configurada para expirar.

Essa opção está disponível somente para usuários que efetuam login com um ID do SoftLayer. Para atualizar sua expiração de senha, deve-se ser um proprietário da conta ou ter a configuração Login gerenciado pelo usuário ativada para você por seu administrador de conta na página de detalhes do Usuário do IAM.
{: note}

## Configurando a autenticação do TOTP
{: #MFA}

Para configurar sua autenticação do TOTP, clique em **Configurar**.

A MFA do TOTP inclui uma camada extra de segurança em sua conta, requerendo uma senha TOTP, além do ID padrão e da senha durante o login. Deve-se configurar a autenticação do TOTP antes que seu administrador de conta possa ativar esse requisito da MFA para você.

Também poderá ser solicitada a você uma senha única baseada em tempo se a configuração TOTP não estiver configurada e ativada. Isso é porque um proprietário da conta pode ativar a MFA do IBMid para uma conta para a qual você tenha acesso. Esse tipo de MFA se aplica a cada usuário na conta quando essa configuração está ativada e é necessário usá-la. Para obter mais informações, veja [Tipos de autenticação de diversos fatores](/docs/iam?topic=iam-types).


## Configurando a autenticação externa
{: #third-party-MFA}

Você ou seu administrador de conta pode pedir a autenticação da Symantec ou baseada em telefone para por um custo mensal. Para pedir a autenticação externa, é necessário ter as permissões de inclusão de infraestrutura de serviços. Para descobrir se a autenticação externa está ativada, acesse o ícone **{{site.data.keyword.avatar}}** ![Ícone do Avatar](../icons/i-avatar-icon.svg) > **Perfil e configurações** e selecione **Configurações de login**.

### Configurando a autenticação da Symantec

Se seu administrador de conta escolher pedir proteção de identidade Symantec, deve-se trabalhar com seu administrador para ajudá-lo a concluir a ordem, fornecendo seu ID de credencial:

1. Acesse [Symantec VIP](https://vip.symantec.com/).
2. Clique em **Download**.
3. Obtenha seu ID de credencial e forneça o ID para o seu administrador para concluir a ordem.

Depois que seu administrador pede e ativa a opção, é possível usar o app para autenticação de login.

### Configurando a autenticação baseada em telefone

É possível configurar e usar a proteção de identidade baseada em telefone depois que o administrador de conta pedir e ativar.

1. Acesse o ícone **{{site.data.keyword.avatar}}** ![Ícone Avatar](../icons/i-avatar-icon.svg) > **Perfil e configurações** e selecione **Configurações de login**.
2. Se a MFA baseada em telefone estiver desativada, clique em **Acessar detalhes do usuário**.
3. Na seção Gerenciar login do usuário, ative a autenticação baseada em telefone.
4. Para fornecer informações de contato para a autenticação, clique no ícone **Editar** ![Ícone Editar](../icons/edit-tagging.svg).
5. Preencha todos os campos. É possível especificar se deseja receber um telefonema ou uma mensagem de texto como o método de autenticação. Se desejar requerer um PIN, selecione a opção na lista **Tipo de PIN** e forneça o PIN que deseja usar.  
6. Clique em **Aplicar**.
