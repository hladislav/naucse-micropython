## Instalace

Nejdříve propoj modul s počítačem přes USB kabel,
jako kdybys připojoval{{a}} třeba mobil.

> [note]
> Je potřeba použít kvalitní datový kabel.
> Nekvalitní nebo nedatové kabely (např. spousta kabelů k
> nabíječkám) jsou často nepoužitelné.

## Instalace `mpremote`

S modulem si budeme “povídat” pomocí speciálního programu jménem `mpremote`.
Je poměrně nový a nemáme s ním tolik zkušeností; kdyby na tvém počítači
nefungoval tak se koukni na starší ale ověřenější návody dole.

Nainstaluj si `mpremote` do virtuálního prostředí:

> [warning]
> Při instalaci pozor na překlepy!
> Knihovnu na stažení může nahrát kdokoli a některé knihovny můžou
> být „zavirované“.
> Instaluješ ověřenou knihovnu `mpremote` (**M**icro**P**ython **remote**).
> Jiné můžou být „zavirované“ -- podobný program na Internet může nahrát
> kdokoli.
> Kdybys omylem nainstaloval{{a}} něco jiného, pověz o tom odborníkovi,
> který zkontroluje co se ztalo.

```console
(env)$ python -m pip install mpremote
```

Pak spusť příkaz `mpremote`. Měl by se objevit následující text.

```console
(env)$ mpremote
Connected to MicroPython at /dev/ttyUSB0
Use Ctrl-] to exit this shell

>>>
```

Stiskni Enter a objeví se známé tři „zobáčky“, za které můžeš psát
příkazy Pythonu:

```console
Connected to MicroPython at /dev/ttyUSB0
Use Ctrl-] to exit this shell

>>> 1+1
2
```

Jak napovídá vypsaný text, pomocí <kbd>Ctrl</kbd>+<kbd>]</kbd> můžeš
`mpremote` ukončit.


## Ostatní návody

Kdyby `mpremote` nefungovalo, postupuj podle operačního systému na svém počítači:

* [Linux]({{ subpage_url('linux') }})
  * `mpremote` hlásí `device not found`
    * může se jednat o problém s oprávněními
    * Ubuntu: je potřeba sa přidat do skupiny `dialout`
      * `usermod -aG dialout JMENO_UZIVATELE`
    * Ostatní distra: je potřeba sa přidat do skupiny `uucp`
      * `usermod -aG uucp JMENO_UZIVATELE`
    * nezapomeňte restartovat počítač, po zadání příkazu `groups` by jste měli vidět
      příslušnou skupinu
  * může pomoct instalace `picocom`
* [macOS]({{ subpage_url('macos') }})
  * může pomoct instalace `screen`
* [Windows]({{ subpage_url('windows') }})
  * `mpremote` hlásí `device not found`
    * možná chybějí ovladače: https://www.pololu.com/docs/0j7/all#2
  * může pomoct instalace PuTTY

Kdyby něco nefungovalo, poraď se s koučem.

Po zprovoznění `picocom`, PuTTY nebo `screen`, pravděpodobně začne fungovat
i `mpremote`. Zkus ho znovu, později se bude hodit!
