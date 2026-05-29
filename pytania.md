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
public class Pojazd {
    protected String marka;

    public Pojazd(String marka) {
        this.marka = marka;
    }

    public void运行 uruchom() {
        System.out.println("Pojazd wystartował");
    }
}

// Klasa pochodna
public class Samochod extends Pojazd {
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
Jaki będzie wynik wykonania poniższego fragmentu kodu?

    int x = 5;
    System.out.println(x++);

- [ ] A) `5`
- [ ] B) `6`
- [ ] C) `0`
- [ ] D) Błąd kompilacji
- [ ] E) Błąd wykonania (Runtime Exception)

**Poprawna odpowiedź:** A
*Wyjaśnienie:* Użyto operatora post-inkrementacji (`x++`), co oznacza, że najpierw pobierana i wypisywana jest aktualna wartość zmiennej (`5`), a dopiero potem jest ona zwiększana w pamięci.

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
Jakie słowo kluczowe stosujemy w sygnaturze metody, aby wskazać, że nie zwraca ona żadnej wartości?
- [ ] A) `null`
- [ ] B) `empty`
- [ ] C) `void`
- [ ] D) `static`
- [ ] E) `public`

**Poprawna odpowiedź:** C
*Wyjaśnienie:* Słowo kluczowe `void` oznacza pusty typ zwracany. Metoda wykonuje operacje, ale nie zwraca niczego za pomocą instrukcji `return`.

---
