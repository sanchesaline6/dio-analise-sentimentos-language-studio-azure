## Análise de Sentimentos com Language Studio no Azure AI

Este projeto demonstra como utilizar o Language Studio para analisar textos.

### Processo

1. Criar um recurso Language
2. Conectar o serviço Azure AI ao Language Studio
3. Analise avaliações no Language Studio 
4. Limpeza

### Criar um recurso Language

1. Em um browser, abra o [Portal Azure](https://portal.azure.com/?azure-portal=true), logando com uma conta associada com uma subscrição do Azure.
2. Clique no botão **+ Create a resource** e pesquise por *Language service*. Selecione  o plano **create a Language service**. Você será levado para uma página para **Select additional features**. Mantenha os padrões selecionados e clique em **Continue to create your resource**.
3. Na página **Create Language**, configure-o com as seguintes configurações:
- **Subscription**: *Sua subscrição Azure*.
- **Resource group**: *Selecione ou crie um grupo de recurso com um nome único*.
- **Region**: East US
- **Name**: *Informe um nome único*.
- **Pricing tier**: *Free F0 or S if Free F0 is not available*.
- **By checking this box I acknowledge that I have read and understood all the terms below**: *Selected.*
4. Selecione **Review + create** então **Create** e aguarde o deploy ser realizado.

## Conectar o serviço Azure AI ao Language Studio

1. Em outra aba do navegador, abra o **Language Studio** no link [https://language.cognitive.azure.com/?azure-portal=true](https://language.cognitive.azure.com/?azure-portal=true) e realize o login.
2. Quando solicitado **Selecione um recurso Azure**, realize as seguintes configurações:
- **Azure Directory**: *Default directory, the directory you are using*.
- **Azure subscription**:*Select the subscription you are using*.
- **Resource type**: *Language*
- **Resource name**: *select the Language service resource you just created*.
3. Então selecione **Done**.

### Analise avaliações no Language Studio

1. Em um navegador, navegue para o [Language Studio](https://language.cognitive.azure.com/?azure-portal=true)
2. Na página inicial **Welcome to Language Studio**, selecione a aba **Classify text**, e então selecione o quadro **Analyze sentiment and mine opinions**.
3. Em *Select text language*, selecione **English**
4. Em *Select your Azure resource*, selecione seu recurso.
5. Em *Enter your own text, upload a file, or use one of our sample texts*, clique em *Browse for a file* e selecione o arquivo ![sentencas.txt](/inputs/sentencas.txt) presente na pasta inputs desse repositório.
6. Marque a caixa para confirmar que a demonstração incorrerá em uso e poderá incorrer em custos e selecione **Run**.
7. Revise a saída. Perceba que o *documento* foi analisado por sentimento, assim como cada *frase*. 

![sentiment-analyze-result.png](/outputs/sentiment-analyse-result.png)

Observe que há um sentimento geral seguido por pontuações próximas a três categorias: pontuação positiva, pontuação neutra, pontuação negativa. Em cada uma das categorias é atribuída uma pontuação entre 0 e 1. Essas pontuações de confiança indicam a probabilidade do texto fornecido ser um sentimento específico.

### Limpeza

1. Abra o [Portal Azure](https://portal.azure.com/) e selecione o grupo de recursos que contém o recurso que você criou.
2. Selecione o recurso e clique em **Deletar** e então **Sim** para confirmar. O recurso foi deletado.