---
title: Jak formatować kod
---

# Jak formatować kod {#code_style_guide_title}

Społeczność zgromadzona wokół języka PHP jest relatywnie duża i zróżnicowana, dzięki czemu powstało wiele bibliotek,
frameworków i komponentów. Typową praktyką stosowaną przez programistów PHP jest wybór kilku takich składników i
stworzenie na bazie tego własnego projektu. Stąd istotną sprawą jest to, aby te biblioteki stosowały wspólne konwencje
i styl kodowania.

Aby wyjść temu problemowi naprzeciw, [Framework Interop Group][fig] (znane także jako 'PHP Standards Group')
wypracowało serię rekomendacji dotyczących stylu kodowania znanych jako [PSR-0][psr0], [PSR-1][psr1],
[PSR-2][psr2] oraz [PSR-4][psr4]. Są one zbiorem konwencji i dobrych praktyk, których powinny trzymać się
programiści tworząc swoje projekty. Już teraz konwencje te stosują m.in. takie projekty jak Drupal,
Zend Framework, CakePHP, phpBB, AWS SDK, FuelPHP, czy Lithium. Oczywiście stosowanie tych zaleceń nie jest
obowiązkowe, równie dobrze możesz tworzyć kod używając swojego własnego stylu.

Decydując się na używanie PSR, ułatwiasz potencjalnym programistom, którzy będę z Tobą współpracować, zrozumienie
Twojego kodu. Struktura dokumentów PSR jest zorganizowana w ten sposób, że stosowanie PSR-1 wymusza stosowanie PSR-0,
ale nie PSR-2, itd.

* [Dowiedz się więcej o PSR-0][psr0]
* [Dowiedz się więcej o PSR-1][psr1]
* [Dowiedz się więcej o PSR-2][psr2]
* [Dowiedz się więcej o PSR-4][psr4]

Aby sprawdzić czy Twój kod spełnia założenia PSR, możesz użyć projektu [PHP_CodeSniffer][phpcs] z użyciem rozszerzenia
[phpcs-psr][phpcs-psr] lub wtyczek do edytorów tekstowych sprawdzających poprawność stylu w locie,
np.: wtyczka [sublime-phpcs][sublime-phpcs] dla edytora Sublime Text.
Aby automatycznie poprawić styl kodu możesz użyć jednego z narzędzi:

* [PHP Coding Standards Fixer][phpcsfixer]
* [PHP Code Beautifier and Fixer][phpcbf]

PHP_CodeSniffer użyty w linii poleceń

    phpcs -sw --standard=PSR2 file.php

wyświetli listę błędów (odstępstw od standardu) wraz z informacją o sposobie usunięcia błędu.
Pakiet PHP_CodeSniffer zawiera drugie polecenie - `phpcbf` - pozwalające automatycznie naprawić wykryte błędy:

    phpcbf -w --standard=PSR2 file.php

PHP Coding Standards Fixer domyślnie naprawia błędy automatycznie, a z odpowiednimi parametrami
(`--dry-run` i `--diff`) wyświetla podsumowanie proponowanych zmian nie zmieniając plików.

Kod powinien być pisany z wykorzystaniem angielskiego nazewnictwa. Komentarze powinny być pisane w języku
zrozumiałym dla aktualnych oraz potencjalnych programistów.

[fig]: http://www.php-fig.org/
[psr0]: http://www.php-fig.org/psr/psr-0/
[psr1]: http://www.php-fig.org/psr/psr-1/
[psr2]: http://www.php-fig.org/psr/psr-2/
[psr4]: http://www.php-fig.org/psr/psr-4/
[phpcs]: http://pear.php.net/package/PHP_CodeSniffer/
[sublime-phpcs]: https://github.com/benmatselby/sublime-phpcs
[phpcs-psr]: https://github.com/klaussilveira/phpcs-psr
[phpcsfixer]: http://cs.sensiolabs.org/
[phpcbf]: https://github.com/squizlabs/PHP_CodeSniffer/wiki/Fixing-Errors-Automatically
