readme
================

## Quarto

Quarto enables you to weave together content and executable code into a
finished document. To learn more about Quarto see <https://quarto.org>.

## Running Code

When you click the **Render** button a document will be generated that
includes both content and the output of embedded code. You can embed
code like this:

Версия ядра

``` {bash}
uname -r
```

Все сведения о ядре

``` {bash}
uname -a
```

release info

``` {bash}
lsb_release -a
```

release info

``` {bash}
cat /etc/*release*
```

Модель процессора

``` {bash}
cat /proc/cpuinfo | grep "model name"
```

Последние 30 строк кольцевого буфера ядра

``` {bash}
dmesg | tail -n 30
```

The `echo: false` option disables the printing of code (only output is
displayed).
