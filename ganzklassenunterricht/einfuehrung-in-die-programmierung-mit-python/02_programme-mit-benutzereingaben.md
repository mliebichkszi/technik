# 02\_Programme mit Benutzereingaben

Anstatt zu zeichnen, verwenden wir den Computer nun, um mit Texten zu arbeiten. Beachte, dass du hier die zwei Befehle zum Laden der Turtle nicht brauchst, da wir ohne die Turtle arbeiten. Alle Daten werden im Computer als Folgen von Symbolen und letztendlich als Folgen von O und 1 gespeichert. Damit der Computer die Daten richtig darstellen kann, muss er wissen, ob er eine gegebene Zeichenfolge als Zahl, Text oder etwas anderes interpretieren soll. Aus diesem Grund gibt es Datentypen, mit welchen wir festhalten können, was die Daten darstellen. Wir stellen hier zuerst einmal drei grundlegende Datentypen vor: `int`, `float` und `str`.

{% hint style="info" %}
**Datentyp Zahl**  
Dieser Datentyp beinhaltet ganze Zahlen und Kommazahlen. Für die ganzen Zahlen verwenden wir die Bezeichnung Integer. In Python wird die Kurz­form `int` benutzt. Für die Kommazahlen verwenden wir die Bezeichnung Float. In Python werden sie mit `float`ezeichnet.   
**Datentyp Text**  
Texte stehen immer in Anführungszeichen. Dadurch sieht der Computer sofort, dass es sich um einen Text handelt. Wir nennen diesen Datentyp String. In Python werden Strings mit `str` bezeichnet.
{% endhint %}

### Beispiel

Schreib das folgende Programm ab und führ es aus. Was steht im Ausgabefenster? Was bewirkt `\n` ?

```python
print("Was machst du?\nich programmiere.")
```

{% hint style="info" %}
`print(Text)`  
Der Befehl print \( "Hallo163"\) bewirkt, dass der Computer im Ausgabefenster den Text «Hallo163» ausgibt und dann im Ausgabefenster in die nächste Zeile springt. Der Text, der ausgegeben werden soll, muss zwischen geraden Anführungszeichen \(" " oder ' '\) stehen.  
`\n`  
Innerhalb von Texten \(und nur dort\) bewirkt die Zeichenfolge  n einen Zeilenumbruch im Ausgabefenster.
{% endhint %}

### Text wiederholen

Wir könnten den Text wiederholen, indem wir ihn einfach zweimal hintereinander notieren oder ihn multiplizieren.

```python
print("Ich programmiere! Ich programmiere!") 
print("Ich programmiere" * 2)
```

Mit `*` kannst du also vervielfältigen, mit `+` Text zusammenhängen \(konkatenieren\).

{% tabs %}
{% tab title="Aufgabe 1" %}

{% endtab %}

{% tab title="Second Tab" %}

{% endtab %}
{% endtabs %}

