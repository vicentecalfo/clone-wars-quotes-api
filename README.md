# Star Wars: The Clone Wars Episode Opening Quotes API
API gratuita para as citações de abertura dos episódios de [Star Wars: A Guerra dos Clones](https://g.co/kgs/7266TV)

## Documentação

A URL base para todos os endpoints: ```https://clone-wars-quotes.herokuapp.com```

## Endpoints

Foram lançadas 7 temporadas, portanto nos *endpoints* que precisam do parâmetro temporada, você deve passar um número de 1 a 7.


```/quotes``` Retorna todas as citações das 7 temporadas.

**Exemplo da resposta:**
```javascript
{

    "1": [
        {
            "season": 1,
            "episodeNumber": 1,
            "episodeName": "Ambush",
            "quote": "Great leaders inspire greatness in others."
        },
        {
            "season": 1,
            "episodeNumber": 2,
            "episodeName": "Rising Malevolence",
            "quote": "Belief is not a matter of choice, but of conviction."
        },
        {
            "season": 1,
            "episodeNumber": 3,
            "episodeName": "Shadow of Malevolence",
            "quote": "Easy is the path to wisdom for those not blinded by ego."
        },
        // ... outros episódios
        ]
        // ...outras temporadas
  }
```


```/randomQuote``` Retorna uma citação aleatória do conjunto das 7 temporadas.

**Exemplo da resposta:**
```javascript
{
    "season": 3,
    "episodeNumber": 14,
    "episodeName": "Witches of the Mist",
    "quote": "The path to evil may bring great power, but not loyalty."
}
```


```/randomQuotesBySeason/{season}``` Retorna uma citação aleatória de uma temporada específica.

**Exemplo**: ```https://clone-wars-quotes.herokuapp.com/randomQuotesBySeason/2``` : Esta requisição traria uma citação aleatória da temporada 2.

```javascript
{
    "season": 2,
    "episodeNumber": 4,
    "episodeName": "Senate Spy",
    "quote": "A true heart should never be doubted."
}
```

```/quote/{season}/{episode}``` Retorna um citação específica de uma temporada específica.

**Exemplo**: ```https://clone-wars-quotes.herokuapp.com/quote/7/8``` : Esta requisição traria a citação do episódio 8 da temporada 7.

```javascript
{
    "season": 7,
    "episodeNumber": 8,
    "episodeName": "Together Again",
    "quote": "You can change who you are, but you cannot run from yourself."
}
```

**Atenção**: Para retornar todas as citações de uma temporada passe 0 (zero) no parâmetro *episode*.

**Exemplo**: ```https://clone-wars-quotes.herokuapp.com/quote/5/0``` : Esta requisição traria todas as citações da temporada 5.

```javascript
[
    {
        "season": 5,
        "episodeNumber": 1,
        "episodeName": "Revival",
        "quote": "Strength of character can defeat strength in numbers."
    },
    {
        "season": 5,
        "episodeNumber": 2,
        "episodeName": "A War on Two Fronts",
        "quote": "Fear is a malleable weapon."
    },
    {
        "season": 5,
        "episodeNumber": 3,
        "episodeName": "Front Runners",
        "quote": "To seek something is to believe in its possibility."
    },
    {
        "season": 5,
        "episodeNumber": 4,
        "episodeName": "The Soft War",
        "quote": "Struggles often begin and end with the truth."
    },
    // ... restante dos episódio da temporada 5
]
```


**Total de episódios por temporada:**

* Temporada 1: 22 episódios;
* Temporada 2: 22 episódios;
* Temporada 3: 22 episódios;
* Temporada 4: 22 episódios;
* Temporada 5: 20 episódios;
* Temporada 6: 13 episódios;
* temporada 7: 12 episódios, no entanto os 4 últimos episódios não possuem citação de abertura, sendo assim somente 8 episódios estão presentes na API para esta temporada.


