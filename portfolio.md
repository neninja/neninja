- [ead](https://github.com/nenitf?tab=repositories&q=ead_&type=source)

```vim
" vimrc
" script para os meus commits padrões de aula
fun! NN_GitAula()
    let log = system("git log --pretty=format:\%s")
    vnew
    put=log
    normal! gg
    if search('^:tv: add aula')>0
        normal! 3W
        let s:numero_aula = expand('<cword>')+1
        echom system("git add -A && git commit -m \":tv: add aula ".s:numero_aula."\"")
    else
        echom system("git add -A && git commit -m \":tv: add aula 1\"")
    endif
    bdelete!
endfun

" vim
:call NN_GitAula
```
```vim
" vim
" para testes unitários
:!yarn test %:p:h:t
:!composer test %

" para executar o mesmo teste
:!!
```

- [poc](https://github.com/nenitf?tab=repositories&q=poc_&type=source)
- [exemplo](https://github.com/nenitf?tab=repositories&q=exemplo_&type=source)
- [template](https://github.com/nenitf?tab=repositories&q=template_&type=source)
