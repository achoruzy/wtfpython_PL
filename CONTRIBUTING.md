Wszelkie propozycje poprawek są mile widziane. Możesz nawet zasugerować jakieś zabawne i wpadające w oko tytuły dla istniejących przykładów. Celem jest stworzenie możliwie najbardziej interesującej lektury.

Jeśli jesteś zainteresowany tłumaczeniem projektu na inny język (pewni ludzie robili to już wcześniej), otwórz issue i daj znać czy potrzebujesz jakiejś pomocy.

Jeśli zmiany, które zasugerowałeś, są rozległe, będziemy wdzięczni za opisanie ich w issue przed wysłaniem. Jeśli chcesz podjąć się pracy nad zgłoszonym przez siebie issue (a mocno do tego zachęcamy), napisz to w opisie podczas tworzenia, a zostaniesz do niego przypisany.

Jeśli dodajesz nowy Przykład, otwórz issue aby go przedyskutować przed wysłaniem poprawek.

Aby dodać nowy Przykład, skorzystaj z poniższego szablonu:

<pre>
### ▶ Jakiś fancy tytuł *
Gwiazdka na końcu tytułu mówi, że Przykład nie był obecny w ostatnim releasie i został dodany niedawno.

```py
# Wprowadzenie kodu.
# Przygotowanie pod magię...
```

**Wynik (wersja Pythona):**
```py
>>> wyrażenie_uruchamiające
Prawdopodobnie nieoczekiwany wynik
```
(Opcjonalnie): Jedna linia wyjaśniająca nieoczekiwany wynik.

#### 💡 Omówienie Przykładu:
* Krótkie omówienie co i dlaczego się wydarzyło.
  ```py
  Wprowadzenie przykładów wyjaśniających (jeśli niezbędne)
  ```
  **Wynik:**
  ```py
  >>> uruchomienie # jakiegoś przykładu, który może w prosty sposób wytłumaczyć magie
  # jakiś rezultat
  ```
```
</pre>


Kilka spraw, które możesz uwzględnić podczas opisywania nowego Przykładu.

- Postaraj się być konsekwentny w nazywaniu zmiennych i nadawanych wartościach. Na przykład większość nazw zmiennych w
projekcie jest nazywana w konwencji `some_string`, `some_list`, `some_dict`, itd. Zobaczysz wiele `x`ów jak jedno-literowe
nazwy zmiennych i `"wtf"` jako wartości stringów. W projekcie wymuszamy ścisły schemat, który możesz zauważyć również w innych przykładach.
- Postaraj się być jak najbardziej kreatywny i dodać jakiś efekt "zaskoczenia" wprowadzając swój przykład. Czasem może to
oznaczać napisanie fragmentu kodu, którym rozsądny programista nie szczyciłby się na co dzień.
- No i nie zapomnij dodać siebie do [contributors list](/CONTRIBUTING.md).