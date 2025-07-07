# Grundlagen 2 – LED anschließen 💡

<div style="display:flex; justify-content:space-between; margin-bottom:1em;">
  <a href="Grundlagen1" style="
    display:inline-block;
    background:#e8f0fe;
    color:#333333;
    padding:0.4em 1em;
    border-radius:4px;
    text-decoration:none;
    font-weight:500;
    border:1px solid #d2e3fc;">
    Zurück
  </a>

  <a href="Grundlagen3" style="
    display:inline-block;
    background:#e8f0fe;
    color:#333333;
    padding:0.4em 1em;
    border-radius:4px;
    text-decoration:none;
    font-weight:500;
    border:1px solid #5f9c80;">
    Weiter
  </a>
</div>

**In diesem Kapitel lernst du, wie du eine LED richtig anschließt und sie mit dem Arduino blinken lässt.**

<div class="aufgabe">
<h3>🛠️ Aufgabe</h3>
<ul>
  <li>Baue die Schaltung nach.</li>
  <li>Teste den Code.</li>
</ul>
</div>

<a href="Grundlagen1" class="button">⬅️ Zurück</a>


**LED** bedeutet *Light Emitting Diode*. LEDs können Licht produzieren, wenn man einen Strom an sie anlegt. Dabei ist es jedoch wichtig, in welche Richtung man sie anschließt. Den Pluspol schließt man bei einer LED immer an das lange Beinchen, den Minuspol immer an das kürzere.

<p align="center">
  <img src="img/LED_plus_minus.jpg" width="300" alt="LED." style="border-radius:8px;">
</p>

<div style="background:#eef3f7; border:1px solid #ccd6dd; padding:1em; border-radius:6px; margin:1em 0;">
➕ Langes Bein = Pluspol  
➖ Kurzes Bein = Minuspol
</div>

Damit die LED nicht kaputtgeht, brauchst du einen **Widerstand**. Ein Widerstand ist ein elektrisches Bauteil, an dem Spannung abfällt. Er sorgt dafür, dass nicht zu viel Strom durch die LED fließt.

<p align="center">
  <img src="img/widerstand.jpg" width="300" alt="Widerstand." style="border-radius:8px;">
</p>

Wir bauen die Schaltung auf dem **Breadboard** auf. Das Breadboard ist der Ort, an dem Ihr Eure Schaltung aufbauen könnt. Normalerweise werden Schaltungen verlötet, damit sie lange halten. Mit einem Breadboard kann man jedoch sehr schnell Schaltungen stecken und sie auch wieder abbauen.

<p align="center">
  <img src="img/breadboard.jpg" width="300" alt="Breadboard." style="border-radius:8px;">
</p>

Mit den Kabel verbinden wir unsere Bauteile. Eine Konvention, an die wir uns halten wollen, ist: Alle Kabel, die zum Pluspol (*5V* / *D1* / etc.) führen, sind rot, alle Kabel, die zum Minuspol (*G* / *Gnd*) führen, sind schwarz.

<div style="background:#eef3f7; border:1px solid #ccd6dd; padding:1em; border-radius:6px; margin:1em 0;">
🔴 Rote Kabel verbinden den Pluspol  
⚫ Schwarze Kabel verbinden den Minuspol
</div>

<p align="center">
  <img src="img/kabel_plus_minus.jpg" width="300" alt="Kabel." style="border-radius:8px;">
</p>

Um zu wissen, wie man Bauteile verbinden soll, kann man in den Schaltplan schauen. Dieser sieht wie folgt aus:

<p align="center">
  <img src="img/Schaltung_g2.jpg" width="500" alt="Schaltplan LED." style="border-radius:8px;">
</p>

---

<div style="border:1px solid #ccd6dd; padding:1em; border-radius:6px; color:#5a3ec8;">
<h3>🛠️ Aufgabe</h3>
<ul>
  <li>Baue die Schaltung aus dem Schaltplan nach.</li>
  <li>Lade folgenden Code auf den Arduino hoch:</li>
</ul>

```cpp
#define ledPin D1

void setup() {
  pinMode(ledPin, OUTPUT);
}

void loop() {
  digitalWrite(ledPin, HIGH);
  delay(500);
  digitalWrite(ledPin, LOW);
  delay(500);
}
```

<ul>
  <li>Beobachte, was passiert. Was macht der Code?</li>
</ul>
</div>

<details>
<summary>💡 Hinweis anzeigen</summary>
<p><em>Wenn du nichts beobachten kannst, überprüfe bitte deine Schaltung.</em></p>
</details>

---

<p align="center">
  <a href="Grundlagen1">⬅️ Zurück</a> |
  <a href="Grundlagen3">➡️ Weiter</a> |
  <a href="Kapiteluebersicht">📚 Kapitelübersicht</a>
</p>
