# Desafio de programação 1
A idéia deste desafio é nos permitir avaliar melhor as habilidades de candidatos, de vários níveis, à vagas de programador.

Este desafio deve ser feito por você em sua casa. Gaste o tempo que você quiser, porém normalmente você não deve precisar de mais do que algumas horas.

## Instruções de entrega do desafio
1. Primeiro, faça um fork deste projeto para sua conta no Github (crie uma se você não possuir).
1. Em seguida, implemente o projeto tal qual descrito abaixo, em seu próprio fork.
1. Por fim, empurre todas as suas alterações para o seu fork no Github e envie um pull request para este repositório original. Se você já entrou em contato com alguém da Luizalabs sobre uma vaga, avise também essa pessoa, informando o seu usuário no Github.

## Instruções alternativas de entrega do desafio (caso você não queira que sua submissão seja pública)
1. Faça um clone deste repositório.
1. Em seguida, implemente o projeto tal qual descrito abaixo, em seu clone local.
1. Por fim, envie via email um arquivo patch para seu contato na Luizalabs.

## Descrição do projeto
Você recebeu um arquivo de texto com os dados de vendas da empresa. Precisamos criar uma maneira para que estes dados sejam importados para um banco de dados.

Sua tarefa é criar uma interface Web que permita você fazer upload desse arquivo e acompanhar o status de importacao. Ao final, deve ser possível exportar a planilha normalizada do banco de dados. O processo de importacao deve ser assícrono, deve normalizar, gravar em uma base de dados relacional e deve mostrar em tela, em caso de erro, a linha e a mensagem de erro em que ocorreram.

Sua aplicação web DEVE:

1. Aceitar (via um formulário) o upload de arquivos separados por TAB com as seguintes colunas: purchaser name, item description, item price, purchase count, merchant address, merchant name. Você pode assumir que as colunas estarão sempre nesta ordem, que sempre haverá dados em cada coluna, e que sempre haverá uma linha de cabeçalho. Um arquivo de exemplo chamado example_input.tab está incluído neste repositório.
1. Ao aceitar o arquivo deve fazer uma inspeção para verificar se o arquivo não esta vazio ou não está com a coluna ou ordem incorretas.
1. De modo assícrono, interpretar ("parsear") o arquivo recebido, normalizar os dados, e salvar corretamente a informação em um banco de dados relacional.
1. Após a conclusão do processo, exibir a receita bruta total representada pelo arquivo enviado após o upload + parser.
1. Ser escrita obrigatoriamente em Java com Spring Boot (ou outra linguagem especificada para a vaga se for o caso).
1. Pode usar sistemas de mensageria (Kafka, RabbitMQ...) caso faça sentido.
1. Pode usar arquitetura hexagonal caso faça sentido
1. Obrigatoriamente, usar docker-compose para executar o projeto (tanto API como o banco de dados relacional ou qualquer outro artefato que venha compor o projeto).

Sua aplicação web não precisa:

1. Lidar com autenticação ou autorização (pontos extras se ela fizer, mais pontos extras se a autenticação for feita via OAuth).
1. Ter uma aparência bonita.

## Avaliação
Seu projeto será avaliado de acordo com os seguintes critérios. 

1. Sua aplicação preenche os requerimentos básicos?
1. Você documentou a maneira de configurar o ambiente e rodar sua aplicação?
1. Você seguiu as instruções de envio do desafio?

Adicionalmente, tentaremos verificar a sua familiarização com as bibliotecas padrões (standard libs), bem como sua experiência com programação orientada a objetos a partir da estrutura de seu projeto.

### Referência

Este desafio foi baseado neste outro desafio: https://github.com/lschallenges/data-engineering
