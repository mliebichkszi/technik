# 01\_Erste Programme und Schleifen

**Programmieren** bedeutet, mit dem Computer zu **kommunizieren**. Wir teilen dem Computer mit, was er tun soll, und zwar in einer Sprache, die er versteht. Solche Sprachen nennt man Programmiersprachen. Wir verwen­den die Programmiersprache [Python](https://www.python.org/), weil sie einfach zu lesen und in Schulen sowie Universitäten weit verbreitet ist. Wie jede natürliche Sprache besteht auch eine Programmiersprache aus Wörtern, die eine bestimmte Bedeutung haben. Weil die einzelnen Wörter Anweisungen zur Ausführung einfacher Aktionen entsprechen, sprechen wir von Befehls­wörtern oder auch einfach von Befehlen. _Ein Programm ist ein grammatisch korrekter Text in einer gegebenen Programmiersprache, der eine Tätigkeit beschreibt_. Als erste Annäherung sehen wir ein Programm deshalb als eine Ab­folge von Anweisungen an.

Das Ziel des Programmierens ist es, eine Tätigkeit zu automatisieren. Das bedeutet, dass wir die Ausübung einer Tätigkeit komplett dem Computer überlassen. Computer sind aber im Unterschied zu Menschen nicht fähig zu improvisieren. Deswegen muss die Beschreibung der Tätigkeit in Form von Programmen eine eindeutige Interpretation besitzen. Das setzt auch voraus, dass wir die gewünschte Tätigkeit vollständig verstehen. In diesem Modul lernst du die ersten Programme zu schreiben. Ausserdem lernst du das Konstrukt der Schleifen kennen, welches dir ermöglicht, den Computer gewisse Tätig­keiten mehrfach wiederholen zu lassen.

![Du schreibst ein Programm, das dann ausgef&#xFC;hrt werden kann.](../../.gitbook/assets/grafik%20%2814%29.png)

Die Programmiersprache Python besitzt viele Befehle. Zu Beginn lernst du einige Befehle kennen, mit denen du den Computer beauftragen kannst, bestimmte Bilder zu zeichnen. Der Vorteil des Zeichnens für die Einführung ins Programmieren ist, dass sofort sichtbar wird, wenn der Computer etwas macht, was sich von der erwarteten Funktionalität unterscheidet. Dadurch kannst du die Programme effizient korrigieren. Schreibe das folgende Beispiel in [replit](https://replit.com/) ab. Melde dich bei replit an und erstelle ein neues Turtle-repl:

{% embed url="https://www.youtube.com/watch?v=StXrtNYMWQ0" %}

Achte dabei darauf, dass dir beim Abschreiben keine Fehler unterlaufen. Auch die Zwischenräume und die Gross- und Kleinschreibung müssen stimmen.

{% tabs %}
{% tab title="Beispiel 1.1" %}
```python
import turtle

t = turtle.Turtle()
t.forward (150) 
t.right ( 90) 
```
{% endtab %}
{% endtabs %}

`turtle.Turtle()`erstellt eine Schildkröte \(turtle\), die wir als `t` abspeichern. `t` kannst du dir wie einen Behälter vorstellen, in dem man etwas speichert. Wir nennen diesen Behälter beim Programmieren "Variable". Fortan können wir auf unsere Schildkröte zugreifen, wenn wir `t` eingeben. Die Schildkröte kann schon gewisse Dinge machen, beispielsweise vorwärtsgehen. Dazu müssen wir die Schildkröte mit `t`aufrufen. Nach einem Punkt `.` können wir dann einen Befehl aufrufen, zum Beispiel `forward`. Der Befehl `forward` verlangt aber noch nach einem Wert \(Probier `forward`mal ohne Wert aus, das gibt eine eindeutige Fehlermeldung 🧐 .

{% hint style="info" %}
**Wichtige Turtle-Befehle**

* forward \(Anzahl Pixel\) Vorwärtsgehen. Mit forward \( 15 0\) geht die Turtle 150 Pixel nach vorne.
* back \(Anzahl Pixel\) Rückwärtsgehen. Mit back \( 1 7\) geht die Turtle 17 Pixel rückwärts.
* left \(Winkel\) Nach links drehen. Mit le f t \( 12 0\) dreht sich die Turtle 120° nach links.
* right \(Winkel\) Nach rechts drehen. Mit right \( 90\) dreht sich die Turtle 90° nach rechts.  Eine Folge von Befehlen in einer Programmiersprache bezeichnen wir als **Programm.** Die vier hier vorgestellten Befehle bestehen aus zwei Teilen. Zuerst kommt der Befehlsname \( forward, back usw.\) und danach in Klammern der Parameterwert. Der Befehlsname bestimmt die Tätigkeit und der Parameter beschreibt den Umfang der Tätigkeit.
{% endhint %}

Das folgende Programm zeichnet ein gleichseitiges Dreieck mit Seitenlänge 150. Die Länge wird in Pixeln angegeben. Lass das Programm vom Computer ausführen. Beachte ausserdem, dass der Drehwinkel gleich dem Aussen­winkel des Dreiecks ist \(also 180° - 60° = 120°\).

{% tabs %}
{% tab title="Beispiel 1.2" %}
```python
import turtle

t = turtle.Turtle()

t.forward(150)
t.right (120)
t.forward (150)
t.right (120)
t.forward(150)
t.right (120)
```
{% endtab %}
{% endtabs %}

{% tabs %}
{% tab title="Aufgabe 1.1" %}
Was bewirkt Zeile 9 des Programms in Beispiel 1.2?
{% endtab %}

{% tab title="Lösung" %}
Die Turtle dreht sich um 120° nach rechts.
{% endtab %}
{% endtabs %}

{% tabs %}
{% tab title="Aufgabe 1.2" %}
Schreib ein Programm, das ein Rechteck der Grösse 200 x 100 zeichnet.
{% endtab %}

{% tab title="Lösung" %}

{% endtab %}
{% endtabs %}

{% tabs %}
{% tab title="Aufgabe 1.3" %}
Schreib  ein Programm, das einen Rhombus gemäss der folgenden Abbildung zeichnet.

![](../../.gitbook/assets/grafik%20%2810%29.png)
{% endtab %}

{% tab title="Lösung" %}

{% endtab %}
{% endtabs %}

{% tabs %}
{% tab title="Aufgabe 1.4" %}
Schreib ein Programm, das einen Blitz wie in der Skizze zeichnet. Wähle selbst die Länge der Linien und die Grösse der Winkel.

![](../../.gitbook/assets/grafik%20%286%29.png)
{% endtab %}

{% tab title="Lösung" %}

{% endtab %}
{% endtabs %}

{% tabs %}
{% tab title="Aufgabe 1.5" %}
Wandle dein Programm aus Aufgabe 1.4 so ab, dass es nur die Befehle back \(\) und left \(\) verwendet. Wie sieht das entstehende Bild aus, wenn du im Programm back \(\) durch forward \(\) ersetzst und left \(\) durch right \(\)? Welche Paare von Befehlen genügen, um alle Bilder zu zeichnen?
{% endtab %}

{% tab title="Lösung" %}

{% endtab %}
{% endtabs %}

### Mit Farben arbeiten

Die Turtle kann mit verschiedenen Farben zeichnen. Du kannst wählen, welche Farbe sie für den Stift verwenden soll. Die Turtle kennt über hundert verschiedene Farben, die du in Englisch angeben kannst. Zudem kannst du auch eine R\(ot\)G\(rün\)B\(lau\)-Wert, kurz RGB-Wert, angeben. Eine passende Farbe kannst du mit Google finden:

{% embed url="https://www.youtube.com/watch?v=w-SZ1tZBkBo" %}

#### 

{% tabs %}
{% tab title="Beispiel 1.3" %}
```python
import turtle

t = turtle.Turtle()

t.width(5)
t.forward(100)
t.left(120)
t.pencolor("red")
t.forward(100)
t.left(120)
t.pencolor(52, 195, 235)
t.forward(100)
t.left(120) 
```
{% endtab %}
{% endtabs %}

{% tabs %}
{% tab title="Aufgabe 1.6" %}
Was geschieht, wenn du die Turtle mit setPenColor \( "white"\) auf dem Bildschirm mit weisser Oberfläche bewegst? Führe das Programm aus und erkläre, was passiert.

```python
import turtle

t = turtle.Turtle()

t.forward(200)
t.pencolor("white")
t.back(100)
```
{% endtab %}

{% tab title="Lösung" %}

{% endtab %}
{% endtabs %}

{% tabs %}
{% tab title="Aufgabe 1.7" %}
Zeichne ein Haus wie in der folgenden Abbildung. Die ausgefüllte Türe kannst du mithilfe von `width()` erzeugen.  


![](../../.gitbook/assets/grafik%20%2818%29.png)
{% endtab %}

{% tab title="Lösung" %}

{% endtab %}
{% endtabs %}

{% hint style="success" %}
**Was du gelernt hast**

Ein Programm kann man als eine Folge von Befehlen ansehen. Zum Zeichnen lädst du zuerst die Turtle und öffnest ein neues Fenster. Danach steuerst du die Turtle mit den Befehlen forward \(\), back \(\), left \(\) und right \(\). Mit setPenColor \(\) kannnst du die Farbe des Stiftes ändern und mit setPenWidth \(\) gibst du an, wie breit der Stift der Turtle sein soll.
{% endhint %}

### Einfache Schleifen

Es gibt eine Möglichkeit, dem Rechner die Anweisung zu geben, dass er bestimmte Vorgänge beliebig viele Male wiederholen soll. So können Sie Programme schreiben, die kürzer und verständlicher sind. Mit der Anweisung repeat 3: sagen Sie dem Computer, dass er eine Folge von Befehlen dreimal wiederholen soll. Studiere die beiden folgenden Ausschnitte aus zwei Programmen. Sie führen genau die gleiche Tätigkeit aus:

```python
import turtle

t = turtle.Turtle()

t.forward(100)
t.left(120)
t.forward(100)
t.left(120)
t.forward(100)
t.left(120) 
t.back(100) 
```

```python
import turtle

t = turtle.Turtle()

for i in range(3):
    t.forward(100)
    t.left (120)
t.back(100) 
```

![Figur, die vom Programm gezeichnet wird](../../.gitbook/assets/grafik%20%2819%29.png)

{% hint style="info" %}
**Neue Konzepte und Begriffe**

* `for i in range (n)`ist eine Anweisung zur Repetition einer Anweisung, wobei `n`die Anzahl Wiederholungen angibt.
* Die Anweisung nach `for i in range(n)`muss eingerückt sein. Die ganze Struktur nennt man eine _Schleife_. Der Python-Interpreter erkennt das Ende 
{% endhint %}

Wir wollen ein regelmässiges Vieleck wie das Sechseck in Abbildung A zeichnen lassen. Zunächst überlegen wir uns, um wie viel Grad sich die Turtle nach dem Zeichnen jeder Seite drehen muss \(siehe Abbildung B\). Damit ein regelmässiges Sechseck entsteht, müssen alle Winkel gleich gross sein. Am einfachsten gehen wir folgender­massen vor: Wir sehen, dass sich die Turtle genau k-mal um den gleichen Winkel drehen muss, wenn sie ein k-Eck zeichnet. Weil die Turtle wieder in der Start­position endet und somit beim Zeichnen einen Rundweg absolviert, hat sie am Schluss eine vollständige Drehung um 360° gemacht. Deswegen dreht sie sich jeweils um  $$360°/k$$ .

![](../../.gitbook/assets/grafik%20%2821%29.png)

![](../../.gitbook/assets/grafik%20%2820%29.png)

```python
import turtle

t = turtle.Turtle()

#mach 6mal:
for i in range(6):
  #das
  print('hallo')
  t.forward(100)
  t.right(360/6)
```

Beachte, dass der Computer beim Aufruf von \`t.right\(360/6\) zuerst den Winkel berechnet \(also 60°\) und dann den Befehl right \(\) mit dem berechneten Parameterwert ausführt. Wir hätten also auch direkt right \( 60\) schreiben können. Durch das Ausschreiben der Rechnung geben wir einen Hinweis darauf, wie wir auf den Drehwinkel gekommen sind. Wir werden bald sehen, dass Berechnungen innerhalb von Programmen noch viel weitreichendere Vorteile bringen.

