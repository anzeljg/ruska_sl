# Slovenska **ruska** tipkovnica

Razporeditev ruskih črk, ki se ujema z razporeditvijo tipk na slovenski tipkovnici, kar pomeni, da če npr. pritisnemo tipko "Č" se pojavi črka "Ч" itd.

Trenutna različica razporeda ruskih črk na slovenski tipkovnici poleg ruščine podpira še beloruščino, bolgarščino, makedonščino, srbščino in ukrajinščino.

```
┌─────┬─────┬─────┬─────┬─────┬─────┬─────┬─────┬─────┬─────┬─────┬─────┬─────┬───────────┐
│ Ь Ъ │ !   │ "   │ #   │ $   │ %   │ &   │ /   │ (   │ )   │ =   │ ?   │ *   │           │
│ ь ъ │ 1 ~ │ 2   │ 3   │ 4   │ 5   │ 6   │ 7   │ 8   │ 9   │ 0   │ '   │ +   │ Backspace │
├─────┴─┬───┴─┬───┴─┬───┴─┬───┴─┬───┴─┬───┴─┬───┴─┬───┴─┬───┴─┬───┴─┬───┴─┬───┴─┬─────────┤
│       │ Ы Ї │ Ё   │ Е Є │ Р   │ Т   │ З Ѕ │ У Ў │ И І │ О   │ П   │ Ш   │ Ю Ђ │         │
│ Tab   │ ы ї │ ё   │ е є │ р   │ т   │ з ѕ │ у ў │ и і │ о   │ п   │ ш   │ ю ђ │   Enter │
├───────┴─┬───┴─┬───┴─┬───┴─┬───┴─┬───┴─┬───┴─┬───┴─┬───┴─┬───┴─┬───┴─┬───┴─┬───┴─┐       │
│ Caps    │ А   │ С   │ Д Џ │ Ф   │ Г Ґ │ Х   │ Й Ј │ К Ќ │ Л Љ │ Ч   │ Щ Ћ │ Ж   │       │
│ Lock    │ а   │ с   │ д џ │ ф   │ г ґ │ х   │ й ј │ к ќ │ л љ │ ч   │ щ ћ │ ж   │       │
├───────┬─┴───┬─┴───┬─┴───┬─┴───┬─┴───┬─┴───┬─┴───┬─┴───┬─┴───┬─┴───┬─┴───┬─┴─────┴───────┤
│       │ >   │ Я   │ Э   │ Ц Ѓ │ В   │ Б   │ Н Њ │ М   │ ;   │ :   │ _   │               │
│ Shift │ <   │ я   │ э   │ ц ѓ │ в @ │ б   │ н њ │ м   │ ,   │ .   │ -   │     Shift     │
├───────┼─────┴─┬───┴───┬─┴─────┴─────┴─────┴─────┴─────┴─────┴───┬─┴─────┼───────┬───────┤
│       │       │       │                                         │       │       │       │
│ Ctrl  │ Meta  │  Alt  │                  Space                  │ AltGr │ Menu  │ Ctrl  │
└───────┴───────┴───────┴─────────────────────────────────────────┴───────┴───────┴───────┘

Q => ы, Shift + Q => Ы, AltGr + Q => ї, AltGr + Shift + Q => Ї
```

Članek z rešitvijo problema lastne razporeditve črk na tipkovnici je bil predstavljen na konferenci [SirIKT 2010](https://skupnost.sio.si/sio_arhiv/sirikt/www.sirikt.si/slo/sirikt2010/predstavitev.html) in objavljen v [zborniku](https://skupnost.sio.si/sio_arhiv/sirikt/www.sirikt.si/fileadmin/sirikt/fotogalerija/2010/Zbornik/SIRIKT2010_Zbornik_WEB_v2.pdf).

## Namestitev

### Windows

Prenesite namestitveni paket in ga razširite v novo mapo. Nato dvo-kliknite datoteko `setup.exe` in počakajte, da se paket namesti.

V opravilni vrstici prikažite vrstico z jeziki, s pomočjo katere boste lahko preklapljali med slovensko in rusko tipkovnico.

### Mac OS X

Prenesite namestitveni paket in ga razširite v novo mapo. Nato datoteko `ruska_sl.keylayout` prenesite v mapo `/Library/Keyboard/Layouts`.

Odprite `System Preferences > Keyboard > Input Sources > + > Others` in preverite, da je nova razporeditev izpisana na seznamu vseh razporeditev.

### Linux

Prenesite namestitveni paket in ga razširite v novo mapo. Nato datoteko `ru_sl` iz mape `xkb/symbols` prenesite v mapo  `/usr/share/X11/xkb/symbols`.

V datoteki `/usr/share/X11/xkb/rules/base.lst` morate v razdelek `! layout` dodati novo razporeditev `ru_sl`:
```
  ru_sl           Russian (Slovenian keyboard)
```

V datoteki `/usr/share/X11/xkb/rules/base.xml` morate v XML element `<layoutList>` dodati novo razporeditev `ru_sl`:
```
    <layout>
      <configItem>
        <name>ru_sl</name>
        <shortDescription>ru</shortDescription>
        <description>Russian (Slovenian keyboard)</description>
        <languageList>
          <iso639Id>rus</iso639Id>
        </languageList>
      </configItem>
    </layout>
```

Nato morate ponovno zagnati sistem.

Odprite `System Preferences > Input Sources > Keyboard > Layouts`, dodajte nov razpored `ru_sl` in obkljukajte možnost `Show layout indicator`.

Odprite `System Preferences > Input Sources > Keyboard > Advanced<` in pri možnosti `Switching to another layout` izberte kombinacijo tipk, s katerimi boste preklapljali med različnimi razporeditvami tipk.
Najbolje se obnese kombinacija `LShift + LCtrl` (levi Shift in levi Ctrl).
