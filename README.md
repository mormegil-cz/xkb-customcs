CustomCS klávesnice pro xkb
===========================

_(English abstract: This is a customized xkb keyboard for the Czech language (cs).)_


Funkce
------

V zásadě se jedná o českou QWERTY klávesnici, která přes <kbd>AltGr</kbd> (pravý <kbd>Alt</kbd>) zpřístupňuje u kláves symbolů a čísel původní anglické klávesy. Tedy např. <kbd>AltGr</kbd>+<kbd>2</kbd> dá `@`, <kbd>AltGr</kbd>+<kbd>3</kbd> dá `#`, <kbd>AltGr</kbd>+<kbd>,</kbd> dá `<` atd.

Dále pak poskytuje některé další užitečné znaky:

Klávesa                                           | Výsledek s <kbd>AltGr</kbd> | Popis
------------------------------------------------- | ------------------ | -----
<kbd>AltGr</kbd>+<kbd>Shift</kbd>+<kbd>Q</kbd>    | `„`                | Levá česká dvojitá uvozovka
<kbd>AltGr</kbd>+<kbd>Shift</kbd>+<kbd>W</kbd>    | `“`                | Pravá česká / levá anglická dvojitá uvozovka
<kbd>AltGr</kbd>+<kbd>Shift</kbd>+<kbd>E</kbd>    | `”`                | Pravá anglická dvojitá uvozovka
<kbd>AltGr</kbd>+<kbd>Shift</kbd>+<kbd>R</kbd>    | `®`                | Registered trademark
<kbd>AltGr</kbd>+<kbd>Shift</kbd>+<kbd>T</kbd>    | `™`                | Trademark
<kbd>AltGr</kbd>+<kbd>Shift</kbd>+<kbd>O</kbd>    | `°`                | Značka stupně
<kbd>AltGr</kbd>+<kbd>P</kbd>                     | `′`                | Značka minut
<kbd>AltGr</kbd>+<kbd>Shift</kbd>+<kbd>P</kbd>    | `″`                | Značka vteřin
<kbd>AltGr</kbd>+<kbd>Shift</kbd>+<kbd>A</kbd>    | `’`                | Apostrof / pravá anglická jednoduchá uvozovka
<kbd>AltGr</kbd>+<kbd>Shift</kbd>+<kbd>S</kbd>    | `‚`                | Levá česká jednoduchá uvozovka
<kbd>AltGr</kbd>+<kbd>Shift</kbd>+<kbd>D</kbd>    | `‘`                | Pravá česká / levá anglická jednoduchá uvozovka
<kbd>AltGr</kbd>+<kbd>H</kbd>                     | `←`                | Šipka vlevo
<kbd>AltGr</kbd>+<kbd>J</kbd>                     | `↑`                | Šipka nahoru
<kbd>AltGr</kbd>+<kbd>K</kbd>                     | `↓`                | Šipka dolů
<kbd>AltGr</kbd>+<kbd>L</kbd>                     | `→`                | Šipka vpravo
<kbd>AltGr</kbd>+<kbd>Shift</kbd>+<kbd>H</kbd>    | `⇐`                | Dvojitá šipka vlevo
<kbd>AltGr</kbd>+<kbd>Shift</kbd>+<kbd>J</kbd>    | `⇑`                | Dvojitá šipka nahoru
<kbd>AltGr</kbd>+<kbd>Shift</kbd>+<kbd>K</kbd>    | `⇓`                | Dvojitá šipka dolů
<kbd>AltGr</kbd>+<kbd>Shift</kbd>+<kbd>L</kbd>    | `⇒`                | Dvojitá šipka vpravo
<kbd>AltGr</kbd>+<kbd>Shift</kbd>+<kbd>C</kbd>    | `©`                | Copyright
<kbd>AltGr</kbd>+<kbd>Shift</kbd>+<kbd>N</kbd>    | `–`                | Půlčtverčíková pomlčka (_n-dash_)
<kbd>AltGr</kbd>+<kbd>Shift</kbd>+<kbd>M</kbd>    | `—`                | Čtverčíková pomlčka (_m-dash_)
<kbd>AltGr</kbd>+<kbd>Shift</kbd>+<kbd>.</kbd>    | `…`                | Výpustka (trojtečka)
<kbd>AltGr</kbd>+<kbd>Space</kbd>                 | ` `                | Nezlomitelná mezera (_nbsp_)
<kbd>AltGr</kbd>+<kbd>Num+</kbd>                  | `±`                | Plusminus
<kbd>AltGr</kbd>+<kbd>Num-</kbd>                  | `−`                | Minus
<kbd>AltGr</kbd>+<kbd>Shift</kbd>+<kbd>Num-</kbd> | `∓`                | Minusplus
<kbd>AltGr</kbd>+<kbd>Num*</kbd>                  | `×`                | Násobení křížek
<kbd>AltGr</kbd>+<kbd>Shift</kbd>+<kbd>Num*</kbd> | `⋅`                 | Násobení tečka
<kbd>AltGr</kbd>+<kbd>Num/</kbd>                  | `÷`                | Dělení znak
<kbd>AltGr</kbd>+<kbd>Shift</kbd>+<kbd>Num/</kbd> | `∕`                | Dělení lomítko


Instalace
---------

Soubor `cz` umístěte do `/usr/share/X11/xkb/symbols/`, přičemž případně nahraďte původní verzi. Poté musíte ručně smazat soubory ve `/var/lib/xkb`, abyste vymazali systémovou cache (vizte [odpověď na SO][1]), zavolat `setxkbmap -layout cz` (X, [odpověď na SO][2]), či poslat D-Bus zprávu `dbus-send --session --type=signal --reply-timeout=100 --dest=org.kde.keyboard /Layouts org.kde.keyboard.reloadConfig` (KDE Plasma + Wayland, [odpověď na SO][3]), podle systému.


   [1]: https://stackoverflow.com/a/18123960/304138
   [2]: https://askubuntu.com/a/968338/146272
   [3]: https://askubuntu.com/a/1510142/146272
