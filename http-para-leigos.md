# HTTP para leigos
Iremos focar em conceitos mais high level, deixando a parte técnica e mais detalhada para outros artigos.

## Conceitos
### Hypertext Transfer Protocol
Hypertext Transfer Protocol ~~Paulistas diriam pra chamar só de HTTP~~ é um protocolo utilizado para transmitir dados na internet. 
> [!NOTE]
> Meio vago, certo? Alguém pode se perguntar: É esse HTTP que faz a transferência dos meus dados de um lugar para outro?
### Protocol
Protocolo é um conjunto de informações, decisões, normas e regras. 
> [!IMPORTANT]
> Agora que sabemos o que é HTTP e o que protocol significa, conseguimos deduzir que HTTP é um conjunto de informações, decisões, normas e regras que ajudam sistemas a transferir dados entre si. Logo podemos dizer que o HTTP em si não faz nenhuma transferência, ele só te informa como proceder.
## Como funciona
Dentre todos os passos realizados para que a transferência seja propriamente feita, conseguimos dividi-los em cinco diferentes etapas. São elas:
1. Resoluçao de DNS
2. Estabelecimento de conexão TCP
3. SSL/TLS Handshake [opcional]
4. Processamento dos dados
5. Finalização de conexão TCP

São nomes/abreviações, bem específicas e difíceis de entender, correto? Vamos tentar simplificá-las!

### Resolução de DNS
Imagina que estamos tentando acessar o site www.nubank.com.br e para isso usamos um Navegador. Para que o navegador consiga exibir o site do Nubank, primeiro ele precisa perguntar para o Nubank qual o conteúdo que será exibido (uma transferência de dados precisa ocorrer).

Agora imagine que o Navegador não é capaz de saber exatamente qual o computador do mundo que detém os dados do Nubank, pois essa informação pode ser completamente dinâmica (computadores mudam, novos sites aparecem).

Para solucionar esse problema foi criado um "catálogo global de sites", onde é possível digitar o nome e receber um endereço. Aqui pode ser feito um paralelo com uma lista de contatos universal, onde você busca o nome da pessoa e encontra o número do telefone celular ou endereço.

### Estabelecimento de conexão TCP
Agora que a gente tem o endereço, podemos nos comunicar com o Nubank. Seguindo ainda a ideia do paralelo com a lista de contatos, agora que você tem o número você pode e vai ligar para a pessoa.
### SSL/TLS Handshake
A tradução literal de handshake é aperto de mão. Mas o que seria isso no mundo virtual? Aqui a gente precisa abstrair um pouco o conceito literal e ser um pouco mais filosofico:

Você assumiria o risco de "apertar a mão" e assumir uma conversa livre sobre sua vida com uma pessoa desconhecida, onde essas conversas poderiam ter dados sensíveis como a sua senha do banco? 

Se sim, então provavelmente você não se da ao trabalho de perguntar "quem fala?" quando atende um telefonema e esse passo é completamente desnecessário pra você.

Nesse momento do telefonema, aqui seria o lugar onde as pessoas se apresentam e tentam provar que são elas mesmas. Trocam número de documentos, nome completo, certidão de nascimento, etc.
### Processamento de dados
Aqui seria o lugar onde o Nubank vai recuperar suas informações e montar a resposta que será lida pelo Navegador. Uma vez que a resposta esteja montada, o Nubank vai transferir essas informações para o Navegador.

Agora que ambos sabem que a conexão/ligação é segura, eles podem falar livremente.
### Finalização de conexão
Agora que os dados foram transferidos, a conexão não precisa permanecer aberta. Então assim que o Nubank responde, a ligação é encerrada. Pois o cliente não deseja gastar seus créditos sem que seja necessário.

Alguns vão argumentar que as vezes é melhor deixar a ligação aberta, mas isso é uma conversa para outro momento!!
