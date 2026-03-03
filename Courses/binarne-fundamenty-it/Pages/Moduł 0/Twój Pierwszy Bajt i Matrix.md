# 💥 Twój Pierwszy Bajt i Matrix

Wiesz już doskonale z poprzedniej misji, że maszyny opierają się na włączonych (1) i wyłączonych (0) przełącznikach. Rozumiesz potęgę dodawania ich wag pozycyjnych. 

Zrozum jednak pewien brutalny inżynieryjny fakt. *__Jeden bit wcale nie zmienia świata__*. Mała 1 czy 0 przekazuje nam koszmarnie mało treści. Jeśli serwer Twojej gry multiplayer prześle Ci z chmury jeden sygnał `1` – nie masz pojęcia, do czego on służy. Mówi o obrażeniach Twojej postaci? Przycisku w menu? A może to współrzędna wroga?

Z tego powodu informatycy wprowadzili standardyzację. Zaczęli grupować te mikroskopijne jednostki w bloki!

---

**Powstanie Bajta (Byte)**

Najbardziej znany logistyczny pojemnik na świecie to **BAJT** (ang. *byte*). 
**1 Bajt** w nowoczesnych maszynach pomieści w sobie dokładnie **8 bitów**. Pomyśl o tym jak o jednym wagonie w pociągu komunikacji sieciowej. Zablokowana ilość bitów (osiem zer i jedynek w paczce) to absolutny szkielet całego cyfrowego świata.

Oto przykładowy przesłany z serwera pojemnik z 8 przełącznikami:
`01000001`

Jako ludzie musielibyśmy zapamiętywać ogromne ilości tych jedynek. Czy musisz pisać je w konsoli, by przeglądać Tik-Toka? Z pomocą nadchodzą kolejne systemy kodowania liter. To mądrość dawnych programistów i konwencji takich, jak slynne **ASCII**. W tym systemie umawiamy się na twardo, że ta konkretna wyżej ułożona paczka bitów ma być dla człowieka i procesora literą `A`!

Możemy to szybko udowodnić. Zapalone wagi w `0 1 0 0  0 0 0 1` to po odpowiednio `64` oraz `1`, czyli dziesiętnie jest to `65`. Numer `65` w tabeli ASCII to wielkie A.

Twoje drugie zadanie infiltracyjne polega na wysłaniu do serwera innej wiadomości z dużego rejestru. Ustaw bajtową wielką literę `C`, na którą składają się wagi o łącznej sumie dziesiętnej `67`.

<data-gate>
  <data-number-system target="67" base="2" digits="8">

  > [!TIP]
  > **Złamany standard ASCII!** Udało Ci się zapalić układ dwóch przełączników (wagi 64, 2 oraz 1). Wynik `67` bezbłędnie przesyła do przeglądarki wielką literę `C`! Tak właśnie pisze się w chmurze!

  </data-number-system>
</data-gate>

---

<data-gate>
**Ostateczne Starcie z Systemem - Przestrzeń Wielkich Danych**
  
Złamałeś zabezpieczenia Bajta! Dostrzegasz już pewnie majestat budowy współczesnego komputera. Każdą pojedynczą literę, każdy kolor małego piksela Twojego monitora, współrzędną GPS Twojego iPhone'a przypisuje się pod matematyczne ciągi Bajtów. 
  
Z czasem te ogromne zbiory (Gigabajty to miliardy sztuk, Terabajty to biliony!) napędzają zaawansowane silniki gier czy sztuczną inteligencję w chat-botach. Ale gdzieś tam w dolinie na dysku NVME to od zawsze miliony osadzonych na sobie mikroprzełączników.

Szybki test logiczny z wiedzy o wagach oraz bitach. Skoro zapamiętałeś, że klasyczna ludzka litera z podstawowej tablicy ze znikomymi znakami specjalnymi pochłania w pamięci krągły **jeden Bajt**...
  
  <data-quiz>
    <question>
    Ile **BITÓW** sumarycznie zostało zużytych do przechowania na twardym nośniku bardzo krótkiego wyrażenia e-sportowego `"GGWP"` (Liczymy 4 bez spacji).
    </question>
    <options>
      <option>4</option>
      <option correct>32</option>
      <option>8</option>
      <option>64</option>
    </options>
  </data-quiz>
  
  <div data-hint="success">
  Bingo, potężne 32 bity! Słowo zbudowane z dokładnie 4 klasycznych znaków oznacza zużycie 4 Bajtów. Ponieważ 1 Bajt to równe 8 mniejszych bitów, wystarczy zwykłe mnożenie `4 * 8 = 32` najmniejsze stany elektryczne, by Twoje 'Good Game Well Played' dotarło do serwera meczowego!
  </div>

  <div data-hint="error">
  Pudło! Przypomnij sobie, z czego dokładnie składa się jeden Bajt. A ile znaków potrzebujesz w powyższej wiadomości? Spróbuj pomnożyć te cechy.
  </div>

Wyobraź sobie potęgę i skalę, w jakiej to wszystko ląduje w świecie Triple-A z budżetami na tekstury i mapy pochłaniającymi całe Terabajty danych. W następnych modułach będziemy programować tę studnię bez dna z zupełnie innej perspektywy. 😎
</data-gate>
