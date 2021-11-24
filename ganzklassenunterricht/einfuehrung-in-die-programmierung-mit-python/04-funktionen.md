# 04 Funktionen

Hast du früher einmal mit LEGO® gespielt? Man baut zu Beginn aus einzelnen Steinen kleine, einfache Elemente. Dann setzt man diese einfachen Elemente zusammen und baut damit etwas Grosses und Komplexes, zum Beispiel ein Fahrzeug oder ein Gebäude. Mehrere Gebäude kann man zu einem Strassenzug oder sogar zu einer ganzen Stadt zusammensetzen. Beim Programmieren verwendest du die gleiche Vorgehensweise: Du schreibst zunächst kleinere Programme, die einfache Tätigkeiten ausführen. Solche kleinen Programme nennen wir Bausteine. Wenn du mehrere Bausteine geschickt zusam­mensetzt, entsteht ein Programm, das eine komplexere Tätigkeit ausführen kann. Die zusam­mengesetzten Programme können wiederum Bausteine sein, aus denen noch komplexere Pro­gramme zusammengebaut werden. Diese Art, Programme zu entwickeln, heisst modularer Entwurf.

In natürlichen Sprachen führen wir immer neue Wörter ein, um uns einfacher und genauer ausdrücken zu können. Auch in Programmier­sprachen kannst du neue Wörter - also neue Befehle - einführen, um eine Tätigkeit einfacher und verständlicher zu beschreiben. Es reicht hierzu, ein Programm zu benennen und diesen Namen als Befehl für die durch das Programm beschriebene Tätigkeit zu verwenden. Du entwickelst die Programmiersprache also selbst weiter und vereinfachst dadurch die Kommu­nikation mit dem Computer. Das Ziel dieses Abschnitts ist, dass du lernst, wie du in Python mithilfe des modularen Entwurfs übersichtliche Programme erstellen kannst . Zusätzlich lernst du, wie der modulare Entwurf es dir erleichtert, Animationen zu program­mieren.

### Neue Befehle definieren und verwenden

Bis jetzt bestand unsere Sprache nur aus elementaren Befehlen, wie zum Beispiel `forward()` und `back()`, die gerade Linien zeichnen können. Python bietet die Möglichkeit, Einzelbefehle zu neuen, komplexeren Befehlen unter einem Namen zusammenzufassen. Somit kann ein Befehl einer beliebig komplexen Tätigkeit entsprechen. Wir wollen der Turtle beibringen, wie sie ein Quadrat mit der Seitenlänge 100 zeichnen kann. Wie jedes Programm beginnt auch dieses mit dem Laden der Turtle in der ersten Zeile. Danach definieren wir mithilfe von `def` den neuen Befehl `quadrat100()`. Die Klammern am Schluss sind grammatisch wichtig: In Python haben alle Befehle am Ende Klammern, die du nicht weglassen darfst. Im folgenden Programm siehst du, wie wir alles, was zum Zeichnen des Quadrates gehört, bezüglich `def` eingerückt haben. Bei der Definition eines neuen Befehls ist es wichtig, dass alles, was den Befehl beschreibt, gleichmässig gegenüber `def` eingerückt ist. Diesen eingerückten Teil nennt man den «Körper des Befehls». Beim Definieren eines neuen Befehls mit def zeichnet der Computer noch nichts. Er lernt nur, was das neue Wort (der neue Befehl) `quadrat100`bedeutet. Ganz am Schluss öffnen wir das Fenster und weisen die Turtle an, ein Quadrat zu zeichnen. Weil wir `quadrat100`vorher definiert haben, können wir den Befehl jetzt einfach aufrufen und die Turtle führt den Körper des mit `quadrat100` benannten Befehls aus.

```python
import turtle as t

def quadrat100():
    for i in range(4):
        t.forward(100)
        t.right(90)
quadrat100()
t.left(45)
quadrat100()
```

Schreib das Programm in Python ab und führe es aus. Achte auf die korrekte Einrückung und den Doppelpunkt nach dem Namen des neuen Befehls - dieser Doppelpunkt ist nötig.

{% tabs %}
{% tab title="Aufgabe 4.1" %}
Schreib selbst ein Programm mit der Definition für einen Befehl `dreieck50()`. Der Befehl soll ein gleichseitiges Dreieck mit der Seitenlänge 50 zeichnen. Rufe den Befehl auf, um das Dreieck zu zeichnen.
{% endtab %}

{% tab title="Second Tab" %}

{% endtab %}
{% endtabs %}

{% hint style="info" %}
def Befehlsname() : Mit def bringst du dem Computer einen neuen Befehl bei. Der Befehls­name muss am Ende immer Klammern haben. Später werden wir den Grund für die Klammern kennen lernen. Nach dem Namen kommt ein Doppelpunkt. Darunter steht gegenüber def eingerückt die Beschreibung des neuen Befehls. Diese Beschreibung bezeichnet man als den Körper des Befehls.&#x20;

Der Name eines Befehls muss ein Wort ohne Leerzeichen oder Umlaute (also «ä», «ö» oder «Ü>>) sein. Wenn du mehrere Wörter zu einem Namen zusammenhängen möchtest,  kannst du Unterstriche verwenden. Du darfst eine Zahl anhängen, aber nicht mit einer Zahl beginnen. Beispiel: name\_mit\_3\_woertern

