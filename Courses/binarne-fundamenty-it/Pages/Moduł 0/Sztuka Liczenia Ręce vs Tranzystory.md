# ✋ Sztuka Liczenia: Ręce vs Tranzystory

Zastanawiałeś się kiedyś, w jakim języku "myśli" Twój komputer? To nie jest magia ani sztuczna inteligencja z przyszłości. Pod maską najnowszych procesorów i kart graficznych siedzi ogromna, niewyobrażalnie szybka siatka przełączników. Mają one tylko dwa stany: **Włączony (*1*)** lub **Wyłączony (*0*)**. To fundament tzw. **Systemu Binarnego** (dwójkowego).

Zanim uznamy to za czarną magię, cofnijmy się do podstaw. Komputery nie wymyśliły liczenia od zera — w zasadzie to my, ludzie, zrobiliśmy to dawno temu, używając własnych rąk! ✋🤚

---

**Liczenie z palca wyssane** 🧠

Używamy na co dzień **systemu dziesiętnego** (decymalnego), zwanego tak ze względu na bazę równą 10. Znaki, którymi dysponujemy to 0, 1, 2, 3, 4, 5, 6, 7, 8 oraz 9. Dlaczego akurat tyle? Bo mamy 10 palców u rąk!

Spójrz na to tak: masz jedną "pozycję" na kartce. Dopóki liczysz do dziewięciu, wszystko mieści się w jednym miejscu. Ale co robisz, gdy dodajesz 1 do 9 i **brakuje Ci znaków**?
![Liczenie na palcach - wersja 1](/public/badanie_kursu/Images/palce0.png)

Dopiero wtedy "przesuwasz się" w lewo, tworzysz nową pozycję o dziesięciokrotnie większej wadze (dziesiątki), wpisujesz tam `1`, a pierwszą pozycję zerujesz. Bam, powstaje **10**.
![Liczenie na palcach - wersja 2](/public/badanie_kursu/Images/palce1.png)

---

**Świat jest pełen innych systemów!**

Zanim przejdziemy do komputera, czy wiedziałeś, że w informatyce powszechnie używa się jeszcze innych baz?
- **System Ósemkowy (Octal)**: Baza 8. Znaki od 0 do 7. Kiedyś bardzo popularny przy nadawaniu uprawnień w systemach Linux (np. `chmod 777`).
- **System Szesnastkowy (Hexadecimal / Hex)**: Baza 16. Skoro brakuje nam cyfr (mamy ich tylko od 0 do 9), po dziewiątce używamy liter: `A` (10), `B` (11), `C` (12), `D` (13), `E` (14), `F` (15). Spotkasz go dosłownie wszędzie, np. w kodach kolorów na stronach WWW (`#FF0000` to czysty czerwony!).

---

**Rozumienie Maszyny - Binarna Brama**

Wracamy do komputera. On nie ma 10 palców. Ma tylko **dwa** znaki: `0` (brak prądu) i `1` (obecność prądu). Wyczerpuje zasób cyfr po jednym mrugnięciu!
Zatem, jak po jedynce ma zapisać cyfrę `2`? Podobnie jak my przy dziesiątce: wykonuje przeniesienie w lewo, dając tam jedynkę i zerując wschodnią kolumnę.

To Twój pierwszy test w terenie. Znajdź cyfrę "DWA" dla maszyny manipulując przełącznikami:

<data-gate>
  <data-number-system target="2" base="2" digits="4">

> [!TIP]
> **Załapałeś system!** Dokładnie! Ucięcie licznika po jedynce zmusiło Cię do przeniesienia wartości na nową, lewą pozycję. Zbudowałeś `0010`. To Twoje pierwsze zakodowane logicznie `2` w pamięci komputera!

  </data-number-system>
</data-gate>

---

**Anatomia Wag, czyli jak rośnie Matrix**
  
Rewelacja, pokonałeś pierwszą bramę! Odkryłeś coś wspaniałego: system dwójkowy polega po prostu na ciągłym dodawaniu kolumn. Pamiętasz, że rozmiary pamięci RAM rosną w dziwnych wielokrotnościach: 8GB, 16GB, 32GB, 64GB? To bezpośredni wynik tych kolumn. Ich wagi rosną potęgami liczby dwa w lewo!

Zbadajmy te wagi z bliska (od prawej do lewej):
- 1 kolumna = Waga `1`
- 2 kolumna = Waga `2`
- 3 kolumna = Waga `4`
- 4 kolumna = Waga `8`

Ustawienie `1` na danej pozycji to po prostu wzięcie jej wagi do sumy, a `0` to zupełne odrzucenie wagi. Żeby zapisać liczbę `5` dziesiętnie, trzeba po prostu połączyć `4` + `1`. W systemie dwójkowym dałoby to kod `0101`!

Udowodnij teraz, że potrafisz przeliczyć te wartości we własnej głowie. Włam się do poniższego zamku, wprowadzając wartość `11`! Zastanów się, z jakich dostępnych wag (8, 4, 2, 1) to zsumujesz!

<data-gate>
  <data-number-system target="11" base="2" digits="4">

> [!TIP]
> **System złamany!** Włączyłeś pozycję 8, pozycję 2 oraz pozycję 1. Suma 8 + 2 + 1 = 11! Doskonale rozumiesz zasadę sumowania sygnałów binarnych. To właśnie w ten sposób Twoja karta graficzna i procesor przechowują wszystkie wartości we wszechświecie gier!

  </data-number-system>
</data-gate>

---

**Koniec Misji 1**
Zrozumiałeś dosłownie całą podstawę tego, jak działa mikroelektronika. Bez robienia czystej magii i bez wykręcania nowych cyfr urządzenie za pomocą zaledwie 4 wirtualnych przewodów przekazało nam masę informacji. Pora na następny etap. Skoro wiesz już jak działają wagi małego modułu, w kolejnej lekcji przeskoczymy oczko wyżej – na pokład potężnych struktur, w których zamkniemy 8 takich przewodów, tworząc **Bajty**! __*Lecimy!*__
