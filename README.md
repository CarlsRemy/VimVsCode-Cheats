# Vim VsCode Cheats Sheet

## Introduction

In this document, I'll share my Vim learnings for the **[VS. Code](https://code.visualstudio.com)**, as well as any tips I find useful about that tool or extension.

Also remember to check the official documentation [VSCodeVim](https://github.com/VSCodeVim/Vim)

<p align="center" width="100%">
    <img width="40%" src="https://raw.githubusercontent.com/VSCodeVim/Vim/master/images/icon.png"> 
</p>


## First advice or clarification

The letters change their behavior depending on whether they are uppercase or lowercase. By using <kbd>Shift</kbd> we tell vim not to add any modifiers to the [Operator](#Operators), otherwise with lower case it will wait for a second and even a third parameter for its execution.

As an example of this we have the <kbd>D</kbd> key. where pressing d with <kbd>Caps Lock</kbd> active or pressing the <kbd>d</kbd> key and <kbd>Shift</kbd> will cut the text from the pointer position to the end of the line, where doing it with lowercase d will do nothing until a second press of the same key is passed a modifier (<kbd>w</kbd> of word, <kbd>s</kbd> sentence, <kbd>p</kbd> of paragraph among others)
### Modes

|              |                                                                                             |
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
|Normal        |is the default mode of files when opening them for the first time. this is read only, since with this we can only cut with <kbd>X</kbd>, <kbd>C</kbd>, <kbd>S</kbd>  and <kbd>D</kbd> |
|Insert        |It is the way that allows us to edit it. <kbd>Crtl</kbd> + <kbd>c</kbd> is blocked, if we press this we will only change to normal mode. this mode is activated from Normal mode with the <kbd>i</kbd> key or <kbd>Insert</kbd> key  |
|Visual		     |this is useful to make selections of words or fragments of a phrase, it is activated from Normal mode with <kbd>v</kbd>|
|Visual Inline |this is useful for making selections of entire paragraphs, it is activated from Normal mode with <kbd>V</kbd>|
|Visual Block  |this is useful for making Text Block selections, it is activated from Normal mode with <kbd>Ctrl</kbd> + <kbd>v</kbd>|
|Replace			 |as its name indicates, it is to replace the text, it is activated from the normal mode with <kbd>R</kbd> or by pressing the <kbd>Insert</kbd> key from the insertion mode|
                                                                                                                                
### Movement / Displacement


|         |     |
|---------|-----|
| <kbd>h</kbd>  |allows us to move to the left. we encode the amount of characters that we will move with numbers example **<kbd>4</kbd> + <kbd>h</kbd>** will move us 4 positions to the left |
| <kbd>j</kbd>	|it would be the same as with **<kbd>h</kbd>** but moving down |
| <kbd>k</kbd>	|we'll move up |
| <kbd>l</kbd> 	|we'll move to the right|
| <kbd>g</kbd>+<kbd>j</kbd> |this would be the same as **<kbd>j</kbd>** |
| <kbd>g</kbd>+<kbd>k</kbd>	|this would be the same as **<kbd>k</kbd>** |
| <kbd>g</kbd>+<kbd>g</kbd> |we move to the first line, but we can also modify the line we go to, for example **<kbd>8</kbd>+<kbd>g</kbd>+<kbd>g</kbd>** positions us on line 8, if it does not exist it directs us to the last line|
| <kbd>G</kbd>  |it moves us to the last line, if it allows a numeric modifier|
| <kbd>[</kbd>+<kbd>[</kbd> |we move to the first line. does not allow numeric modifier|
| <kbd>]</kbd>+<kbd>]</kbd> |we move to the  last line. does not allow numeric modifier|
| <kbd>H</kbd>  |we scroll to the visible top of the screen, it would be the same as pressing the **<kbd>Page Up</kbd>** key|
| <kbd>M</kbd>  |we move to the visible central part of the screen|
| <kbd>L</kbd>  |we scroll to the visible bottom of the screen, it would be the same as pressing the **<kbd>Page Down</kbd>** key|
| <kbd>0</kbd>  |moves to the first character of a line, of the line we are on|
| <kbd>^</kbd>  |moves to the first character of a **non-blank** line, of the line we are on
| <kbd>$</kbd>  |moves to the last character of a line, of the line we are on|
| <kbd>_</kbd>  |moves to the last character of a line, of the line we are on|
| <kbd>g</kbd>+<kbd>_</kbd> |moves to the last character of a **non-blank** line, of the line we are on|
| <kbd>-</kbd>  |moves up positioning it self in the first character that is **non-blank**|
| <kbd>+</kbd>  |moves down to the first **non-blank** character
| <kbd>w</kbd>  |moves to the first letter of each word, from right to the left and when finished go down to the next line|
| <kbd>b</kbd>  |moves to the first letter of each word, from left to right and when finished go up to the previous line  |
| <kbd>e</kbd>  |moves to the last letter of each word, from right to the left and when finished go down to the next line |
| <kbd>g</kbd>+<kbd>e</kbd> |moves to the last letter of each word, from left to right and when finished go up to the previous line   |
| <kbd>(</kbd>  |moves to the next sentence|
| <kbd>)</kbd>	|moves to the previous sentence|
| <kbd>{</kbd>  |moves us one paragraph Up   |
| <kbd>}</kbd>	|moves us one paragraph Down |
| <kbd>%</kbd>  |it moves between the start and end blocks of {},[], () |
| <kbd>z</kbd>+<kbd>z</kbd> |scroll the line with the cursor to the center of the screen
| <kbd>z</kbd>+<kbd>t</kbd> |scroll the line with the cursor to the top
| <kbd>z</kbd>+<kbd>b</kbd> |scroll the line with the cursor to the bottom



### Operators 


operators support numeric values, [moves](#movement--displacement) such as k,w and modifiers. example <kbd>2</kbd> + <kbd>c</kbd> + <kbd>i</kbd> + <kbd>"</kbd> which can be translated as it will cut 2 lines from its position down everything that is inside "

these do not change their function when changing from lowercase to uppercase, they only stop admitting modifiers at the end of them.


|                |     |
|----------------|-----|
| <kbd>c</kbd>   |cuts a line, but does not delete it. after this we will return to insert mode.
| <kbd>d</kbd>   |performs the same function as <kbd>c</kbd> but without changing modes
| <kbd>s</kbd>   |cut character and return to insert mode. only accepts numeric modifiers
| <kbd>S</kbd>   |cut line and return to insert mode. only accepts numeric modifiers
| <kbd>x</kbd>   |cut character below the cursor. only accepts numeric modifiers
| <kbd>X</kbd>   |cut character before cursor. only accepts numeric modifiers
| <kbd>o</kbd>   |inserts a blank line after the line where the cursor is positioned and returns to insert mode. only accepts numeric modifiers  
| <kbd>O</kbd>   |inserts a blank line before the line where the cursor is positioned and returns to insert mode. only accepts numeric modifiers  
| <kbd>y</kbd>   |copy without cutting the text  
| <kbd>p</kbd>   |paste the copied text 
| <kbd>~</kbd>   |change a character from uppercase to lowercase and vice versa. only accepts numeric modifiers   
| <kbd>~</kbd> + <kbd>~</kbd>|is similar to ***~*** but this will do the whole line instead
| <kbd>g</kbd>+<kbd>u</kbd>+<kbd>u</kbd>|change the entire line to lowercase 
| <kbd>g</kbd>+<kbd>U</kbd>+<kbd>U</kbd>|change the entire line to uppercase
| <kbd>u</kbd>   |undo last change. only accepts numeric modifiers 
| <kbd>.</kbd>   |repeat last action. only accepts numeric modifiers
| <kbd>></kbd>+ <kbd>></kbd> |will give a tab to the text. we can indicate the number of moons to affect, <kbd>2</kbd>+<kbd>></kbd>+ <kbd>></kbd> or  <kbd>></kbd>+ <kbd>2</kbd> + <kbd>></kbd> where either of these two ways will have the same result affecting 2 lines|
| <kbd><</kbd>+<kbd><</kbd> |will remove a tab from the text
| <kbd>g</kbd>+<kbd>p</kbd> |paste after cursor
| <kbd>g</kbd>+<kbd>P</kbd> |paste before cursor
| <kbd>g</kbd>+<kbd>c</kbd>+<kbd>c</kbd> |make a comment in line
| <kbd>g</kbd>+<kbd>C</kbd>+<kbd>C</kbd> |make a comment in blocks
| <kbd>g</kbd>+<kbd>c</kbd>+<kbd>-</kbd> |comment up. we can indicate how many lines up we want to affect in this way  <kbd>g</kbd>+<kbd>C</kbd>+<kbd>2</kbd>+<kbd>-</kbd> , here we indicate that we want to affect 2 lines |
| <kbd>g</kbd>+<kbd>c</kbd>+<kbd>+</kbd> |is very similar to the previous sentence with the deference that this one goes down |
| <kbd>J</kbd> |join the line where we are positioned with the line below with a space between both |
| <kbd>g</kbd>+<kbd>J</kbd> |Similar to the previous statement only this one does not add any space
| <kbd>g</kbd>+<kbd>t</kbd> |allow us to move to the next tab. if we pass a numeric modifier to the tab that corresponds to the number we pass
| <kbd>g</kbd>+<kbd>T</kbd> |allow us to move to the previous tab. If we pass a numeric modifier, it will move as many tabs back as we indicate. example if we are in sale 2 and spend  <kbd>2</kbd>+<kbd>g</kbd>+<kbd>T</kbd>  this will be positioned in the last


### Modifiers

    
|                |     |
|----------------|-----|
| <kbd>i</kbd>   |represents the part inside a text, example the text that is inside " " |
| <kbd>a</kbd>   |renders the entire text object, including "", (), spaces, tabs |
| <kbd>s</kbd>   |represents the sentences    |
| <kbd>p</kbd>   |represents the paragraphs   |
| <kbd>b</kbd>   |represents the blocks of () |
| <kbd>B</kbd>   |represents the blocks of {} |
| <kbd>t</kbd>   |represents the tag blocks <>.for this to work we must indicate em modifier a or i before this since there is another modifier that works with the T, this would be the way to do it <kbd>c</kbd>+<kbd>a</kbd>+<kbd>t</kbd>  |
| <kbd>/</kbd>   |represents the text from the cursor position to the appearance of the search occurrence, if it is not found it will do nothing, example <kbd>d</kbd> <kbd>/</kbd> ***fire*** will delete all the text found before the word fire |
| <kbd>f</kbd>   |represents the text from to the position of the occurrence including itself, it searches for characters |
| <kbd>F</kbd>   |it is similar to the previous sentence only that it looks for the previous occurrence |
| <kbd>t</kbd>   |represents the text from to the position of the occurrence does not include itself, it searches for characters |
| <kbd>T</kbd>   |it is similar to the previous sentence only that it looks for the previous occurrence |
| <kbd><</kbd>   |represent that character | 
| <kbd>></kbd>   |represent that character | 
| <kbd>(</kbd>   |represent that character |  
| <kbd>)</kbd>   |represent that character | 
| <kbd>{</kbd>   |represent that character |  
| <kbd>}</kbd>   |represent that character | 
| <kbd>[</kbd>   |represent that character | 
| <kbd>]</kbd>   |represent that character |
| <kbd>"</kbd>   |represent that character | 
| <kbd>'</kbd>   |represent that character | 
| <kbd>`</kbd>   |represent that character | 

### Visual mode

|                           |     |
|---------------------------|-----|
| <kbd>a</kbd>+<kbd>w</kbd> | select a word              |
| <kbd>a</kbd>+<kbd>b</kbd> | select block of ()         |
| <kbd>a</kbd>+<kbd>B</kbd> | select block of {}         |
| <kbd>a</kbd>+<kbd>t</kbd> | select tag block <>        |
| <kbd>i</kbd>+<kbd>b</kbd> | select text inside ()      |
| <kbd>i</kbd>+<kbd>B</kbd> | select text inside {}      |
| <kbd>i</kbd>+<kbd>t</kbd> | select text inside tags <> |
| <kbd>o</kbd>              | moves the cursor between the last letter of the selection and the first | 

### Search

allows us to search the current file easily. allows us to use Regular Expression (regex), which is a huge advantage over Vs Code's built-in search engine. 

to search for a specific word we use < /> , it is useful when we search for words that could be contained in other words, for example sensitive and insensitive, it would be done ***/<sensitive/>***

|                |     |
|----------------|-----|
| <kbd>/</kbd>   |allows you to search forwards  |
| <kbd>?</kbd>   |allows you to search backwards |
| <kbd>#</kbd>   |af we are in normal mode, it allows us to search for the word under the cursor, then when it finds consistency, it allows us to scroll down between them |
| <kbd>*</kbd>   |performs the same function, only it allows us to scroll up|
| <kbd>n</kbd>   |next occurrence     |
| <kbd>N</kbd>   |previous occurrence |

### Flag search

|                |     |
|----------------|-----|
| <kbd>c</kbd>   |case insensitive |
| <kbd>C</kbd>   |case sensitive |




### Commands

the commands in vim begin with ":" followers of the sentence to be executed, the vast majority are descriptive and allow abbreviations which I will indicate with [] the syllables that are optional for their operation, example: w is the abbreviation for :write , which in the document will be written like this :w[rite]

|                |     |
|----------------|-----|
| :e[dit]        |create or edit file. we must indicate the file after said command example ***:e main.js***
| :w[rite]       |save a file
| :q[uit]        |close file. it will give an error if it finds unsaved changes
| :q!            |! at the end of the command causes the same to close discarding any unsaved changes
| :wq            |close and save changes
| :wa[ll]        |save changes to all files
| :qa[ll]        |close all files
| :tabnew        |open file in new tab
| :tabn[ext]     |move to the next tab
| :tabp[revious] |move to the previous tab
| :tabm[over]    |allows us to change the position of the tab, it goes from index 0
| :tabc[lose]    |close current tab
| :tab[only]     |close all tabs and keep open only the focused one
| :tabdo         |run command on all tabs example ***:tabdo wq*** (will save and close each tab)
| :sp[lit]	     |split into two windows, top half and bottom half
| :vs[plit]      |split into two windows, left and right
| :noh[lsearch]  |clear search
| :%s/ / /       |It is used to find and replace one text with another in a file. %s/Search/replace/flag where good search is the word or pattern to search for, replace the replacement obviously and flag [the filter or search flag](#flag-substitution)
| :.!            |we can execute terminal commands and add the text returned by it to our file. in windows we can execute cmd commands


### Flag substitution

|                |     |
|----------------|-----|
| <kbd>g</kbd>   |find each occurrence
| <kbd>i</kbd>   |case insensitive 
| <kbd>I</kbd>   |case sensitive
| <kbd>c</kbd>   |ask for confirmation before replacing. 

### Ranges

ranges are a good way to indicate a range of action for commands. 
these are written towards ***:.,2d*** where <kbd>d</kbd> is an [operator](#operators) to be executed

|                |     |
|----------------|-----|
| :%             |indicates that you want to affect the entire file |
| :.,2           |this range consists of 2 parts start qwhich in this case is <kbd>.</kbd> which is expressed as the current position of the cursor and the 2 indicates that the range ends at line 2 |
| :.,$           |this would be similar to the previous one with the slight difference that <kbd>$</kbd> implies that it will start at the current cursor position and end at the last line of the file. |
| :1,.-1         |here it is indicated that the range begins on line 1 and ends one line before the current position of the cursor, we can also do .+1 to indicate that it ends one line below the current position of the cursor |

### Other curious things 

|                |     |
|----------------|-----|
| <kbd>i</kbd>   |return to insert mode place the cursor one character before the previous position
| <kbd>I</kbd>   |return to insert mode place cursor on first character
| <kbd>a</kbd>   |return to insert mode place cursor on last character
| <kbd>A</kbd>   |return to insert mode place the cursor one character after the previous position
| <kbd>e</kbd> <kbd>a</kbd> |will return to insert mode by placing the cursor on the last letter of the word in which we were positioned |
| <kbd>g</kbd>+<kbd>d</kbd> |go to the definition of the word under the cursor |


