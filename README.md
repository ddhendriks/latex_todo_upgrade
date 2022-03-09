# latex_todo_upgrade
Package that combines todonotes and some mouseover utilities that allow for easy tracking of tasks

## requirements 
This package relies on two packages:
- `todonotes`: to track the tasks and provide the functionality around that
- `pdfcomment`: to provide mouseover additional information

## useage
### importing
To import this package:
```
\usepackage{<PATH TO tex_todo.sty without the file ending>}
```

as an example: 
```
\usepackage{/home/david/dotfiles/custom_tex/tex_todos/tex_todo}
```

There is currently 1 package option:
- `hide`

If we add that to the import:
```
\usepackage[hide]{/home/david/dotfiles/custom_tex/tex_todos/tex_todo}
```

All of the tasks and tasklist will be hidden from view.

### adding tasks
To register a task in somewhere in the text:

```
\newtodo{<inline text>}{<mouseover text>}
```

Example:
```
\newtodo{Update this number}{This number is based on old calulations and is not up to date.}
```

The second argument can be empty, but you then have to write it like this:
```
\newtodo{Update this number}{}
```

### Displaying list of tasks
To display the entire list of tasks:

```
\listoftodos
```

## Example documents:
An example document with the tasks: [example](example/main.pdf)
An example document with everything hidden: [example hide](example/main_hide.pdf)


## Note
Not all pdf viewers seem to handle the mouseover functionality. The ones that worked for me were:
- acroread
- overleaf
