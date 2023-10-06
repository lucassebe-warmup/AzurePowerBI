# Integração de Dados do Azure DevOps Test Plan com Power BI

ℹ️ Este guia irá te ajudar a integrar os dados do Azure DevOps Test Plan com o Power BI utilizando consultas OData. 
Ele está dividído entre duas sessões: Benefícios e Passos.
 
## Benefícios
A união do Azure com o Power BI é uma grande vantagem para melhorar a qualidade. Isso traz
benefícios importantes:

### Dados Mais Fáceis de Entender:
Todos na equipe podem ver os resultados dos testes em um só lugar, o que torna a informação mais
clara.

### Monitoramento Personalizado:
Podemos ajustar os gráficos e informações para ver os resultados dos testes como quisermos, o que
ajuda na análise.

### Histórico e Comparação:
Mantemos um registro de como os testes evoluem ao longo do tempo, o que ajuda a comparar ciclos
de testes diferentes.

### Decisões Baseadas em Dados:
Com informações claras no Power BI, podemos decidir quando lançar novas versões, priorizar
correções e usar recursos de teste de forma eficaz.

### Avaliação da Qualidade:
Podemos ver se a qualidade está melhorando ou piorando após os testes.

Em resumo, a integração do Power BI com o Azure torna mais fácil entender a qualidade, tomar
decisões informadas e melhorar constantemente nossos processos de teste.

## Passos

### 1. Crie um Personal Access Token (PAT)

1. Acesse o Azure DevOps e vá para as configurações do seu perfil.
2. Em "Segurança", clique em "Personal access tokens" e crie um novo token com permissões de leitura para os dados do Test Plan.
   
![image](https://github.com/lucassebe-warmup/AzurePowerBI/blob/main/assets/Captura%20de%20tela%202023-10-06%20131640.png)


### 2. Obtenha a URL do Azure DevOps

1. Acesse o Azure DevOps e vá para a Pipeline que deseja coletar os dados.
2. Entre dentro da última Run na sessão de "Testes".

![image](https://github.com/lucassebe-warmup/AzurePowerBI/blob/main/assets/Captura%20de%20tela%202023-10-06%20132936.png)

3. Aperte F12. Em "Network" filtre por "odata" e copie a URL da requisição que aparecer.
A URL que você irá utilizar deve ser semelhante à: https://analytics.dev.azure.com/{organização}/{id}/_odata/v4.0-preview/TestResultsDaily?[...]

**Caso as requisições não apareçam atualize a página.

![image](https://github.com/lucassebe-warmup/AzurePowerBI/blob/main/assets/Captura%20de%20tela%202023-10-06%20133108.png)


### 3. Abra o Power BI Desktop

Abra o Power BI Desktop e crie um novo projeto ou abra um existente.

### 4. Importe os Dados

1. Na barra de navegação, clique em "Página Inicial" e selecione "Obter Dados".
2. Escolha "OData Feed" e cole a URL que você copiou anteriormente, porém você irá colar até a palavra preview:
https://analytics.dev.azure.com/{organização}/{id}/_odata/v4.0-preview/

![image](https://github.com/lucassebe-warmup/AzurePowerBI/blob/main/assets/Captura%20de%20tela%202023-10-06%20133643.png)

4. Siga as instruções para autenticação, selecione "Autenticação Básica" e insira o seu email e o Personal Access Token (PAT) que você criou.

### 5. Configure as Opções de Importação

1. Na janela de configuração do OData Feed, escolha as entidades e dados que deseja importar.

![image](https://github.com/lucassebe-warmup/AzurePowerBI/blob/main/assets/Captura%20de%20tela%202023-10-06%20133919.png)

2. Clique em "OK" para iniciar a importação.

### 6. Transforme e Limpe os Dados

Após a importação, você pode precisar realizar algumas transformações e limpezas nos dados para melhorar a qualidade da visualização.

![image](https://github.com/lucassebe-warmup/AzurePowerBI/blob/main/assets/Captura%20de%20tela%202023-10-06%20134050.png)


### 7. Modele os Dados

Crie relacionamentos entre as tabelas, se necessário, para garantir a precisão dos dados.

### 8. Crie Visualizações

Agora, você pode começar a criar suas visualizações e relatórios com base nos dados importados.

![image](https://github.com/lucassebe-warmup/AzurePowerBI/blob/main/assets/Captura%20de%20tela%202023-10-06%20134112.png)


🎉 Agora você integrou com sucesso os dados do Azure DevOps Test Plan com o Power BI! Personalize seus relatórios e análises conforme necessário.
