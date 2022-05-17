# 06\_Listen

Statt in einer Variablen kann man Werte auch bequem in einer Liste abspeichern und sie später bearbeiten.

Du kannst den Code der nachfolgenden Beispiele kopieren, falls du ihn in deinem repl ausprobieren willst.

Wir könnten bspw. Werte eines Temperatur-Sensors (hier 3 Werte: x, y, z) in einer Liste speichern:

```python
temperaturen = [x, y, z]
```

Auf diese Werte können wir über danach über den sogenannten _Index_ zugreifen:

```python
    x_temperatur = temperaturen[0]
    y_temperatur = temperaturen[1]
    z_temperatur = temperaturen[2]
```

Wir können auch mit `for` durch die Liste durchgehen ("durchiterieren"):

```python
    for element in temperaturen:
      print (element)
```

Probiere es in [https://repl.it/](https://repl.it/) aus.\
\
Du kannst Listen sogar verschachteln, also eine Liste in einer Liste haben:

```python
sensordaten = [['montag', 'dienstag'], [22, 30]]
```

Es gibt vordefinierte Befehle ("Funktionen"), die wir auf Listen anwenden können:

```python
    # Gibt die Länge der Liste aus:
    len(liste)
```

Du kannst mit `enumerate` auch den Index und den zugehörigen Wert ausgeben:

```python
    for i, wert in enumerate (liste, 1):
      print (i, wert)
```

Elemente kannst du wie folgt hinzufügen oder löschen:

```python
    liste = [1, 'hi']
    # fügt einen Wert hinzu
    liste.append(24.0)
    # fügt an Position 5 einen Wert hinzu. Achtung: die Liste muss schon entsprechend gross sein
    liste[5] = 'Hallo'
    # fügt an erster Stelle 'informatik' hinzu
    liste.insert(0, 'informatik')
    # löscht den ersten Wert
    liste.pop(0)
    # löscht das Element 'Hallo'
    liste.remove('Hallo')
```

Du kannst eine Liste mit `for i in range` auch rasch mit Werten füllen:

```python
    '''Erzeugt eine Liste mit den ersten 100 quadrierten Zahlen, von 0 aus
    startend'''

    liste = [x**2 for x in range(100)]
```

{% tabs %}
{% tab title="Aufgabe 1" %}
Schreib in [https://repl.it](https://repl.it) ein Einkaufslisten-Programm. Das Programm soll dich zuerst zweimal hintereinander nach den einzukaufenden Produkten fragen. Danach soll es dir erlauben, ein Listenelement zu löschen (liste.remove(element)).&#x20;
{% endtab %}

{% tab title="Lösung" %}

{% endtab %}
{% endtabs %}

{% tabs %}
{% tab title="Aufgabe 2" %}
Du kennst sicher das Spiel "Schiffe versenken". Bei diesem Spiel muss ein Spieler erraten, wo das gegnerische Schiff auf dem Spielfeld liegt.

![](<../../.gitbook/assets/grafik (49).png>)

Im Unterricht werden wir den Anfang des Spiels programmieren. Versuche, das Spiel weiterzuentwickeln, sodass auf einem grösseren Spielfeld

&#x20;gespielt werden kann.
{% endtab %}

{% tab title="Lösung (in Progress)" %}
```python
import random

geratene = []

def computerzug():
  computerfeld = []
  computerfeld1 = []
  for i in range(10):
    computerfeld.append('')
    computerfeld1.append('')
  zufallspos = random.randint(0,7)
  computerfeld[zufallspos] = 'X'
  computerfeld[zufallspos+1] = 'X'
  computerfeld[zufallspos+2] = 'X'
  computerfeld1[zufallspos] = 'X'
  computerfeld1[zufallspos+1] = 'X'
  computerfeld1[zufallspos+2] = 'X'
  print(computerfeld)
  print(computerfeld1)
  # danke villmal fürs fäld
  return computerfeld

def spielerzug(computerfeld,geratene):
  treffer = 0
  while treffer < 3:
    geratene_pos = int(input('Wo vermutest du das Schiff? ')) - 1
    print(geratene)
    if geratene_pos in geratene:
      print('Das hast du schon mal probiert')
    elif computerfeld[geratene_pos] == 'X':
      print('Treffer!')
      treffer = treffer + 1
      geratene.append(geratene_pos)
    # elif ist eine Abkürzung für else if
    elif computerfeld[geratene_pos] != 'X':
      print('Leider daneben!')
      geratene.append(geratene_pos)
  print('Du hast das Schiff versenkt!')

spielerzug(computerzug(), geratene)
```
{% endtab %}
{% endtabs %}
