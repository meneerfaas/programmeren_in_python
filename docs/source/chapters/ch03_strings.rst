.. role:: python(code)
    :language: python

Strings
=======

Je weet nu hoe je in Python met getallen kunt rekenen en hoe je getallen opslaat in variabelen, maar computerprogramma's verwerken veel meer soorten informatie dan alleen getallen. In dit hoofdstuk leer je hoe je in Python code met tekst kunt werken. Programmeurs noemen een stuk tekst meestal een *string*. Letterlijk vertaald is dat een *sliert* van tekens, of ook wel een *tekenreeks*.

Aanhalingstekens
----------------

In Python maak je een string door aanhalingstekens (:python:`'`) om de tekst te zetten:

.. prompt:: python >>> auto
    
    >>> begroeting = 'Hartelijk welkom'
    >>> begroeting
    'Hartelijk welkom' 

Dubbele aanhalingstekens (:python:`"`) mogen ook:

.. prompt:: python >>> auto
    
    >>> begroeting = "Hartelijk welkom"
    >>> begroeting
    'Hartelijk welkom'

Je ziet dat Python de dubbele aanhalingstekens hier zelf vervangt door enkele. Maar let op, je mag de enkele en dubbele aanhalingstekens niet mixen:

.. prompt:: python >>> auto
    
    >>> begroeting = 'Hartelijk welkom"
    SyntaxError: incomplete input
    >>> begroeting = "Hartelijk welkom'
    SyntaxError: incomplete input

Wanneer je een string *begint* met een enkel aanhalingsteken, verwacht Python dat de string ook *eindigt* met een enkel aanhalingsteken, en hetzelfde geldt voor dubbele aanhalingstekens. Dit kun je gebruiken om *binnen*  een string aanhalingstekens toe te passen:

.. prompt:: python >>> auto
    
    >>> uitspraak = 'Guido zei: "Heb je Monty Python and the Holy Grail al gezien?"'
    >>> uitspraak
    'Guido zei: "Heb je Monty Python and the Holy Grail al gezien?"'
    >>> filmtitel = "Monty Python's Life of Brian"
    >>> filmtitel
    "Monty Python's Life of Brian"

Het gaat echter mis wanneer je binnen een string zowel enkele als dubbele aanhalingstekens wilt gebruiken:

.. prompt:: python >>> auto
    
    >>> uitspraak = 'Guido zei: "Heb je Monty Python's Life of Brian al gezien?"'
    SyntaxError: unterminated string literal (detected at line 1)

Python ziet dat de string begint met een enkel aanhalingsteken en denkt daardoor dat de string eindigt bij het enkele aanhalingsteken in :python:`Python's`. Dit probleem kun je op twee manieren oplossen: met escaping of met multiline strings.

Escaping
^^^^^^^^

Je kunt aan de manier waarop Python aanhalingstekens interpreteert *ontsnappen* door backslashes (:python:`\\`) te plaatsen voor de aanhalingstekens binnen de string. Python zal dan deze aanhalingsteken niet zien als het begin of einde van een string. Om het effect hiervan goed te zien, gebruik je de :python:`print()` functie. In onderstaand voorbeeld zie je dat :python:`print()` de tekst precies weergeeft zoals we willen, terwijl het commando :python:`uitspraak` de waarde van de variabele toont waarin de buitenste aanhalingstekens en de backslash nog zichtbaar zijn.

.. prompt:: python >>> auto
    
    >>> uitspraak = 'Guido zei: "Heb je Monty Python\'s Life of Brian al gezien?"'
    >>> uitspraak
    'Guido zei: "Heb je Monty Python\'s Life of Brian al gezien?"'
    >>> print(uitspraak)
    Guido zei: "Heb je Monty Python's Life of Brian al gezien?"

Multiline strings
^^^^^^^^^^^^^^^^^

Een multiline string is een string die begint en eindigt met drie enkele aanhalingstekens (:python:`'''`). Binnen zo'n string kun je naar hartelust andere aanhalingstekens gebruiken, zolang het maar niet drie enkele aanhalingstekens zijn.

.. prompt:: python >>> auto
    
    >>> uitspraak = '''Guido zei: "Heb je Monty Python's Life of Brian al gezien?"'''
    >>> uitspraak
    'Guido zei: "Heb je Monty Python\'s Life of Brian al gezien?"'
    >>> print(uitspraak)
    Guido zei: "Heb je Monty Python's Life of Brian al gezien?"

Je ziet dat het effect hetzelfde is al bij escaping. Sterker nog, Python heeft nu zelf een backslash in de string geplaatst om het aanhalingsteken te escapen!

Multiline betekent meerregelig, en een multiline string kan dus ook meerdere regels beslaan:

.. prompt:: python >>>,... auto
    
    >>> regels = '''Dit is de eerste regel.
    ... Dit is de tweede regel.
    ... Dit is de derde regel.'''
    >>> regels
    'Dit is de eerste regel.\nDit is de tweede regel.\nDit is de derde regel.'
    >>> print(regels)
    Dit is de eerste regel.
    Dit is de tweede regel.
    Dit is de derde regel.

.. note:: 
    Het escape karakter :python:`\\n` is het *new line* karakter, waardoor Python het vervolg van de string op een nieuwe regel afdrukt. Er zijn meer van dit soort escape karakters, bijvoorbeeld :python:`\\t`, waarmee je een *tab* kunt invoegen. Tabs worden vaak gebruikt om tekst mooi recht onder elkaar uit te lijnen.

Rekenen met strings
-------------------

Met getallen kun je rekenen, maar kan het ook met tekst? Niet echt, maar in Python kun je wel de operators :python:`+` en :python:`*` toepassen op strings. Met de eerste voeg je strings samen en met de tweede kun je strings herhalen.

Concatenatie
^^^^^^^^^^^^

Het aan elkaar plakken van twee strings wordt door programmeurs *concatenatie*  genoemd. Een moeilijk woord voor een eenvoudige bewerking, zie de voorbeelden hieronder.

.. prompt:: python >>>,... auto
    
    >>> 'Hallo' + 'Python'
    'HalloPython'
    >>> voornaam = 'John'
    >>> achternaam = 'Cleese'
    >>> print(voornaam + ' ' + achternaam)
    John Cleese

Repetitie
^^^^^^^^^

Om een string een aantal keren te herhalen (repeteren), gebruik je de :python:`*` operator, zie de voorbeelden hieronder.

.. prompt:: python >>>,... auto
    
    >>> 2 * 'bla'
    'blabla'
    >>> antwoord = 'ni'
    >>> print(5 * antwoord)
    ninininini
