### [Link to vim.org](http://www.vim.org/scripts/script.php?script_id=1735)

### Install
Throw **[echofunc.vim](https://github.com/mbbill/echofunc/blob/master/plugin/echofunc.vim)** into *plugin* directory and that's all.

### How to use
1. *echofunc.vim* get function information from tags file. So first of all you need to create tags for your code.
Use the following command to generate tags with language and signature fields:
$ctags -R --fields=+lS .
1. *echofunc.vim* maps **(** in insert mode in order to automatically display function info after left bracket is pressed. So please make sure the left bracket **(** is not mapped by other plugins. You may check it using `:imap (`.
1. The function info is displayed in message line by default. Since the message line may be flushed by other trivial messages, a better way is to show function info in status line by appendding `%{EchoFuncGetStatusLine()}` into your `statusline` option. 
1. Another feature of *echofunc.vim* is to privide a balloon tip when the mouse cursor hovers a function name, macro name, etc. This feature is enabled when `+balloon_eval` is compiled in.

### Screenshot
![](https://sites.google.com/site/mbbill/echofunc_demo1.png)
![](https://sites.google.com/site/mbbill/echofunc_demo1.png)

