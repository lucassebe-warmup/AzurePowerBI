# Integração de Dados do Azure DevOps Test Plan com Power BI

ℹ️ Este guia irá te ajudar a integrar os dados do Azure DevOps Test Plan com o Power BI utilizando consultas OData. 

## Passos

### 1. Crie um Personal Access Token (PAT)

1. Acesse o Azure DevOps e vá para as configurações do seu perfil.
2. Em "Segurança", clique em "Personal access tokens" e crie um novo token com permissões de leitura para os dados do Test Plan.
   
![image](https://github.com/lucassebe-warmup/AzurePowerBI/assets/137821053/56e437b1-bea0-415e-8889-c291361db6e2)


### 2. Obtenha a URL do Azure DevOps

1. Acesse o Azure DevOps e vá para a Pipeline que deseja coletar os dados.
2. Entre dentro da última Run na sessão de "Testes".

![image](https://github.com/lucassebe-warmup/AzurePowerBI/assets/137821053/6d52483e-180f-4da8-9fd9-7bc647627fef)

3. Aperte F12. Em "Network" filtre por "odata" e copie a URL da requisição que aparecer.
A URL que você irá utilizar deve ser semelhante à: https://analytics.dev.azure.com/{organização}/{id}/_odata/v4.0-preview/TestResultsDaily? **[...]**
**Caso as requisições não apareçam atualize a página.

![image](https://github.com/lucassebe-warmup/AzurePowerBI/assets/137821053/6f542b0e-30b0-4fda-ac05-333cc9c8a705)


### 3. Abra o Power BI Desktop

Abra o Power BI Desktop e crie um novo projeto ou abra um existente.

### 4. Importe os Dados

1. Na barra de navegação, clique em "Página Inicial" e selecione "Obter Dados".
2. Escolha "OData Feed" e cole a URL que você copiou anteriormente, porém você irá colar até a palavra preview:
https://analytics.dev.azure.com/{organização}/{id}/_odata/v4.0-preview/

![image](https://github.com/lucassebe-warmup/AzurePowerBI/assets/137821053/e8dc70ce-f645-421f-8dcb-0e67d638abd1)

4. Siga as instruções para autenticação, selecione "Autenticação Básica" e insira o seu email e o Personal Access Token (PAT) que você criou.

### 5. Configure as Opções de Importação

1. Na janela de configuração do OData Feed, escolha as entidades e dados que deseja importar.

![image](https://github.com/lucassebe-warmup/AzurePowerBI/assets/137821053/0b2d1f42-a3fe-421d-bcc4-8cca7e19f9d1)

2. Clique em "OK" para iniciar a importação.

### 6. Transforme e Limpe os Dados

Após a importação, você pode precisar realizar algumas transformações e limpezas nos dados para melhorar a qualidade da visualização.

![image](https://github.com/lucassebe-warmup/AzurePowerBI/assets/137821053/9539de3b-d345-496f-b07e-f3e10ac400e5)


### 7. Modele os Dados

Crie relacionamentos entre as tabelas, se necessário, para garantir a precisão dos dados.

### 8. Crie Visualizações

Agora, você pode começar a criar suas visualizações e relatórios com base nos dados importados.

![image](https://github.com/lucassebe-warmup/AzurePowerBI/assets/137821053/9ce10fcb-b1fc-446f-9aa2-52e697ad6718)


🎉 Agora você integrou com sucesso os dados do Azure DevOps Test Plan com o Power BI! Personalize seus relatórios e análises conforme necessário.
