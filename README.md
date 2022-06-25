<p align="center"><img src="/images/logo.png" alt=""></p>
<h1 align="center">What the f*ck Python! 😱</h1>
<h3 align="center">Co do kur.. Python! 😱</h3><hr>
<p align="center">Odkrywanie i rozumienie Pythona z pomocą zaskakujących fragmentów kodu.</p>

Tłumaczenia: [Angielski English](https://github.com/satwikkansal/wtfpython) | [Chiński 中文](https://github.com/leisurelicht/wtfpython-cn) | [Dodaj tłumaczenie](https://github.com/satwikkansal/wtfpython/issues/new?title=Add%20translation%20for%20[LANGUAGE]&body=Expected%20time%20to%20finish:%20[X]%20weeks.%20I%27ll%20start%20working%20on%20it%20from%20[Y].)

Inne tryby: [Interaktywny](https://colab.research.google.com/github/satwikkansal/wtfpython/blob/3.0/irrelevant/wtf.ipynb) | [CLI](https://pypi.python.org/pypi/wtfpython)

Python, będąc wspaniale zaprojektowanym, wysoko-poziomowym, interpretowanym językiem programowania, zapewnia nam wiele funkcji zwiększających wygodę programowania. Czasami jednak, wyniki pewnych fragmentów kodu mogą okazać się niejasne na pierwszy rzut oka.

wtfpython to zabawny projekt starający się wytłumaczyć co dokładnie dzieje się pod maską Pythona podczas używania pewnych nieintuicyjnych i mniej znanych funkcji.

Podczas gdy niektóre z Przykładów, które znajdziesz poniżej, mogą nie być typowo WTF, to jednak pokazują pewne interesujące zachowania Pythona, których możesz nie znać. Uważam, że jest to dobry sposób na poznanie wnętrza języka programowania i wierzę, że Ciebie też to zainteresuje!

Jeśli jesteś zaawansowanym programistą Pythona, możesz wziąć za wyzwanie samodzielne rozwiązanie tych problemów. Może doświadczyłeś już pewnych z nich i przypomnisz sobie tamte piękne chwile! :sweat_smile:

PS: Jeśli jesteś tu po raz kolejny, o nowościach i modyfikacjach dowiesz się [stąd](https://github.com/satwikkansal/wtfpython/releases/).

No to lecimy...

# Spis treści

<!-- Generated using "markdown-toc -i README.md --maxdepth 3"-->

<!-- toc -->

- [Structure of the Examples](#structure-of-the-examples)
    + [▶ Some fancy Title](#-some-fancy-title)
- [Usage](#usage)
- [👀 Examples](#-examples)
  * [Section: Strain your brain!](#section-strain-your-brain)
    + [▶ First things first! *](#-first-things-first-)
    + [▶ Strings can be tricky sometimes](#-strings-can-be-tricky-sometimes)
    + [▶ Hash brownies](#-hash-brownies)
    + [▶ Deep down, we're all the same.](#-deep-down-were-all-the-same)
    + [▶ Disorder within order *](#-disorder-within-order-)
    + [▶ Keep trying... *](#-keep-trying-)
    + [▶ For what?](#-for-what)
    + [▶ Evaluation time discrepancy](#-evaluation-time-discrepancy)
    + [▶ How not to use `is` operator](#-how-not-to-use-is-operator)
    + [▶ `is not ...` is not `is (not ...)`](#-is-not--is-not-is-not-)
    + [▶ A tic-tac-toe where X wins in the first attempt!](#-a-tic-tac-toe-where-x-wins-in-the-first-attempt)
    + [▶ The sticky output function](#-the-sticky-output-function)
    + [▶ The chicken-egg problem *](#-the-chicken-egg-problem-)
    + [▶ Subclass relationships](#-subclass-relationships)
    + [▶ All-true-ation *](#-all-true-ation-)
    + [▶ The surprising comma](#-the-surprising-comma)
    + [▶ Strings and the backslashes](#-strings-and-the-backslashes)
    + [▶ not knot!](#-not-knot)
    + [▶ Half triple-quoted strings](#-half-triple-quoted-strings)
    + [▶ What's wrong with booleans?](#-whats-wrong-with-booleans)
    + [▶ Class attributes and instance attributes](#-class-attributes-and-instance-attributes)
    + [▶ Non-reflexive class method *](#-non-reflexive-class-method-)
    + [▶ yielding None](#-yielding-none)
    + [▶ Yielding from... return! *](#-yielding-from-return-)
    + [▶ Nan-reflexivity *](#-nan-reflexivity-)
    + [▶ Mutating the immutable!](#-mutating-the-immutable)
    + [▶ The disappearing variable from outer scope](#-the-disappearing-variable-from-outer-scope)
    + [▶ The mysterious key type conversion](#-the-mysterious-key-type-conversion)
    + [▶ Let's see if you can guess this?](#-lets-see-if-you-can-guess-this)
  * [Section: Slippery Slopes](#section-slippery-slopes)
    + [▶ Modifying a dictionary while iterating over it](#-modifying-a-dictionary-while-iterating-over-it)
    + [▶ Stubborn `del` operation](#-stubborn-del-operation)
    + [▶ The out of scope variable](#-the-out-of-scope-variable)
    + [▶ Deleting a list item while iterating](#-deleting-a-list-item-while-iterating)
    + [▶ Lossy zip of iterators *](#-lossy-zip-of-iterators-)
    + [▶ Loop variables leaking out!](#-loop-variables-leaking-out)
    + [▶ Beware of default mutable arguments!](#-beware-of-default-mutable-arguments)
    + [▶ Catching the Exceptions](#-catching-the-exceptions)
    + [▶ Same operands, different story!](#-same-operands-different-story)
    + [▶ Be careful with chained operations](#-be-careful-with-chained-operations)
    + [▶ Name resolution ignoring class scope](#-name-resolution-ignoring-class-scope)
    + [▶ Needles in a Haystack *](#-needles-in-a-haystack-)
    + [▶ Splitsies *](#-splitsies-)
    + [▶ Wild imports *](#-wild-imports-)
    + [▶ All sorted? *](#-all-sorted-)
    + [▶ Midnight time doesn't exist?](#-midnight-time-doesnt-exist)
  * [Section: The Hidden treasures!](#section-the-hidden-treasures)
    + [▶ Okay Python, Can you make me fly?](#-okay-python-can-you-make-me-fly)
    + [▶ `goto`, but why?](#-goto-but-why)
    + [▶ Brace yourself!](#-brace-yourself)
    + [▶ Let's meet Friendly Language Uncle For Life](#-lets-meet-friendly-language-uncle-for-life)
    + [▶ Even Python understands that love is complicated](#-even-python-understands-that-love-is-complicated)
    + [▶ Yes, it exists!](#-yes-it-exists)
    + [▶ Ellipsis *](#-ellipsis-)
    + [▶ Inpinity](#-inpinity)
    + [▶ Let's mangle](#-lets-mangle)
  * [Section: Appearances are deceptive!](#section-appearances-are-deceptive)
    + [▶ Skipping lines?](#-skipping-lines)
    + [▶ Teleportation](#-teleportation)
    + [▶ Well, something is fishy...](#-well-something-is-fishy)
  * [Section: Miscellaneous](#section-miscellaneous)
    + [▶ `+=` is faster](#--is-faster)
    + [▶ Let's make a giant string!](#-lets-make-a-giant-string)
    + [▶ Minor Ones *](#-minor-ones-)
- [Contributing](#contributing)
- [Acknowledgements](#acknowledgements)
- [🎓 License](#-license)
  * [Surprise your friends as well!](#surprise-your-friends-as-well)
  * [More content like this?](#more-content-like-this)

<!-- tocstop -->

# Struktura Przykładu

Wszystkie przykłady posiadają strukturę jak poniżej:

> ### ▶ Jakiś fikuśny tytuł
>
> ```py
> # Wprowadzenie kodu.
> # Przygotowanie pod magię...
> ```
>
> **Wynik (wersja lub wersje Pythona):**
>
> ```py
> >>> wyrażenie_uruchamiające
> Jakiś nieoczekiwany wynik
> ```
> (Opcjonalnie): Jedna linia wyjaśniająca nieoczekiwany wynik.
>
>
> #### 💡 Wyjaśnienie:
>
> * Krótkie omówienie co i dlaczego się wydarzyło.
> ```py
> # Wprowadzenie kodu.
> # Wprowadzenie przykładów wyjaśniających (jeśli niezbędne)
> ```
> **Wynik (wersja lub wersje Pythona):**
>
> ```py
> >>> uruchomienie # jakiegoś przykładu, który może w prosty sposób wytłumaczyć magie
>  # jakiś rezultat
> ```

**Uwaga:** Wszystkie przykłady zostały przetestowane w środowisku Python 3.5.2 interactive interpreter, i powinny działać we wszystkich wersjach Python 3, chyba że przed opisaniem wyniku stwierdzono inaczej.

# Używanie

Dobrym sposobem na wyciągnięcie jak najwięcej z poniższych przykładów, w mojej opinii, jest czytanie ich chronologicznie i dla każdego przykładu:
- Ostrożne przeczytanie kodu inicjującego przykład. Jeśli jesteś doświadczonym programistą Pythona, przez większość czasu z powodzeniem będziesz przewidywał, co się wydarzy.
- Przeczytanie wyniku i:
    + Porównanie czy wynik jest taki jak się tego spodziewałeś.
    + Upewnienie się, że rozumiesz powód, dla którego wynik jest właśnie taki.
        - Jeśli nie rozumiesz (co jest całkowicie w porządku), weź głęboki oddech i przeczytaj wyjaśnienie (a jeśli nadal nie rozumiesz, daj znać! stwórz issue [tutaj](https://github.com/satwikkansal/wtfPython)).
        - Jeśli rozumiesz, poklep się po ramieniu i kontynuuj z następnym przykładem.

PS: Możesz również czytać WTFPython z użyciem wiersza poleceń / terminala (tylko oryginalna wersja angielska) używając [paczkę pypi](https://pypi.python.org/pypi/wtfpython),
```sh
$ pip install wtfpython -U
$ wtfpython
```
---

# 👀 Przykłady

## Sekcja: Gimnastyka dla mózgu!

### ▶ Pierwsze - najważniejsze! *

<!-- Example ID: d3d73936-3cf1-4632-b5ab-817981338863 -->
<!-- read-only -->

Z jakiegoś powodu udostępniony w Python 3.8 "Walrus" operator (`:=`) stał się całkiem popularny. Sprawdźmy go!

1\.

```py
# Python version 3.8+

>>> a = "wtf_walrus"
>>> a
'wtf_walrus'

>>> a := "wtf_walrus"
File "<stdin>", line 1
    a := "wtf_walrus"
      ^
SyntaxError: invalid syntax

>>> (a := "wtf_walrus") # A tutaj działa
>>> a
'wtf_walrus'
```

2 \.

```py
# Python version 3.8+

>>> a = 6, 9
>>> a
(6, 9)

>>> (a := 6, 9)
>>> a
6

>>> a, b = 6, 9 # Typowy unpacking
>>> a, b
(6, 9)
>>> (a, b = 16, 19) # Oops
  File "<stdin>", line 1
    (a, b = 6, 9)
          ^
SyntaxError: invalid syntax

>>> (a, b := 16, 19) # Tutaj printuje dziwny 3-wartościowy tuple
(6, 16, 19)

>>> a # a nadal bez zmian?
6

>>> b
16
```



#### 💡 Wyjaśnienie

**Szybkie przypomnienie o walrus operator**

Walrus operator (`:=`) został wprowadzony w Python 3.8 i może być przydatny w sytuacjach gdy chcesz nadać wartość zmiennej wewnątrz wyrażenia.

```py
def some_func():
        # Załóżmy tutaj jakieś ciężkie obliczenia
        # time.sleep(1000)
        return 5

# Więc zamiast
if some_func():
        print(some_func()) # Co nie jest dobrą praktyką bo obliczenia dzieją się dwa razy

# lub zamiast
a = some_func()
if a:
    print(a)

# Możesz śmiało użyć
if a := some_func():
        print(a)
```

**Wynik (> 3.8):**

```py
5
5
5
```

To pozwoliło zaoszczędzić linię kodu i zapobiegło niejawnemu użyciu `some_func` drugi raz.

- Niezawarcie w nawiasach "wyrażenia przypisania" (użycia walrus operator) jest niedozwolone, stąd `SyntaxError` przy `a := "wtf_walrus"` w pierwszym fragmencie kodu. Wzięcie go w nawias zadziałało jak tego oczekiwaliśmy, przypisując wartość do zmiennej `a`.  

- Typowo, wzięcie w nawias wyrażenia zawierającego `=` jest niedozwolone. Stąd syntax error przy `(a, b = 6, 9)`. 

- Składnia Walrus operator ma formułę `NAZWA: wyrażenie`, gdzie `NAZWA` to poprawny identyfikator, a `wyrażenie` jest poprawnym wyrażeniem. Dlatego pakowanie i rozpakowywanie iterałów nie jest wspierane, co znaczy, że 

  - `(a := 6, 9)` jest tożsame z `((a := 6), 9)` jak również z `(a, 9) ` (gdzie wartość `a` to 6')

    ```py
    >>> (a := 6, 9) == ((a := 6), 9)
    True
    >>> x = (a := 696, 9)
    >>> x
    (696, 9)
    >>> x[0] is a # Oba wskazują to samo miejsce w pamięci
    True
    ```

  - Podobnie `(a, b := 16, 19)` jest tożsame z `(a, (b := 16), 19)`, które jest niczym innym jak 3-wartościowym tuplem. 

---

### ▶ Stringi bywają zdradliwe

<!-- Example ID: 30f1d3fc-e267-4b30-84ef-4d9e7091ac1a --->
1\.

```py
>>> a = "some_string"
>>> id(a)
140420665652016
>>> id("some" + "_" + "string") # Zauważ, że obydwa id są takie same.
140420665652016
```

2\.
```py
>>> a = "wtf"
>>> b = "wtf"
>>> a is b
True

>>> a = "wtf!"
>>> b = "wtf!"
>>> a is b
False

```

3\.

```py
>>> a, b = "wtf!", "wtf!"
>>> a is b # Wszystkie wersje Python oprócz 3.7.x
True

>>> a = "wtf!"; b = "wtf!"
>>> a is b # To zwróci True lub False zależnie od tego jak skrypt zostanie wywołany (python shell / ipython / jako skrypt)
False
```

```py
# Tym razen w jakimś pliku some_file.py
a = "wtf!"
b = "wtf!"
print(a is b)

# printuje True gdy ten moduł jest wywołany w innym module!
```

4\.

**Wynik (< Python3.7 )**

```py
>>> 'a' * 20 is 'aaaaaaaaaaaaaaaaaaaa'
True
>>> 'a' * 21 is 'aaaaaaaaaaaaaaaaaaaaa'
False
```

Zrozumiałe, no nie?

#### 💡 Wyjaśnienie:
+ Zachowanie w pierwszym i drugim fragmencie jest związane z optymalizacją CPython (nazywaną string interning [w polskiej wersji będę używał określenia 'odcinanie', które dobrze oddaje sens tego działania]), która stara się użyć w pewnych przypadkach istniejące niemutowalne obiekty zamiast tworzyć nowy obiekt za każdym razem.
+ Po byciu 'odciętym', wiele zmiennych odwołuje się do tego obiektu string w pamięci (oszczędzając użycie pamięci tym sposobem).
+ We fragmentach powyżej stringi są niejawnie odcinane. Decyzja o tym, kiedy niejawnie odciąć stringa jest zależna od implementacji. Są pewne zasady, które mogą pomóc w odgadnięciu czy string będzie odcięty czy nie:
    * Wszystkie stringi o ilości znaków 0 lub jeden są odcinane.
    * Stringi są odcinane w momencie kompilacji (`'wtf'` będzie odcięte ale już `''.join(['w', 't', 'f']` nie będzie)
    * Stringi, które nie są zbudowane ze znaków ASCII, cyfr lub znaków podkreślenia, nie są odcinane. To tłumaczy dlaczego `'wtf!'` nie zostało odcięte posiadając `!`. Implementacja tych zasad w CPython jest do sprawdzenia [tutaj](https://github.com/python/cpython/blob/3.6/Objects/codeobject.c#L19)
    ![image](/images/string-intern/string_intern.png)
+ Gdy do `a` i `b` jest przypisane `"wtf!"` w tym samym wierszu kodu, interpreter Pythona tworzy nowy obiekt, na który w tym samym czasie wskazuje pierwszą i drugą zmienną. Jeśli przypisania są w oddzielnych liniach, interpreter nie wie, że jest już `wtf!` jako obiekt (ponieważ `"wtf!"` nie jest niejawnie odcięty w zgodzie z faktami powyżej). Jest to optymalizacja w czasie kompilacji. Ta optymalizacja nie występuje w wersjach 3.7.x CPython (w tym [issue](https://github.com/satwikkansal/wtfpython/issues/100) znajdziesz dyskusję na ten temat).
+ Jednostka kompilująca w środowisku interaktywnym, takim jak IPython składa się z pojedynczego wyrażenia, natomiast w przypadku modułów składa się z całego modułu. `a, b = "wtf!", "wtf!"` to pojedyncze wyrażenie, podczas gdy `a = "wtf!"; b = "wtf!"` to dwa wyrażenia w jednym wierszu. To wyjaśnia, dlaczego tożsamości są różne w `a = "wtf!"; b = "wtf!"`, a także wyjaśnia, dlaczego są one takie same, gdy są wywoływane w `some_file.py`
+ Nagła zmiana wyniku czwartego fragmentu jest spowodowana techniką [peephole optimization](https://en.wikipedia.org/wiki/Peephole_optimization) znaną jako składanie stałych (Constant folding). Oznacza to, że wyrażenie `'a'*20` jest zastępowane przez `'aaaaaaaaaaaaaaaaaaa'` podczas kompilacji, aby zaoszczędzić kilka cykli zegara w czasie wykonywania. Zwijanie stałych występuje tylko w przypadku stringów o długości mniejszej niż 20. (Dlaczego? Wyobraź sobie jakiś plik `.pyc` wygenerowany jako rezultat wyrażenia `'a'*10**10`). [Tutaj](https://github.com/python/cpython/blob/3.6/Python/peephole.c#L288) znajdziesz opis implementacji tej optymalizacji.
+ Uwaga: W Python 3.7 składanie stałych zostało przeniesione z optymizatora peephole do nowego optymizatora AST z pewnymi zmianami w logice, stąd trzeci fragment nie działa dla Python 3.7. Więcej na ten temat możesz przeczytać [tutaj](https://bugs.python.org/issue11549).

---

### ▶ Ciasteczka z hashem
<!-- Example ID: eb17db53-49fd-4b61-85d6-345c5ca213ff --->
1\.
```py
some_dict = {}
some_dict[5.5] = "JavaScript"
some_dict[5.0] = "Ruby"
some_dict[5] = "Python"
```

**Wynik:**

```py
>>> some_dict[5.5]
"JavaScript"
>>> some_dict[5.0] # czy "Python" zamordował "Ruby"?
"Python"
>>> some_dict[5] 
"Python"

>>> complex_five = 5 + 0j
>>> type(complex_five)
complex
>>> some_dict[complex_five]
"Python"
```

Więc dlaczego "Python" jest w każdym z miejsc?


#### 💡 Wyjaśnienie

* Słowniki (dicty) w pythonie podczas wywoływania i przypisywania sprawdzają równość wartości i porównują wartość hasha aby stwierdzić czy klucze są tożsame.
* W pythonie niemutowalne obiekty mające tą samą wartość mają zawsze taki sam hash.
  ```py
  >>> 5 == 5.0 == 5 + 0j
  True
  >>> hash(5) == hash(5.0) == hash(5 + 0j)
  True
  ```
  **Uwaga:** Obiekty z różnymi wartościami również mogą mieć taki sam hash (jest to znane jako [hash collision](https://en.wikipedia.org/wiki/Collision_(computer_science))).

* Gdy wyrażenie `some_dict[5] = "Python"` jest wykonywane, istniejąca wartość "Ruby" jest nadpisywana przez "Python" ponieważ python rozpoznaje `5` i `5.0` jako ten sam klucz w słowniku `some_dict`.
*  [Ta odpowiedź](https://stackoverflow.com/a/32211042/4354153) na StackOverflow przedstawia racjonalne wyjaśnienie stojące za tym problemem.

---

### ▶ Bo wszyscy polacy to jedna rodzina
<!-- Example ID: 8f99a35f-1736-43e2-920d-3b78ec35da9b --->
```py
class WTF:
  pass
```

**Output:**
```py
>>> WTF() == WTF() # dwie oddzielne instancje nie mogą być równe
False
>>> WTF() is WTF() # tożsamości obiektów również są różne
False
>>> hash(WTF()) == hash(WTF()) # hashe _powinny_ być również różne
True
>>> id(WTF()) == id(WTF())
True
```

#### 💡 Wyjaśnienie:

* Gdy `id` zostało wywołane, python stworzył obiekt klasy `WTF` i podał go do funkcji `id`. Funkcja `id` użyła id obiektu (adres obiektu w pamięci), i odrzuciła sam obiekt, który został usunięty.
* Gdy zrobimy to raz za razem, python alokuje ten sam adres pamięci również do drugiego obiektu. Odkąd (w CPython) `id` używa adresu pamięci jako id obiektu, id obydwu obiektów będzie tym samym id.
* A więc id obiektu będzie unikalne tylko na czas istnienia tego obiektu. Po tym jak obiekt zostanie usunięty lub przed tym jak zostanie stworzony, inny obiekt może posiadać to id.
* ale dlaczego operator `is` zwrócił `False`? Spójrzmy na fragment kodu.

  ```py
  class WTF(object):
    def __init__(self): print("I")
    def __del__(self): print("D")
  ```

  **Wynik:**
  ```py
  >>> WTF() is WTF()
  I
  I
  D
  D
  False
  >>> id(WTF()) == id(WTF())
  I
  D
  I
  D
  True
  ```
  Jak widać, kolejność, w której obiekty są niszczone tłumaczy różnicę.

---

### ▶ Uporządkowany nieporządek *
<!-- Example ID: 91bff1f8-541d-455a-9de4-6cd8ff00ea66 --->
```py
from collections import OrderedDict

dictionary = dict()
dictionary[1] = 'a'; dictionary[2] = 'b';

ordered_dict = OrderedDict()
ordered_dict[1] = 'a'; ordered_dict[2] = 'b';

another_ordered_dict = OrderedDict()
another_ordered_dict[2] = 'b'; another_ordered_dict[1] = 'a';

class DictWithHash(dict):
    """
    Dict z implementacją magicznej metody __hash__.
    """
    __hash__ = lambda self: 0

class OrderedDictWithHash(OrderedDict):
    """
    OrderedDict z implementacją magicznej metody __hash__.
    """
    __hash__ = lambda self: 0
```

**Wynik**
```py
>>> dictionary == ordered_dict # Jeśli a == b ...
True
>>> dictionary == another_ordered_dict # ...i b == c
True
>>> ordered_dict == another_ordered_dict # ...to dlaczego nie c == a ??
False

# Wszyscy wiemy, że typ set zawiera jedynie unikalne elementy,
# spróbujmy więc stworzyć set z tych słowników i sprawdźmy co się wydarzy...

>>> len({dictionary, ordered_dict, another_ordered_dict})
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: unhashable type: 'dict'

# Ma to sens jako, że dict nie posiada implementacji metody __hash__.  
# Użyjmy naszych klas-wrapperów.
>>> dictionary = DictWithHash()
>>> dictionary[1] = 'a'; dictionary[2] = 'b';
>>> ordered_dict = OrderedDictWithHash()
>>> ordered_dict[1] = 'a'; ordered_dict[2] = 'b';
>>> another_ordered_dict = OrderedDictWithHash()
>>> another_ordered_dict[2] = 'b'; another_ordered_dict[1] = 'a';
>>> len({dictionary, ordered_dict, another_ordered_dict})
1
>>> len({ordered_dict, another_ordered_dict, dictionary}) # zmieniając kolejność
2
```

Co się tutaj odwaliło?

#### 💡 Wyjaśnienie:

- Równość pomiędzy `dictionary`, `ordered_dict` i `another_ordered_dict` nie występuje z powodu metody `__eq__` zaimplementowanej w klasie `OrderedDict`. temat do sprawdzenia [tutaj](https://docs.python.org/3/library/collections.html#ordereddict-objects)
  
    > Sprawdzenie równości obiektów OrderedDict jest wrażliwe na kolejność, ponadto będąc zaimplementowane jako `list(od1.items())==list(od2.items())`.Sprawdzenie równości pomiędzy obiektami `OrderedDict` i innymi obiektami mapującymy (Mapping objects) jest niewrażliwe na kolejność jak przy zwykłych słownikach (dict).
- Powód, dla którego taka implementacja sprawdzania równości została wprowadzona, to umożliwienie obiektom `OrderedDict` bycie bezpośrednim substytutem podstawowych obiektów `dict` tam są użyte.
- OK, ale dlaczego zmiana kolejności wpływa na wygenerowanie obiektu `set`? Odpowiedzią jest po prostu brak przenoszonej równości. Jako, że sety są "nieuporządkowanymi" kolekcjami unikalnych elementów, kolejność dodawanych elementów nie powinna mieć znaczenia. Jednak w tej sytuacji ta własność nie ma znaczenia. Sprawdźmy to.
    ```py
    >>> some_set = set()
    >>> some_set.add(dictionary) # dodajemy obiekty mapujące z fragmentów kodu wyżej
    >>> ordered_dict in some_set
    True
    >>> some_set.add(ordered_dict)
    >>> len(some_set)
    1
    >>> another_ordered_dict in some_set
    True
    >>> some_set.add(another_ordered_dict)
    >>> len(some_set)
    1

    >>> another_set = set()
    >>> another_set.add(ordered_dict)
    >>> another_ordered_dict in another_set
    False
    >>> another_set.add(another_ordered_dict)
    >>> len(another_set)
    2
    >>> dictionary in another_set
    True
    >>> another_set.add(another_ordered_dict)
    >>> len(another_set)
    2
    ```
    A więc niespójność występuje przez `another_ordered_dict in another_set` równe `False` ponieważ `ordered_dict` był już obecny w `another_set` i jak zaobserwowano wcześniej, `ordered_dict == another_ordered_dict` jest równe `False`.

---

### ▶ Próbuj, próbuj... *
<!-- Example ID: b4349443-e89f-4d25-a109-82616be9d41a --->
```py
def some_func():
    try:
        return 'from_try'
    finally:
        return 'from_finally'

def another_func(): 
    for _ in range(3):
        try:
            continue
        finally:
            print("Finally!")

def one_more_func(): # Przyłapana!
    try:
        for i in range(3):
            try:
                1 / i
            except ZeroDivisionError:
                # Wyrzućmy błąd tutaj i zajmijmy się nim na zewnątrz pętli for
                raise ZeroDivisionError("A trivial divide by zero error")
            finally:
                print("Iteration", i)
                break
    except ZeroDivisionError as e:
        print("Zero division error ocurred", e)
```

**Wynik:**

```py
>>> some_func()
'from_finally'

>>> another_func()
Finally!
Finally!
Finally!

>>> 1 / 0
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
ZeroDivisionError: division by zero

>>> one_more_func()
Iteration 0

```

#### 💡 Wyjaśnienie:

- Jeśli `return`, `break` lub `continue` są wywołane w sekcji `try` wyrażenia "try…finally", sekcja `finally` jest również wywoływana na koniec.
- Wartość zwracana jest determinowana przez ostatni wywołany `return`. Jako, że sekcja `finally` jest zawsze wywoływana, `return` wywoływany w `finally` będzie zawsze tym ostatnim.
- Ciekawostką jest, że jeśli sekcja `finally` wywołuje `return` lub `break` to tymczasowo zapamiętany wyjątek (błąd) zostaje zapomniany.

---


### ▶ For what?
<!-- Example ID: 64a9dccf-5083-4bc9-98aa-8aeecde4f210 --->
```py
some_string = "wtf"
some_dict = {}
for i, some_dict[i] in enumerate(some_string):
    i = 10
```

**Output:**
```py
>>> some_dict # Powstaje słownik z indeksami
{0: 'w', 1: 't', 2: 'f'}
```

####  💡 Wyjaśnienie:

* Wyrażenie `for` jest zdefiniowane w [Python grammar](https://docs.python.org/3/reference/grammar.html) jako:
  ```
  for_stmt: 'for' exprlist 'in' testlist ':' suite ['else' ':' suite]
  ```
  Gdzie `exprlist` to cel przypisania wartości. Oznacza to, że tożsame dla `{exprlist} = {next_value}` jest **wykonanie dla każdej wartości** w iteratorze.
  Ciekawy przykład, który to ilustruje:
  ```py
  for i in range(4):
      print(i)
      i = 10
  ```

  **Wynik:**
  ```
  0
  1
  2
  3
  ```

  Spodziewałeś się wykonania pętli tylko raz?

  **💡 Wyjaśnienie:**

    - Wyrażenie przypisania `i = 10` nigdy nie wpływa na wykonanie pętli, z uwagi na to jak działa wykonywanie pętli w Python. Przed rozpoczęciem każdej iteracji, kolejna wartość wydawana przez iterator (`range(4)` w tym przypadku) jest wypakowana i przypisana do listy zmiennych docelowych (`i` w tym przypadku).

* Funkcja `enumerate(some_string)` wydaje nową wartość `i` (licznik narastający) i literę z  `some_string` w każdej iteracji. Następnie ustawia (dopiero co przypisany) klucz `i` słownika `some_dict` do tej litery. Rozwinięcie pętli można pokazać prościej jako:
  ```py
  >>> i, some_dict[i] = (0, 'w')
  >>> i, some_dict[i] = (1, 't')
  >>> i, some_dict[i] = (2, 'f')
  >>> some_dict
  ```

---

### ▶ Rozbieżności podczas sprawdzania
<!-- Example ID: 6aa11a4b-4cf1-467a-b43a-810731517e98 --->
1\.
```py
array = [1, 8, 15]
# Typowo stworzony generator
gen = (x for x in array if array.count(x) > 0)
array = [2, 8, 22]
```

**Wynik:**

```py
>>> print(list(gen)) # Gdzie podziały się pozostałe wartości?
[8]
```

2\.

```py
array_1 = [1,2,3,4]
gen_1 = (x for x in array_1)
array_1 = [1,2,3,4,5]

array_2 = [1,2,3,4]
gen_2 = (x for x in array_2)
array_2[:] = [1,2,3,4,5]
```

**Wynik:**
```py
>>> print(list(gen_1))
[1, 2, 3, 4]

>>> print(list(gen_2))
[1, 2, 3, 4, 5]
```

3\.

```py
array_3 = [1, 2, 3]
array_4 = [10, 20, 30]
gen = (i + j for i in array_3 for j in array_4)

array_3 = [4, 5, 6]
array_4 = [400, 500, 600]
```

**Wynik:**
```py
>>> print(list(gen))
[401, 501, 601, 402, 502, 602, 403, 503, 603]
```

#### 💡 Wyjaśnienie

- W [generatorach](https://wiki.python.org/moin/Generators) człon `in` jest sprawdzany w czasie deklaracji ale człon warunkujący już podczas wykonywania.
- Przed samym wykonaniem `array` jest ponownie przypisany do listy `[2, 8, 22]`, i skoro brakuje w niej `1` i `15`, a tylko ilość `8` jest większa niż `0`, generator wydaje tylko `8`.
- Różnica pomiędzy wynikami `gen_1` i `gen_2` w drugim fragmencie wynika z tego jak zmienne `array_1` i `array_2` mają ponownie przypisywane wartości.
- W pierwszym przypadku `array_1` jest związany z nowym obiektem `[1,2,3,4,5]` i skoro `in` jest sprawdzany w czasie deklaracji to nadal odnosi się do starego obiektu `[1,2,3,4]` (który został zniszczony).
- W drugim przypadku, przypisanie części (slice) listy `array_2` aktualizuje ten stary obiekt `[1,2,3,4]` do `[1,2,3,4,5]`. Stąd oba `gen_2` i `array_2` nadal wskazują na ten sam obiekt (który został teraz zaktualizowany do `[1,2,3,4,5]`).
- OK, idąc za omawianą logiką, czy wartość `list(gen)` w trzecim fragmencie nie powinna być równa `[11, 21, 31, 12, 22, 32, 13, 23, 33]`? (skoro `array_3` i `array_4` będą się zachowywały jak `array_1`). Powód, dla którego tylko wartości z `array_4` zostały zaktualizowane znajduje się w [PEP-289](https://www.python.org/dev/peps/pep-0289/#the-details)
  
    > Tylko wyrażenie najbardziej na wierzchu (pierwsze) pętli for jest sprawdzane natychmiast, pozostałe wyrażenia są odraczane do momentu uruchomienia generatora.

---

### ▶ Jak nie używać operatora `is`
<!-- Example ID: 230fa2ac-ab36-4ad1-b675-5f5a1c1a6217 --->
Poniżej jest dobrze znany i spotykany w internecie przykład.

1\.

```py
>>> a = 256
>>> b = 256
>>> a is b
True

>>> a = 257
>>> b = 257
>>> a is b
False
```

2\.

```py
>>> a = []
>>> b = []
>>> a is b
False

>>> a = tuple()
>>> b = tuple()
>>> a is b
True
```

3\.
**Wynik**

```py
>>> a, b = 257, 257
>>> a is b
True
```

**Wynik (jedynie dla Python 3.7.x)**

```py
>>> a, b = 257, 257
>> a is b
False
```

#### 💡 Wyjaśnienie:

**Różnica pomiędzy `is` i `==`**

* `is` sprawdza czy oba argumenty wskazują na ten sam obiekt(np. sprawdza czy id argumentów jest takie samo).
* `==` sprawdza wartości argumentów i to czy są one takie same.
* Więc `is` jest do sprawdzania wskazywania tego samego obiektu a `==` do sprawdzania równowartości. Przykład by to rozjaśnić,
  ```py
  >>> class A: pass
  >>> A() is A() # Są to dwa puste obiekty trzymane w dwóch różnych miejscach w pamięci.
  False
  ```

**`256` to istniejący już obiekt, a `257` nie**

Kiedy włączasz pythona, numery od `-5` do `256` będą już alokowane. Są one bardzo często używane, stąd rozsądne jest mieć je już w pogotowiu.

Cytując z https://docs.python.org/3/c-api/long.html
> Aktualna implementacja zachowuje tablicę obiektów typu integer dla wszystkich liczb pomiędzy -5 i 256, gdy tworzysz int z tego zasięgu, po prostu odwołujesz się do istniejącego już obiektu. A więc powinna być możliwa zmiana wartości 1. Podejrzewam, że zachowanie Pythona, w tym wypadku, nie zostało zdefiniowane. :-)

```py
>>> id(256)
10922528
>>> a = 256
>>> b = 256
>>> id(a)
10922528
>>> id(b)
10922528
>>> id(257)
140084850247312
>>> x = 257
>>> y = 257
>>> id(x)
140084850247440
>>> id(y)
140084850247344
```

Interpreter nie jest tutaj wystarczająco mądry aby podczas wykonywania kodu rozpoznać przy `y = 257`, że stworzyliśmy już wcześniej int o wartości `257,` i tworzy kolejny obiekt w pamięci.

Podobna optymalizacja aplikuje się do innych **niemutowalnych** obiektów, w tym pustych tupli. Skoro listy są mutowalne, to `[] is []` zwróci `False` a `() is ()` zwróci `True`. To wyjaśnia nasz drugi fragment kodu. A teraz przejdźmy do trzeciego, 

**Oba `a` i `b` wskazują na ten sam obiekt gdy są inicjalizowane w takiej samej wartości w tym samym wierszu.**

**Wynik**

```py
>>> a, b = 257, 257
>>> id(a)
140640774013296
>>> id(b)
140640774013296
>>> a = 257
>>> b = 257
>>> id(a)
140640774013392
>>> id(b)
140640774013488
```

* Gdy do a i b zostaje przypisane `257` w tym samym wierszu, interpreter pythona tworzy nowy obiekt i przypisuje go do drugiej zmiennej w tym samym czasie. Jeśli zrobisz to w oddzielnych wersach, interpreter "nie wie", że jest już taki obiekt jak `257`.

* Jest to optymalizacja kompilatora i bezpośrednio odnosi się do interaktywnego środowiska. Jeśli wprowadzisz dwa wersy kodu do interpretera 'w locie', będą kompilowane oddzielnie, stąd też optymalizowane oddzielnie. Jeśli sp©óbujesz tego przykładu w pliku `.py`, nie zobaczysz tego samego zachowania ponieważ plik jest kompilowany w całości. Ta optymalizacja nie jest ograniczona do integerów i działa również dla innych typów niemutowalnych takich jak stringi albo floaty,

  ```py
  >>> a, b = 257.0, 257.0
  >>> a is b
  True
  ```

* Dlaczego nie działa to w Python 3.7? Ponieważ pewne optymalizacje kompilatora są zaimplementowane zależnie od pewnych zmiennych (np. wersji Pythona, systemu operacyjnego, itp.). Nadal dochodzę do tego jaka dokładnie implementacja zmieniła to zachowanie, co możesz śledzić w tym [issue](https://github.com/satwikkansal/wtfpython/issues/100).

---

### ▶ `is not ...` to nie `is (not ...)`
<!-- Example ID: b26fb1ed-0c7d-4b9c-8c6d-94a58a055c0d --->
```py
>>> 'something' is not None
True
>>> 'something' is (not None)
False
```

#### 💡 Wyjaśnienie

- `is not` to jednostkowy operator binarny, a jego zachowanie różni się od użycia `is` i `not` oddzielnie.
- `is not` zwraca `False` jeśli zmienne po obu stronach operatora wskazują ten sam obiekt, a `True` w sytuacji odwrotnej.

---

### ▶ Kółko i krzyżyk, ale X wygrywa w pierwszym podejściu!
<!-- Example ID: 69329249-bdcb-424f-bd09-cca2e6705a7a --->

```py
# Stwórzmy jeden wiersz
row = [""] * 3 #wiersz i['', '', '']
# A teraz całą planszę
board = [row] * 3
```

**Wynik:**

```py
>>> board
[['', '', ''], ['', '', ''], ['', '', '']]
>>> board[0]
['', '', '']
>>> board[0][0]
''
>>> board[0][0] = "X"
>>> board
[['X', '', ''], ['X', '', ''], ['X', '', '']]
```

Ale przecież nie przypisaliśmy trzech `"X"`, co nie?

#### 💡 Wyjaśnienie:

Ta wizualizacja przedstawia co się dzieje gdy inicjalizujemy zmienną `row`

![image](/images/tic-tac-toe/after_row_initialized.png)

A gdy `board` zostaje zainicjalizowany poprzez pomnożenie zmiennej `row`, to dzieje się wewnątrz pamięci (każdy z elementów `board[0]`, `board[1]` i `board[2]` wskazuje na tę samą listę przypisaną do zmiennej `row`)

![image](/images/tic-tac-toe/after_board_initialized.png)

Możemy uniknąć tego problemu nie używając `row` aby wygenerować `board`. (Zapytano w [tym](https://github.com/satwikkansal/wtfpython/issues/68) issue).

```py
>>> board = [['']*3 for _ in range(3)]
>>> board[0][0] = "X"
>>> board
[['X', '', ''], ['', '', ''], ['', '', '']]
```

---

### ▶ Przyczepiony wynik funkcji
<!-- Example ID: 4dc42f77-94cb-4eb5-a120-8203d3ed7604 --->

1\.

```py
funcs = []
results = []
for x in range(7):
    def some_func():
        return x
    funcs.append(some_func)
    results.append(some_func())  # zauważ, że wywołujemy tu funkcję

funcs_results = [func() for func in funcs]
```

**Wynik:**

```py
>>> results
[0, 1, 2, 3, 4, 5, 6]
>>> funcs_results
[6, 6, 6, 6, 6, 6, 6]
```
Pomimo, że wartości zmiennej `x` były różne w każdej iteracji przed dodaniem `some_func` do `funcs`, wszystkie funkcje zwróciły 6.

2\.

```py
>>> powers_of_x = [lambda x: x**i for i in range(10)]
>>> [f(2) for f in powers_of_x]
[512, 512, 512, 512, 512, 512, 512, 512, 512, 512]
```

#### 💡 Wyjaśnienie

- Kiedy definiujemy wewnątrz pętli funkcję, która używa zmiennych pętli, obliczenie tej funkcji (stworzonej wewnątrz pętli) jest powiązane ze zmienną, a nie z jej wartością. Stąd wszystkie funkcje używają do obliczeń ostatniej wartości przypisanej do tej zmiennej.

- Aby zachowanie było zgodne z oczekiwanym, wystarczy użyć zmiennej z pętli jako parametru dla funkcji. **Dlaczego to zadziała?** Ponieważ zdefiniuje to zmnienną ponownie w zakresie funkcji.

    ```py
    funcs = []
    for x in range(7):
        def some_func(x=x):
            return x
        funcs.append(some_func)
    ```

    **Wynik:**
    ```py
    >>> funcs_results = [func() for func in funcs]
    >>> funcs_results
    [0, 1, 2, 3, 4, 5, 6]
    ```

---

### ▶ Jajko czy kura *
<!-- Example ID: 60730dc2-0d79-4416-8568-2a63323b3ce8 --->
1\.
```py
>>> isinstance(3, int)
True
>>> isinstance(type, object)
True
>>> isinstance(object, type)
True
```

Więc, która z klas jest tą "ostateczną" klasą bazową? Tu mamy więcej niezrozumiałych rzeczy,

2\. 

```py
>>> class A: pass
>>> isinstance(A, A)
False
>>> isinstance(type, type)
True
>>> isinstance(object, object)
True
```

3\.

```py
>>> issubclass(int, object)
True
>>> issubclass(type, object)
True
>>> issubclass(object, type)
False
```


#### 💡 Wyjaśnienie

- `type` to  [metaklasa](https://realpython.com/python-metaclasses/) w Pythonie.
- **Wszystko** jest `object` (obiektem) w Pythonie, włącznie z klasami i ich obiektami (instancjami).
- klasa `type` jest metaklasą klasy `object`, a każda klasa (włączając `type`) dziedziczy bezpośrednio lub pośrednio po `object`.
- Nie można wskazać jasno klasy bazowej pomiędzy `object` i `type`. Niejasność z powyższych fragmentów kodu bierze się z tego, że postrzegamy te relacje (`issubclass` i `isinstance`) w kontekście klas Pythona. Relacja pomiędzy `object` i `type` nie może zostać zreprodukowana w czystym pythonie. Dla doprecyzowania, następujące relacje nie mogą zostać odtworzone w czystym pythonie,
    + klasa A jest instancją klasy B, a klasa B jest instancją klasy A.
    + klasa A jest instancją samej siebie.
- Relacje pomiędzy `object` i `type` (gdzie obie są instancjami tej drugiej, a przy tym też samej siebie) występuje w Pythonnie przez "oszukiwanie" na poziomie implementacji języka.

---

### ▶ Relacje podklas
<!-- Example ID: 9f6d8cf0-e1b5-42d0-84a0-4cfab25a0bc0 --->
**Output:**
```py
>>> from collections import Hashable
>>> issubclass(list, object)
True
>>> issubclass(object, Hashable)
True
>>> issubclass(list, Hashable)
False
```

Spodziewali byśmy się, że powiązania będą przechodziły, prawda? (np., jeśli `A` jest subklasą `B`, i `B` jest subklasą `C` to `A` _powinno być_ subklasą `C`)

#### 💡 Wyjaśnienie:

* Relacje subklas nie koniecznie przechodzą w Pythonie. Każdy może zdefiniować swoje własne sprawdzenie `__subclasscheck__` w metaklasie.
* Gdy `issubclass(cls, Hashable)` jest wywołana, po prostu szuka nie-Falsującą metodę "`__hash__`" w `cls` lub w czymkolwiek z czego ona dziedziczy.
* Jako, że `object` jest hashowalny, a `list` nie jest hashowalna, psuje to przechodzenie w relacji.
* Bardziej dokładne wytłumaczenie znajduje się [tutaj](https://www.naftaliharris.com/blog/python-subclass-intransitivity/).

---

### ▶ Wszytko tru(e)je *

<!-- Example ID: dfe6d845-e452-48fe-a2da-0ed3869a8042 -->

```py
>>> all([True, True, True])
True
>>> all([True, True, False])
False

>>> all([])
True
>>> all([[]])
False
>>> all([[[]]])
True
```

Skąd się bierze ta różnica True-False?

#### 💡 Wyjaśnienie:

- Implementacja funkcji `all` jest tożsama z

- ```py
  def all(iterable):
      for element in iterable:
          if not element:
              return False
      return True
  ```

- `all([])` zwraca `True` bo iterator jest pusty. 
- `all([[]])` zwraca `False` ponieważ `not []` to `True` a więc jest tożsame z `not False` jako, że lista wewnątrz iteratora jest pusta.
- `all([[[]]])` i wyższe warianty będą zawsze `True` jako, że `not [[]]`, `not [[[]]]` itd. są tożsame z `not True`.

---

### ▶ Zaskakujący przecinek
<!-- Example ID: 31a819c8-ed73-4dcc-84eb-91bedbb51e58 --->
**Wynik (< 3.6):**

```py
>>> def f(x, y,):
...     print(x, y)
...
>>> def g(x=4, y=5,):
...     print(x, y)
...
>>> def h(x, **kwargs,):
  File "<stdin>", line 1
    def h(x, **kwargs,):
                     ^
SyntaxError: invalid syntax

>>> def h(*args,):
  File "<stdin>", line 1
    def h(*args,):
                ^
SyntaxError: invalid syntax
```

#### 💡 Wyjaśnienie:

- Przecinek na końcu nie zawsze jest dozwolony w formalnej liście parametrów funkcji Pythona.
-  W Pythonie lista argumentów jest częściowo zdefiniowana z przecinkami wiodącymi, a częściowo z przecinkami końcowymi. Ten konflikt powoduje sytuacje, w których przecinek jest uwięziony w środku i żadna reguła go nie akceptuje.
-  **Uwaga:** Problem przecinka końcowego [naprawiono w Python 3.6](https://bugs.python.org/issue9232). Uwagi w [tym miejscu](https://bugs.python.org/issue9232#msg248399) w skrócie omawiają różne zastosowania przecinków końcowych w Pythonie.

---

### ▶ Stringi i backslashe
<!-- Example ID: 6ae622c3-6d99-4041-9b33-507bd1a4407b --->
**Wynik:**
```py
>>> print("\"")
"

>>> print(r"\"")
\"

>>> print(r"\")
File "<stdin>", line 1
    print(r"\")
              ^
SyntaxError: EOL while scanning string literal

>>> r'\'' == "\\'"
True
```

#### 💡 Wyjaśnienie

- W typowym stringu pythona, backslash używany jest jako dzika karta dla znaków o specjalnym użyciu w pythonie (jak pojedynczy cudzysłów, cudzysłów, i sam backslash).
    ```py
    >>> 'wt\"f'
    'wt"f'
    ```
- W 'surowym' (raw) stringu (na co wskazuje przedrostek `r`), backslashe przechodzą same, a przy tym są też dziką kartą dla kolejnego znaku.
    ```py
    >>> r'wt\"f' == 'wt\\"f'
    True
    >>> print(repr(r'wt\"f')
    'wt\\"f'

    >>> print("\n")

    >>> print(r"\\n")
    '\\\\n'
    ```
— Oznacza to, że gdy parser napotka backslash w surowym stringu, oczekuje kolejnego znaku następującego po nim. W naszym przypadku (`print(r"\")`), backslash był dziką kartą dla końcowego cudzysłowu, pozostawiając parser bez zamykającego cudzysłowu (stąd `SyntaxError`). Dlatego odwrotne ukośniki nie działają na końcu surowego stringa.

---

### ▶ not knot!
<!-- Example ID: 7034deb1-7443-417d-94ee-29a800524de8 --->
```py
x = True
y = False
```

**Wynik:**
```py
>>> not x == y
True
>>> x == not y
  File "<input>", line 1
    x == not y
           ^
SyntaxError: invalid syntax
```

#### 💡 Wyjaśnienie:

* Pierwszeństwo operatorów wpływa na to jak wyrażenie jest wykonywane, a `==` ma wyższe pierwszeństwo niż operator `not` w Pythonie.
* Stąd `not x == y` jest tożsame z `not (x == y)`, które jest tożsame z `not (True == False)` ostatecznie zwracające `True`.
* Jednak `x == not y` podnosi `SyntaxError` ponieważ wyrażenie jest tożsame z `(x == not) y` a nie `x == (not y)`, czego można nie przewidzieć na pierwszy rzut oka.
* Parser spodziewa się słowa `not` jako części operatora `not in` (ponieważ oba operatory `==` i `not in` mają ten sam poziom pierwszeństwa), jednak nie mogąc znaleźć słowa `in` za słowem `not` podnosi błąd `SyntaxError`.

---

### ▶ Potrójne cudzysłowy
<!-- Example ID: c55da3e2-1034-43b9-abeb-a7a970a2ad9e --->
**Wynik:**
```py
>>> print('wtfpython''')
wtfpython
>>> print("wtfpython""")
wtfpython
>>> # The following statements raise `SyntaxError`
>>> # print('''wtfpython')
>>> # print("""wtfpython")
  File "<input>", line 3
    print("""wtfpython")
                        ^
SyntaxError: EOF while scanning triple-quoted string literal
```

#### 💡 Wyjaśnienie:
+ Python wspiera wewnętrzną [konkatenacje stringów](https://docs.python.org/2/reference/lexical_analysis.html#string-literal-concatenation), Przykład,
  ```
  >>> print("wtf" "python")
  wtfpython
  >>> print("wtf" "") # or "wtf"""
  wtf
  ```
+ `'''` i `"""` to również ograniczniki stringów w Pythonie (patrz docstring), co powoduje wystąpienie błędu składni ponieważ interpreter Pythona skanując kolejne znaki (uznając je za wnętrze stringa) oczekuje kolejnego potrójnego cudzysłowu jako ogranicznika zamykającego, którego nie znajduje.

---

### ▶ Co jest nie tak z boolami?
<!-- Example ID: 0bba5fa7-9e6d-4cd2-8b94-952d061af5dd --->
1\.

```py
# Prosty przykład zliczania ilości booli i
# integerów w iteratorze z różnymi typami danych.
mixed_list = [False, 1.0, "some_string", 3, True, [], False]
integers_found_so_far = 0
booleans_found_so_far = 0

for item in mixed_list:
    if isinstance(item, int):
        integers_found_so_far += 1
    elif isinstance(item, bool):
        booleans_found_so_far += 1
```

**Wynik:**
```py
>>> integers_found_so_far
4
>>> booleans_found_so_far
0
```


2\.
```py
>>> some_bool = True
>>> "wtf" * some_bool
'wtf'
>>> some_bool = False
>>> "wtf" * some_bool
''
```

3\.

```py
def tell_truth():
    True = False
    if True == False:
        print("I have lost faith in truth!")
```

**Wynik (< 3.x):**

```py
>>> tell_truth()
I have lost faith in truth!
```



#### 💡 Wyjaśnienie:

* `bool` jest podklasą `int` w Pythonie
    
    ```py
    >>> issubclass(bool, int)
    True
    >>> issubclass(int, bool)
    False
    ```
    
* stąd, `True` i `False` są instancjami `int`
  ```py
  >>> isinstance(True, int)
  True
  >>> isinstance(False, int)
  True
  ```

* wartość integera `True` to `1` a `False` to `0`.
  ```py
  >>> int(True)
  1
  >>> int(False)
  0
  ```

* Zerknij na pytanie na [StackOverflow](https://stackoverflow.com/a/8169049/4354153), które to wyjaśnia.

* Początkowo Python nie posiadał typu `bool` (używano 0 zamiast false i wartości niezerowej, przykładowo 1, dla true).  `True`, `False`, i typ `bool` zostały dodane w wersji 2.x, ale dla kompatybilności wstecznej, `True` i `False` nie mogły zostać stworzone jako stałe. Były więc wbudowanymi zmiennymi, co pozwoliło na zmiany przypisania do zmiennych.

* Python 3 jest niekompatybilny wstecz. Problem został ostatecznie naprawiony. Stąd też ostatni fragment kodu nie zadziała w Python 3.x!

---

### ▶ Atrybuty klas i atrybuty instancji
<!-- Example ID: 6f332208-33bd-482d-8106-42863b739ed9 --->
1\.
```py
class A:
    x = 1

class B(A):
    pass

class C(A):
    pass
```

**Wynik:**
```py
>>> A.x, B.x, C.x
(1, 1, 1)
>>> B.x = 2
>>> A.x, B.x, C.x
(1, 2, 1)
>>> A.x = 3
>>> A.x, B.x, C.x # C.x zmieniono ale już B.x nie
(3, 2, 3)
>>> a = A()
>>> a.x, A.x
(3, 3)
>>> a.x += 1
>>> a.x, A.x
(4, 3)
```

2\.
```py
class SomeClass:
    some_var = 15
    some_list = [5]
    another_list = [5]
    def __init__(self, x):
        self.some_var = x + 1
        self.some_list = self.some_list + [x]
        self.another_list += [x]
```

**Wynik:**

```py
>>> some_obj = SomeClass(420)
>>> some_obj.some_list
[5, 420]
>>> some_obj.another_list
[5, 420]
>>> another_obj = SomeClass(111)
>>> another_obj.some_list
[5, 111]
>>> another_obj.another_list
[5, 420, 111]
>>> another_obj.another_list is SomeClass.another_list
True
>>> another_obj.another_list is some_obj.another_list
True
```

#### 💡 Wyjaśnienie:

* Zmienne klasowe i zmienne instancji klas są trzymane wewnętrznie w obiektach klas w słownikach (dict). Jeśli nazwa zmiennej nie zostanie znaleziona w słowniku aktualnej klasy, superklasy są przeszukiwane w następnej kolejności.
* Operator `+=` modyfikuje mutowalny obiekt w miejscu bez tworzenia nowego obiektu. Stąd modyfikacja atrybutu instancji wpływa na inne instancje i atrybuty samej klasy.

---

### ▶ Non-reflexive class method *

<!-- Example ID: 3649771a-f733-413c-8060-3f9f167b83fd -->

```py
class SomeClass:
        def instance_method(self):
                pass
        
        @classmethod
        def class_method(cls):
                pass
```

**Output:**

```py
>>> SomeClass.instance_method is SomeClass.instance_method
True
>>> SomeClass.class_method is SomeClass.class_method
False
>>> id(SomeClass.class_method) == id(SomeClass.class_method)
True
```

#### 💡 Explanation:

- The reason `SomeClass.class_method is SomeClass.class_method` is `False` is due to the `@classmethod` decorator. 

  ```py
  >>> SomeClass.instance_method
  <function __main__.SomeClass.instance_method(self)>
  >>> SomeClass.class_method
  <bound method SomeClass.class_method of <class '__main__.SomeClass'>
  ```

  A new bound method every time `SomeClass.class_method` is accessed.

-  `id(SomeClass.class_method) == id(SomeClass.class_method)` returned `True` because the second allocation of memory for `class_method` happened at the same location of first deallocation (See Deep Down, we're all the same example for more detailed explanation). 

---


### ▶ yielding None
<!-- Example ID: 5a40c241-2c30-40d0-8ba9-cf7e097b3b53 --->
```py
some_iterable = ('a', 'b')

def some_func(val):
    return "something"
```

**Output (<= 3.7.x):**

```py
>>> [x for x in some_iterable]
['a', 'b']
>>> [(yield x) for x in some_iterable]
<generator object <listcomp> at 0x7f70b0a4ad58>
>>> list([(yield x) for x in some_iterable])
['a', 'b']
>>> list((yield x) for x in some_iterable)
['a', None, 'b', None]
>>> list(some_func((yield x)) for x in some_iterable)
['a', 'something', 'b', 'something']
```

#### 💡 Explanation:
- This is a bug in CPython's handling of `yield` in generators and comprehensions.
- Source and explanation can be found here: https://stackoverflow.com/questions/32139885/yield-in-list-comprehensions-and-generator-expressions
- Related bug report: http://bugs.python.org/issue10544
- Python 3.8+ no longer allows `yield` inside list comprehension and will throw a `SyntaxError`.

---


### ▶ Yielding from... return! *
<!-- Example ID: 5626d8ef-8802-49c2-adbc-7cda5c550816 --->
1\.

```py
def some_func(x):
    if x == 3:
        return ["wtf"]
    else:
        yield from range(x)
```

**Output (> 3.3):**

```py
>>> list(some_func(3))
[]
```

Where did the `"wtf"` go? Is it due to some special effect of `yield from`? Let's validate that,

2\.

```py
def some_func(x):
    if x == 3:
        return ["wtf"]
    else:
        for i in range(x):
          yield i
```

**Output:**

```py
>>> list(some_func(3))
[]
```

The same result, this didn't work either.

#### 💡 Explanation:

+ From Python 3.3 onwards, it became possible to use `return` statement with values inside generators (See [PEP380](https://www.python.org/dev/peps/pep-0380/)). The [official docs](https://www.python.org/dev/peps/pep-0380/#enhancements-to-stopiteration) say that,

> "... `return expr` in a generator causes `StopIteration(expr)` to be raised upon exit from the generator."

+ In the case of `some_func(3)`, `StopIteration` is raised at the beginning because of `return` statement. The `StopIteration` exception is automatically caught inside the `list(...)` wrapper and the `for` loop. Therefore, the above two snippets result in an empty list.

+ To get `["wtf"]` from the generator `some_func` we need to catch the `StopIteration` exception,

  ```py
  try:
      next(some_func(3))
  except StopIteration as e:
      some_string = e.value
  ```

  ```py
  >>> some_string
  ["wtf"]
  ```

---

### ▶ Nan-reflexivity *

<!-- Example ID: 59bee91a-36e0-47a4-8c7d-aa89bf1d3976 --->

1\.

```py
a = float('inf')
b = float('nan')
c = float('-iNf')  # These strings are case-insensitive
d = float('nan')
```

**Output:**

```py
>>> a
inf
>>> b
nan
>>> c
-inf
>>> float('some_other_string')
ValueError: could not convert string to float: some_other_string
>>> a == -c # inf==inf
True
>>> None == None # None == None
True
>>> b == d # but nan!=nan
False
>>> 50 / a
0.0
>>> a / a
nan
>>> 23 + b
nan
```

2\.

```py
>>> x = float('nan')
>>> y = x / x
>>> y is y # identity holds
True
>>> y == y # equality fails of y
False
>>> [y] == [y] # but the equality succeeds for the list containing y
True
```



#### 💡 Explanation:

- `'inf'` and `'nan'` are special strings (case-insensitive), which, when explicitly typecast-ed to `float` type, are used to represent mathematical "infinity" and "not a number" respectively.

- Since according to IEEE standards ` NaN != NaN`, obeying this rule breaks the reflexivity assumption of a collection element in Python i.e. if `x` is a part of a collection like `list`, the implementations like comparison are based on the assumption that `x == x`.  Because of this assumption, the identity is compared first (since it's faster) while comparing two elements, and the values are compared only when the identities mismatch. The following snippet will make things clearer,

  ```py
  >>> x = float('nan')
  >>> x == x, [x] == [x]
  (False, True)
  >>> y = float('nan')
  >>> y == y, [y] == [y]
  (False, True)
  >>> x == y, [x] == [y]
  (False, False)
  ```

  Since the identities of `x` and `y` are different, the values are considered, which are also different; hence the comparison returns `False` this time.

- Interesting read: [Reflexivity, and other pillars of civilization](https://bertrandmeyer.com/2010/02/06/reflexivity-and-other-pillars-of-civilization/)

---

### ▶ Mutating the immutable!

<!-- Example ID: 15a9e782-1695-43ea-817a-a9208f6bb33d --->

This might seem trivial if you know how references work in Python.

```py
some_tuple = ("A", "tuple", "with", "values")
another_tuple = ([1, 2], [3, 4], [5, 6])
```

**Output:**
```py
>>> some_tuple[2] = "change this"
TypeError: 'tuple' object does not support item assignment
>>> another_tuple[2].append(1000) #This throws no error
>>> another_tuple
([1, 2], [3, 4], [5, 6, 1000])
>>> another_tuple[2] += [99, 999]
TypeError: 'tuple' object does not support item assignment
>>> another_tuple
([1, 2], [3, 4], [5, 6, 1000, 99, 999])
```

But I thought tuples were immutable...

#### 💡 Explanation:

* Quoting from https://docs.python.org/2/reference/datamodel.html

    > Immutable sequences
        An object of an immutable sequence type cannot change once it is created. (If the object contains references to other objects, these other objects may be mutable and may be modified; however, the collection of objects directly referenced by an immutable object cannot change.)

* `+=` operator changes the list in-place. The item assignment doesn't work, but when the exception occurs, the item has already been changed in place.

---

### ▶ The disappearing variable from outer scope
<!-- Example ID: 7f1e71b6-cb3e-44fb-aa47-87ef1b7decc8 --->

```py
e = 7
try:
    raise Exception()
except Exception as e:
    pass
```

**Output (Python 2.x):**
```py
>>> print(e)
# prints nothing
```

**Output (Python 3.x):**
```py
>>> print(e)
NameError: name 'e' is not defined
```

#### 💡 Explanation:

* Source: https://docs.python.org/3/reference/compound_stmts.html#except

  When an exception has been assigned using `as` target, it is cleared at the end of the `except` clause. This is as if

  ```py
  except E as N:
      foo
  ```

  was translated into

  ```py
  except E as N:
      try:
          foo
      finally:
          del N
  ```

  This means the exception must be assigned to a different name to be able to refer to it after the except clause. Exceptions are cleared because, with the traceback attached to them, they form a reference cycle with the stack frame, keeping all locals in that frame alive until the next garbage collection occurs.

* The clauses are not scoped in Python. Everything in the example is present in the same scope, and the variable `e` got removed due to the execution of the `except` clause. The same is not the case with functions that have their separate inner-scopes. The example below illustrates this:

     ```py
     def f(x):
         del(x)
         print(x)

     x = 5
     y = [5, 4, 3]
     ```

     **Output:**
     ```py
     >>>f(x)
     UnboundLocalError: local variable 'x' referenced before assignment
     >>>f(y)
     UnboundLocalError: local variable 'x' referenced before assignment
     >>> x
     5
     >>> y
     [5, 4, 3]
     ```

* In Python 2.x, the variable name `e` gets assigned to `Exception()` instance, so when you try to print, it prints nothing.

    **Output (Python 2.x):**
    ```py
    >>> e
    Exception()
    >>> print e
    # Nothing is printed!
    ```

---


### ▶ The mysterious key type conversion
<!-- Example ID: 00f42dd0-b9ef-408d-9e39-1bc209ce3f36 --->
```py
class SomeClass(str):
    pass

some_dict = {'s': 42}
```

**Output:**
```py
>>> type(list(some_dict.keys())[0])
str
>>> s = SomeClass('s')
>>> some_dict[s] = 40
>>> some_dict # expected: Two different keys-value pairs
{'s': 40}
>>> type(list(some_dict.keys())[0])
str
```

#### 💡 Explanation:

* Both the object `s` and the string `"s"` hash to the same value because `SomeClass` inherits the `__hash__` method of `str` class.
* `SomeClass("s") == "s"` evaluates to `True` because `SomeClass` also inherits `__eq__` method from `str` class.
* Since both the objects hash to the same value and are equal, they are represented by the same key in the dictionary.
* For the desired behavior, we can redefine the `__eq__` method in `SomeClass`
  ```py
  class SomeClass(str):
    def __eq__(self, other):
        return (
            type(self) is SomeClass
            and type(other) is SomeClass
            and super().__eq__(other)
        )

    # When we define a custom __eq__, Python stops automatically inheriting the
    # __hash__ method, so we need to define it as well
    __hash__ = str.__hash__

  some_dict = {'s':42}
  ```

  **Output:**
  ```py
  >>> s = SomeClass('s')
  >>> some_dict[s] = 40
  >>> some_dict
  {'s': 40, 's': 42}
  >>> keys = list(some_dict.keys())
  >>> type(keys[0]), type(keys[1])
  (__main__.SomeClass, str)
  ```

---

### ▶ Let's see if you can guess this?
<!-- Example ID: 81aa9fbe-bd63-4283-b56d-6fdd14c9105e --->
```py
a, b = a[b] = {}, 5
```

**Output:**
```py
>>> a
{5: ({...}, 5)}
```

#### 💡 Explanation:

* According to [Python language reference](https://docs.python.org/2/reference/simple_stmts.html#assignment-statements), assignment statements have the form
  ```
  (target_list "=")+ (expression_list | yield_expression)
  ```
  and
  
> An assignment statement evaluates the expression list (remember that this can be a single expression or a comma-separated list, the latter yielding a tuple) and assigns the single resulting object to each of the target lists, from left to right.

* The `+` in `(target_list "=")+` means there can be **one or more** target lists. In this case, target lists are `a, b` and `a[b]` (note the expression list is exactly one, which in our case is `{}, 5`).

* After the expression list is evaluated, its value is unpacked to the target lists from **left to right**. So, in our case, first the `{}, 5` tuple is unpacked to `a, b` and we now have `a = {}` and `b = 5`.

* `a` is now assigned to `{}`, which is a mutable object.

* The second target list is `a[b]` (you may expect this to throw an error because both `a` and `b` have not been defined in the statements before. But remember, we just assigned `a` to `{}` and `b` to `5`).

* Now, we are setting the key `5` in the dictionary to the tuple `({}, 5)` creating a circular reference (the `{...}` in the output refers to the same object that `a` is already referencing). Another simpler example of circular reference could be
  ```py
  >>> some_list = some_list[0] = [0]
  >>> some_list
  [[...]]
  >>> some_list[0]
  [[...]]
  >>> some_list is some_list[0]
  True
  >>> some_list[0][0][0][0][0][0] == some_list
  True
  ```
  Similar is the case in our example (`a[b][0]` is the same object as `a`)

* So to sum it up, you can break the example down to
  ```py
  a, b = {}, 5
  a[b] = a, b
  ```
  And the circular reference can be justified by the fact that `a[b][0]` is the same object as `a`
  ```py
  >>> a[b][0] is a
  True
  ```

---
---

## Section: Slippery Slopes

### ▶ Modifying a dictionary while iterating over it
<!-- Example ID: b4e5cdfb-c3a8-4112-bd38-e2356d801c41 --->
```py
x = {0: None}

for i in x:
    del x[i]
    x[i+1] = None
    print(i)
```

**Output (Python 2.7- Python 3.5):**

```
0
1
2
3
4
5
6
7
```

Yes, it runs for exactly **eight** times and stops.

#### 💡 Explanation:

* Iteration over a dictionary that you edit at the same time is not supported.
* It runs eight times because that's the point at which the dictionary resizes to hold more keys (we have eight deletion entries, so a resize is needed). This is actually an implementation detail.
* How deleted keys are handled and when the resize occurs might be different for different Python implementations.
* So for Python versions other than Python 2.7 - Python 3.5, the count might be different from 8 (but whatever the count is, it's going to be the same every time you run it). You can find some discussion around this [here](https://github.com/satwikkansal/wtfpython/issues/53) or in [this](https://stackoverflow.com/questions/44763802/bug-in-python-dict) StackOverflow thread.
* Python 3.8 onwards, you'll see `RuntimeError: dictionary keys changed during iteration` exception if you try to do this.

---

### ▶ Stubborn `del` operation
<!-- Example ID: 777ed4fd-3a2d-466f-95e7-c4058e61d78e --->
<!-- read-only -->

```py
class SomeClass:
    def __del__(self):
        print("Deleted!")
```

**Output:**
1\.
```py
>>> x = SomeClass()
>>> y = x
>>> del x # this should print "Deleted!"
>>> del y
Deleted!
```

Phew, deleted at last. You might have guessed what saved from `__del__` being called in our first attempt to delete `x`. Let's add more twists to the example.

2\.
```py
>>> x = SomeClass()
>>> y = x
>>> del x
>>> y # check if y exists
<__main__.SomeClass instance at 0x7f98a1a67fc8>
>>> del y # Like previously, this should print "Deleted!"
>>> globals() # oh, it didn't. Let's check all our global variables and confirm
Deleted!
{'__builtins__': <module '__builtin__' (built-in)>, 'SomeClass': <class __main__.SomeClass at 0x7f98a1a5f668>, '__package__': None, '__name__': '__main__', '__doc__': None}
```

Okay, now it's deleted :confused:

#### 💡 Explanation:
+ `del x` doesn’t directly call `x.__del__()`.
+ Whenever `del x` is encountered, Python decrements the reference count for `x` by one, and `x.__del__()` when x’s reference count reaches zero.
+ In the second output snippet, `y.__del__()` was not called because the previous statement (`>>> y`) in the interactive interpreter created another reference to the same object, thus preventing the reference count from reaching zero when `del y` was encountered.
+ Calling `globals` caused the existing reference to be destroyed, and hence we can see "Deleted!" being printed (finally!).

---

### ▶ The out of scope variable
<!-- Example ID: 75c03015-7be9-4289-9e22-4f5fdda056f7 --->
```py
a = 1
def some_func():
    return a

def another_func():
    a += 1
    return a
```

**Output:**
```py
>>> some_func()
1
>>> another_func()
UnboundLocalError: local variable 'a' referenced before assignment
```

#### 💡 Explanation:
* When you make an assignment to a variable in scope, it becomes local to that scope. So `a` becomes local to the scope of `another_func`,  but it has not been initialized previously in the same scope, which throws an error.
* Read [this](http://sebastianraschka.com/Articles/2014_python_scope_and_namespaces.html) short but an awesome guide to learn more about how namespaces and scope resolution works in Python.
* To modify the outer scope variable `a` in `another_func`, use `global` keyword.
  ```py
  def another_func()
      global a
      a += 1
      return a
  ```

  **Output:**
  ```py
  >>> another_func()
  2
  ```

---

### ▶ Deleting a list item while iterating
<!-- Example ID: 4cc52d4e-d42b-4e09-b25f-fbf5699b7d4e --->
```py
list_1 = [1, 2, 3, 4]
list_2 = [1, 2, 3, 4]
list_3 = [1, 2, 3, 4]
list_4 = [1, 2, 3, 4]

for idx, item in enumerate(list_1):
    del item

for idx, item in enumerate(list_2):
    list_2.remove(item)

for idx, item in enumerate(list_3[:]):
    list_3.remove(item)

for idx, item in enumerate(list_4):
    list_4.pop(idx)
```

**Output:**
```py
>>> list_1
[1, 2, 3, 4]
>>> list_2
[2, 4]
>>> list_3
[]
>>> list_4
[2, 4]
```

Can you guess why the output is `[2, 4]`?

#### 💡 Explanation:

* It's never a good idea to change the object you're iterating over. The correct way to do so is to iterate over a copy of the object instead, and `list_3[:]` does just that.

     ```py
     >>> some_list = [1, 2, 3, 4]
     >>> id(some_list)
     139798789457608
     >>> id(some_list[:]) # Notice that python creates new object for sliced list.
     139798779601192
     ```

**Difference between `del`, `remove`, and `pop`:**
* `del var_name` just removes the binding of the `var_name` from the local or global namespace (That's why the `list_1` is unaffected).
* `remove` removes the first matching value, not a specific index, raises `ValueError` if the value is not found.
* `pop` removes the element at a specific index and returns it, raises `IndexError` if an invalid index is specified.

**Why the output is `[2, 4]`?**
- The list iteration is done index by index, and when we remove `1` from `list_2` or `list_4`, the contents of the lists are now `[2, 3, 4]`. The remaining elements are shifted down, i.e., `2` is at index 0, and `3` is at index 1. Since the next iteration is going to look at index 1 (which is the `3`), the `2` gets skipped entirely. A similar thing will happen with every alternate element in the list sequence.

* Refer to this StackOverflow [thread](https://stackoverflow.com/questions/45946228/what-happens-when-you-try-to-delete-a-list-element-while-iterating-over-it) explaining the example
* See also this nice StackOverflow [thread](https://stackoverflow.com/questions/45877614/how-to-change-all-the-dictionary-keys-in-a-for-loop-with-d-items) for a similar example related to dictionaries in Python.

---


### ▶ Lossy zip of iterators *
<!-- Example ID: c28ed154-e59f-4070-8eb6-8967a4acac6d --->

```py
>>> numbers = list(range(7))
>>> numbers
[0, 1, 2, 3, 4, 5, 6]
>>> first_three, remaining = numbers[:3], numbers[3:]
>>> first_three, remaining
([0, 1, 2], [3, 4, 5, 6])
>>> numbers_iter = iter(numbers)
>>> list(zip(numbers_iter, first_three)) 
[(0, 0), (1, 1), (2, 2)]
# so far so good, let's zip the remaining
>>> list(zip(numbers_iter, remaining))
[(4, 3), (5, 4), (6, 5)]
```
Where did element `3` go from the `numbers` list?

#### 💡 Explanation:

- From Python [docs](https://docs.python.org/3.3/library/functions.html#zip), here's an approximate implementation of zip function,
    ```py
    def zip(*iterables):
        sentinel = object()
        iterators = [iter(it) for it in iterables]
        while iterators:
            result = []
            for it in iterators:
                elem = next(it, sentinel)
                if elem is sentinel: return
                result.append(elem)
            yield tuple(result)
    ```
- So the function takes in arbitrary number of itreable objects, adds each of their items to the `result` list by calling the `next` function on them, and stops whenever any of the iterable is exhausted. 
- The caveat here is when any iterable is exhausted, the existing elements in the `result` list are discarded. That's what happened with `3` in the `numbers_iter`.
- The correct way to do the above using `zip` would be,
    ```py
    >>> numbers = list(range(7))
    >>> numbers_iter = iter(numbers)
    >>> list(zip(first_three, numbers_iter))
    [(0, 0), (1, 1), (2, 2)]
    >>> list(zip(remaining, numbers_iter))
    [(3, 3), (4, 4), (5, 5), (6, 6)]
    ```
    The first argument of zip should be the one with fewest elements.

---

### ▶ Loop variables leaking out!
<!-- Example ID: ccec7bf6-7679-4963-907a-1cd8587be9ea --->
1\.
```py
for x in range(7):
    if x == 6:
        print(x, ': for x inside loop')
print(x, ': x in global')
```

**Output:**
```py
6 : for x inside loop
6 : x in global
```

But `x` was never defined outside the scope of for loop...

2\.
```py
# This time let's initialize x first
x = -1
for x in range(7):
    if x == 6:
        print(x, ': for x inside loop')
print(x, ': x in global')
```

**Output:**
```py
6 : for x inside loop
6 : x in global
```

3\.

**Output (Python 2.x):**
```py
>>> x = 1
>>> print([x for x in range(5)])
[0, 1, 2, 3, 4]
>>> print(x)
4
```

**Output (Python 3.x):**
```py
>>> x = 1
>>> print([x for x in range(5)])
[0, 1, 2, 3, 4]
>>> print(x)
1
```

#### 💡 Explanation:

- In Python, for-loops use the scope they exist in and leave their defined loop-variable behind. This also applies if we explicitly defined the for-loop variable in the global namespace before. In this case, it will rebind the existing variable.

- The differences in the output of Python 2.x and Python 3.x interpreters for list comprehension example can be explained by following change documented in [What’s New In Python 3.0](https://docs.python.org/3/whatsnew/3.0.html) changelog:

    > "List comprehensions no longer support the syntactic form `[... for var in item1, item2, ...]`. Use `[... for var in (item1, item2, ...)]` instead. Also, note that list comprehensions have different semantics: they are closer to syntactic sugar for a generator expression inside a `list()` constructor, and in particular, the loop control variables are no longer leaked into the surrounding scope."

---

### ▶ Beware of default mutable arguments!
<!-- Example ID: 7d42dade-e20d-4a7b-9ed7-16fb58505fe9 --->

```py
def some_func(default_arg=[]):
    default_arg.append("some_string")
    return default_arg
```

**Output:**
```py
>>> some_func()
['some_string']
>>> some_func()
['some_string', 'some_string']
>>> some_func([])
['some_string']
>>> some_func()
['some_string', 'some_string', 'some_string']
```

#### 💡 Explanation:

- The default mutable arguments of functions in Python aren't really initialized every time you call the function. Instead, the recently assigned value to them is used as the default value. When we explicitly passed `[]` to `some_func` as the argument, the default value of the `default_arg` variable was not used, so the function returned as expected.

    ```py
    def some_func(default_arg=[]):
        default_arg.append("some_string")
        return default_arg
    ```

    **Output:**
    ```py
    >>> some_func.__defaults__ #This will show the default argument values for the function
    ([],)
    >>> some_func()
    >>> some_func.__defaults__
    (['some_string'],)
    >>> some_func()
    >>> some_func.__defaults__
    (['some_string', 'some_string'],)
    >>> some_func([])
    >>> some_func.__defaults__
    (['some_string', 'some_string'],)
    ```

- A common practice to avoid bugs due to mutable arguments is to assign `None` as the default value and later check if any value is passed to the function corresponding to that argument. Example:

    ```py
    def some_func(default_arg=None):
        if not default_arg:
            default_arg = []
        default_arg.append("some_string")
        return default_arg
    ```

---

### ▶ Catching the Exceptions
<!-- Example ID: b5ca5e6a-47b9-4f69-9375-cda0f8c6755d --->
```py
some_list = [1, 2, 3]
try:
    # This should raise an ``IndexError``
    print(some_list[4])
except IndexError, ValueError:
    print("Caught!")

try:
    # This should raise a ``ValueError``
    some_list.remove(4)
except IndexError, ValueError:
    print("Caught again!")
```

**Output (Python 2.x):**
```py
Caught!

ValueError: list.remove(x): x not in list
```

**Output (Python 3.x):**
```py
  File "<input>", line 3
    except IndexError, ValueError:
                     ^
SyntaxError: invalid syntax
```

#### 💡 Explanation

* To add multiple Exceptions to the except clause, you need to pass them as parenthesized tuple as the first argument. The second argument is an optional name, which when supplied will bind the Exception instance that has been raised. Example,
  ```py
  some_list = [1, 2, 3]
  try:
     # This should raise a ``ValueError``
     some_list.remove(4)
  except (IndexError, ValueError), e:
     print("Caught again!")
     print(e)
  ```
  **Output (Python 2.x):**
  ```
  Caught again!
  list.remove(x): x not in list
  ```
  **Output (Python 3.x):**
  ```py
    File "<input>", line 4
      except (IndexError, ValueError), e:
                                       ^
  IndentationError: unindent does not match any outer indentation level
  ```

* Separating the exception from the variable with a comma is deprecated and does not work in Python 3; the correct way is to use `as`. Example,
  ```py
  some_list = [1, 2, 3]
  try:
      some_list.remove(4)

  except (IndexError, ValueError) as e:
      print("Caught again!")
      print(e)
  ```
  **Output:**
  ```
  Caught again!
  list.remove(x): x not in list
  ```

---

### ▶ Same operands, different story!
<!-- Example ID: ca052cdf-dd2d-4105-b936-65c28adc18a0 --->
1\.
```py
a = [1, 2, 3, 4]
b = a
a = a + [5, 6, 7, 8]
```

**Output:**
```py
>>> a
[1, 2, 3, 4, 5, 6, 7, 8]
>>> b
[1, 2, 3, 4]
```

2\.
```py
a = [1, 2, 3, 4]
b = a
a += [5, 6, 7, 8]
```

**Output:**
```py
>>> a
[1, 2, 3, 4, 5, 6, 7, 8]
>>> b
[1, 2, 3, 4, 5, 6, 7, 8]
```

#### 💡 Explanation:

*  `a += b` doesn't always behave the same way as `a = a + b`.  Classes *may* implement the *`op=`* operators differently, and lists do this.

* The expression `a = a + [5,6,7,8]` generates a new list and sets `a`'s reference to that new list, leaving `b` unchanged.

* The expression `a += [5,6,7,8]` is actually mapped to an "extend" function that operates on the list such that `a` and `b` still point to the same list that has been modified in-place.

---


### ▶ Be careful with chained operations
<!-- Example ID: 07974979-9c86-4720-80bd-467aa19470d9 --->
```py
>>> (False == False) in [False] # makes sense
False
>>> False == (False in [False]) # makes sense
False
>>> False == False in [False] # now what?
True

>>> True is False == False
False
>>> False is False is False
True

>>> 1 > 0 < 1
True
>>> (1 > 0) < 1
False
>>> 1 > (0 < 1)
False
```

#### 💡 Explanation:

As per https://docs.python.org/2/reference/expressions.html#not-in

> Formally, if a, b, c, ..., y, z are expressions and op1, op2, ..., opN are comparison operators, then a op1 b op2 c ... y opN z is equivalent to a op1 b and b op2 c and ... y opN z, except that each expression is evaluated at most once.

While such behavior might seem silly to you in the above examples, it's fantastic with stuff like `a == b == c` and `0 <= x <= 100`.

* `False is False is False` is equivalent to `(False is False) and (False is False)`
* `True is False == False` is equivalent to `True is False and False == False` and since the first part of the statement (`True is False`) evaluates to `False`, the overall expression evaluates to `False`.
* `1 > 0 < 1` is equivalent to `1 > 0 and 0 < 1` which evaluates to `True`.
* The expression `(1 > 0) < 1` is equivalent to `True < 1` and
  ```py
  >>> int(True)
  1
  >>> True + 1 #not relevant for this example, but just for fun
  2
  ```
  So, `1 < 1` evaluates to `False`

---

### ▶ Name resolution ignoring class scope
<!-- Example ID: 03f73d96-151c-4929-b0a8-f74430788324 --->
1\.
```py
x = 5
class SomeClass:
    x = 17
    y = (x for i in range(10))
```

**Output:**
```py
>>> list(SomeClass.y)[0]
5
```

2\.
```py
x = 5
class SomeClass:
    x = 17
    y = [x for i in range(10)]
```

**Output (Python 2.x):**
```py
>>> SomeClass.y[0]
17
```

**Output (Python 3.x):**
```py
>>> SomeClass.y[0]
5
```

#### 💡 Explanation
- Scopes nested inside class definition ignore names bound at the class level.
- A generator expression has its own scope.
- Starting from Python 3.X, list comprehensions also have their own scope.

---

### ▶ Needles in a Haystack *

<!-- Example ID: 52a199b1-989a-4b28-8910-dff562cebba9 --->

I haven't met even a single experience Pythonist till date who has not come across one or more of the following scenarios,

1\.

```py
x, y = (0, 1) if True else None, None
```

**Output:**

```py
>>> x, y  # expected (0, 1)
((0, 1), None)
```

2\.

```py
t = ('one', 'two')
for i in t:
    print(i)

t = ('one')
for i in t:
    print(i)

t = ()
print(t)
```

**Output:**

```py
one
two
o
n
e
tuple()
```

3\.

```
ten_words_list = [
    "some",
    "very",
    "big",
    "list",
    "that"
    "consists",
    "of",
    "exactly",
    "ten",
    "words"
]
```

**Output**

```py
>>> len(ten_words_list)
9
```

4\. Not asserting strongly enough

```py
a = "python"
b = "javascript"
```

**Output:**

```py
# An assert statement with an assertion failure message.
>>> assert(a == b, "Both languages are different")
# No AssertionError is raised
```

5\.

```py
some_list = [1, 2, 3]
some_dict = {
  "key_1": 1,
  "key_2": 2,
  "key_3": 3
}

some_list = some_list.append(4) 
some_dict = some_dict.update({"key_4": 4})
```

**Output:**

```py
>>> print(some_list)
None
>>> print(some_dict)
None
```

6\.

```py
def some_recursive_func(a):
    if a[0] == 0:
        return 
    a[0] -= 1
    some_recursive_func(a)
    return a

def similar_recursive_func(a):
        if a == 0:
                return a
        a -= 1
        similar_recursive_func(a)
        return a
```

**Output:**

```py
>>> some_recursive_func([5, 0])
[0, 0]
>>> similar_recursive_func(5)
4
```

#### 💡 Explanation:

* For 1, the correct statement for expected behavior is `x, y = (0, 1) if True else (None, None)`.

* For 2, the correct statement for expected behavior is `t = ('one',)` or `t = 'one',` (missing comma) otherwise the interpreter considers `t` to be a `str` and iterates over it character by character.

* `()` is a special token and denotes empty `tuple`.

* In 3, as you might have already figured out, there's a missing comma after 5th element (`"that"`) in the list. So by implicit string literal concatenation,

  ```py
  >>> ten_words_list
  ['some', 'very', 'big', 'list', 'thatconsists', 'of', 'exactly', 'ten', 'words']
  ```

* No `AssertionError` was raised in 4th snippet because instead of asserting the individual expression `a == b`, we're asserting entire tuple. The following snippet will clear things up,

  ```py
  >>> a = "python"
  >>> b = "javascript"
  >>> assert a == b
  Traceback (most recent call last):
      File "<stdin>", line 1, in <module>
  AssertionError
  
  >>> assert (a == b, "Values are not equal")
  <stdin>:1: SyntaxWarning: assertion is always true, perhaps remove parentheses?
  
  >>> assert a == b, "Values are not equal"
  Traceback (most recent call last):
      File "<stdin>", line 1, in <module>
  AssertionError: Values aren not equal
  ```

* As for the fifth snippet, most methods that modify the items of sequence/mapping objects like `list.append`, `dict.update`, `list.sort`, etc. modify the objects in-place and return `None`. The rationale behind this is to improve performance by avoiding making a copy of the object if the operation can be done in-place (Referred from [here](http://docs.python.org/2/faq/design.html#why-doesn-t-list-sort-return-the-sorted-list)).

* Last one should be fairly obvious, passing mutable object (like  `list` ) results in a call by reference, whereas an immutable object (like `int`)  results in a call by value.

* Being aware of these nitpicks can save you hours of debugging effort in the long run. 

---


### ▶ Splitsies *
<!-- Example ID: ec3168ba-a81a-4482-afb0-691f1cc8d65a --->
```py
>>> 'a'.split()
['a']

# is same as
>>> 'a'.split(' ')
['a']

# but
>>> len(''.split())
0

# isn't the same as
>>> len(''.split(' '))
1
```

#### 💡 Explanation:

- It might appear at first that the default separator for split is a single space `' '`, but as per the [docs](https://docs.python.org/2.7/library/stdtypes.html#str.split)
    >  If sep is not specified or is `None`, a different splitting algorithm is applied: runs of consecutive whitespace are regarded as a single separator, and the result will contain no empty strings at the start or end if the string has leading or trailing whitespace. Consequently, splitting an empty string or a string consisting of just whitespace with a None separator returns `[]`.
    > If sep is given, consecutive delimiters are not grouped together and are deemed to delimit empty strings (for example, `'1,,2'.split(',')` returns `['1', '', '2']`). Splitting an empty string with a specified separator returns `['']`.
- Noticing how the leading and trailing whitespaces are handled in the following snippet will make things clear,
    ```py
    >>> ' a '.split(' ')
    ['', 'a', '']
    >>> ' a '.split()
    ['a']
    >>> ''.split(' ')
    ['']
    ```

---

### ▶ Wild imports *
<!-- Example ID: 83deb561-bd55-4461-bb5e-77dd7f411e1c --->
<!-- read-only -->

```py
# File: module.py

def some_weird_name_func_():
    print("works!")

def _another_weird_name_func():
    print("works!")

```

**Output**

```py
>>> from module import *
>>> some_weird_name_func_()
"works!"
>>> _another_weird_name_func()
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
NameError: name '_another_weird_name_func' is not defined
```

#### 💡 Explanation:

- It is often advisable to not use wildcard imports. The first obvious reason for this is, in wildcard imports, the names with a leading underscore get imported. This may lead to errors during runtime.
- Had we used `from ... import a, b, c` syntax, the above `NameError` wouldn't have occurred.
    ```py
    >>> from module import some_weird_name_func_, _another_weird_name_func
    >>> _another_weird_name_func()
    works!
    ```
- If you really want to use wildcard imports, then you'd have to define the list `__all__` in your module that will contain a list of public objects that'll be available when we do wildcard imports.
    ```py
    __all__ = ['_another_weird_name_func']

    def some_weird_name_func_():
        print("works!")

    def _another_weird_name_func():
        print("works!")
    ```
    **Output**

    ```py
    >>> _another_weird_name_func()
    "works!"
    >>> some_weird_name_func_()
    Traceback (most recent call last):
      File "<stdin>", line 1, in <module>
    NameError: name 'some_weird_name_func_' is not defined
    ```

---

### ▶ All sorted? *

<!-- Example ID: e5ff1eaf-8823-4738-b4ce-b73f7c9d5511 -->

```py
>>> x = 7, 8, 9
>>> sorted(x) == x
False
>>> sorted(x) == sorted(x)
True

>>> y = reversed(x)
>>> sorted(y) == sorted(y)
False
```

#### 💡 Explanation:

- The `sorted` method always returns a list, and comparing lists and tuples always returns `False` in Python. 

- ```py
  >>> [] == tuple()
  False
  >>> x = 7, 8, 9
  >>> type(x), type(sorted(x))
  (tuple, list)
  ```

- Unlike `sorted`, the `reversed` method returns an iterator. Why? Because sorting requires the iterator to be either modified in-place or use an extra container (a list), whereas reversing can simply work by iterating from the last index to the first.

- So during comparison `sorted(y) == sorted(y)`, the first call to `sorted()` will consume the iterator `y`, and the next call will just return an empty list.

  ```py
  >>> x = 7, 8, 9
  >>> y = reversed(x)
  >>> sorted(y), sorted(y)
  ([7, 8, 9], [])
  ```

---

### ▶ Midnight time doesn't exist?
<!-- Example ID: 1bce8294-5619-4d70-8ce3-fe0bade690d1 --->
```py
from datetime import datetime

midnight = datetime(2018, 1, 1, 0, 0)
midnight_time = midnight.time()

noon = datetime(2018, 1, 1, 12, 0)
noon_time = noon.time()

if midnight_time:
    print("Time at midnight is", midnight_time)

if noon_time:
    print("Time at noon is", noon_time)
```

**Output (< 3.5):**

```py
('Time at noon is', datetime.time(12, 0))
```
The midnight time is not printed.

#### 💡 Explanation:

Before Python 3.5, the boolean value for `datetime.time` object was considered to be `False` if it represented midnight in UTC. It is error-prone when using the `if obj:` syntax to check if the `obj` is null or some equivalent of "empty."

---
---



## Section: The Hidden treasures!

This section contains a few lesser-known and interesting things about Python that most beginners like me are unaware of (well, not anymore).

### ▶ Okay Python, Can you make me fly?
<!-- Example ID: a92f3645-1899-4d50-9721-0031be4aec3f --->
Well, here you go

```py
import antigravity
```

**Output:**
Sshh... It's a super-secret.

#### 💡 Explanation:
+ `antigravity` module is one of the few easter eggs released by Python developers.
+ `import antigravity` opens up a web browser pointing to the [classic XKCD comic](http://xkcd.com/353/) about Python.
+ Well, there's more to it. There's **another easter egg inside the easter egg**. If you look at the [code](https://github.com/python/cpython/blob/master/Lib/antigravity.py#L7-L17), there's a function defined that purports to implement the [XKCD's geohashing algorithm](https://xkcd.com/426/).

---

### ▶ `goto`, but why?
<!-- Example ID: 2aff961e-7fa5-4986-a18a-9e5894bd89fe --->

```py
from goto import goto, label
for i in range(9):
    for j in range(9):
        for k in range(9):
            print("I am trapped, please rescue!")
            if k == 2:
                goto .breakout # breaking out from a deeply nested loop
label .breakout
print("Freedom!")
```

**Output (Python 2.3):**
```py
I am trapped, please rescue!
I am trapped, please rescue!
Freedom!
```

#### 💡 Explanation:
- A working version of `goto` in Python was [announced](https://mail.python.org/pipermail/python-announce-list/2004-April/002982.html) as an April Fool's joke on 1st April 2004.
- Current versions of Python do not have this module.
- Although it works, but please don't use it. Here's the [reason](https://docs.python.org/3/faq/design.html#why-is-there-no-goto) to why `goto` is not present in Python.

---

### ▶ Brace yourself!
<!-- Example ID: 5c0c75f2-ddd9-4da3-ba49-c4be7ec39acf --->
If you are one of the people who doesn't like using whitespace in Python to denote scopes, you can use the C-style {} by importing,

```py
from __future__ import braces
```

**Output:**
```py
  File "some_file.py", line 1
    from __future__ import braces
SyntaxError: not a chance
```

Braces? No way! If you think that's disappointing, use Java. Okay, another surprising thing, can you find where's the `SyntaxError` raised in `__future__` module [code](https://github.com/python/cpython/blob/master/Lib/__future__.py)?

#### 💡 Explanation:
+ The `__future__` module is normally used to provide features from future versions of Python. The "future" in this specific context is however, ironic.
+ This is an easter egg concerned with the community's feelings on this issue.
+ The code is actually present [here](https://github.com/python/cpython/blob/025eb98dc0c1dc27404df6c544fc2944e0fa9f3a/Python/future.c#L49) in `future.c` file.
+ When the CPython compiler encounters a [future statement](https://docs.python.org/3.3/reference/simple_stmts.html#future-statements), it first runs the appropriate code in `future.c` before treating it as a normal import statement.

---

### ▶ Let's meet Friendly Language Uncle For Life
<!-- Example ID: 6427fae6-e959-462d-85da-ce4c94ce41be --->
**Output (Python 3.x)**
```py
>>> from __future__ import barry_as_FLUFL
>>> "Ruby" != "Python" # there's no doubt about it
  File "some_file.py", line 1
    "Ruby" != "Python"
              ^
SyntaxError: invalid syntax

>>> "Ruby" <> "Python"
True
```

There we go.

#### 💡 Explanation:
- This is relevant to [PEP-401](https://www.python.org/dev/peps/pep-0401/) released on April 1, 2009 (now you know, what it means).
- Quoting from the PEP-401
  
  > Recognized that the != inequality operator in Python 3.0 was a horrible, finger-pain inducing mistake, the FLUFL reinstates the <> diamond operator as the sole spelling.
- There were more things that Uncle Barry had to share in the PEP; you can read them [here](https://www.python.org/dev/peps/pep-0401/).
- It works well in an interactive environment, but it will raise a `SyntaxError` when you run via python file (see this [issue](https://github.com/satwikkansal/wtfpython/issues/94)). However, you can wrap the statement inside an `eval` or `compile` to get it working,
    ```py
    from __future__ import barry_as_FLUFL
    print(eval('"Ruby" <> "Python"'))
    ```

---

### ▶ Even Python understands that love is complicated
<!-- Example ID: b93cad9e-d341-45d1-999c-fcdce65bed25 --->
```py
import this
```

Wait, what's **this**? `this` is love :heart:

**Output:**
```
The Zen of Python, by Tim Peters

Beautiful is better than ugly.
Explicit is better than implicit.
Simple is better than complex.
Complex is better than complicated.
Flat is better than nested.
Sparse is better than dense.
Readability counts.
Special cases aren't special enough to break the rules.
Although practicality beats purity.
Errors should never pass silently.
Unless explicitly silenced.
In the face of ambiguity, refuse the temptation to guess.
There should be one-- and preferably only one --obvious way to do it.
Although that way may not be obvious at first unless you're Dutch.
Now is better than never.
Although never is often better than *right* now.
If the implementation is hard to explain, it's a bad idea.
If the implementation is easy to explain, it may be a good idea.
Namespaces are one honking great idea -- let's do more of those!
```

It's the Zen of Python!

```py
>>> love = this
>>> this is love
True
>>> love is True
False
>>> love is False
False
>>> love is not True or False
True
>>> love is not True or False; love is love  # Love is complicated
True
```

#### 💡 Explanation:

* `this` module in Python is an easter egg for The Zen Of Python ([PEP 20](https://www.python.org/dev/peps/pep-0020)).
* And if you think that's already interesting enough, check out the implementation of [this.py](https://hg.python.org/cpython/file/c3896275c0f6/Lib/this.py). Interestingly, **the code for the Zen violates itself** (and that's probably the only place where this happens).
* Regarding the statement `love is not True or False; love is love`, ironic but it's self-explanatory (if not, please see the examples related to `is` and `is not` operators).

---

### ▶ Yes, it exists!
<!-- Example ID: 4286db3d-1ea7-47c9-8fb6-a9a04cac6e49 --->
**The `else` clause for loops.** One typical example might be:

```py
  def does_exists_num(l, to_find):
      for num in l:
          if num == to_find:
              print("Exists!")
              break
      else:
          print("Does not exist")
```

**Output:**
```py
>>> some_list = [1, 2, 3, 4, 5]
>>> does_exists_num(some_list, 4)
Exists!
>>> does_exists_num(some_list, -1)
Does not exist
```

**The `else` clause in exception handling.** An example,

```py
try:
    pass
except:
    print("Exception occurred!!!")
else:
    print("Try block executed successfully...")
```

**Output:**
```py
Try block executed successfully...
```

#### 💡 Explanation:
- The `else` clause after a loop is executed only when there's no explicit `break` after all the iterations. You can think of it as a "nobreak" clause.
- `else` clause after a try block is also called "completion clause" as reaching the `else` clause in a `try` statement means that the try block actually completed successfully.

---
### ▶ Ellipsis *
<!-- Example ID: 969b7100-ab3d-4a7d-ad7d-a6be16181b2b --->
```py
def some_func():
    Ellipsis
```

**Output**
```py
>>> some_func()
# No output, No Error

>>> SomeRandomString
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
NameError: name 'SomeRandomString' is not defined

>>> Ellipsis
Ellipsis
```

#### 💡 Explanation
- In Python, `Ellipsis` is a globally available built-in object which is equivalent to `...`.
    ```py
    >>> ...
    Ellipsis
    ```
- Eliipsis can be used for several purposes,
    + As a placeholder for code that hasn't been written yet (just like `pass` statement)
    + In slicing syntax to represent the full slices in remaining direction
    ```py
    >>> import numpy as np
    >>> three_dimensional_array = np.arange(8).reshape(2, 2, 2)
    array([
        [
            [0, 1],
            [2, 3]
        ],

        [
            [4, 5],
            [6, 7]
        ]
    ])
    ```
    So our `three_dimensional_array` is an array of array of arrays. Let's say we want to print the second element (index `1`) of all the innermost arrays, we can use Ellipsis to bypass all the preceding dimensions
    ```py
    >>> three_dimensional_array[:,:,1]
    array([[1, 3],
       [5, 7]])
    >>> three_dimensional_array[..., 1] # using Ellipsis.
    array([[1, 3],
       [5, 7]])
    ```
    Note: this will work for any number of dimensions. You can even select slice in first and last dimension and ignore the middle ones this way (`n_dimensional_array[firs_dim_slice, ..., last_dim_slice]`)
    + In [type hinting](https://docs.python.org/3/library/typing.html) to indicate only a part of the type (like `(Callable[..., int]` or `Tuple[str, ...]`))
    + You may also use Ellipsis as a default function argument (in the cases when you want to differentiate between the "no argument passed" and "None value passed" scenarios).

---

### ▶ Inpinity
<!-- Example ID: ff473ea8-a3b1-4876-a6f0-4378aff790c1 --->
The spelling is intended. Please, don't submit a patch for this.

**Output (Python 3.x):**
```py
>>> infinity = float('infinity')
>>> hash(infinity)
314159
>>> hash(float('-inf'))
-314159
```

#### 💡 Explanation:
- Hash of infinity is 10⁵ x π.
- Interestingly, the hash of `float('-inf')` is "-10⁵ x π" in Python 3, whereas "-10⁵ x e" in Python 2.

---

### ▶ Let's mangle
<!-- Example ID: 37146d2d-9e67-43a9-8729-3c17934b910c --->
1\.
```py
class Yo(object):
    def __init__(self):
        self.__honey = True
        self.bro = True
```

**Output:**
```py
>>> Yo().bro
True
>>> Yo().__honey
AttributeError: 'Yo' object has no attribute '__honey'
>>> Yo()._Yo__honey
True
```

2\.
```py
class Yo(object):
    def __init__(self):
        # Let's try something symmetrical this time
        self.__honey__ = True
        self.bro = True
```

**Output:**
```py
>>> Yo().bro
True

>>> Yo()._Yo__honey__
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
AttributeError: 'Yo' object has no attribute '_Yo__honey__'
```

Why did `Yo()._Yo__honey` work?

3\.

```py
_A__variable = "Some value"

class A(object):
    def some_func(self):
        return __variable # not initiatlized anywhere yet
```

**Output:**
```py
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
AttributeError: 'A' object has no attribute '__variable'

>>> >>> A().some_func()
'Some value'
```


#### 💡 Explanation:

* [Name Mangling](https://en.wikipedia.org/wiki/Name_mangling) is used to avoid naming collisions between different namespaces.
* In Python, the interpreter modifies (mangles) the class member names starting with `__` (double underscore a.k.a "dunder") and not ending with more than one trailing underscore by adding `_NameOfTheClass` in front.
* So, to access `__honey` attribute in the first snippet, we had to append `_Yo` to the front, which would prevent conflicts with the same name attribute defined in any other class.
* But then why didn't it work in the second snippet? Because name mangling excludes the names ending with double underscores.
* The third snippet was also a consequence of name mangling. The name `__variable` in the statement `return __variable` was mangled to `_A__variable`, which also happens to be the name of the variable we declared in the outer scope.
* Also, if the mangled name is longer than 255 characters, truncation will happen.

---
---

## Section: Appearances are deceptive!

### ▶ Skipping lines?
<!-- Example ID: d50bbde1-fb9d-4735-9633-3444b9d2f417 --->
**Output:**
```py
>>> value = 11
>>> valuе = 32
>>> value
11
```

Wut?

**Note:** The easiest way to reproduce this is to simply copy the statements from the above snippet and paste them into your file/shell.

#### 💡 Explanation

Some non-Western characters look identical to letters in the English alphabet but are considered distinct by the interpreter.

```py
>>> ord('е') # cyrillic 'e' (Ye)
1077
>>> ord('e') # latin 'e', as used in English and typed using standard keyboard
101
>>> 'е' == 'e'
False

>>> value = 42 # latin e
>>> valuе = 23 # cyrillic 'e', Python 2.x interpreter would raise a `SyntaxError` here
>>> value
42
```

The built-in `ord()` function returns a character's Unicode [code point](https://en.wikipedia.org/wiki/Code_point), and different code positions of Cyrillic 'e' and Latin 'e' justify the behavior of the above example.

---

### ▶ Teleportation

<!-- Example ID: edafe923-0c20-4315-b6e1-0c31abfc38f5 --->

```py
# `pip install nump` first.
import numpy as np

def energy_send(x):
    # Initializing a numpy array
    np.array([float(x)])

def energy_receive():
    # Return an empty numpy array
    return np.empty((), dtype=np.float).tolist()
```

**Output:**
```py
>>> energy_send(123.456)
>>> energy_receive()
123.456
```

Where's the Nobel Prize?

#### 💡 Explanation:

* Notice that the numpy array created in the `energy_send` function is not returned, so that memory space is free to reallocate.
* `numpy.empty()` returns the next free memory slot without reinitializing it. This memory spot just happens to be the same one that was just freed (usually, but not always).

---

### ▶ Well, something is fishy...
<!-- Example ID: cb6a37c5-74f7-44ca-b58c-3b902419b362 --->
```py
def square(x):
    """
    A simple function to calculate the square of a number by addition.
    """
    sum_so_far = 0
    for counter in range(x):
        sum_so_far = sum_so_far + x
  return sum_so_far
```

**Output (Python 2.x):**

```py
>>> square(10)
10
```

Shouldn't that be 100?

**Note:** If you're not able to reproduce this, try running the file [mixed_tabs_and_spaces.py](/mixed_tabs_and_spaces.py) via the shell.

#### 💡 Explanation

* **Don't mix tabs and spaces!** The character just preceding return is a "tab",  and the code is indented by multiple of "4 spaces" elsewhere in the example.
* This is how Python handles tabs:
  
  > First, tabs are replaced (from left to right) by one to eight spaces such that the total number of characters up to and including the replacement is a multiple of eight <...>
* So the "tab" at the last line of `square` function is replaced with eight spaces, and it gets into the loop.
* Python 3 is kind enough to throw an error for such cases automatically.

    **Output (Python 3.x):**
    ```py
    TabError: inconsistent use of tabs and spaces in indentation
    ```

---
---

## Section: Miscellaneous


### ▶ `+=` is faster
<!-- Example ID: bfd19c60-a807-4a26-9598-4912b86ddb36 --->

```py
# using "+", three strings:
>>> timeit.timeit("s1 = s1 + s2 + s3", setup="s1 = ' ' * 100000; s2 = ' ' * 100000; s3 = ' ' * 100000", number=100)
0.25748300552368164
# using "+=", three strings:
>>> timeit.timeit("s1 += s2 + s3", setup="s1 = ' ' * 100000; s2 = ' ' * 100000; s3 = ' ' * 100000", number=100)
0.012188911437988281
```

#### 💡 Explanation:
+ `+=` is faster than `+` for concatenating more than two strings because the first string (example, `s1` for `s1 += s2 + s3`) is not destroyed while calculating the complete string.

---

### ▶ Let's make a giant string!
<!-- Example ID: c7a07424-63fe-4504-9842-8f3d334f28fc --->
```py
def add_string_with_plus(iters):
    s = ""
    for i in range(iters):
        s += "xyz"
    assert len(s) == 3*iters

def add_bytes_with_plus(iters):
    s = b""
    for i in range(iters):
        s += b"xyz"
    assert len(s) == 3*iters

def add_string_with_format(iters):
    fs = "{}"*iters
    s = fs.format(*(["xyz"]*iters))
    assert len(s) == 3*iters

def add_string_with_join(iters):
    l = []
    for i in range(iters):
        l.append("xyz")
    s = "".join(l)
    assert len(s) == 3*iters

def convert_list_to_string(l, iters):
    s = "".join(l)
    assert len(s) == 3*iters
```

**Output:**

```py
# Executed in ipython shell using %timeit for better readablity of results.
# You can also use the timeit module in normal python shell/scriptm=, example usage below
# timeit.timeit('add_string_with_plus(10000)', number=1000, globals=globals())

>>> NUM_ITERS = 1000
>>> %timeit -n1000 add_string_with_plus(NUM_ITERS)
124 µs ± 4.73 µs per loop (mean ± std. dev. of 7 runs, 100 loops each)
>>> %timeit -n1000 add_bytes_with_plus(NUM_ITERS)
211 µs ± 10.5 µs per loop (mean ± std. dev. of 7 runs, 1000 loops each)
>>> %timeit -n1000 add_string_with_format(NUM_ITERS)
61 µs ± 2.18 µs per loop (mean ± std. dev. of 7 runs, 1000 loops each)
>>> %timeit -n1000 add_string_with_join(NUM_ITERS)
117 µs ± 3.21 µs per loop (mean ± std. dev. of 7 runs, 1000 loops each)
>>> l = ["xyz"]*NUM_ITERS
>>> %timeit -n1000 convert_list_to_string(l, NUM_ITERS)
10.1 µs ± 1.06 µs per loop (mean ± std. dev. of 7 runs, 1000 loops each)
```

Let's increase the number of iterations by a factor of 10.

```py
>>> NUM_ITERS = 10000
>>> %timeit -n1000 add_string_with_plus(NUM_ITERS) # Linear increase in execution time
1.26 ms ± 76.8 µs per loop (mean ± std. dev. of 7 runs, 1000 loops each)
>>> %timeit -n1000 add_bytes_with_plus(NUM_ITERS) # Quadratic increase
6.82 ms ± 134 µs per loop (mean ± std. dev. of 7 runs, 1000 loops each)
>>> %timeit -n1000 add_string_with_format(NUM_ITERS) # Linear increase
645 µs ± 24.5 µs per loop (mean ± std. dev. of 7 runs, 1000 loops each)
>>> %timeit -n1000 add_string_with_join(NUM_ITERS) # Linear increase
1.17 ms ± 7.25 µs per loop (mean ± std. dev. of 7 runs, 1000 loops each)
>>> l = ["xyz"]*NUM_ITERS
>>> %timeit -n1000 convert_list_to_string(l, NUM_ITERS) # Linear increase
86.3 µs ± 2 µs per loop (mean ± std. dev. of 7 runs, 1000 loops each)
```

#### 💡 Explanation
- You can read more about [timeit](https://docs.python.org/3/library/timeit.html) or [%timeit](https://ipython.org/ipython-doc/dev/interactive/magics.html#magic-timeit) on these links. They are used to measure the execution time of code pieces.
- Don't use `+` for generating long strings — In Python, `str` is immutable, so the left and right strings have to be copied into the new string for every pair of concatenations. If you concatenate four strings of length 10, you'll be copying (10+10) + ((10+10)+10) + (((10+10)+10)+10) = 90 characters instead of just 40 characters. Things get quadratically worse as the number and size of the string increases (justified with the execution times of `add_bytes_with_plus` function)
- Therefore, it's advised to use `.format.` or `%` syntax (however, they are slightly slower than `+` for very short strings).
- Or better, if already you've contents available in the form of an iterable object, then use `''.join(iterable_object)` which is much faster.
- Unlike `add_bytes_with_plus` because of the `+=` optimizations discussed in the previous example, `add_string_with_plus` didn't show a quadratic increase in execution time. Had the statement been `s = s + "x" + "y" + "z"` instead of `s += "xyz"`, the increase would have been quadratic.
  ```py
  def add_string_with_plus(iters):
      s = ""
      for i in range(iters):
          s = s + "x" + "y" + "z"
      assert len(s) == 3*iters

  >>> %timeit -n100 add_string_with_plus(1000)
  388 µs ± 22.4 µs per loop (mean ± std. dev. of 7 runs, 1000 loops each)
  >>> %timeit -n100 add_string_with_plus(10000) # Quadratic increase in execution time
  9 ms ± 298 µs per loop (mean ± std. dev. of 7 runs, 100 loops each)
  ```
- So many ways to format and create a giant string are somewhat in contrast to the [Zen of Python](https://www.python.org/dev/peps/pep-0020/), according to which,
  
    > There should be one-- and preferably only one --obvious way to do it.

---

### ▶ Minor Ones *
<!-- Example ID: f885cb82-f1e4-4daa-9ff3-972b14cb1324 --->
* `join()` is a string operation instead of list operation. (sort of counter-intuitive at first usage)

  **💡 Explanation:** If `join()` is a method on a string, then it can operate on any iterable (list, tuple, iterators). If it were a method on a list, it'd have to be implemented separately by every type. Also, it doesn't make much sense to put a string-specific method on a generic `list` object API.
  
* Few weird looking but semantically correct statements:
  + `[] = ()` is a semantically correct statement (unpacking an empty `tuple` into an empty `list`)
  + `'a'[0][0][0][0][0]` is also a semantically correct statement as strings are [sequences](https://docs.python.org/3/glossary.html#term-sequence)(iterables supporting element access using integer indices) in Python.
  + `3 --0-- 5 == 8` and `--5 == 5` are both semantically correct statements and evaluate to `True`.

* Given that `a` is a number, `++a` and `--a` are both valid Python statements but don't behave the same way as compared with similar statements in languages like C, C++, or Java.
  ```py
  >>> a = 5
  >>> a
  5
  >>> ++a
  5
  >>> --a
  5
  ```

  **💡 Explanation:**
  + There is no `++` operator in Python grammar. It is actually two `+` operators.
  + `++a` parses as `+(+a)` which translates to `a`. Similarly, the output of the statement `--a` can be justified.
  + This StackOverflow [thread](https://stackoverflow.com/questions/3654830/why-are-there-no-and-operators-in-python) discusses the rationale behind the absence of increment and decrement operators in Python.

* You must be aware of the Walrus operator in Python. But have you ever heard about *the space-invader operator*?
  ```py
  >>> a = 42
  >>> a -=- 1
  >>> a
  43
  ```
  It is used as an alternative incrementation operator, together with another one
  ```py
  >>> a +=+ 1
  >>> a
  >>> 44
  ```
  **💡 Explanation:** This prank comes from [Raymond Hettinger's tweet](https://twitter.com/raymondh/status/1131103570856632321?lang=en). The space invader operator is actually just a malformatted `a -= (-1)`. Which is equivalent to `a = a - (- 1)`. Similar for the `a += (+ 1)` case.
  
* Python has an undocumented [converse implication](https://en.wikipedia.org/wiki/Converse_implication) operator. 
     
     ```py
     >>> False ** False == True
     True
     >>> False ** True == False
     True
     >>> True ** False == True
     True
     >>> True ** True == True
     True
     ```

     **💡 Explanation:** If you replace `False` and `True` by 0 and 1 and do the maths, the truth table is equivalent to a converse implication operator. ([Source](https://github.com/cosmologicon/pywat/blob/master/explanation.md#the-undocumented-converse-implication-operator))
     
* Since we are talking operators, there's also `@` operator for matrix multiplication (don't worry, this time it's for real).

     ```py
     >>> import numpy as np
     >>> np.array([2, 2, 2]) @ np.array([7, 8, 8])
     46
     ```

     **💡 Explanation:** The `@` operator was added in Python 3.5 keeping sthe cientific community in mind. Any object can overload `__matmul__` magic method to define behavior for this operator.

* From Python 3.8 onwards you can use a typical f-string syntax like `f'{some_var=}` for quick debugging. Example,
    ```py
    >>> some_string = "wtfpython"
    >>> f'{some_string=}'
    "string='wtfpython'"
    ``` 

* Python uses 2 bytes for local variable storage in functions. In theory, this means that only 65536 variables can be defined in a function. However, python has a handy solution built in that can be used to store more than 2^16 variable names. The following code demonstrates what happens in the stack when more than 65536 local variables are defined (Warning: This code prints around 2^18 lines of text, so be prepared!):
     
     ```py
     import dis
    exec("""
    def f():
        """ + """
        """.join(["X" + str(x) + "=" + str(x) for x in range(65539)]))

    f()

    print(dis.dis(f))
    ```
     
* Multiple Python threads won't run your *Python code* concurrently (yes, you heard it right!). It may seem intuitive to spawn several threads and let them execute your Python code concurrently, but, because of the [Global Interpreter Lock](https://wiki.python.org/moin/GlobalInterpreterLock) in Python, all you're doing is making your threads execute on the same core turn by turn. Python threads are good for IO-bound tasks, but to achieve actual parallelization in Python for CPU-bound tasks, you might want to use the Python [multiprocessing](https://docs.python.org/2/library/multiprocessing.html) module.

* Sometimes, the `print` method might not print values immediately. For example,

     ```py
     # File some_file.py
     import time
     
     print("wtfpython", end="_")
     time.sleep(3)
     ```

     This will print the `wtfpython` after 10 seconds due to the `end` argument because the output buffer is flushed either after encountering `\n` or when the program finishes execution. We can force the buffer to flush by passing `flush=True` argument.

* List slicing with out of the bounds indices throws no errors
  ```py
  >>> some_list = [1, 2, 3, 4, 5]
  >>> some_list[111:]
  []
  ```

* Slicing an iterable not always creates a new object. For example,
    ```py
    >>> some_str = "wtfpython"
    >>> some_list = ['w', 't', 'f', 'p', 'y', 't', 'h', 'o', 'n']
    >>> some_list is some_list[:] # False expected because a new object is created.
    False
    >>> some_str is some_str[:] # True because strings are immutable, so making a new object is of not much use.
    True
    ```

* `int('١٢٣٤٥٦٧٨٩')` returns `123456789` in Python 3. In Python, Decimal characters include digit characters, and all characters that can be used to form decimal-radix numbers, e.g. U+0660, ARABIC-INDIC DIGIT ZERO. Here's an [interesting story](http://chris.improbable.org/2014/8/25/adventures-in-unicode-digits/) related to this behavior of Python.

* You can seperate numeric literals with underscores (for better readablity) from Python 3 onwards.

     ```py
     >>> six_million = 6_000_000
     >>> six_million
     6000000
     >>> hex_address = 0xF00D_CAFE
     >>> hex_address
     4027435774
     ```

* `'abc'.count('') == 4`. Here's an approximate implementation of `count` method, which would make the things more clear
  ```py
  def count(s, sub):
      result = 0
      for i in range(len(s) + 1 - len(sub)):
          result += (s[i:i + len(sub)] == sub)
      return result
  ```
  The behavior is due to the matching of empty substring(`''`) with slices of length 0 in the original string.

**That's all folks!**

---
---

# Contributing

A few ways in which you can contribute to wtfpython,

- Suggesting new examples
- Helping with translation (See [issues labeled translation](https://github.com/satwikkansal/wtfpython/issues?q=is%3Aissue+is%3Aopen+label%3Atranslation))
- Minor corrections like pointing out outdated snippets, typos, formatting errors, etc.
- Identifying gaps (things like inadequate explanation, redundant examples, etc.)
- Any creative suggestions to make this project more fun and useful

Please see [CONTRIBUTING.md](/CONTRIBUTING.md) for more details. Feel free to create a new [issue](https://github.com/satwikkansal/wtfpython/issues/new) to discuss things.

PS: Please don't reach out with backlinking requests, no links will be added unless they're highly relevant to the project.

# Acknowledgements

The idea and design for this collection were initially inspired by Denys Dovhan's awesome project [wtfjs](https://github.com/denysdovhan/wtfjs). The overwhelming support by Pythonistas gave it the shape it is in right now.

#### Some nice Links!
* https://www.youtube.com/watch?v=sH4XF6pKKmk
* https://www.reddit.com/r/Python/comments/3cu6ej/what_are_some_wtf_things_about_python
* https://sopython.com/wiki/Common_Gotchas_In_Python
* https://stackoverflow.com/questions/530530/python-2-x-gotchas-and-landmines
* https://stackoverflow.com/questions/1011431/common-pitfalls-in-python
* https://www.python.org/doc/humor/
* https://github.com/cosmologicon/pywat#the-undocumented-converse-implication-operator
* https://www.codementor.io/satwikkansal/python-practices-for-efficient-code-performance-memory-and-usability-aze6oiq65
* https://github.com/wemake-services/wemake-python-styleguide/search?q=wtfpython&type=Issues

# 🎓 License

[![WTFPL 2.0][license-image]][license-url]

&copy; [Satwik Kansal](https://satwikkansal.xyz)

[license-url]: http://www.wtfpl.net
[license-image]: https://img.shields.io/badge/License-WTFPL%202.0-lightgrey.svg?style=flat-square

## Surprise your friends as well!

If you like wtfpython, you can use these quick links to share it with your friends,

[Twitter](https://twitter.com/intent/tweet?url=https://github.com/satwikkansal/wtfpython&text=If%20you%20really%20think%20you%20know%20Python,%20think%20once%20more!%20Check%20out%20wtfpython&hastags=python,wtfpython) | [Linkedin](https://www.linkedin.com/shareArticle?url=https://github.com/satwikkansal&title=What%20the%20f*ck%20Python!&summary=If%20you%20really%20thing%20you%20know%20Python,%20think%20once%20more!) | [Facebook](https://www.facebook.com/dialog/share?app_id=536779657179021&display=page&href=https%3A%2F%2Fgithub.com%2Fsatwikkansal%2Fwtfpython&quote=If%20you%20really%20think%20you%20know%20Python%2C%20think%20once%20more!)  

## More content like this?

If you're interested in more content like this, you can share your email [here](https://satwikkansal.xyz/content-like-wtfpython/).
*PS: On a sidenote, consider [buying me a meal](https://ko-fi.com/satwikkansal) or [planting a tree](https://teamtrees.org/).*
