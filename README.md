# Neovim defaults for Vim

This tiny plug-in sets options to Neovim's default values where they differ from
Vim's defaults. Intended for use by those who share configuration between Vim
and Neovim and don't want to set redundant options in their nvimrc.

See also [Sensible.vim][sensible] for additional sensible defaults.

If you use a plug-in manager, such as vim-plug, you can load it conditionally:

```vim
if !has('nvim')
  Plug 'noahfrederick/vim-neovim-defaults'
endif
```

Or using Pathogen:

```vim
let g:pathogen_disabled = []

if has('nvim')
  call add(g:pathogen_disabled, 'vim-neovim-defaults')
endif
```

You must first source the plug-in before overriding one or more of these
defaults in your vimrc:

```vim
runtime! plugin/neovim_defaults.vim

" ...
```

Otherwise you may place overrides in `after/plugin/neovim_defaults.vim`.

## Credits and License

Copyright © Noah Frederick. Distributed under the same terms as Vim itself.
See `:help license`.

[sensible]: https://github.com/tpope/vim-sensible
