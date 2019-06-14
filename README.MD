# МАГИСТЕРСКАЯ ДИССЕРТАЦИЯ

Этот репозиторий содержит мою магистерскую диссертацию

## Включает
 - Пояснительную записку ([pdf](build/thesis.pdf))
 - автореферат ([pdf](build/00-autoreferat.pdf))
 - презентацию к защите ([pdf](build/presentation.pdf), [раздатка](build/handout.pdf)) 
 - множество лишних картинок

## Как собрать (один из вариантов)
TexLive:
 - базовая схема (plain и latex)
 - языки: английский, кириллица

Установить пакеты с помощью tlmgr:
```bash
$ tlmgr install <package>
```

Список пакетов: 
```
biber, latexmk, extsizes, biblatex, biblatex-gost, mathtools, titlesec, caption, enumitem,
setspace, soul, csquotes, algorithms, algorithmicx, chngcntr, lastpage, logreq, float, cmap
```

Сборка:
```bash
$ latexmk -pdf  -bibtex  -synctex=1 -interaction=nonstopmode -output-directory=build thesis.tex 
$ latexmk -pdf  -bibtex  -synctex=1 -interaction=nonstopmode -output-directory=build 00-autoreferat.tex
```

Можно воспользоваться IDE TexStduio. Профиль с настройками: `cfg/texstudio_profile.txsprofile`.
