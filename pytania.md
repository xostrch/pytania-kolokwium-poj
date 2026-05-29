# PYTANIE OTWARTE

Napisz klasę o nazwie Pojazd oraz klasę Samochod, która po niej dziedziczy.

## 1. Klasa Pojazd (klasa bazowa) powinna zawierać:
- pole chronione `marka` (typ tekstowy)
- konstruktor przyjmujący `marka` i ustawiający wartość pola

## 2. Klasa Samochod (klasa pochodna) powinna zawierać:
- prywatne pole `liczbaDrzwi` (typ int)
- konstruktor dwuparametrowy przyjmujący `marka` oraz `liczbaDrzwi`, konstruktor musi poprawnie wywoływać konstruktor klasy nadrzędnej
- napisaną metodę `uruchom()`, która wypisuje komunikat: „Samochod marki [nazwa_marki] wystartowal”

```java
class Pojazd {
    protected String marka;

    public Pojazd(String marka) {
        this.marka = marka;
    }

    public void uruchom() {
        System.out.println("Pojazd wystartował");
    }
}

// Klasa pochodna
class Samochod extends Pojazd {
    private int liczbaDrzwi;

    public Samochod(String marka, int liczbaDrzwi) {
        super(marka); 
        this.liczbaDrzwi = liczbaDrzwi;
    }

    @Override
    public void uruchom() {
        System.out.println("Samochód marki " + marka + " wystartował");
    }
}
```


---

# PYTANIA TESTOWE (JEDNOKROTNEGO WYBORU)

## Pytanie 1
Które z poniższych słów kluczowych w języku Java służy do uniemożliwienia dalszego dziedziczenia po danej klasie?
- [ ] A) `static`
- [ ] B) `abstract`
- [ ] C) `final`
- [ ] D) `private`
- [ ] E) `protected`

**Poprawna odpowiedź:** C
*Wyjaśnienie:* Oznaczenie klasy jako `final` sprawia, że żadna inna klasa nie może z niej dziedziczyć.

---

## Pytanie 2
Która z wymienionych klas w Javie reprezentuje niemodyfikowalny (*immutable*) ciąg znaków?
- [ ] A) `StringBuilder`
- [ ] B) `StringBuffer`
- [ ] C) `String`
- [ ] D) `CharBuffer`
- [ ] E) `ArrayList`

**Poprawna odpowiedź:** C
*Wyjaśnienie:* Obiekty klasy `String` są niemodyfikowalne. Każda operacja zmiany tekstu (np. konkatenacja) powoduje utworzenie nowego obiektu w pamięci.

---

## Pytanie 3
Które słowo kluczowe służy w Javie do wywołania konstruktora klasy nadrzędnej (superklasy)?
- [ ] A) `this`
- [ ] B) `super`
- [ ] C) `parent`
- [ ] D) `extends`
- [ ] E) `base`

**Poprawna odpowiedź:** B
*Wyjaśnienie:* Wywołanie `super()` pozwala na uruchomienie konstruktora klasy, po której bezpośrednio dziedziczymy.

---

## Pytanie 4
W jaki sposób poprawnie porównać zawartość dwóch obiektów klasy `String` pod kątem identyczności tekstowej?
- [ ] A) Używając operatora `==`
- [ ] B) Używając metody `equals()`
- [ ] C) Używając metody `compareTo()`, która zwraca wartość `boolean`
- [ ] D) Używając metody `isEqual()`
- [ ] E) Nie da się porównać zawartości obiektów `String`

**Poprawna odpowiedź:** B
*Wyjaśnienie:* Metoda `equals()` jest nadpisana w klasie `String` i porównuje łańcuchy znak po znaku. Operator `==` sprawdza jedynie, czy obie referencje wskazują na ten sam obiekt w pamięci.

---

## Pytanie 5
Który z poniższych bloków w konstrukcji `try-catch-finally` wykona się **zawsze**, niezależnie od tego, czy wyjątek został rzucony, czy nie?
- [ ] A) `try`
- [ ] B) `catch`
- [ ] C) `finally`
- [ ] D) `throws`
- [ ] E) Żaden z powyższych

**Poprawna odpowiedź:** C
*Wyjaśnienie:* Blok `finally` służy najczęściej do zamykania zasobów i gwarantuje wykonanie zawartego w nim kodu bez względu na to, czy w sekcji `try` wystąpił błąd, czy też kod wykonał się poprawnie.

---
