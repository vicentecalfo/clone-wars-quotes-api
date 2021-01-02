# Star Wars: The Clone Wars Episode Opening Quotes API
API gratuita para as citações de abertura dos episódios de [Star Wars: A Guerra dos Clones](https://g.co/kgs/7266TV)

## Documentação

A URL base para todos os endpoints: ```https://clone-wars-quotes.herokuapp.com```

## Endpoints

Foram lançadas 7 temporadas, portanto nos *endpoints* que precisam do paramêtro temporada, você deve passar um número de 1 a 7.


```/quotes``` Retorna todas as citações das 7 temporadas.

```/randomQuote``` Retorna uma citação aleatória do conjunto das 7 temporadas.

```/randomQuotesBySeason/{season}``` Retorna uma citação aleatória de uma temporada específica.

**Exemplo**: ```https://clone-wars-quotes.herokuapp.com/randomQuotesBySeason/2``` : Esta requisição traria uma citação aleatória da temporada 2.

```/quote/{season}/{episode}``` Retorna um citação específica de uma temporada específica.

**Exemplo**: ```https://clone-wars-quotes.herokuapp.com/quote/7/8``` : Esta requisição traria a citação do episódio 8 da temporada 7.

**Atenção**: Para retornar todas as citações de uma temporada passe 0 (zero) no parâmetro *episode*.

**Total de episódios por temporada:*

* Temporada 1: 22 episódios;
* Temporada 2: 22 episódios;
* Temporada 3: 22 episódios;
* Temporada 4: 22 episódios;
* Temporada 5: 20 episódios;
* Temporada 6: 13 episódios;
* temporada 7: 12 episódios, no entanto os 4 últimos episódios não possuem citação de abertura, sendo assim somente 8 episódios estão presentes na API para esta temporada.


