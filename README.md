# Integração de Dados do Azure DevOps Test Plan com Power BI

ℹ️ Este guia irá te ajudar a integrar os dados do Azure DevOps Test Plan com o Power BI utilizando consultas OData. 

## Passos

### 1. Crie um Personal Access Token (PAT)

1. Acesse o Azure DevOps e vá para as configurações do seu perfil.
2. Em "Segurança", clique em "Personal access tokens" e crie um novo token com permissões de leitura para os dados do Test Plan.

### 2. Obtenha a URL do Azure DevOps

1. Acesse o Azure DevOps e vá para a seção do Test Plan.
2. Na barra lateral, clique em "Test Plans" e depois em "Queries".
3. Selecione a query desejada e clique em "Editar Query". Copie a URL do navegador.

### 3. Abra o Power BI Desktop

Abra o Power BI Desktop e crie um novo projeto ou abra um existente.

### 4. Importe os Dados

1. Na barra de navegação, clique em "Página Inicial" e selecione "Obter Dados".
2. Escolha "OData Feed" e cole a URL que você copiou anteriormente.
3. Siga as instruções para autenticação, selecione "Autenticação Básica" e insira o Personal Access Token (PAT) que você criou.

### 5. Configure as Opções de Importação

1. Na janela de configuração do OData Feed, escolha as entidades e dados que deseja importar.
2. Clique em "OK" para iniciar a importação.

### 6. Transforme e Limpe os Dados

Após a importação, você pode precisar realizar algumas transformações e limpezas nos dados para melhorar a qualidade da visualização.

### 7. Modele os Dados

Crie relacionamentos entre as tabelas, se necessário, para garantir a precisão dos dados.

### 8. Crie Visualizações

Agora, você pode começar a criar suas visualizações e relatórios com base nos dados importados.


🎉 Agora você integrou com sucesso os dados do Azure DevOps Test Plan com o Power BI! Personalize seus relatórios e análises conforme necessário.
