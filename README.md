OTRS Business Solution™ Manual
==============================

This repository contains the sources of the OTRS Business Solution™ manual.
They are located in en/ and stored in docbook format. The other languages are
automatically generated with the help of po4a and the translation files in i18n.


How to Generate HTML from the Sources
-------------------------------------

You need to install the xsltproc and docbook-xsl packages (names may vary depending
on your distribution).

Then you can run

```
cd /tmp
xsltproc --xinclude /usr/share/xsl/docbook-xsl/html/chunk.xsl /path/to/doc-otrsbusiness/en/book.xml
```

The paths may vary, on MacOS docbook-xsl is located in /opt/local/xsl/...


How to Validate the Sources
---------------------------

You need to install the xmllint and docbook-xml packages.

Then you can run
```
xmllint --postvalid --nonet --xinclude --noout /path/to/doc-otrsbusiness/en/book.xml
```

Generating Translation Sources Manually
---------------------------------------

If you add any new files, make sure to include them in `po4a.conf`.

Then you can run
```
po4a -v -k0 /path/to/doc-otrsbusiness/po4a.conf
```

The command will generate files for all supported languages.


Translating the Sources
-----------------------

Please refer to http://doc.otrs.org/developer/stable/en/html/translating-docs.html.
