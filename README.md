O ScreenMatch é um projeto backend feito com Java e Spring Boot que consome dados de séries através da API do OMDb.

A ideia aqui foi praticar bastante consumo de API, manipulação de dados e uso de Streams no Java, simulando um sistema simples de busca e análise de séries pelo terminal.

Quando você roda o projeto, ele te permite buscar uma série e ver informações como temporadas, episódios, avaliações e ainda fazer algumas análises em cima desses dados.

⚙️ Como funciona

Quando a aplicação inicia:

o Spring Boot sobe normalmente
a execução vai direto pra classe Principal
tudo roda no console (sem API REST)

Você digita o nome da série e o sistema começa a buscar tudo pela API do OMDb.

🚀 O que dá pra fazer no sistema
Buscar séries pelo nome
Ver temporadas e episódios
Listar todos os episódios da série
Filtrar episódios por parte do nome
Filtrar episódios por ano de lançamento
Ver os episódios melhor avaliados
Ver média de avaliação por temporada
Ter uma visão geral de estatísticas da série

🧠 Tecnologias usadas
Java
Spring Boot
Streams API
Collections (List, Map)
Optional
Jackson (pra trabalhar com JSON)
API do OMDb
LocalDate

🔄 Como os dados entram no sistema

Os dados vêm direto da API do OMDb e são organizados assim:

DadosSerie → informações gerais da série
DadosTemporada → temporadas com lista de episódios
DadosEpisodio → dados crus de cada episódio

Depois disso tudo é convertido para o modelo Episodio, onde os dados são tratados e usados de verdade no sistema.

🧩 Estrutura do projeto
screenmatch
 ┣ ScreenmatchApplication.java
 ┣ principal
 ┃ ┗ Principal.java
 ┣ model
 ┃ ┣ Episodio.java
 ┃ ┣ DadosSerie.java
 ┃ ┣ DadosTemporada.java
 ┃ ┗ DadosEpisodio.java
 ┣ services
 ┃ ┣ ConsumoAPI.java
 ┃ ┗ ConverteDados.java
 

📊 O que esse projeto me ajudou a treinar

Esse projeto foi bem importante pra treinar:

consumo de API na prática
manipulação de JSON
uso de Streams de verdade (filter, map, flatMap, collect)
organização de código em camadas
tratamento de dados reais (não só exemplo de aula)

🚀 Ideias de evolução
transformar isso em uma API REST
salvar dados em banco de dados
colocar Docker
criar uma interface web
adicionar autenticação
