# ScreenMatch

## MODEL

1. DadosEpisodios.java - Record que armazena dados vindo do JSON providenciado pela API da IMDB que armazena o titulo, numero do episódio, avaliação, e data de lançamento de episódios.
 

1. DadosSeries.java - Record que armazena dados vindo do JSON providenciado pela API da IMDB que armazena o titulo, total de temporadas e avaliação de séries.
   

1. DadosTemporadas.java - Record que armazena dados vindo do JSON providenciado pela API da IMDB que o número da temporada e uma lista de episodios.
   
   
1. Episodios.java - Classe com construtor e atributos detalhando mais cada episódio.
   

## REPOSITORY

  1. IConverteDados.java - Interface usando um método genérico, podendo retornar qualquer entidade.

## SERVICE

  1. ConsumoAPI.java - Classe que obtém dados atráves de um HTTP Request e retorna uma "resposta" como JSON.

  1. ConverteDados.java - Classe que implementa "ConsumoAPI.java" e usa a biblioteca do Jackson para fazer a conversão do JSON retornado.

  1. BuscaSerie.java - Classe que retorna uma série dependendo da escolha do usuário, obtendo um JSON do endereço e da KEYAPI da IMBD fornecido.

  1. RetornaEpisodios.java - Classe que retorna episódios de uma série escolhida pelo usuário, usando mapeamento para os dados.

  1. TemporadaTopEpisodios.java - Classe que mostra os episódios top 10 da temporada da série escolhida pelo usuário, usando um filtro fornecido pela stream, onde buscamos somente pela avaliação do episódio, comparando-o com os restantes.

 1. AvaliacoesSeries.java - Classe que usa mapeamento e stream para filtrar as avaliações de cada temporada, obtendo a média de avaliação da série por temporada. Também faz o uso da classe DoubleSummaryStatistics do Java 8, usado para fins de obter estatísticas precisas, usado no projeto para se obter a quantidade de episódios, média dos episódios, assim também como o melhor e pior episódio.
