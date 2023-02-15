---
layout: newsletter
title: "Neovim News 2022"
category: newsletter
permalink: /news/2023/03
---


source: "https://twitter.com/Neovim/status/1454239184688984064"
---
![Neovim](images/Neovim-2386262630.jpg)
Neovim ([@Neovim](https://twitter.com/Neovim))

GitHub Copilot for [#neovim](https://twitter.com/hashtag/neovim)  ... by the great [@tpope](https://twitter.com/tpope) ! [twitter.com/tpope/status/1…](https://twitter.com/tpope/status/1453434985147510790)

[Tweet link](https://twitter.com/Neovim/status/1454239184688984064)


source: "https://twitter.com/Neovim/status/1504784802398023726"
---
![Neovim](images/Neovim-2386262630.jpg)
Neovim ([@Neovim](https://twitter.com/Neovim))

Try ":set laststatus=3" in Nvim HEAD:

[github.com/neovim/neovim/…](https://github.com/neovim/neovim/issues/9342)

[Tweet link](https://twitter.com/Neovim/status/1504784802398023726)


source: "https://twitter.com/Neovim/status/1521284137344245761"
---
![Neovim](images/Neovim-2386262630.jpg)
Neovim ([@Neovim](https://twitter.com/Neovim))

[#neovim](https://twitter.com/hashtag/neovim)  HEAD added nvim_parse_cmd. It's a step towards nvim_cmd([list]), and the "user cmd-preview" work!

:echo nvim_parse_cmd('.,$g/foo/bar', {})
{
 'cmd': 'global',
 'args': ['/foo/bar'],
 'mods': {…},
 'magic': {'file': v:false, 'bar': v:false}
}

[github.com/neovim/neovim/…](https://github.com/neovim/neovim/pull/18231)

[Tweet link](https://twitter.com/Neovim/status/1521284137344245761)


source: "https://twitter.com/Neovim/status/1521478149594353667"
---
![Neovim](images/Neovim-2386262630.jpg)
Neovim ([@Neovim](https://twitter.com/Neovim))

[#neovim](https://twitter.com/hashtag/neovim)  HEAD now sets [[$NVIM](https://twitter.com/search?q=%24NVIM)](https://twitter.com/search?q=%24NVIM) in jobstart() and :terminal jobs, so that child processes have an unambiguous hint that they are children of Nvim.

$NVIM_LISTEN_ADDRESS had conflicting "dual purposes". It's no longer passed to children. 

[github.com/neovim/neovim/…](https://github.com/neovim/neovim/pull/11009)

[Tweet link](https://twitter.com/Neovim/status/1521478149594353667)


source: "https://twitter.com/Neovim/status/1524523685218070530"
---
![Neovim](images/Neovim-2386262630.jpg)
Neovim ([@Neovim](https://twitter.com/Neovim))

[#neovim](https://twitter.com/hashtag/neovim)  HEAD: use nvim_cmd() to call any Vim legacy command in a structured way, like system([...]). Don't need fnameescape(); special chars controlled by "magic" param.

nvim_cmd({cmd='vimgrep', args={'/%s/j', '**'}}, {}) [twitter.com/Neovim/status/…](https://twitter.com/Neovim/status/1521284137344245761)

[Tweet link](https://twitter.com/Neovim/status/1524523685218070530)


source: "https://twitter.com/Neovim/status/1524756847449853952"
---
![Neovim](images/Neovim-2386262630.jpg)
Neovim ([@Neovim](https://twitter.com/Neovim))

Nvim now stores "session data" (shada, persistent undo, ...) in `$XDG_STATE_HOME` (~/.local/state) instead of `$XDG_CACHE_HOME` (~/.cache). (No change on Windows)

Plugins can also use stdpath('log') to get the recommended location for log files.

[github.com/neovim/neovim/…](https://github.com/neovim/neovim/pull/15583)

[Tweet link](https://twitter.com/Neovim/status/1524756847449853952)


source: "https://twitter.com/Neovim/status/1526167702452244480"
---
![Neovim](images/Neovim-2386262630.jpg)
Neovim ([@Neovim](https://twitter.com/Neovim))

"gO" in the [#neovim](https://twitter.com/hashtag/neovim)  manpage viewer (:help :Man) shows an outline (table of contents) in the location list. Now the outline also lists the flags. 

(Nvim 0.8 / prerelease)
[github.com/neovim/neovim/…](https://github.com/neovim/neovim/pull/17558) [pic.twitter.com/Om9u904tns](https://twitter.com/Neovim/status/1526167702452244480/photo/1)

![](images/3_1526166272706215938.jpg)

[Tweet link](https://twitter.com/Neovim/status/1526167702452244480)


source: "https://twitter.com/Neovim/status/1527025192756715521"
---
![Neovim](images/Neovim-2386262630.jpg)
Neovim ([@Neovim](https://twitter.com/Neovim))

new core events: LspAttach, LspDetach

vim.lsp.get_active_clients() learned to filter:

get_active_clients({id=42})
get_active_clients({bufnr=99})
get_active_clients({name='tsserver'})

this will be a standard pattern in the Lua stdlib.

[github.com/neovim/neovim/…](https://github.com/neovim/neovim/pull/18507)

[Tweet link](https://twitter.com/Neovim/status/1527025192756715521)


source: "https://twitter.com/Neovim/status/1527849682570977282"
---
![Neovim](images/Neovim-2386262630.jpg)
Neovim ([@Neovim](https://twitter.com/Neovim))

'winbar' = extra statusline at the top of each window, works nicely with laststatus=3:

set winbar=%f
set laststatus=3

'winbar' (and 'statusline') will also gain support for mouse-click regions (as 'tabline' has in [#neovim](https://twitter.com/hashtag/neovim)  since 2016): [github.com/neovim/neovim/…](https://github.com/neovim/neovim/pull/18650) [pic.twitter.com/KUVJq3e1NV](https://twitter.com/Neovim/status/1527849682570977282/photo/1)

![](images/3_1527849187110440961.jpg)

[Tweet link](https://twitter.com/Neovim/status/1527849682570977282)


source: "https://twitter.com/Neovim/status/1528717143243644930"
---
![Neovim](images/Neovim-2386262630.jpg)
Neovim ([@Neovim](https://twitter.com/Neovim))

Removed 'insertmode' option, which was used in Vim to implement "easy vim".

[github.com/neovim/neovim/…](https://github.com/neovim/neovim/pull/18547#issuecomment-1134613097)

We want to drive towards making the same behavior possible as a plugin. See ":help 'insertmode'" in Nvim HEAD.

Do you use 'insertmode' (the option, not the mode!)?

|Option|Votes|
|---|:---:|
|no|270|
|yes|17|

[Tweet link](https://twitter.com/Neovim/status/1528717143243644930)


source: "https://twitter.com/Neovim/status/1531381349071962112"
---
![Neovim](images/Neovim-2386262630.jpg)
Neovim ([@Neovim](https://twitter.com/Neovim))

a brief summary of [#neovim](https://twitter.com/hashtag/neovim)  'packpath' improvements: [pic.twitter.com/fZholsOJPm](https://twitter.com/Neovim/status/1531381349071962112/photo/1)

![](images/3_1531381005990473730.jpg)

[Tweet link](https://twitter.com/Neovim/status/1531381349071962112)


source: "https://twitter.com/Neovim/status/1531677398193905664"
---
![Neovim](images/Neovim-2386262630.jpg)
Neovim ([@Neovim](https://twitter.com/Neovim))

on [#neovim](https://twitter.com/hashtag/neovim)  dev you can now implement 'inccommand' preview for any user-defined command.
[github.com/neovim/neovim/…](https://github.com/neovim/neovim/pull/18194)

vim.api.nvim_create_user_command(
  'MyCmd',
  my_cmd,
  { …, preview = my_cmd_preview })

Next: live preview of :normal, :global, etc.

[github.com/neovim/neovim/…](https://github.com/neovim/neovim/pull/18815)

[Tweet link](https://twitter.com/Neovim/status/1531677398193905664)


source: "https://twitter.com/Neovim/status/1536284653224710144"
---
![Neovim](images/Neovim-2386262630.jpg)
Neovim ([@Neovim](https://twitter.com/Neovim))

*experimental* feature in [#neovim](https://twitter.com/hashtag/neovim)  dev:

:set cmdheight=0

[github.com/neovim/neovim/…](https://github.com/neovim/neovim/pull/16251)

thanks to [@ShougoMatsu](https://twitter.com/ShougoMatsu)'s perseverance!

[Tweet link](https://twitter.com/Neovim/status/1536284653224710144)


source: "https://twitter.com/Neovim/status/1537129140935081986"
---
![Neovim](images/Neovim-2386262630.jpg)
Neovim ([@Neovim](https://twitter.com/Neovim))

[#neovim](https://twitter.com/hashtag/neovim)  is the world's most-loved editor. That's just science.

[insights.stackoverflow.com/survey/2021#mo…](https://insights.stackoverflow.com/survey/2021#most-loved-dreaded-and-wanted-new-collab-tools-love-dread) [pic.twitter.com/G7TDJYUY2S](https://twitter.com/Neovim/status/1537129140935081986/photo/1)

![](images/3_1537128649228537859.jpg)

[Tweet link](https://twitter.com/Neovim/status/1537129140935081986)


source: "https://twitter.com/Neovim/status/1538221323356450818"
---
![Neovim](images/Neovim-2386262630.jpg)
Neovim ([@Neovim](https://twitter.com/Neovim))

fast, slick [#neovim](https://twitter.com/hashtag/neovim)  folds:
[github.com/kevinhwang91/n…](https://github.com/kevinhwang91/nvim-ufo)

nice work, Kevin! [pic.twitter.com/6q6gu9d32b](https://twitter.com/Neovim/status/1538221323356450818/video/1)

[Tweet link](https://twitter.com/Neovim/status/1538221323356450818)


source: "https://twitter.com/Neovim/status/1540684915716636677"
---
![Neovim](images/Neovim-2386262630.jpg)
Neovim ([@Neovim](https://twitter.com/Neovim))

[#neovim](https://twitter.com/hashtag/neovim)  universal binary (ARM/M1, Intel) for macOS 11+ now provided in our nightly + stable releases.
[github.com/neovim/neovim/…](https://github.com/neovim/neovim/releases)

[github.com/neovim/neovim/…](https://github.com/neovim/neovim/pull/19029)

Huge thank you to Carlo Cabrera!

[Tweet link](https://twitter.com/Neovim/status/1540684915716636677)


source: "https://twitter.com/Neovim/status/1542495764768759808"
---
![Neovim](images/Neovim-2386262630.jpg)
Neovim ([@Neovim](https://twitter.com/Neovim))

[#neovim](https://twitter.com/hashtag/neovim)  0.8: marks can save and restore viewport info.

    :set jumpoptions=view

When you jump around, or switch buffers with ctrl-^ the viewport is restored instead of resetting/recentering vertically.

[github.com/neovim/neovim/…](https://github.com/neovim/neovim/pull/15831)

[Tweet link](https://twitter.com/Neovim/status/1542495764768759808)


source: "https://twitter.com/Neovim/status/1544965666888884224"
---
![Neovim](images/Neovim-2386262630.jpg)
Neovim ([@Neovim](https://twitter.com/Neovim))

[#neovim](https://twitter.com/hashtag/neovim)  0.8 feature: 'mousescroll' option controls vertical/horizontal mouse scroll behavior.

:set mousescroll=ver:5,hor:2

[github.com/neovim/neovim/…](https://github.com/neovim/neovim/pull/12355)

[Tweet link](https://twitter.com/Neovim/status/1544965666888884224)


source: "https://twitter.com/Neovim/status/1545387817215434753"
---
![Neovim](images/Neovim-2386262630.jpg)
Neovim ([@Neovim](https://twitter.com/Neovim))

[#neovim](https://twitter.com/hashtag/neovim)  0.8 filetype detection now uses Lua + "on-demand" strategy => 7x speedup vs filetype.vim, saves 5+ms on startup:

before:
  9.0ms: sourcing …/runtime/filetype.vim

after:
  1.3ms: sourcing …/runtime/filetype.lua

[github.com/neovim/neovim/…](https://github.com/neovim/neovim/issues/18604)

[Tweet link](https://twitter.com/Neovim/status/1545387817215434753)


source: "https://twitter.com/Neovim/status/1545913194660728832"
---
![Neovim](images/Neovim-2386262630.jpg)
Neovim ([@Neovim](https://twitter.com/Neovim))

"nvim --startuptime" now reports Lua require() times ([#neovim](https://twitter.com/hashtag/neovim)  0.8).

000.010  000.010: --- NVIM STARTING ---
000.198  000.188: event init
...
026.333  001.109  001.101: require('vim.lsp.protocol')
028.144  000.423  000.423: require('vim.lsp._snippet')
...

[github.com/neovim/neovim/…](https://github.com/neovim/neovim/pull/19267)

[Tweet link](https://twitter.com/Neovim/status/1545913194660728832)


source: "https://twitter.com/Neovim/status/1548665836285591552"
---
![Neovim](images/Neovim-2386262630.jpg)
Neovim ([@Neovim](https://twitter.com/Neovim))

'mouse' option is now set by default (again). Was disabled since 2017 "until a better approach".  Now we have it:

mouse=nvi
Type ":" (cmdline-mode) to temporarily disable mouse. Right-click shows a popup menu.
Try it!

[github.com/neovim/neovim/…](https://github.com/neovim/neovim/pull/19290)

[Tweet link](https://twitter.com/Neovim/status/1548665836285591552)


source: "https://twitter.com/Neovim/status/1548806464663339012"
---
![Neovim](images/Neovim-2386262630.jpg)
Neovim ([@Neovim](https://twitter.com/Neovim))

nvim-oxi: "first-class Rust bindings (FFI to Nvim C) to the rich API exposed by [#neovim](https://twitter.com/hashtag/neovim) ."

[github.com/noib3/nvim-oxi](https://github.com/noib3/nvim-oxi)

[Tweet link](https://twitter.com/Neovim/status/1548806464663339012)


source: "https://twitter.com/Neovim/status/1552681133187506179"
---
![Neovim](images/Neovim-2386262630.jpg)
Neovim ([@Neovim](https://twitter.com/Neovim))

a nice summary of the history and status of [#neovim](https://twitter.com/hashtag/neovim)  builtin LSP support:

[vikasraj.dev/blog/lsp-neovi…](https://www.vikasraj.dev/blog/lsp-neovim-retrospective)

[Tweet link](https://twitter.com/Neovim/status/1552681133187506179)


source: "https://twitter.com/Neovim/status/1554440835046965250"
---
![Neovim](images/Neovim-2386262630.jpg)
Neovim ([@Neovim](https://twitter.com/Neovim))

this week [#neovim](https://twitter.com/hashtag/neovim)  core closed two refactor epics started in 2014 and 2017, thanks to the continued work of dundargoc!

[github.com/neovim/neovim/…](https://github.com/neovim/neovim/issues/567)
[github.com/neovim/neovim/…](https://github.com/neovim/neovim/issues/7401)

[Tweet link](https://twitter.com/Neovim/status/1554440835046965250)


source: "https://twitter.com/Neovim/status/1561460599762161665"
---
![Neovim](images/Neovim-2386262630.jpg)
Neovim ([@Neovim](https://twitter.com/Neovim))

'winhighlight' was throughly reimplemented as window-local highlight namespaces. Should be fully backwards-compatible while enabling many new usecases, like window-local syntax highlighting.

[#neovim](https://twitter.com/hashtag/neovim)  0.8

[github.com/neovim/neovim/…](https://github.com/neovim/neovim/pull/13457)

[Tweet link](https://twitter.com/Neovim/status/1561460599762161665)


source: "https://twitter.com/Neovim/status/1564580707212709888"
---
![Neovim](images/Neovim-2386262630.jpg)
Neovim ([@Neovim](https://twitter.com/Neovim))

[#neovim](https://twitter.com/hashtag/neovim)  0.8 LSP client now supports connecting to language servers by TCP.

vim.lsp.start({ name = 'godot', cmd = vim.lsp.rpc.connect('127.0.0.1', 6008) })

[github.com/neovim/neovim/…](https://github.com/neovim/neovim/pull/19916)

[Tweet link](https://twitter.com/Neovim/status/1564580707212709888)


source: "https://twitter.com/Neovim/status/1567932781644095496"
---
![Neovim](images/Neovim-2386262630.jpg)
Neovim ([@Neovim](https://twitter.com/Neovim))

[#neovim](https://twitter.com/hashtag/neovim)  0.8 (unreleased) now includes treesitter parsers for C, Lua, and Vimscript. This is a step towards "treesitter by default" for common languages, instead of regex-based vim syntax definitions.

[github.com/neovim/neovim/…](https://github.com/neovim/neovim/pull/15391)

[Tweet link](https://twitter.com/Neovim/status/1567932781644095496)


source: "https://twitter.com/Neovim/status/1575455161186664451"
---
![Neovim](images/Neovim-2386262630.jpg)
Neovim ([@Neovim](https://twitter.com/Neovim))

Exciting progress on vim9script => Nvim-Lua transpiler from core maintainer [@teej_dv](https://twitter.com/teej_dv). This will enable us to continue pulling test coverage from Vim into [#neovim](https://twitter.com/hashtag/neovim) , plus syntax, ftplugins, and even plugins like cfilter. [twitter.com/teej_dv/status…](https://twitter.com/teej_dv/status/1575450247173738498)

[Tweet link](https://twitter.com/Neovim/status/1575455161186664451)


source: "https://twitter.com/Neovim/status/1577345338956038150"
---
![Neovim](images/Neovim-2386262630.jpg)
Neovim ([@Neovim](https://twitter.com/Neovim))

[#neovim](https://twitter.com/hashtag/neovim)  docs HTML v2: [neovim.io/doc/user/](https://neovim.io/doc/user/)

We can have nice things. [twitter.com/justinmk/statu…](https://twitter.com/justinmk/status/1577344345736466432)

> ![justinmk](images/justinmk-17546928.jpg)
> justinmk ([@justinmk](https://twitter.com/justinmk))
> 
> 
> new [#neovim](https://twitter.com/hashtag/neovim)  :help docs HTML: 
> 
> [neovim.io/doc/user/](https://neovim.io/doc/user/)
> 
> Features:
> - improved styling
> - nested lists
> - soft-wrapped "flow" layout on selected pages (example: [neovim.io/doc/user/luare…](https://neovim.io/doc/user/luaref.html) )
> - Lua+treesitter script replaces old AWK script
> - treesitter parser useful for other apps [pic.twitter.com/znrTxmhhLG](https://twitter.com/justinmk/status/1577344345736466432/photo/1) [twitter.com/justinmk/statu…](https://twitter.com/justinmk/status/1572985116518977536)
> 
![](images/3_1577344309233434642.jpg)
> 

> ![justinmk](images/justinmk-17546928.jpg)
> justinmk ([@justinmk](https://twitter.com/justinmk))
> 
> 
> [#neovim](https://twitter.com/hashtag/neovim)  HTML docs beta™ is live at user2/ :
> [neovim.io/doc/user2/](https://neovim.io/doc/user2/)
> 
> Hold off on bug reports for now, >50% will be fixed with:
> [github.com/vigoux/tree-si…](https://github.com/vigoux/tree-sitter-vimdoc/pull/16)
> 
> To help with styling: [github.com/neovim/neovim.…](https://github.com/neovim/neovim.github.io/issues/288) [twitter.com/justinmk/statu…](https://twitter.com/justinmk/status/1564267123048071171)
> 

> ![justinmk](images/justinmk-17546928.jpg)
> justinmk ([@justinmk](https://twitter.com/justinmk))
> 
> 
> working on better [#neovim](https://twitter.com/hashtag/neovim)  :help docs HTML. 
> 
> Current status (old vs new): [pic.twitter.com/RJcaJJFlTX](https://twitter.com/justinmk/status/1564267123048071171/photo/1)
> 
![](images/3_1564266982698090496.jpg)

[Tweet link](https://twitter.com/justinmk/status/1564267123048071171)

[Tweet link](https://twitter.com/justinmk/status/1572985116518977536)

[Tweet link](https://twitter.com/justinmk/status/1577344345736466432)

[Tweet link](https://twitter.com/Neovim/status/1577345338956038150)


source: "https://twitter.com/Neovim/status/1578146342991527938"
---
![Neovim](images/Neovim-2386262630.jpg)
Neovim ([@Neovim](https://twitter.com/Neovim))

first(?) plugin to use vim.ui_attach feature of [#neovim](https://twitter.com/hashtag/neovim)  0.8: [github.com/folke/noice.nv…](https://github.com/folke/noice.nvim)

vim.ui_attach (experimental) enables in-process Lua plugins to hook into the same events exposed to all Nvim UIs. [neovim.io/doc/user/lua.h…](https://neovim.io/doc/user/lua.html#vim.ui_attach%28%29) [pic.twitter.com/w9U87jGfIL](https://twitter.com/Neovim/status/1578146342991527938/photo/1)

[Tweet link](https://twitter.com/Neovim/status/1578146342991527938)


source: "https://twitter.com/Neovim/status/1580933880579641344"
---
![Neovim](images/Neovim-2386262630.jpg)
Neovim ([@Neovim](https://twitter.com/Neovim))

removed cscope support in [#neovim](https://twitter.com/hashtag/neovim)  0.9, because it is mostly redundant with the LSP client (:help lsp).
[github.com/neovim/neovim/…](https://github.com/neovim/neovim/pull/20545)

ctags support will *never* be removed, it is far more common and generally useful.

[Tweet link](https://twitter.com/Neovim/status/1580933880579641344)


source: "https://twitter.com/Neovim/status/1581951864639082496"
---
![Neovim](images/Neovim-2386262630.jpg)
Neovim ([@Neovim](https://twitter.com/Neovim))

MacVim will use the [#neovim](https://twitter.com/hashtag/neovim)  :help docs HTML generator for their docs website!
[macvim-dev.github.io/macvim/](https://macvim-dev.github.io/macvim/)
[github.com/neovim/neovim/…](https://github.com/neovim/neovim/pull/20690) [twitter.com/Neovim/status/…](https://twitter.com/Neovim/status/1577345338956038150)

[Tweet link](https://twitter.com/Neovim/status/1581951864639082496)


source: "https://twitter.com/Neovim/status/1585647751018467328"
---
![Neovim](images/Neovim-2386262630.jpg)
Neovim ([@Neovim](https://twitter.com/Neovim))

[#neovim](https://twitter.com/hashtag/neovim)  'inccommand' was added in 2017 to the effects of :substitute (:s/foo/bar) as you type. 

With Nvim 0.8, plugins can provide live preview of any command. 
[neovim.io/doc/user/map.h…](https://neovim.io/doc/user/map.html#%3Acommand-preview)

This plugin adds preview for :normal and macros:
[github.com/smjonas/live-c…](https://github.com/smjonas/live-command.nvim) [pic.twitter.com/XASLXNLAjl](https://twitter.com/Neovim/status/1585647751018467328/video/1)

[Tweet link](https://twitter.com/Neovim/status/1585647751018467328)


source: "https://twitter.com/Neovim/status/1589401961618890752"
---
![Neovim](images/Neovim-2386262630.jpg)
Neovim ([@Neovim](https://twitter.com/Neovim))

nice post about Nvim Lua!

"Lua plugins [are] basically the same as a vim plugin, except the file extension is .lua instead of .vim and the file contains Lua code instead of vimscript."

^ simple interface that required lots of careful work, largely thanks to [@bfredlbfredl](https://twitter.com/bfredlbfredl) ❤️ [twitter.com/mfussenegger/s…](https://twitter.com/mfussenegger/status/1589318696778235905)

[Tweet link](https://twitter.com/Neovim/status/1589401961618890752)


source: "https://twitter.com/Neovim/status/1589420555799007233"
---
![Neovim](images/Neovim-2386262630.jpg)
Neovim ([@Neovim](https://twitter.com/Neovim))

Try the new diff-mode "linematch" feature in [#neovim](https://twitter.com/hashtag/neovim)  0.9 (unreleased) for better understanding of same-line changes:

    :set diffopt+=linematch:60

[github.com/neovim/neovim/…](https://github.com/neovim/neovim/pull/14537) [pic.twitter.com/fYO2ICpJFa](https://twitter.com/Neovim/status/1589420555799007233/photo/1)

![](images/3_1589419182713602048.jpg)

[Tweet link](https://twitter.com/Neovim/status/1589420555799007233)


source: "https://twitter.com/Neovim/status/1589469857388834816"
---
![Neovim](images/Neovim-2386262630.jpg)
Neovim ([@Neovim](https://twitter.com/Neovim))

in [#neovim](https://twitter.com/hashtag/neovim)  0.9 (unreleased) the ":write" command gained the "++p" flag, so this:

    :edit parent/dir/file.txt
    :write ++p

creates parent/dir/ if it doesn't exist.

[github.com/neovim/neovim/…](https://github.com/neovim/neovim/issues/19884)

[Tweet link](https://twitter.com/Neovim/status/1589469857388834816)


source: "https://twitter.com/Neovim/status/1609952832526090240"
---
![Neovim](images/Neovim-2386262630.jpg)
Neovim ([@Neovim](https://twitter.com/Neovim))

Nvim is now self-hosting:
[github.com/neovim/neovim/…](https://github.com/neovim/neovim/pull/18375)

[#neovim](https://twitter.com/hashtag/neovim)  UIs are just (inverted) plugins. "nvim" in a terminal starts the TUI, which spawns "nvim --embed" subprocess.

Connect TUI to any server! Try this (Nvim 0.9):

  nvim --listen ./s
  nvim --remote-ui --server ./s [pic.twitter.com/bHYGCn842E](https://twitter.com/Neovim/status/1609952832526090240/photo/1)

![](images/3_1609951283833716739.jpg)

[Tweet link](https://twitter.com/Neovim/status/1609952832526090240)


source: "https://twitter.com/Neovim/status/1610676006947360775"
---
![Neovim](images/Neovim-2386262630.jpg)
Neovim ([@Neovim](https://twitter.com/Neovim))

[#neovim](https://twitter.com/hashtag/neovim)  0.9 now supports editorconfig by default [editorconfig.org](https://editorconfig.org) . Nvim detects ".editorconfig" files in your project and applies the settings.

To opt-out of this feature, add to init.lua:
    vim.g.editorconfig_enable = false

thanks gpanders!
[github.com/neovim/neovim/…](https://github.com/neovim/neovim/pull/21633)

[Tweet link](https://twitter.com/Neovim/status/1610676006947360775)


source: "https://twitter.com/Neovim/status/1612753358602833923"
---
![Neovim](images/Neovim-2386262630.jpg)
Neovim ([@Neovim](https://twitter.com/Neovim))

'statuscolumn' in [#neovim](https://twitter.com/hashtag/neovim)  0.9 = full control of the "gutter", w/ 'statusline' format.

Try it!
:set rnu nu 
:let &stc='%#NonText#%{&nu?v:lnum:""}%=%{&rnu&&(v:lnum%2)?"\ ".v:relnum:""}%#LineNr#%{&rnu&&!(v:lnum%2)?"\ ".v:relnum:""}'

thanks to luukvbaal!
[github.com/neovim/neovim/…](https://github.com/neovim/neovim/pull/20621) [pic.twitter.com/I0GRZ16SIv](https://twitter.com/Neovim/status/1612753358602833923/video/1)

[Tweet link](https://twitter.com/Neovim/status/1612753358602833923)


source: "https://twitter.com/Neovim/status/1612755020885237760"
---
![Neovim](images/Neovim-2386262630.jpg)
Neovim ([@Neovim](https://twitter.com/Neovim))

also supports click events, just like [#neovim](https://twitter.com/hashtag/neovim)  'statusline', 'tabline', and 'winbar'.

plugin by feature author luukvbaal w/ various pre-packaged 'statuscolumn' configs:
[github.com/luukvbaal/stat…](https://github.com/luukvbaal/statuscol.nvim)

[Tweet link](https://twitter.com/Neovim/status/1612755020885237760)


