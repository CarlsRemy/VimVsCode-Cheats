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
### Modes

|              |                                                                                             |
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
|Normal        |is the default mode of files when opening them for the first time. this is read only, since with this we can only cut with X, C and D |
|Insert        |It is the way that allows us to edit it. Crtl + c is blocked, if we press this we will only change to normal mode. this mode is activated from Normal mode with the i key or Insert key  |
|Visual		     |this is useful to make selections of words or fragments of a phrase, it is activated from Normal mode with v|
|Visual Inline |this is useful for making selections of entire paragraphs, it is activated from Normal mode with V|
|Visual Block  |this is useful for making Text Block selections, it is activated from Normal mode with Ctrl + v|
|Replace			 |as its name indicates, it is to replace the text, it is activated from the normal mode with R or by pressing the Insert key from the insertion mode|
                                                                                                                                
### Movement / Displacement

|         |     |
|---------|-----|
| <kbd>h</kbd> |allows us to move to the left. we encode the amount of characters that we will move with numbers example **4h** will move us 4 positions to the left |
| j 			|it would be the same as with **h** but moving down |
| k 			|we'll move up |
| l 			|we'll move to the right|
| gj      |this would be the same as **j** |
| gk			|this would be the same as **k** |
| gg      |we move to the first line, but we can also modify the line we go to, for example **40gg** positions us on line 40, if it does not exist it directs us to the last line|
| G       |it moves us to the last line, if it allows a numeric modifier|
| [[      |we move to the first line. does not allow numeric modifier|
| ]]      |we move to the  last line. does not allow numeric modifier|
| H       |we scroll to the visible top of the screen, it would be the same as pressing the **Page Up** key|
| M       |we move to the visible central part of the screen|
| L       |we scroll to the visible bottom of the screen, it would be the same as pressing the **Page Down** key|
| 0       |moves to the first character of a line, of the line we are on|
| ^       |moves to the first character of a **non-blank** line, of the line we are on
| $       |moves to the last character of a line, of the line we are on|
| _       |moves to the last character of a line, of the line we are on|
| g_      |moves to the last character of a **non-blank** line, of the line we are on|
| -       |moves up positioning it self in the first character that is **non-blank**|
| +       |moves down to the first **non-blank** character
| w       |moves to the first letter of each word, from right to the left and when finished go down to the next line|
| b       |moves to the first letter of each word, from left to right and when finished go up to the previous line  |
| e       |moves to the last letter of each word, from right to the left and when finished go down to the next line |
| ge      |moves to the last letter of each word, from left to right and when finished go up to the previous line   |
| {       |moves us one paragraph Up   |
| }	      |moves us one paragraph Down |


