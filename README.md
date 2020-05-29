# Generic testing

## Purpose

The purpose of this project is to assemble testing data in one central place. Often, either at work or on private projects, we see ourself writing ad hoc test data. This of course, isn't scientific, comparable or scalable.

## Example: `nlp >> da >> docs.json`

This specific document is useful when you are creating a sentencizer. The `meta` field are stating, that this document takes the form of an e-mail, are missing punctuations and includes emoji's. The document (`doc`) is splitted into sentences (`sentences`), which can be used to evaluate your sentencizer.

```json
{
    "doc": "Kære Carlsberg\n\nHvornår kommer der flere procenter i jeres øl 🤔\n\nDet er efterhånden som at drikke koldt pis\n\nMed venlig hilsen Tommy Kenter",
    "sentences": [
        "Kære Carlsberg",
        "Hvornår kommer der flere procenter i jeres øl 🤔",
        "Det er efterhånden som at drikke koldt pis",
        "Med venlig hilsen Tommy Kenter"
    ],
    "meta": {
        "doc": "mail",
        "sentences": ["missing punctuation", "emojis"]
    }
}
```