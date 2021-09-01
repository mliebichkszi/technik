# Eine Blume mit der Turtle zeichnen

## Ein Blütenblatt zeichnen

Das folgende Programm zeichnet ein Blütenblatt.Das Blatt besteht aus zwei Drittelkreisen. Die Drehung in Zeile 7 richtet die Turtle so aus, dass das Blatt vertikal gezeichnet werden kann.

![](.gitbook/assets/grafik%20%2825%29.png)

```python
import turtle

t = turtle.Turtle()

t.left(150)

for i in range(120):
  t.forward(3)
  t.right(1)
t.right(60)

for i in range(120):
  t.forward(3)
  t.right(1)

t.right(60)
t.right(60)
```

## Vierblättrige Blüte

Das folgende Programm zeichnet mehrere Blätter:

![](.gitbook/assets/grafik%20%2824%29.png)

{% hint style="info" %}
Im untenstehenden Programm werden mehrere Wiederholungen \(Schleifen\) innerhalb der Schleife `for i in range(4):`durchlaufen.  
Man spricht von "inneren" und "äusseren" Schleifen.
{% endhint %}

```python
import turtle

t = turtle.Turtle()

t.left(120)

for i in range(4):
  for i in range(60):
    t.forward(3)
    t.right(1)
  t.right(120)

  for i in range(60):
    t.forward(3)
    t.right(1)

  t.right(120)
  t.right(360/4)

t.right(30)
```

{% hint style="success" %}
Schreibe in [https://repl.it](https://repl.it) ein Python-Skript, das die folgende Blüte mit der Turtle zeichnet.
{% endhint %}

![](.gitbook/assets/grafik%20%2826%29.png)

## 💐 🌹 🌸 🌷 

{% hint style="success" %}
Fülle die Blütenblätter mit unterschiedlichen Farben und lade die farbige Blüte in Teams hoch.
{% endhint %}

{% hint style="success" %}
Erfinde deine ganz eigene Blüte. Schreibe dazu ein Programm, das auch Zufallszahlen verwendet. Zufallszahlen kannst du mit dem Python-Modul `random` erzeugen:
{% endhint %}

```python
import turtle
import random

# Eine Turtle erzeugen
fred = turtle.Turtle()

# Diese Farben sind bereits im turtle Modul definiert und können gleich verwendet werden
farben  = ["red","green","blue","orange","purple","pink","yellow"]
# Zufällig eine Farbe wählen
farbe = random.choice(farben)
# Mit diesem Code bekommt deine Turtle eine zufällige Farbe
fred.color(farbe)
```