Wenn Du einen Befehl mit def definierst, dann zeichnet die Turtle noch nichts. Der Computer lernt zwar die Bedeutung eines neuen Wortes, aber dies ist auf dem Bildschirm nicht sichtbar. Der Computer zeichnet mit der Turtle erst dann etwas, wenn du den neuen Befehl auch im Programm aufrufst. Ein neuer Befehl muss immer vor dem ersten Aufruf definiert werden.
{% endhint %}

Das Fenster in der Abbildung unten kann man ganz einfach zeichnen: drei waagrechte Linien mit Länge 200, drei senkrechte Linien mit Länge 200. Noch einfacher geht es aber mithilfe eines Bausteins: Wir setzen das Bild aus vier Quadraten zusammen. Dazu definieren und verwenden wir wieder den Befehl quadratl00 (). Die Turtle steht zu Beginn in der Mitte des Fensters und zeichnet zuerst das Quadrat rechts oben. Danach dreht sie sich um 90° nach rechts und zeichnet das Quadrat rechts unten usw.

![](<../../.gitbook/assets/grafik (39) (1).png>)

```python
import turtle as t

def quadrat100():
    for i in range(4):
        t.forward(100)
        t.right(90)
        
for i in range(4):
    quadrat100()
    t.right(90)
```

{% tabs %}
{% tab title="Aufgabe 4.2" %}
Definiere einen Befehl `blatt()`, der ein Blatt wie in der Abbildung unten aus zwei Drittelkreisen zeichnet. Nutze den Befehl `blatt()`, um:

...eine Blume mit 12 Blättern zu zeichnen.

...eine Blume mit 18 Blättern zu zeichnen, wobei die Farbe zwischen Rot und Gelb wechselt.&#x20;

...vier Blätter nacheinander wie im folgenden Bild zu zeichnen.

![](<../../.gitbook/assets/grafik (38) (1).png>)![](<../../.gitbook/assets/grafik (37) (1) (1).png>)
{% endtab %}

{% tab title="Lösung" %}

{% endtab %}
{% endtabs %}

Wir haben den Befehl `quadrat100()` erstellt. Um häufig verwendete Befehle nicht in jedem Programm neu definieren zu müssen, ist es möglich, sie ein für alle Mal in einem Modul zu definieren und somit in einer separaten Python-Datei zu speichern (z.B. mit dem Namen «meine\_befehle.py»). Die in diesem Modul definierten Befehle können dann über eine import-Anweisung geladen werden. Der Dateiname muss mit dem Namen des Moduls überein­stimmen, dem die Erweiterung «.py» hinzugefügt wird, und das Modul muss sich im gleichen Ordner wie die Programmdatei befinden.

Du kannst dann in einem anderen Programm beliebig viele von den im Modul definierten Befehlen verwenden. Dazu musst du diese Befehle mithilfe der Anweisung `from meine_befehle import *` in das aktuelle Programm in die 1. Zeile einfügen.

{% tabs %}
{% tab title="Aufgabe 4.3" %}
Schau dir das folgende Programm an und überlege dir, was es zeichnet. Skizziere das Bild zunächst auf einem Blatt, indem du den Programmanweisungen folgst. Überprüfe dann deine Lösung, indem du den Computer das Programm ausführen lässt. Beachte, dass der Computer den Befehl `quadrat100`bereits kennt, weil du ihn abgespeicherst hast.

```python
import turtle as t
from meine_befehle import *

for i in range 8:
    quadrat100()
    right(45)
```
{% endtab %}
{% endtabs %}

{% tabs %}
{% tab title="Aufgabe 4.4" %}
Definiere einen Befehl `dreieck100()`zum Zeichnen eines gleichseitigen Dreiecks mit Seitenlänge 100 wie in Abbildung A. Nutze `dreieck100()` um eine Form wie in Abbildung B zu zeichnen.

![](<../../.gitbook/assets/grafik (41).png>)![](<../../.gitbook/assets/grafik (45) (1) (1).png>)
{% endtab %}

{% tab title="Lösung" %}

{% endtab %}
{% endtabs %}

{% tabs %}
{% tab title="Aufgabe 4.5" %}
Verwende den Befehl `quadrat100()`um folgende Bilder zu zeichnen.

![](<../../.gitbook/assets/grafik (37) (1).png>)![](<../../.gitbook/assets/grafik (42).png>)![](<../../.gitbook/assets/grafik (40).png>)
{% endtab %}

{% tab title="Lösung" %}

{% endtab %}
{% endtabs %}

{% tabs %}
{% tab title="Aufgabe 4.6" %}
Verwende die Befehle `quadrate100()`und `dreieck100()`, um eine Form wie in der folgenden Abbildung zu zeichnen.

![](<../../.gitbook/assets/grafik (43).png>)
{% endtab %}

{% tab title="Lösung" %}

{% endtab %}
{% endtabs %}

{% tabs %}
{% tab title="Aufgabe 4.7" %}
Definiere einen Befehl `offenes_quadrat()`, der ein offenes Quadrat wie in Abbildung A zeichnet. Schreibe dann ein Programm, das den neuen Befehl `offenes_quadrat`verwendet, um das Kreuz in Abbildung B zu zeichnen.

![](<../../.gitbook/assets/grafik (38).png>)![](<../../.gitbook/assets/grafik (39).png>)
{% endtab %}

{% tab title="Lösung" %}

{% endtab %}
{% endtabs %}
