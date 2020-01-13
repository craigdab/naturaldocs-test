# Lilypond-Natural Docs test case

Testing the integration between LilyPond files (.ly, .ily, .scm, .md, .txt) and Natural Docs

### Install and run
1. Download and install NaturalDocs from here:
https://www.naturaldocs.org/getting_started/getting_set_up/#download_and_install

2. To create documemtation run this code from the NaturalDocs folder:
```NaturalDocs.exe C:\My Project\Natural Docs Config Folder```
on Mac
```mono NaturalDocs.exe C:\My Project\Natural Docs Config Folder```


### Customisations
The Natural Docs `Project.txt` file has been configured to add custom languages for Lilypond files (.ly, .ily), Scheme files (.scm), and Markdown files (.md).

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
Every comment in a Lilypond, Scheme or Markdown file needs an additional line of code from Natural Docs preceeding it: `keyword: title`.

See this list of available Keywords
https://www.naturaldocs.org/reference/keywords/

Lilypond example:
```
\version "2.19.83"

%{
Title: openLilyLib package
Copyright (C) 2019 Author

About: License
For the GNU General Public License, see <http://www.gnu.org/licenses/>.
%}
```
or
```
\version "2.19.83"

% Title: openLilyLib package
% Copyright (C) 2019 Author
%
% About: License
% For the GNU General Public License, see <http://www.gnu.org/licenses/>.
```

Scheme example:
```
; Function: stack implementation
; a stack implementation with methods push, pop and get
(define-class <stack> ()
```
or
```
#!
Function: stack implementation
a stack implementation with methods push, pop and get
!#
(define-class <stack> ()
```

Markdown example:
```
<!--
Title: README file
Introduction to LilyPond package
-->
```
