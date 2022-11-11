# Vim VsCode Cheats Sheet

## Introduction

In this document, I'll share my Vim learnings for the **[VS. Code](https://code.visualstudio.com)**, as well as any tips I find useful about that tool or extension.

Also remember to check the official documentation [VSCodeVim](https://github.com/VSCodeVim/Vim)

<p align="center" width="100%">
    <img width="40%" src="https://raw.githubusercontent.com/VSCodeVim/Vim/master/images/icon.png"> 
</p>


## First advice or clarification

The letters change their behavior depending on whether they are uppercase or lowercase. By using Shift we tell vim not to add any modifiers to the operator (key pressed), otherwise with lower case it will wait for a second and even a third parameter for its execution.

As an example of this we have the D key. where pressing d with Caps Lock active or pressing the d key and Shift will cut the text from the pointer position to the end of the line, where doing it with lowercase d will do nothing until a second press of the same key is passed a modifier (w of word, s sentence, p of paragraph among others)


