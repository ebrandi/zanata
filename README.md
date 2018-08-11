
# For Translators

It's preferable to use Zanata interface to translate documents.

If you want to translate documents through another tool, use always the .po
files, ignore .pot files, they are used only for Zanata.


# For Zanata administrators

The `.pot` files are used as template/source for all languages.
In future we could generate them in the `en_US.ISO8859-1` directory in FreeBSD
Doc repository.

The Zanata Command line client (CLI) is the perfect way to connect to a Zanata
server to push and pull content.

## zanata-cli

You can download [zanata-cli here](http://docs.zanata.org/en/release/client/).

### config

To config your zanata-cli:

```SHELL
cat ~/.config/zanata.ini
[servers]
translate_zanata_org.url=https://translate.zanata.org/
translate_zanata_org.username=YOUR_USERNAME
translate_zanata_org.key=YOUR_KEY
```

### main commands

Main commands to push and pull translations:

`zanata-cli push --push-type both  --locales pt-BR`
`zanata-cli push --push-type trans --locales pt-BR`

```
 --push-type TYPE                   : Type of push to perform on the server:
                                        "source" (default) pushes source documents only.
                                        "trans" pushes translation documents only.
                                        "both" pushes both source and translation documents.
```

`zanata-cli pull`
`zanata-cli pull --pull-type trans --locales pt-BR`

```
 --pull-type TYPE               : Type of pull to perform from the server: "source" pulls source documents only.
                                  "trans" (default) pulls translation documents only.
                                  "both" pulls both source and translation documents.
```
