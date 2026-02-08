# Tasca-LMSGI04.1
Lenguajes de marcas y sistemas de gestión de información (DAM_LMSGI)


Aquí tens la informació dels exercicis transformada a format **Markdown**, estructurada per facilitar-ne la lectura i organitzada per seccions.

---

# Exercici 1: Gestió de dades CIFP Pau Casesnoves

L'objectiu és representar la informació d'alumnes i professors mitjançant diferents formats de dades (XML, DTD, XSD i JSON).

## Estructura del Document

* **Arrel:** `<cifp>`
* **Contingut:** Múltiples elements `<alumne>` i `<professor>`.

### 1. Elements comuns

Tant `alumne` com `professor` han de tenir:

* **id:** Atribut obligatori (integer).
* **nom:** Element obligatori (string).
* **llinatges:** Element obligatori (string).
* **data_naixement:** Opcional (string).
* **correu:** Opcional (string).
* **telefon:** Opcional (string).
* **adreça:** Opcional (string).

### 2. Elements específics

| Tipus | Elements Obligatoris | Valors Restringits |
| --- | --- | --- |
| **Alumne** | `data_matricula`, `curs` | DAM, DAW, ASIX, SMX, SEIA, ER, AUT |
| **Professor** | `data_incorporació`, `departament` | Informàtica, Electricitat, Automoció |

#### Detalls de l'element `assignatura` (Professor)

Es tracta d'un element opcional i repetible que conté:

* **id_assignatura:** Atribut obligatori (integer).
* **nom_assignatura:** Element obligatori (string).
* **cicle:** Atribut obligatori de `nom_assignatura` (mateixos valors restringits que `curs`).


* **data_inici / data_final:** Opcional (string).

---

## Tasques a realitzar

1. **1.1. DTD:** Crear un fitxer amb la definició del vocabulari.
2. **1.2. XML (DTD):** Document XML vàlid que referenciï el DTD extern.
3. **1.3. XSD:** Fitxer XML Schema (identificadors com `integer`, la resta `string`).
4. **1.4. XML (XSD):** Document XML vàlid que referenciï l'esquema XSD.
5. **1.5. JSON Schema:** Representació del vocabulari.
* *Nota:* `alumne` i `professor` han de ser arrays dins de `cifp`. `assignatura` també és un array.


6. **1.6. JSON:** Document JSON vàlid que compleixi l'esquema anterior.

---

# Exercici 2: Sindicació de Continguts

A partir d'un document HTML sobre notícies de motor, cal generar formats de subscripció.

## Font de dades (HTML)

* **Títol:** Notícies sobre cotxes.
* **Notícia 1:** Ferrari presenta el seu nou model híbrid, el SF-2024 (14/11/2024).
* **Notícia 2:** Volkswagen anuncia una inversió de 10.000 milions (12/11/2024).

## Tasques a realitzar

* **2.1. Document RSS:** Crear el fitxer RSS i validar-lo al [W3C Feed Validator](https://validator.w3.org/feed/). Incloure captura de pantalla de la validació.
* **2.2. Document Atom:** Crear el fitxer Atom a partir del mateix HTML i validar-lo. Incloure captura de pantalla.

---

# ⚠️ Instruccions Importants per al lliurament

> [!IMPORTANT]
> **La validesa és prioritària:** Si un arxiu (DTD, XSD o XML) presenta errors de validació, l'apartat **no puntuarà**. És preferible entregar un document amb menys requeriments però que sigui vàlid, que un de complet amb errors sintàctics.

* **Eines:** Recorda que *XML Copy Editor* no valida la forma dels fitxers `.dtd`, només dels `.xml`.
* **Entrega:** S'han d'adjuntar els fitxers de codi generats i el document d'explicacions amb les captures de les validacions.

---


