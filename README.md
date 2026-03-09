# Giant Leap Site

Sito ufficiale di **Giant Leap**, org italiana di Star Citizen. Costruito con [Hugo](https://gohugo.io/) e il tema [Blowfish](https://blowfish.page/).

Deploy: [giantleapsite.netlify.app](https://giantleapsite.netlify.app/)

## Requisiti

- [Hugo](https://gohugo.io/installation/) (extended version)
- Git (per i submodule del tema)

## Primo avvio

Clona il repo con i submodule:

```bash
git clone --recurse-submodules <repo-url>
cd giant-leap-site
```

Se hai già clonato senza `--recurse-submodules`:

```bash
git submodule update --init --recursive
```

## Avviare il server di sviluppo

```bash
hugo server
```

Il sito sarà disponibile su [http://localhost:1313](http://localhost:1313) con live reload.

Per un avvio più veloce (esclude `content/guides` e `content/users`):

```bash
hugo server -e development
```

## Build produzione

```bash
hugo
```

L'output viene generato nella cartella `public/`.

## Aggiungere un post al Diario di Bordo

```bash
hugo new content/diario-di-bordo/titolo-post/index.md
```

I nuovi post vengono creati con `draft: true`. Per pubblicare, impostare `draft: false` nel front matter.
