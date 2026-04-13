# Portfolio Website | Salvatore De Roma

![Logo del progetto](./assets/img/svg/logo02_white.svg)

Portfolio personale multipagina realizzato in HTML e SCSS per presentare profilo, progetti e contatti in una struttura chiara, responsive e modulare.

## Obiettivo Del Progetto

L'obiettivo del progetto è creare un sito portfolio statico che:

- presenti in modo professionale il profilo di Salvatore De Roma;
- raccolga in sezioni distinte Home, About, Projects, CV e Contact;
- mantenga una base di codice semplice da aggiornare;
- usi SCSS modulare per gestire layout, componenti e responsive design;
- applichi una nomenclatura BEM coerente nelle classi principali.

## Caratteristiche Principali

- Sito multipagina con pagine HTML separate.
- Layout responsive per mobile, tablet e desktop.
- Header con menu mobile e navigazione adattiva.
- SCSS organizzato per `abstract`, `base`, `components`, `layout` e `pages`.
- CSS compilato in `dist/css/main.css`.
- Componenti riutilizzabili, come il bottone `.btn`.

## Stack Tecnologico

- HTML5
- SCSS
- CSS3
- Google Fonts: `Figtree`

## Struttura Del Progetto

```text
.
├── CV_page.html
├── README.md
├── about_page.html
├── assets
│   └── img
│       ├── favicon
│       │   ├── apple-touch-icon.png
│       │   ├── favicon-96x96.png
│       │   ├── favicon.ico
│       │   ├── favicon.svg
│       │   ├── site.webmanifest
│       │   ├── web-app-manifest-192x192.png
│       │   └── web-app-manifest-512x512.png
│       ├── social_icon
│       │   ├── facebook.png
│       │   ├── instagram-2.png
│       │   └── linkedin-2.png
│       ├── svg
│       │   ├── image_seo_salvatoreDeRoma.jpg
│       │   ├── logo02_white.svg
│       │   ├── logo_deroma_salvatore.svg
│       │   ├── logo_deroma_salvatore_small.svg
│       │   ├── logo_deroma_salvatore_white.svg
│       │   ├── logo_deroma_salvatore_white2.jpg
│       │   └── logo_deroma_salvatore_white2.svg
│       ├── foto_salvatore_deRoma.jpg
│       ├── jsCounterCopertina.jpg
│       └── project_placeHolder.jpg
├── contact_page.html
├── dist
│   └── css
│       ├── main.css
│       └── main.css.map
├── index.html
├── project_page.html
└── src
    └── scss
        ├── abstract
        │   ├── _transactions.scss
        │   └── _variables.scss
        ├── base
        │   ├── _normalize.scss
        │   └── _reset.scss
        ├── components
        │   ├── _button.scss
        │   └── _cardStyle.scss
        ├── layout
        │   ├── _footerStyle.scss
        │   ├── _header.scss
        │   └── _heroSection.scss
        ├── pages
        │   ├── _abouteMePage.scss
        │   ├── _contactPage.scss
        │   ├── _cvPage.scss
        │   ├── _homePage.scss
        │   └── _projectPageStyle.scss
        └── main.scss
```

## Organizzazione SCSS

Il file entrypoint e `src/scss/main.scss`, che importa i moduli del progetto:

- `abstract/_variables.scss`: variabili globali di colori, font e radius.
- `abstract/_transactions.scss`: transizioni e timing riutilizzabili.
- `base/_reset.scss` e `base/_normalize.scss`: base di stile cross-browser.
- `components/_button.scss`: componenti riutilizzabili.
- `components/_cardStyle.scss`: card riutilizzabili.
- `layout/*.scss`: stili condivisi per header, hero e footer.
- `pages/*.scss`: stili specifici delle varie pagine.
- `dist/css/main.css`: output compilato pronto per il browser.

## Convenzione BEM Negli SCSS

Nel progetto viene usata una nomenclatura in stile BEM per mantenere leggibili blocchi e sotto-elementi.

Esempi reali presenti nel codice:

```scss
.header {
    &__image { ... }
}

.menu {
    &__list {
        &__items { ... }
    }
}

.hero {
    &__title { ... }
    &__title--small { ... }
}

.form {
    &__fieldset { ... }
    &__group { ... }
    &__input {
        &__areaText { ... }
    }
}
```

Lettura rapida:

- `.hero` è il block
- `.hero__title` è un elemento del block
- `.hero__title--small` è un modifier dell'elemento

Nota tecnica: in alcuni punti il progetto usa una variante molto annidata, ad esempio `.menu__list__items` o `.form__input__areaText`. Funziona, ma in ottica BEM più rigorosa potresti in futuro semplificare alcuni nomi per rendere i blocchi ancora più chiari.

## Pagine Del Sito

- `index.html`: homepage e presentazione principale.
- `about_page.html`: sezione descrittiva personale.
- `project_page.html`: raccolta progetti.
- `contact_page.html`: form contatti.
- `CV_page.html`: pagina CV.

## Come Avviare Il Progetto

Per visualizzare il sito:

1. Clona o scarica la repository.
2. Apri `index.html` nel browser.
3. Naviga tra le altre pagine dal menu.

## Compilazione SCSS

Per ricompilare il CSS a partire dagli SCSS:

```bash
sass src/scss/main.scss dist/css/main.css
```

Il source map viene generato in `dist/css/main.css.map`.

## Identita Visiva

Il progetto usa una palette semplice e riconoscibile, definita in `src/scss/abstract/_variables.scss`:

- `rgb(6, 174, 213)` come colore principale
- `#018fae` come variante scura
- `#000` e `#fff` per contrasto e leggibilita

## Autore

Salvatore De Roma

- LinkedIn: <https://www.linkedin.com/in/salvatore-de-roma-755728222>
- Facebook: <https://www.facebook.com/totore.deroma/>
- Instagram: <https://www.instagram.com/salvatore_de_roma>

## Licenza

Progetto realizzato per finalita formative e di portfolio personale.
