# Changes applied after fork
1. Changed DiagnosticUnderline highlights to use undercurl instead.

# Solarized Neovim

This aims to be a complete port [vim-solarized8](https://github.com/lifepillar/vim-solarized8) with support for lua
plugins, LSP and Treesitter for neovim 0.5.

## NOTE
Also added 8 bit color support.(Can't be a complete port if the theme isn't accessible for all neovim users.)
I used this Javascript [code](https://gist.github.com/ishan9299/d87713b43dc04d49fa060711fdc7dd6d) to convert the rgb to
neared 8 bit color.

## Installation

### VIM Packages
```
git submodule add --name nvim-solarized-lua https://github.com/ishan9299/nvim-solarized-lua
pack/packages/start/solarized
```

### Plug
```
Plug 'ishan9299/nvim-solarized-lua'
```

## Options
- **italics**
Enable italics for comments (default: enabled)

```lua
vim.g.solarized_italics = 1
```

- **visibility**
SpecialChars (like trailing whitespace and tabs) visibility
  + low
  + normal (default)
  + high

```lua
vim.g.solarized_visibility = 'normal'
```

- **diffmode**
  + low
  + normal (default)
  + high
 
```lua
vim.g.solarized_diffmode = 'normal'
```

- **termtrans**
If you want to keep the transparency in your terminal (default: disabled)

```lua
-- To enable transparency
if vim.fn.has('gui_running') == 0 then
    vim.g.solarized_termtrans = 0
else
    vim.g.solarized_termtrans = 1
end
```

- **statusline**
  + low
  + flat
  + normal (default)

 ```lua
 vim.g.solarized_statusline = 'normal'
 ```
  **NOTE** :-
  - If you set statusline option's `normal` and `flat` are the same when using the solarized-flat colorscheme.
  - This option doesn't affect the lua line plugin it has it's own solarized theme.

## Variants

- **solarized**

The normal solarized scheme.  
`vim.cmd('colorscheme solarized')`

- **solarized-high**

This one has a higher contrast ratio.  
`vim.cmd('colorscheme solarized-high')`

- **solarized-flat**

This is the flat variant.  
`vim.cmd('colorscheme solarized-flat')`

- **solarized-low**

This is the low contrast option.  
`vim.cmd('colorscheme solarized-low')`

## Screenshots
![Screenshot from 2021-05-12 10-01-23](https://user-images.githubusercontent.com/47824004/117919013-e00da400-b309-11eb-845a-a54f675e7a90.png)


## TODO

- ~~The light colorscheme~~
- Plugins :-  
   - [x] LSP  
   - [x] Treesitter  
   - [x] Telescope  
   - [x] FZF  
   - [x] lualine  
   - [x] lspsaga
   - [x] nvim-navic

# NOTE
- Thanks for lifepillar's vim-solarized8 for providing most of the highlights and color codes for this scheme.
- If you have an issue with the highlight groups in theme open an issue but also mention the variant of the colorscheme
  you are using.
- If any more plugins are needed then open an issue.

## Maybe Checkout
- [modus-theme-vim](https://github.com/ishan9299/modus-theme-vim)
