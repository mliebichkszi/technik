# Listen und Funktionen

## Listen und Summen <a href="#listen-und-summen" id="listen-und-summen"></a>

### **Einführung**

Die Primzahlen eignen sich hervorragend als Beispiel- Liste, weil die Zahlen nicht regelmässig verteilt sind. In diesem Ab- schnitt stellen wir verschiedene Techniken vor, um die Summe einer Liste von Primzahlen (oder anderem) zu berechnen.

**For-Schleife** For-Schleifen in Python arbeiten _immer_ mit Listen: Die Laufvariable geht der Reihe nach alle Elemente einer Liste durch. Damit ist diese Technik prädestiniert, um die Summe zu bilden.

```python
primes = [2, 3, 5, 7, 11, 13, 17, 19]
summe = 0
for p in primes:
    summe += p
print (summe)
```

### **Funktionen**&#x20;

In Python wird eine Funktion mit **def** definiert und gibt mit **return** ein Resultat zurück. Indem wir den Code oben in eine Funktion verpacken, haben wir flexibleren, wiederverwendbaren Code:

```python
def summe(liste): result = 0
    for zahl in liste: result += zahl
    return result
    primes = [2, 3, 5, 7, 11, 13, 17, 19]
print (summe(primes))
```

### **Eine Funktion für alles**

Weil Variablen in Python keinen festen Typ haben, können wir die Summenfunktion auch so umschreiben, dass sie Strings (Zeichenketten) zusammenhängt.

```python
def summe(liste):
    if liste != []:
        result = head(liste)
        for item in tail(liste):
            result += item
        return result
    else:
        return None
primes = [2, 3, 5, 7, 11, 13, 17, 19]
print (summe(primes))
print (summe(["Tic", "Tac", "Toe"])
```

## **AUFGABEN**

{% tabs %}
{% tab title="Aufgabe 1" %}
Schreibe eine Funktion fakult(n), die die Fakultät _n_! = 1 _·_ 2 _·_ 3 _· · · n_

einer Zahl _n_ berechnet.

Natürlich geht das auf völlig verschiedene Arten und die interessante Aufgabe wäre, möglichst viele verschiedene Wege für die Berechnung zu finden.
{% endtab %}

{% tab title="Lösung" %}
```python
def fakultaet(zahl):
  produkt = 1
  for i in range(zahl-1):
    produkt = produkt * zahl
    zahl = zahl - 1

  print('Das Resultat ist: ', produkt)

fakultaet(int(input('Welche Zahl? '))
```
{% endtab %}
{% endtabs %}

{% tabs %}
{% tab title="Aufgabe 2" %}
Ein altes Rätsel von Sam Loyd (1841–1911):



![](../../../.gitbook/assets/0)

_Neulich sah ich mir zusammen mit einem Freund die Attraktionen auf Coney Is- land an, und dabei lernten wir kennen, was uns jemand als das ehrlichste Spiel am ganzen Strand anpries. Da waren zehn kleine Figuren, die man mit einem Ball umwerfen musste. Der Mann sagte: «Für 1 Cent haben Sie einen Wurf, und Sie können werfen, so oft Sie wollen, und so dicht ’rangehen, wie Sie wollen. Zählen Sie die Zahlen auf den Figuren, die Sie umwerfen zusammen, und wenn Sie genau 50 haben, nicht mehr und nicht weniger, erhalten Sie eine prächtige Maggie-Cline- Zigarre mit einem Goldband drum herum.»_

_Unser Geld war alle, noch bevor wir heraus hatten, wie man eigentlich gewin- nen konnte. Ausserdem fiel uns auf, dass eine ganze Menge Leute genauso wenig Maggie-Cline-Zigarren rauchten wie wir. Wissen Sie, wie man genau 50 Punkte macht?_

Die Aufgabe besteht also darin, aus den gegebenen Zahlen jene heraus- zusuchen, die zusammen die Summe 50 ergeben:

25_,_ 27_,_ 3_,_ 12_,_ 6_,_ 15_,_ 9_,_ 30_,_ 21_,_ 19

Schreibe ein Programm, das diese Aufgabe für dich übernimmt!
{% endtab %}

{% tab title="Lösung" %}

{% endtab %}
{% endtabs %}

****
