# Conoscenze preliminari

Per seguire questo workshop, assicurati di soddisfare i prerequisiti indicati di seguito.
<!-- 
## Software richiesto

* VSCode con estensione ESP-IDF installati<br>
   _Puoi seguire [la guida in questa repo](../setup/README.md)_

> [!WARNING]
> Si consiglia vivamente di installare **VS Code** e il plugin **ESP-IDF** *prima* dell’inizio del workshop.
> In caso di problemi, sarà comunque disponibile del tempo durante il primo esercizio per completare l’installazione.


## Hardware richiesto

* La scheda **ESP-C3-DevKit-RUST-2** (fornita durante il workshop).
  *È possibile utilizzare anche una scheda **ESP32-C3-Devkit**, ma in tal caso sarà necessario adattare la configurazione dei pin GPIO.*

--- -->

## Conoscenze di base

* Elettronica di base

  * Resistenze, condensatori, alimentatori DC/DC
  * Lettura di un semplice schema elettrico
* Programmazione embedded di base
  * Memoria Flash
  * Differenza tra “compilare” e “flashare”
  * Conoscenza di base delle periferiche standard dei microcontrollori (almeno GPIO e I2C)
* Fondamenti del linguaggio C
  * file header
  * compilatore / linker
  * `define`
  * `struct` e `typedef`
* Formati [JSON](https://it.wikipedia.org/wiki/JavaScript_Object_Notation) e [YAML](https://it.wikipedia.org/wiki/YAML)
* HTML e i suoi principali tag (`<html>`, `<body>`, `<h1>`, `<h2>`, `<p>`)
* Conoscenza di base dei metodi di richiesta HTTP (`GET`, `POST`) e del concetto di URI e route

## Tabella riferimenti

| Prerequisito              | Descrizione                                                                                                               | Riferimento                                                                                                                                                                          |
| ------------------------- | ------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Tipi di memoria MCU       | Differenza tra Flash, RAM ed EEPROM                                                                                       | [L. Harvie (Medium)](https://medium.com/@lanceharvieruntime/embedded-systems-memory-types-flash-vs-sram-vs-eeprom-93d0eed09086)                                                      |
| Periferiche seriali MCU   | Differenza tra SPI, I2C e UART                                                                                            | [nextpcb.com](https://www.nextpcb.com/blog/spi-i2c-uart)                                                                                                                             |
| File header e linker      | A cosa servono i file header e qual è il ruolo del linker                                                                 | [CBootCamp](https://gribblelab.org/teaching/CBootCamp/12_Compiling_linking_Makefile_header_files.html), [themewaves](https://themewaves.com/understanding-linkers-in-c-programming/) |
| JSON                      | Formato di dati indipendente dal linguaggio, derivato da JavaScript. Base delle API REST                                  | [Wikipedia](https://en.wikipedia.org/wiki/JSON)                                                                                                                                      |
| YAML                      | Formato leggibile per la serializzazione di dati, utilizzato per la gestione delle dipendenze tramite `idf_component.yml` | [Wikipedia](https://en.wikipedia.org/wiki/YAML), [datacamp.com](https://www.datacamp.com/blog/what-is-yaml)                                                                          |
| Tag HTML                  | Introduzione ai tag HTML di base                                                                                          | [Freecodecamp](https://www.freecodecamp.org/news/introduction-to-html-basics/)                                                                                                       |
| Metodi di richiesta HTTP  | Introduzione ai metodi di richiesta HTTP (GET, POST, ecc.) e loro differenze                                              | [Restfulapi.net](https://restfulapi.net/http-methods/)                                                                                                                               |
| Plugin ESP-IDF per VSCode | Estensione ufficiale Espressif per VSCode                                                                                 | [vscode-esp-idf-extension installation](https://github.com/espressif/vscode-esp-idf-extension?tab=readme-ov-file#how-to-use)                                                         |


