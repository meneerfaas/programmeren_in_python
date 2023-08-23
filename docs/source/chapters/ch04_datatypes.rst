.. role:: python(code)
    :language: python

Datatypes
=========

In het vorige hoofdstuk leerde je dat met de concatenatie operator :python:`+` twee strings aan elkaar kunt plakken. Je kunt de :python:`+` dus gebruiken om twee getallen op te tellen of om twee strings samen te voegen. Maar wat gebeurt er als je de :python:`+` toepast op een getal én een string?

.. prompt:: python >>> auto
    
    >>> 10 + 'kilo'
    Traceback (most recent call last):
    File "<stdin>", line 1, in <module>
    TypeError: unsupported operand type(s) for +: 'int' and 'str'
    
.. prompt:: python >>> auto

    >>> 'nummer' + 3
    Traceback (most recent call last):
    File "<stdin>", line 1, in <module>
    TypeError: can only concatenate str (not "int") to str

Beide voorbeelden veroorzaken een TypeError waarmee Python aangeeft dat het niet mogelijk is een string bij een getal op te tellen of een getal aan een string te concateneren.

De informatie waarmee een computerprogramma werkt, noemen we data. Die data kan vele verschijningsvormen hebben. We hebben al kennisgemaakt met getallen en tekst, maar er zijn nog veel meer mogelijkheden. Voor Python is het van belang te weten met wat voor soort data het te maken heeft, bijvoorbeeld om te kunnen beoordelen of twee gegevens opgeteld kunnen worden of niet. Het soort data noemen we het *datatype*.

Vooralsnog beschouwen de de volgende drie datatypes:

.. list-table:: Eenvoudige datatypes
    :header-rows: 1
    :align: center

    * - Datatype
      - Naam
      - Waarde
    * - int
      - integer
      - geheel getal
    * - float
      - floating point number
      - getal met decimalen
    * - str
      - string
      - tekst

.. TODO: add concatenate to glossary

Bekijk de assignment statements hieronder. Kun je nu zeggen wat de datatypes zijn van de variabelen :python:`spam`, :python:`eggs` en :python:`ham`?

.. prompt:: python >>> auto

    >>> spam = 8.0
    >>> eggs = '8'
    >>> ham = 8

De aanhalingstekens vertellen je dat :python:`eggs` een string variabele is. Ook al staat er een getal tussen die aanhalingstekens, Python behandelt de waarde als tekst. De variabelen :python:`spam` en :python:`ham` daarentegen bevatten getallen. Van die twee is :python:`spam` een float en :python:`ham` een integer variabele, omdat :python:`spam` een kommagetal bevat en :python:`ham` een geheel getal zonder komma.

De functie type()
-----------------

Je bent nu in staat om de datatypes :python:`int`, :python:`float` en :python:`str` te onderscheiden, en gelukkig kan Python dat zelf ook. Om dat in actie te zien, gebruik je de :python:`type()` functie:

.. prompt:: python >>> auto

    >>> spam = 8.0
    >>> eggs = '8'
    >>> ham = 8
    >>> type(spam)
    <class 'float'>
    >>> type(eggs)
    <class 'str'>
    >>> type(ham)
    <class 'int'>

In plaats van een variabele kun je aan :python:`type()` ook direct een waarde meegeven:

.. prompt:: python >>> auto
    
    >>> type(100)
    <class 'int'>
    >>> type('hallo')
    <class 'str'>

Type casting
------------

Helaas is de data waarmee een computerprogramma moet werken niet altijd meteen van het juiste type. Soms ontvangt je code (van de gebruiker of vanuit andere code) een stringwaarde terwijl je een integer nodig hebt. Of er komt een float binnen, terwijl je juist een string had willen hebben. In dat geval is het handig als je de waarde kunt converteren naar een ander datatype. Dat noemen we *type casting*. 

Voor de datatypes :python:`int`, :python:`float` en :python:`str` heeft Python de type casting functies :python:`int()`, :python:`float()` en :python:`str()`.

.. prompt:: python >>> auto
    
    >>> spam = 8.0          # spam bevat een float
    >>> ham = int(spam)     # int(spam) converteert de float naar een int
    >>> ham
    8
    >>> eggs = str(ham)     # str(ham) converteert de int naar een str
    >>> eggs
    '8'

Zou je met deze kennis de derde regel van onderstaande code kunnen aanpassen zodat het resultaat niet :python:`'25'` is, maar :python:`'7'`?

.. prompt:: python >>> auto
    
    >>> a = '2'
    >>> b = '5'
    >>> a + b
    '25'

De oplossing:

.. prompt:: python >>> auto
    
    >>> a = '2'
    >>> b = '5'
    >>> str(int(a) + int(b))
    '7'

De variabelen :python:`a` en :python:`b` bevatten getallen vermomd als strings. Om de getallen te kunnen optellen, converteer je ze met de functie :python:`int()` naar integers. Met de functie :python:`str()` vermom je het antwoord weer terug naar een string.

Met de functieaanroep :python:`int('2')` kun je dus de string :python:`'2'` converteren naar de integer :python:`2`. Maar wat zou er gebeuren als je tussen de haakjes een stringwaarde zet die geen getal bevat, zoals bijvoorbeeld :python:`int('a')`? Probeer het eens uit!