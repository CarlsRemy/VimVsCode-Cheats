# Vim VsCode Cheats Sheet


## Introduction
---------------
In this document, I'll share my Vim learnings for the **[VS. Code](https://code.visualstudio.com)**, as well as any tips I find useful about that tool or extension.

Also remember to check the official documentation [VSCodeVim](https://github.com/VSCodeVim/Vim)

<p align="center" width="100%">
    <img width="40%" src="https://raw.githubusercontent.com/VSCodeVim/Vim/master/images/icon.png"> 
</p>


## First advice or clarification

Las letras cambian su funcionamiento según sean mayúsculas o minúsculas. Al usar Mayúsculas le indicamos a vim que no agregaremos ningún modificador al operador (tecla presionada), de lo contrario con minúsculas esperará un segundo e incluso un tercer parámetro para su ejecución.

As an example of this we have the D key. where pressing d with Caps Lock active or pressing the d key and Shift will cut the text from the pointer position to the end of the line, where doing it with lowercase d will do nothing until a second press of the same key is passed a modifier (w of word, s sentence, p of paragraph among others)


