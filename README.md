# Natural Docs test

Testing the integration between LilyPond files (.ly, .ily, .scm, .md, .txt) and Natural Docs

### Customisations
The Natural Docs `Project.txt` file has been configured to add Lilypond files (.ly, .ily), Scheme files (.scm), Markdown files (.md) as custom languages:

```
Language: Lilypond

   Extensions: ly ily

   Simple Identifier: lilypond

   Line Comment: %
   Block Comment: %{ %}

Language: Scheme

   Extension: scm

   Line Comment: ;
   Block Comment: #! !#

Language: Markdown

   Extension: md

   Block Comment: <!-- -->
```
### Additions to current Lilypond/Scheme Code
Every comment needs an additional line of code from Natural Docs preceeding it: `keyword: title`.

List of Keywords
https://www.naturaldocs.org/reference/keywords/

Example:
```
Title: gridly - simple segmented grid for LilyPond
Copyright (C) 2015 Matteo Ceccarello
```

### Running Natural Docs

Change to the Natural Docs directory:
`cd Natural Docs`
