.. role:: python(code)
    :language: python

Berekeningen in de CLI
======================

Het woord 'computer' komt van het Latijnse computare, dat 'berekenen' betekent. Soms ook wordt een computer gekscherend een uit de kluiten gewassen rekenmachine genoemd. Het is vrijwel onmogelijk een computerprogramma te maken waarin niets wordt berekend. Daarom is het belangrijk dat je leert hoe rekenen in Python werkt.

De CLI
------
In dit hoofdstuk gebruik je de :term:`CLI`, de Command Line Interface. De CLI wordt ook wel *Interactieve Prompt* genoemd. *Interactief* geeft aan dat je direct met Python communiceert: je typt een commando, drukt op Enter en ziet meteen het resultaat. *Prompt* staat voor het symbool dat aangeeft dat je een commando kunt typen. In Python is dat vaak :python:`˃˃˃`.

.. prompt:: python ˃˃˃ auto
    
    ˃˃˃ 2+2
    4
    ˃˃˃

Hieronder lees je waar je de CLI kunt vinden in IDLE, Mu en Replit.

CLI in IDLE
^^^^^^^^^^^

In IDLE is de CLI het eenvoudigst te vinden. Je krijgt hem namelijk meteen te zien wanneer je IDLE opstart.

.. figure:: ../images/CLI_IDLE.png
   :alt: de CLI in Python IDLE
   :align: center

   CLI in Python IDLE

CLI in Mu
^^^^^^^^^

In Mu dien je een paar extra stappen uit te voeren om bij de CLI te komen. Mu start namelijk standaard met een bestand waarin je programmacode kunt typen. Laat dit bestand leeg, maar sla het wel op, bijvoorbeeld onder de naam :file:`blank.py`. Klik daarna op de :guilabel:`Run` knop om de (niet bestaande) code uit te voeren. Daardoor wordt in het onderste deel van het Mu venster de CLI geopend.

.. figure:: ../images/CLI_Mu.png
   :alt: de CLI in Mu
   :align: center

   CLI in Mu

CLI in Replit
^^^^^^^^^^^^^
In Replit wordt de CLI *Console* genoemd. Dit tabblad wordt standaard geopend, maar mocht dat niet het geval zijn, dan kun je het altijd toevoegen door op de + te klikken naast de geopende tabbladen. Merk op dat Replit niet de standaard Python prompt :python:`˃˃˃` gebruikt, maar slechts één :python:`˃`.

.. figure:: ../images/CLI_Replit.png
   :alt: de CLI in Replit
   :align: center

   CLI (Console) in Replit

Optellen, aftrekken, vermenigvuldigen en delen
----------------------------------------------

In het dagelijks leven gebruiken we meestal de symbolen :math:`+`, :math:`-`, :math:`\times` en :math:`:` voor optellen, aftrekken, vermenigvuldigen en delen. In Python noemen we de symbolen voor berekeningen :term:`operators<operator>` en ze wijken voor vermenigvuldigen en delen af van de symbolen die je gewend bent.

.. list-table:: Rekenkundige operators
    :header-rows: 1
    :align: center

    * - Berekening
      - Dagelijks leven
      - Python
    * - Optellen
      - :math:`+`
      - :math:`+`
    * - Aftrekken
      - :math:`-`
      - :math:`-`
    * - Vermenigvuldigen
      - :math:`\times`
      - :math:`*`
    * - Delen
      - :math:`:`
      - :math:`/`

Probeer de rekenkundige operators eens uit in de CLI. Voer bijvoorbeeld de volgende berekeningen in en druk telkens op :kbd:`Enter` om Python het antwoord te laten geven:

.. prompt:: python ˃˃˃ auto
    
    ˃˃˃ 15 + 49
    64
    ˃˃˃ 1048 - 256
    792
    ˃˃˃ 12 * 14
    168
    ˃˃˃ 345 / 23
    15.0

Het antwoord op de deling :python:`345 / 23` wekt misschien enige verbazing. Waarom antwoordt Python hier :python:`15.0` en niet gewoon :python:`15`? Daar komen we later op terug in het hoofdstuk datatypes.

..
    TODO: verwijzing maken naar hoofdstuk datatypes.

.. note:: 

    Wellicht is je opgevallen dat in de voorbeelden spaties zijn gebruikt in de berekeningen: :python:`15 + 49` in plaats van :python:`15+49`. De reden hiervoor is betere leesbaarheid. Voor Python maakt het niet uit of je wel of geen spaties tussen de operator en de getallen typt.
