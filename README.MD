# МАГИСТЕРСКАЯ ДИССЕРТАЦИЯ

Этот репозиторий содержит мою магистерскую диссертацию

## Включает
 - диссертацию (LaTeX)
 - автореферат (LaTeX)
 - презентацию к защите (MS Power Point)
 - всё вышеперечисленное в формате pdf
 - множество лишних картинок

## Как собрать (один из вариантов)
TexLive:
	- базовая схема (plain и latex)
	- языки: английский, кириллица

Установить пакеты с помощью tlmgr:
```bash
$ tlmgr install <package>
```

Список пакетов: biber, latexmk, extsizes, biblatex, biblatex-gost, mathtools, titlesec, caption, enumitem, setspace, soul, csquotes, algorithms, algorithmicx, chngcntr, lastpage, logreq, float

Сборка:
```bash
$ latexmk -pdf  -bibtex  -synctex=1 -interaction=nonstopmode -output-directory=build thesis.tex 
$ latexmk -pdf  -bibtex  -synctex=1 -interaction=nonstopmode -output-directory=build 00-autoreferat.tex
```

Можно воспользоваться IDE TexStduio. Профиль с настройками: `cfg/texstudio_profile.txsprofile`.