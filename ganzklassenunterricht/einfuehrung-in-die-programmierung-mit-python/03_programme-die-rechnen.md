# 03\_Programme, die rechnen

Computer können besonders schnell rechnen. Deswegen wurden die Computer ursprünglich gebaut und «Rechner» genannt. Somit können Sie den Computer als Taschenrechner verwenden. Mit dem Befehl `print ( )` gibst du das Resultat der Rechnung direkt aus. Wir wollen den arithmetischen Ausdruck (163 · 3) - (77 · 4) berechnen lassen und das Resultat ausgeben. Dazu schreiben wir das folgende Programm und führen es aus.

```python
print((163 * 3) - (77 * 4))
```

Welche Unterschiede beobachtest du bei der Ausgabe der folgenden vier Zeilen? Inwiefern unterscheiden sich die beiden Operatoren / und / / für die Division? Was macht der %-Operator?

```python
print (7/4)
print (7//4)
print ("7/4")
print (7%4)
```

Wir möchten eine ganze Rechnung ausgeben und danach das Resultat.

```python
print ('Das Quadrat von 15 ist:', 15**2)
```

{% hint style="info" %}
Unter einem Ausdruck verstehen wir einen arithmetischen Ausdruck oder einen Text. Für arithmetische Ausdrücke gilt:

**print (Ausdruck1,Ausdruck2,Ausdruck3, ... )**\
Der Computer wertet zuerst jeden Ausdruck aus und gibt die Resultate anschliessend in einer Zeile im Ausgabefenster aus.\
**Zahl1 + Zahl2**\
Berechnet die Summe von Zahl1 und Zahl2.\
**Zahl1 - Zahl2**\
Berechnet die Differenz von Zahl1 und Zahl2.\
**Zahl1\*Zahl2**\
__Berechnet die Multiplikation von Zahl1 und Zahl2.\
**Zahl1 / Zahl2** \
Berechnet die Division von Zahl1 durch Zahl2.\
**Zahl1 / / Zahl2**\
Berechnet die ganzzahlige Division von Zahl1 durch Zahl2.\
**Zahl1 % Zahl2**\
Berechnet den Rest der ganzzahligen Division von Zahl1 durch Zahl2.\
**Zahl\* n**\
Berechnet die n-te Potenz von Zahl.\
**sqrt (Zahl)**\
Berechnet die Quadratwurzel von Zahl.
{% endhint %}

{% tabs %}
{% tab title="Aufgabe 3.1" %}
Der arithmetische Ausdruck 4 · 4 · 4 · 4 + 1 ergibt eine Primzahl. Lass die Zahl von Python berechnen und gib sie auf dem Bildschirm aus.
{% endtab %}
{% endtabs %}

{% tabs %}
{% tab title="Aufgabe 3.2" %}
Berechnen Sie den Goldenen Schnitt $$\phi = (1+\sqrt(5) )/ 2$$&#x20;
{% endtab %}
{% endtabs %}

{% tabs %}
{% tab title="Aufgabe 3.3" %}
Wir möchten ein rechtwinkliges gleichschenkliges Dreieck wie in der Abbildung zeichnen. Das Dreieck hat einen 90°-Winkel und zwei 45°-Winkel. Die kürzeren Seiten (Katheten) haben eine beliebige Länge x. Die Länge der längeren Seite (Hypotenuse) kann mit der Formel $$x\cdot\sqrt2$$ berechnet werden. Statt dass wir die konkrete Länge der Hypotenuse selbst mühsam ausrechnen, lassen wir dies den Computer tun.\


![Gleichschenkliges Dreieck](<../../.gitbook/assets/grafik (30).png>)
{% endtab %}

{% tab title="Lösung" %}
```python
import turtle

t = turtle.Turtle()
t.right(45)
t.forward(60)
t.right(90)
t.forward(60)
t.right(135)
t.forward(60 * sqrt(2))
```
{% endtab %}
{% endtabs %}

{% tabs %}
{% tab title="Aufgabe 3.4" %}
Schreib ein Programm, das mit der Turtle ein Haus wie in der Abbildung zeichnet. Das Haus besteht aus vielen rechtwinkligen gleichschenkligen Drei­ecken wie im vorherigen Beispiel. Damit kannst du dir auch überlegen, wie viel länger oder kürzer die einzelnen Strecken sind. Das Grundquadrat hat hier eine Seiten­länge von 185 Pixeln.\


![](<../../.gitbook/assets/grafik (31).png>)
{% endtab %}

{% tab title="Lösung" %}

{% endtab %}
{% endtabs %}

{% tabs %}
{% tab title="Aufgabe 3.5" %}
Schreib ein Programm, das mit der Turtle zunächst ein gleichseitiges Dreieck mit der Seitenlänge 144 Pixel zeichnet. Danach zeichnest du mit der Turtle die Höhe in roter Farbe ein. Das Programm soll die Höhe selbst berechnen.
{% endtab %}

{% tab title="Lösung" %}

{% endtab %}
{% endtabs %}

{% tabs %}
{% tab title="Aufgabe 3.6" %}
Erweitere das Programm aus Aufgabe 3.5 so, dass es zusätzlich mit roter Farbe die Höhe des Hauses vom Boden bis zur Dachspitze zeichnet.
{% endtab %}

{% tab title="Lösung" %}

{% endtab %}
{% endtabs %}

{% hint style="success" %}
Anstelle von Zahlenwerten kannst du in Python auch ganze Rechnungen in Form von arithmetischen Ausdrücken einsetzen. Python wertet alle diese arithmetischen Ausdrücke zuerst aus und arbeitet dann mit den Ergebnissen weiter. Ein Ausdruck in Anführungszeichen ist für Python einfach ein Text, der mit dem Befehl print () Zeichen für Zeichen ausgegeben wird.
{% endhint %}
