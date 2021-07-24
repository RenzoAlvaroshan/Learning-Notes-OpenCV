# macOS Vim Manual - 98 User Manual - quickref.txt - Vim Quick Reference…

# macOS Vim Manual - 98 User Manual - quickref.txt - Vim Quick Reference Guide (official)

*macOS Vim Manual - 98 User Manual - quickref.txt - Vim Quick Reference Guide (official)*

--------------------

*quickref.txt*  For Vim version 8.2.  Last change: 2020 Jan 17

`          VIM REFERENCE MANUAL    by Bram Moolenaar`
`
`
`                ``Quick Reference Guide``
`
`
`
`                             *quickref* *Contents*`
` tag      subject                        tag      subject    ~`
`|Q_ct|``    list of help files            ``|Q_re|``    Repeating commands`
`|Q_lr|``    motion: Left-right            ``|Q_km|``    Key mapping`
`|Q_ud|``    motion: Up-down               ``|Q_ab|``    Abbreviations`
`|Q_tm|``    motion: Text object           ``|Q_op|``    Options`
`|Q_pa|``    motion: Pattern searches      ``|Q_ur|``    Undo/Redo commands`
`|Q_ma|``    motion: Marks                 ``|Q_et|``    External commands`
`|Q_vm|``    motion: Various               ``|Q_qf|``    Quickfix commands`
`|Q_ta|``    motion: Using tags            ``|Q_vc|``    Various commands`
`|Q_sc|``    Scrolling                     ``|Q_ce|``    Ex: Command-line editing`
`|Q_in|``    insert: Inserting text        ``|Q_ra|``    Ex: Ranges`
`|Q_ai|``    insert: Keys                  ``|Q_ex|``    Ex: Special characters`
`|Q_ss|``    insert: Special keys          ``|Q_st|``    Starting Vim`
`|Q_di|``    insert: Digraphs              ``|Q_ed|``    Editing a file`
`|Q_si|``    insert: Special inserts       ``|Q_fl|``    Using the argument list`
`|Q_de|``    change: Deleting text         ``|Q_wq|``    Writing and quitting`
`|Q_cm|``    change: Copying and moving    ``|Q_ac|``    Automatic commands`
`|Q_ch|``    change: Changing text         ``|Q_wi|``    Multi-window commands`
`|Q_co|``    change: Complex               ``|Q_bu|``    Buffer list commands`
`|Q_vi|``    Visual mode                   ``|Q_sy|``    Syntax highlighting`
`|Q_to|``    Text objects                  ``|Q_gu|``    GUI commands`
`                                        ``|Q_fo|``    Folding``
`

------------------------------------------------------------------------------
N is used to indicate an optional count that can be given before the command
------------------------------------------------------------------------------

**## motion - Left-right****## 
**

`|h|     N  ``h``          `_`left`_` (also:  ``Ctrl-h`` , <``BS``>, or <``Left``> key)                     $$$$$`
`|l|     N  ``l``          `_`right`_` (also: <``Space``> or <``Right``> key)                           $$$$$`
`                      (`_`Notes by CP`_`: ``Ctrl-h``/``j``/``k``/``l`` have been bound for win navigation)`
`
`
`|0|        ``0``          to `_`first character`_` in line (also: <``Home``> key)                  $$$$$``
`
`|^|        ``^``          to `_`first non-blank character`_` in line                           $$$$$``
`
`|$|     N  ``$``          to last character in line (`*`N`*`-1 lines lower)                    $$$$$``
`
`           ``           (also: <``End``> key)``
`
`
`
`|g0|``       ``g0``         to `_`first character`_` in screen line                              $$$$*`
`                      (differs from “0" when lines wrap)`
`|g^|``       ``g^``         to `_`first non-blank character`_` in screen line                    $$$$*`
`                      (differs from "^" when lines wrap)`
`|g$|``    N  ``g$``         to `_`last character`_` in screen line                               $$$$*`
`                      (differs from “$" when lines wrap)`
`|gm|``       ``gm``         to `_`m`_`iddle of `_`screen line`_`                                       $$$**`
`|gM|``       ``gM``         to `_`m`_`iddle of `_`line`_`                                              $$$**`
`|bar|``   N  ``|``          to `_`column`_` `*`N`*` (default: 1)                                       $$$$*`
`
`
`|f|``     N  ``f``{``char``}``    to `*`N`*`th occurrence of ``{``char``}`` to `_`right`_`                           $$$$$`
`|F|``     N  ``F``{``char``}``    to `*`N`*`th occurrence of ``{``char``}`` to `_`left`_`                            $$$$*`
`|t|``     N  ``t``{``char``}``    `_`t`_`ill before `*`N`*`th occurrence of ``{``char``}`` to `_`right`_`                  $$$$*`
`|T|``     N  ``T``{``char``}``    `_`t`_`ill before `*`N`*`th occurrence of ``{``char``}`` to `_`left`_`                   $$$$*`
`|;|``     N  ``;``          `_`repeat`_` last ``f``/``F``/``t``/``T`` `*`N`*` times — `_`same`_` direction                   $$$**`
`|,|``     N  ``,``          `_`repeat`_` last ``f``/``F``/``t``/``T`` `*`N`*` times — `_`opposite`_` direction               $$$**`
`                      (`_`Notes by CP`_`:``  ``f``/``F``/``t``/``T``  is `_`linewise`_` (left or right)`
`                      Whilst search ``/`` and ``?`` `_`bufferwise`_`
`

`--------------------`
`
`
**## motion - Up-down****## 
**

`|k|     N  ``k``          `*`N`*` lines `_`up`_` (also: ``Ctrl-`_`p`_` and <``Up``>)                             $$$$$``
`
`|-|``     N  ``-``          `*`N`*` lines up (on first non-blank character)                      $$$$*`
`                      (``Notes by CP:`` ``-`` key has been bound to NERDTree)`
`
`
`|j|``     N  ``j``          `*`N`*` lines `_`down`_` (also: ``Ctrl-j``, ``Ctrl-`_`n`_`, ``<``NL``>``, and ``<``Down``>``)          $$$$$``
`
`|+|``     N  ``+``          `*`N`*` lines down (on first non-blank char (also: ``Ctrl-M`` and ``<``CR``>``)  $$$$*`
`|_|``     N  ``_``          `*`N`*`-1 lines down (on first non-blank character)                  $$***`
`
`
`|gg|    N  ``gg``         ``to line `*`N`*` (on first non-blank character) (default: `_`first`_` line) $$$$$``
`
`|G|     N  ``G``          ``to line `*`N`*` (on first non-blank character) (default: `_`last`_` line)  $$$$$``
`
`|N%|    N  ``%``          to line `*`N-`*`percentage down in file                              $$$**`
`                      (`*`N`*` must be given, otherwise it is |%| command)`
`
`
`|gk|``    N  ``gk``         `*`N`*` `_`screen-lines`_` `_`up`_` (differs from ``k`` when line wraps)             $$$$*`
`|gj|``    N  ``gj``         `*`N`*` screen-lines `_`down`_` (differs from ``j`` when line wraps)           $$$$*``
`

--------------------

**## motion - Text object****## 
**

`|w|     N  ``w``          `*`N`*` `_`word`_` `_`beg`_` `_`forward`_`                                             $$$$$``
`
`|b|     N  ``b``          `*`N`*` word beg `_`backward`_`                                            $$$$$``
`
`|e|     N  ``e``          `*`N`*` word `_`end`_` `_`forward`_`                                             $$$$$``
`
`|ge|``    N  ``ge``         `*`N`*` word end `_`backward`_`                                            $$$$*`
`
`
`|W|``     N  ``W``          `*`N`*` `_`WORD`_` `_`beg`_` `_`forward`_` (blank-separated)                           $$$$$`
`|B|``     N  ``B``          `*`N`*` WORD beg `_`backward`_` (blank-separated)                          $$$$*`
`|E|``     N  ``E``          `*`N`*` WORD `_`end`_` `_`forward`_` (blank-separated)                           $$$$*`
`|gE|``    N  ``gE``         `*`N`*` WORD end `_`backward`_` (blank-separated)                          $$$**`
`
`
`|(|``     N  ``(``          `*`N`*` `_`sentence`_` `_`backward`_` (separator: ``<``space``>``,`` ``.`` dot)                $$***`
`|)|``     N  ``)``          `*`N`*` sentence `_`forward`_`  (separator: ``<``space``>``,`` ``.`` dot)                $$***`
`|{|``     N  ``{``          `*`N`*` `_`paragraph`_` `_`backward`_` (separator: blank line)                   $$***`
`|}|``     N  ``}``          `*`N`*` paragraph `_`forward`_` (separator: blank line)                    $$***`
`
`
`|[[|``    N  ``[[``         `*`N`*` `_`section`_` `_`backward`_` or to `_`previous`_` ``{`` in first column            $****`
`|]]|``    N  ``]]``         `*`N`*` section `_`forward`_` or to `_`next`_` ``{`` in first column                 $****`
`
`
`|[]|``    N  ``[]``         N section `_`backward`_` or to `_`previous`_` ``}`` in first column            $****`
`|][|``    N  ``][``         `*`N`*` section `_`forward`_` or to `_`next`_` ``}`` in first column                 $****`
`
`
`|[(|``    N  ``[(``         `*`N`*` times `_`backward`_` to unmatched or unclosed ``(``                    $****`
`|])|``    N  ``])``         `*`N`*` times `_`forward`_` to unmatched or unclosed ``)``                     $****`
`
`
`|[{|``    N  ``[{``         `*`N`*` times `_`backward`_` to unmatched or unclosed ``{``                    $****`
`|]}|``    N  ``]}``         `*`N`*` times `_`forward`_` to unmatched or unclosed ``}``                     $****`
`
`
`|[m|``    N  ``[m``         `*`N`*` times `_`backward`_` to `_`beg`_`-of-`_`method`_` (for Java)                   $****`
`|]m|``    N  ``]m``         `*`N`*` times `_`forward`_` to beg-of-method (for Java)                    $****`
`
`
`|[M|``    N  ``[M``         `*`N`*` times `_`backward`_` to `_`end`_`-of-method (for Java)                   $****`
`|]M|``    N  ``]M``         `*`N`*` times `_`forward`_` to end-of-method (for Java)                    $****`
`
`
`|[#|``    N  ``[#``         `*`N`*` times `_`backward`_` to unclosed ``#if`` or ``#else``                      $****`
`|]#|``    N  ``]#``         `*`N`*` times `_`forward`_` to unclosed ``#else`` or ``#endif``                    $****`
`
`
`|[star|`` N  ``[*``         `*`N`*` times `_`backward`_` to `_`beg`_`-of-comment ``/*``                          $$***`
`|]star|`` N  ``]*``         `*`N`*` times `_`forward`_` to `_`end`_`-of-comment ``*/``                           $$***``
`

--------------------

**## motion - Pattern searches****## 
**

`|/|``     N  ``/``{``pattern``}[``/``{``offset``}]<``CR``>                                ``                 $$$**`
`                      search `_`forward`_` for `*`N`*`th occurrence of ``{``pattern``}``
`
`|?|``     N  ``?``{``pattern``}[``?``{``offset``}]<``CR``>                                ``                 $$$**`
`                      search `_`backward`_` for `*`N`*`th occurrence of ``{``pattern``}``
`
`|/<Cr>|`` N  ``/``<``CR``>``      repeat last search, in `_`forward`_` direction``     ``                  $$***`
`                      (alternative: ``//`` (without ``<``Enter``>``, no need to ``:nohl``)           $$***`
`|?<Cr>|`` N  ``?``<``CR``>``      repeat last search, in `_`backward`_` direction``     ``                 $$***`
`                      (alternative: ``??`` (without ``<``Enter``>``, no need to ``:nohl``)           $$***`
`|n|``     N  ``n``          repeat last search``     ``                                        $$$**`
`|N|``     N  ``N``          repeat last search, in `_`opposite`_` direction``     ``                 $$$**`
`|star|``  N  ``*``          search `_`forward`_` for identifier under cursor``     ``                $$$$*`
`|#|``     N  ``#``          search `_`backward`_` for identifier under cursor``     ``               $$$$*`
`|gstar|`` N  ``g*``         like "``*``", but also find partial matches``     ``                   $$$**`
`|g#|``    N  ``g#``         like "``#``", but also find partial matches``     ``                   $$$**`
`|gd|``       ``gd``         goto `_`local`_` `_`d`_`eclaration of identifier under cursor``     ``         $$***`
`|gD|``       ``gD``         goto `_`global`_` `_`d`_`eclaration of identifier under cursor``     ``        $$***`

**### |pattern|****###              ****_### Special characters_****###  in search patterns****### 
**

`                      meaning               magic   nomagic    ~``
`
`               match any single character     .       \.``     ``                        $$***`
`                  match beg-of-line (BoL)     ^       ^``     ``                         $$***`
`                  match end-of-line (EoL)     $       $``     ``                         $$***`
`                  match beg-of-word (BoW)     \<      \<``     ``                        $$***`
`                  match end-of-word (EoW)     \>      \>``     ``                        $$***`
`           match a `_`single`_` char from range     [a-z]   \[a-z]``     ``                    $$***`
`         match a single char `_`not`_` in range     [^a-z]  \[^a-z]``     ``                   $$***`
`            match an `_`i`_`dentifier character     \i      \i``     ``                        $****`
`              -idem- but `_`excluding`_` digits     \I      \I``     ``                        $****`
`                match a keyword character     \k      \k``     ``                        $****`
`              -idem- but `_`excluding`_` digits     \K      \K``     ``                        $****`
`               match a `_`f`_`ilename character     \f      \f``     ``                        $****`
`              -idem- but `_`excluding`_` digits     \F      \F``     ``                        $****`
`              match a `_`p`_`rintable character     \p      \p``     ``                        $****`
`              -idem- but `_`excluding`_` digits     \P      \P``     ``                        $****`
`            match a `_`white`_` `_`s`_`pace character     \s      \s``     ``                        $$***`
`        match a `_`non-white`_` space character     \S      \S``     ``                        $$***`
`
`
`                             match <`_`E`_`sc>      \e      \e``     ``                        $$***`
`                             match <`_`T`_`ab>      \t      \t``     ``                        $$***`
`                              match <C`_`R`_`>      \r      \r``     ``                        $$***`
`                              match <`_`B`_`S>      \b      \b``     ``                        $$***`
`
`
`       match 0 or more of preceding atom      *      \* ``     ``                        $****`
`       match 1 or more of preceding atom      \+     \+ ``     ``                        $****`
`          match 0 or 1 of preceding atom      \=     \= ``     ``                        $****`
`          match 2 to 5 of preceding atom      \{2,5} \{2,5} ``     ``                    $****`
`               separate two alternatives      \|     \| ``     ``                        $****`
`            group a pattern into an atom      \(\)   \(\) ``     ``                      $****``
`

**### |search-offset|       Offsets allowed after search command****### 
**

`    ``[``num``]``       [num] lines downward, in column 1``     ``                               $****`
`    ``+``[``num``]``      [num] lines downward, in column 1``     ``                               $****`
`    ``-``[``num``]``      [num] lines upward, in column 1``     ``                                 $****`
`    ``e``[``+``num``]``     [num] characters to right of `_`e`_`nd of match``     ``                       $****`
`    ``e``[``-``num``]``     [num] characters to left of `_`e`_`nd of match``     ``                        $****`
`    ``s``[``+``num``]``     [num] characters to right of `_`s`_`tart of match``     ``                     $****`
`    ``s``[``-``num``]``     [num] characters to left of `_`s`_`tart of match``     ``                      $****`
`    ``b``[``+``num``]``     [num] identical to ``s``[``+num``]`` above (mnemonic: `_`b`_`egin)``     ``              $****`
`    ``b``[``-``num``]``     [num] identical to ``s``[``-num``]`` above (mnemonic: `_`b`_`egin)``     ``              $****`
`    ``;``{``search-command``}     ``                                                           $****`
`                execute ``{``search-command``}`` next`

--------------------

**## motion - Marks****## 
**

`|m|``        ``m``{``a-zA-Z``}``  mark current position with mark ``{``a-zA-Z``}     ``                  $****`
`|`a|``       `````{``a-z``}``     go to mark ``{``a-z``}`` within `_`current`_` file`` (local)``    ``               $****`
`|`A|``       `````{``A-Z``}``     go to mark ``{``A-Z``}`` in `_`any`_` file`` (global)``     ``                     $****           `
`|`0|``       `````{``0-9``}``     go to position where Vim was previously exited``     ``            $****``     ``                  `
`|``|``       ``````         go to position `_`before last jump`_`     ``                           $****`
`|`quote|``   ```"``         go to position when `_`last editing`_` this file``     ``                $****`
`|`[|``       ```[``         go to `_`start`_` of previously operated or `_`put`_` text``     ``            $****`
`|`]|``       ```]``         go to `_`end`_` of previously operated or `_`put`_` text``     ``              $****`
`|`<|``       ```<``         go to `_`start`_` of (previous) `_`Visual`_` area``     ``                     $****`
`|`>|``       ```>``         go to `_`end`_` of (previous) `_`Visual`_` area``     ``                       $****`
`|`.|``       ```.``         go to position of `_`last change`_` in this file``     ``                $****`
`|'|``        ``'``{``a-zA-Z0-9[]'"<>.``}     ``              `` ``                  `` ``                $****`
`                      same as `**```**`, but on first non-blank in line`
`|:marks|``   ``:marks``     print active marks``     ``                     `` ``                  $****`
`|Ctrl-o|`` N ``Ctrl-o``     go to `*`N`*`th `_`older`_` position in jump list``     ``                     $****`
`|Ctrl-i|`` N ``Ctrl-I``     go to `*`N`*`th `_`newer`_` position in jump list``     ``                     $****`
`|:ju|``      ``:ju``[``mps``]``   print jump list``     ``              `` ``                  `` ``         $****``
`

--------------------

**## motion - Various****## 
**

`|%|``        ``%``          find next brace, bracket, comment, or "``#if``" or`` ``"``#else``" ``    ``    $****`
`                      or "``#endif``" in this line, and go to its match                  $****`
`|H|``     N  ``H``          go to `*`N`*`th line in window, on first non-blank                   $****`
`|M|``        ``M``          go to middle line in window, on first non-blank                $****`
`|L|``     N  ``L``          go to `*`N`*`th line from bottom, on first non-blank                 $****`
`
`
`|go|``    N  ``go``         go to `*`N`*`th byte in buffer                                       $****`
`|:go|``      ``:``[``range``]``go``[``to``] [``off``]``                                                      $****`
`                      go to ``[``off``]`` byte in buffer``
`

--------------------

**## motion - Using tags****## 
**

`|:ta|``      ``:ta``[``g``][``!``] {``tag``}``        jump to tag ``{``tag``}``                                  $$***      `
`|:ta|``      ``:``[``count``]``ta``[``g``][``!``]``       jump to ``[``count``]``'th newer tag in tag list           $$$**`
`|Ctrl-]|``   ``Ctrl-]``                 jump to tag under cursor, unless changes           $$$**`
`                                  have been made                                     $****`
`|:ts|``      ``:ts``[``elect``][``!``] [``tag``]``    list matching tags and select one to jump to       $****`
`|:tjump|``   ``:tj``[``ump``][``!``] [``tag``]``      jump to tag ``[``tag``]`` or select from list when         $****`
`                                  there are multiple matches`
`|:ltag|``    ``:lt``[``ag``][``!``] [``tag``]``       jump to tag ``[``tag``]`` and add matching tags to         $****`
`                                  location list`
`
`
`|:tags|``    ``:tags``                  print tag list                                     $****`
`|Ctrl-t|`` N ``Ctrl-t``                 jump back from `*`N`*`th older tag in tag list           $****`
`|:po|``      ``:``[``count``]``po``[``p``][``!``]``       jump back from ``[``count``]``'th older tag in tag list    $****`
`|:tnext|``   ``:``[``count``]``tn``[``ext``][``!``]``     jump to ``[``count``]``'th next matching tag               $****`
`|:tp|``      ``:``[``count``]``tp``[``revious``][``!``]`` jump to ``[``count``]``'th previous matching tag           $****`
`|:tr|``      ``:``[``count``]``tr``[``ewind``][``!``]``   jump to ``[``count``]``'th matching tag                    $****`
`|:tl|``      ``:tl``[``ast``][``!``]``            jump to last matching tag                          $****`
`
`
`|:ptag|``    ``:pt``[``ag``] {``tag``}``          open a `_`p`_`review window to show `_`t`_`ag ``{``tag``}``            $****`
`|Ctrl-w_}|`` ``Ctrl-w }``               like ``Ctrl-j`` but show tag in `_`preview`_` `_`window`_`         $****`
`|:pts|``     ``:pts``[``elect``]``            like "``:tselect``" but show `_`t`_`ag in `_`p`_`review window     $****`
`|:ptjump|``  ``:ptj``[``ump``]``              like "``:tjump``" but show `_`t`_`ag in `_`p`_`review window       $****`
`|:pclose|``  ``:pc``[``lose``]``              `_`c`_`lose tag `_`p`_`review window                           $****`
`|Ctrl-w_z|`` ``Ctrl-w z``               `_`close`_` tag preview `_`window`_`                           $****`

--------------------

**## Scrolling****## 
**

`
`
`|Ctrl-d|`` N  ``Ctrl-d``    window `*`N`*` `_`lines`_` `_`Downwards`_` (default: 1/2 window)                 $$$$$`
`|Ctrl-u|`` N  ``Ctrl-u``    window `*`N`*` lines `_`Upwards`_`   (default: 1/2 window)                 $$$$$`
`|Ctrl-e|`` N  ``Ctrl-e``    window `*`N`*` `_`lines`_` `_`downwards`_` (default: 1)                          $****`
`|Ctrl-y|`` N  ``Ctrl-y``    window `*`N`*` lines `_`upwards`_`   (default: 1)                          $****`
`|Ctrl-f|`` N  ``Ctrl-f``    window `*`N`*` pages `_`Forwards`_`  (downwards)                           $****``
`
`|Ctrl-b|`` N  ``Ctrl-b``    window `*`N`*` `_`pages`_` `_`Backwards`_` (upwards)                             $****`
`
`
`|z|``         ``z``<``CR``>`` ``or`` ``zt``                                                              $****`
`                      redraw, current line at `_`top`_` of window                          $****`
`|z.|``        ``z.`` ``or`` ``zz``  redraw, current line at `_`center`_` of window                       $****`
`|z-|``        ``z-`` ``or`` ``zb``  redraw, current line at `_`bottom`_` of window                       $****`
`
`
`These only work when 'wrap' is off:`
`|zh|``    N  ``zh``         scroll screen `*`N`*` `_`characters`_` to `_`right`_`                            $****`
`|zl|``    N  ``zl``         scroll screen `*`N`*` characters to `_`left`_`                             $****`
`|zH|``    N  ``zH``         scroll screen `_`half`_` a screenwidth to `_`right`_`                      $****`
`|zL|``    N  ``zL``         scroll screen half a screenwidth to `_`left`_`                       $****``
`
![macOS Vim Manual - 98 User Manual - quickref-txt - Vim Quick Reference…](images/macOS%20Vim%20Manual%20-%2098%20User%20Manual%20-%20quickref-txt%20-%20Vim%20Quick%20Reference….png)

--------------------

**## insert - Inserting text****## 
**

`|a|``     N  ``a``          append text `_`after`_` cursor (`*`N`*` times)                             $****`
`|A|``     N  ``A``          append text at `_`end-of-line`_` (`*`N`*` times)                           $****`
`|i|``     N  ``i``          insert text `_`before`_` cursor (`*`N`*` times) (also: ``<``Inser``>``)            $****`
`|I|``     N  ``I``          insert text before `_`first non-blank`_` in line (`*`N`*` times)           $****`
`|gI|``    N  ``gI``         insert text in `_`column 1`_` (`*`N`*` times)                              $****`
`|o|``     N  ``o``          open a new line `_`below`_` current line, append text (`*`N`*` times)      $****`
`|O|``     N  ``O``          open a new line `_`above`_` current line, append text (`*`N`*` times)      $****`
`|:startinsert|``  ``:star``[``tinsert``][``!``]``                                                    $****`
`                      start Insert-mode, append when ``[``!``]`` used`
`|:startreplace|`` ``:startr``[``eplace``][``!``]``                                                   $****`
`                      start Replace-mode, at EOL when ``[``!``]`` used`
`
`
`in Visual block mode:`
`|v_b_I|``    ``I``          insert same text in front of all selected lines                $****`
`|v_b_A|``    ``A``          append same text after all selected lines                      $****``
`

--------------------

**## insert - Insert-mode keys****## 
**

`|insert-index|``        alphabetical index of Insert-mode commands                     $****`
`
`
`leaving Insert-mode:`
`|i_<Esc>|``  ``<``Esc``>``      end Insert-mode, back to Normal-mode                           $****`
`|i_CTRL-C|`` ``Ctrl-c``     like ``<``Esc``>``, but do not use an abbreviation                     $****`
`|i_CTRL-O|`` ``Ctrl-o`` {``command``}``
`
`                      execute ``{``command``}`` and return to Insert-mode                    $****`
`                      `
`moving around:`
`|i_<Up>|``     ``<``cursor keys``>               ``                                            $****``
`
`               ``       move cursor left/right/up/down`
`|i_<S-Left>|`` ``<``Shift-left/right``>``                                                      $****``
`
`               ``       one word left/right`
`|i_<S-Up>|``   ``<``Shift-up/down``>``                                                         $****`
`               ``       one screenful backward/forward`
`|i_<End>|``    ``<``End``>``    cursor `_`after`_` last character in line                            $****`
`|i_<Home>|``   ``<``Home``>``     cursor `_`to`_` first character in line                            $****``
`

--------------------

**## insert - Special keys in Insert mode****## 
**

`|i_Ctrl-v|``    ``Ctrl-v`` {``char``}``..                                     ``                   $****`
`                      insert character `_`literally`_`, or enter `_`decimal byte value`_`
`
`|i_<NL>|``      ``<``NL``>`` ``or`` ``<``CR``>`` ``or`` ``Ctrl-m`` ``or`` ``Ctrl-j`` ``                                    ``  ``$****`
`                      begin new line ``(CP: Ctrl-j not working on 20210706)``
`
`|i_Ctrl-e|``    ``Ctrl-e``  insert character from `_`below`_` cursor                             $****`
`|i_Ctrl-Y|``    ``Ctrl-Y``  insert character from `_`above`_` cursor                             $****`
`
`
`|i_Ctrl-a|``    ``Ctrl-a``  insert `_`previously inserted`_` text                                $****`
`|i_Ctrl-@|``    ``Ctrl-@``  insert `_`previously inserted`_` text and stop Insert-mode           $****`
`|i_Ctrl-r|``    ``Ctrl-r`` ``{``register``}``                                                      $****`
`                      insert contents of a `_`r`_`egister`
`
`
`|i_Ctrl-n|``    ``Ctrl-n``  insert `_`next`_` match of identifier before cursor                  $****`
`|i_Ctrl-p|``    ``Ctrl-p``  insert `_`prev`_` match of identifier before cursor                  $****`
`|i_Ctrl-x|``    ``Ctrl-x`` ``...``                                                             $****`
`                      complete word before cursor in various ways`
`
`
`|i_<BS>|``      ``<``BS``>`` ``or`` ``Ctrl-h``                                                         $****`
`               ``       delete character before cursor`
`|i_<Del>|``     ``<``Del``>``   delete `_`character`_` under cursor                                  $****`
`|i_Ctrl-w|``    ``Ctrl-w``  delete `_`word`_` `_`before`_` cursor                                      $****`
`|i_Ctrl-u|``    ``Ctrl-u``  delete all entered characters in current line                  $****`
`|i_Ctrl-t|``    ``Ctrl-t``  insert one shiftwidth of indent in front of current line       $****`
`|i_Ctrl-d|``    ``Ctrl-d``  delete one shiftwidth of indent in front of current line       $****`
`|i_0_Ctrl-d|``  ``0 Ctrl-d``                                                               $****`
`               ``       `_`d`_`elete all `_`indent`_` in current line                              $****`
`|i_^_Ctrl-d|``  ``^ Ctrl-d           ``                                                    $****`
`               ``       (similar above) but restore indent in next line`

--------------------

**## insert - Digraphs****## 
**

`|:dig|``     ``:dig``[``raphs``]``  show current list of digraphs                                $****`
`|:dig|``     ``:dig``[``raphs``]`` ``{``char1``}{``char2``} {``number``} ... ``                                  $****`
`                      add digraph(s) to list`
`
`
`In Insert or Command-line mode:`
`|i_Ctrl-k|``  ``Ctrl-k ``{``char1``} {``char2``}``                                                   $****`
`                      enter digraph`
`|i_digraph|`` ``{``char1``} <``BS``> {``char2``}``                                                     $****`
`                      enter digraph if 'digraph' option set`

--------------------

**## insert - Special inserts****## 
**

`|:r|``       ``:r`` ``[``file``]``      insert contents of ``[``file``]`` below cursor                         $****`
`|:r!|``      ``:r!`` ``{``command``}``  insert standard output of ``{``command``}`` below cursor               $****``
`

--------------------

**## change - Deleting text****## 
**

`|x|``     N  ``x``          `_`delete`_` `*`N`*` characters `_`under`_` and `_`after`_` cursor                     $$$$*`
`|<Del>|`` N  ``<``Del``>``      `_`delete`_` `*`N`*` characters `_`under`_` and `_`after`_` cursor                     $$$$*`
`|X|``     N  ``X``          `_`delete`_` `*`N`*` characters `_`before`_` cursor                              $$$**`
`|d|``     N  ``d``{``motion``}``  `_`d`_`elete text that is `_`moved over`_` with ``{``motion``}``                   $$$**`
`|v_d|``      ``{``visual``}``d``  `_`d`_`elete `_`highlighted`_` text                                        $$$**`
`|dd|``    N  ``dd``         `_`d`_`elete `*`N`*` `_`lines`_`                                                 $$$$*`
`|D|``     N  ``D``          `_`d`_`elete to end-of-line (and N-1 more lines)                     $$$$*`
`|J|``     N  ``J``          join `*`N`*`-1 lines (delete <EOL>s)                                 $$$**`
`                      (``Notes CP:`` currently bound to moving line down/up ``Shit-j``/``k``)`
`|v_J|``      ``{``visual``}``J``  join highlighted lines                                         $****`
`|gJ|``    N  ``gJ``         like "``J``", but without inserting spaces                         $****`
`|v_gJ|``     ``{``visual``}``gJ`` like "``{``visual``}``J``", but without inserting `_`spaces`_`                 $****`
`|:d|``       ``:``[``range``]``d``[``elete``] [``x``]``
`
`                      `_`d`_`elete ``[``range``]`` lines ``[``into register ``x``]``                         $$***`

--------------------

**## change - Copying and moving text****## 
**

`|quote|``    ``"``{``char``}``    use register ``{``char``}`` for next `_`delete`_`, `_`yank`_`, or `_`put`_`              $$$**`
`|:reg|``     ``:reg``[``isters``]``
`
`               ``       show contents of all registers                                 $$$$*`
`|:reg|``     ``:reg``[``isters``]`` ``{``arg``}`` `
`                      show contents of registers mentioned in ``{``arg``}``                  $$$$*`
`|y|``     N  ``y``{``motion``}``  yank text moved over with ``{``motion``}`` into a register             $$$**`
`|v_y|``      ``{``visual``}``y``  yank highlighted text into a register                          $$$**`
`|yy|``    N  ``yy``         `_`y`_`ank `*`N`*` lines into a register                                   $$$$*`
`|Y|``     N  ``Y``          `_`y`_`ank `*`N`*` lines into a register                                   $$$$*`
`|p|``     N  ``p`` ``         `_`p`_`ut a register `_`after`_` cursor position (`*`N`*` times)                 $$$$*`
`|P|``     N  ``P``          `_`p`_`ut a register `_`before`_` cursor position (`*`N`*` times)                $$$**`
`|]p|``    N  ``]p``         like ``p``{``ut``}``, but `_`adjust indent`_` to current line                  $$$**`
`|[p|``    N  ``[p``         like ``P``{``ut``}``, but adjust indent to current line                  $$$**`
`|gp|``    N  ``gp``         like ``p``{``ut``}``, but `_`leave cursor`_` after new text                    $$$**`
`|gP|``    N  ``gP`` ``        like ``P``{``ut``}``, but leave cursor after new text                    $$$**`

--------------------

**## change - Changing text****## 
**

`|r|``     N  ``r``{``char``}``    replace `*`N`*` characters with ``{``char``}``                               $****`
`|gr|``    N  ``gr``{``char``}``   replace `*`N`*` characters without affecting layout                  $****`
`|R|``     N  ``R``          enter Replace mode (repeat entered text `*`N`*` times)               $****`
`|gR|``    N  ``gR``         enter virtual Replace-mode: like Replace-mode but              $****`
`                      without affecting layout`
`|v_b_r|``    ``{``visual``}``r``{``char``}``                                                           $****`
`                      in Visual-block mode: Replace each char of                     `
`                      selected text with ``{``char``}``
`
`
`
`            (change = delete text and enter Insert-mode)`
`|c|``     N  ``c``{``motion``}``  `_`c`_`hange text that is moved over with ``{``motion``}``                   $****`
`|v_c|``      ``{``visual``}``c``  `_`c`_`hange highlighted text                                        $****`
`|cc|``    N  ``cc``         `_`c`_`hange `*`N`*` lines                                                 $****`
`|S|``     N  ``S``          `_`s`_`ubstitute (change) `*`N`*` `_`lines`_`                                    $****`
`|C|``     N  ``C``          `_`c`_`hange to end-of-line (and `*`N`*`-1 more lines)                     $****`
`|s|``     N  ``s``          `_`s`_`ubstitute (change) `*`N`*` `_`characters`_`                               $****`
`|v_b_c|``    ``{``visual``}``c``  in Visual-block mode: Change each of selected                  $****`
`                      lines with entered text`
`|v_b_C|``    ``{``visual``}``C``  in Visual-block mode: Change each of selected                  $****`
`                      lines until end-of-line with entered text`
`
`
`|~|``     N  ``~``          switch case for `*`N`*` characters and advance cursor                $****`
`|v_~|``      ``{``visual``}``~``  switch case for highlighted text                               $****`
`|v_u|``      ``{``visual``}``u``  make highlighted text lowercase                                $****`
`|v_U|``      ``{``visual``}``U``  make highlighted text uppercase                                $****`
`|g~|``       ``g~``{``motion``}`` switch case for text that is moved over with ``{``motion``}``          $****`
`|gu|``       ``gu``{``motion``}`` make text that is moved over with ``{``motion``}`` `_`lowercase`_`           $****`
`|gU|``       ``gU``{``motion``}`` make text that is moved over with ``{``motion``}`` uppercase           $****`
`|v_g?|``     ``{``visual``}``g?`` perform rot13 encoding on highlighted text                     $****`
`|g?|``       ``g?``{``motion``}`` perform rot13 encoding on text that is moved over w/ ``{``motion``}``  $****`
`
`
`|Ctrl-a|`` N ``Ctrl-a``     `_`add`_` `*`N`*` to number at or after cursor                             $****`
`|Ctrl-x|`` N ``Ctrl-x``     `_`subtract`_` `*`N`*` from number at or after cursor                      $****`
`
`
`|<|``     N  ``<``{``motion``}``  move lines that are moved w/ ``{``motion``}`` one shiftwidth `_`left`_`      $****`
`|<<|``    N  ``<<``         move `*`N`*` lines one shiftwidth `_`left`_`                               $****`
`|>|``     N  ``>``{``motion``}``  move lines that are moved w/ ``{``motion``}`` one shiftwidth `_`right`_`     $****`
`|>>|``    N  ``>>``         move `*`N`*` lines one shiftwidth `_`right`_`                              $****`
`|gq|``    N  ``gq``{``motion``}`` format lines that are moved w/ ``{``motion``}`` to 'textwidth' length  $****`
`|:ce|``      ``:``[``range``]``ce``[``nter``] [``width``]``                                                  $****`
`                      center lines in ``[``range``]``
`
`|:le|``      ``:``[``range``]``le``[``ft``] [``indent``]``                                                   $****`
`                      left-align lines in ``[``range``]`` (with ``[``indent``]``)`
`|:ri|``      ``:``[``range``]``ri``[``ght``] [``width``]``                                                   $****`
`                      right-align lines in ``[``range``]``
`

--------------------

**## change - Complex changes****## 
**

`|!|``     N  ``!``{``motion``}{``command``}``                                                        $****`
`                      filter lines that are moved over through ``{``command``}``
`
`|!!|``    N  ``!!``{``command``}<``CR``>``                                                           $****`
`                      filter `*`N`*` lines through ``{``command``}``
`
`|v_!|``      ``{``visual``}!{``command``}<``CR``>``                                                    $****`
`                      filter highlighted lines through ``{``command``}``
`
`|:range!|``  ``:``[``range``]``!`` {``command``}``                                                       $****`
`                      filter ``[``range``]`` lines through ``{``command``}``
`
`|=|``     N  ``=``{``motion``}  ``filter lines that are moved over through '``equalprg``'            $****`
`|==|``    N  ``==``         filter `*`N`*` lines through '``equalprg``'                              $****`
`|v_=|``      ``{``visual``}``=``  filter highlighted lines through '``equalprg``'                    $****`
`|:s|``       ``:``[``range``]``s``[``ubstitute``]``/``{``pattern``}``/``{``string``}/[``g``][``c``]``                            $****`
`                      substitute ``{``pattern``}`` by ``{``string``}`` in ``[``range``]`` lines;`
`                         with ``[``g``]``, replace all occurrences of ``{``pattern``}``;`
`                         with ``[``c``]``, confirm each replacement`
`|:s|``       ``:``[``range``]``s``[``ubstitute``] [``g``][``c``]``                                               $****`
`                      repeat previous "``:s``" with new range and options`
`|&|``        ``&``          repeat previous "``:s``" on current line without options           $****`
`|:ret|``     ``:``[``range``]``ret``[``ab``][``!``] [``tabstop``]``                                              $****`
`                      set '``tabstop``' to new value and adjust white space accordingly``
`

--------------------

**## Visual mode****## 
**

`|visual-index|    list of Visual-mode commands`
`
`
`|v|``        ``v``          start highlighting `_`characters`_` ``}`` move cursor and use            $****`
`|V|``        ``V``          start highlighting `_`linewise`_`   ``}`` operator to affect             $****`
`|Ctrl-v|``   ``Ctrl-v``     start highlighting `_`blockwise`_`  ``}`` highlighted text               $****`
`|v_o|``      ``o``          `_`exchange`_` cursor position with start of highlighting            $****`
`|gv|``       ``gv``         start highlighting on `_`previous`_` visual area                     $****`
`|v_v|``      ``v``          highlight `_`characterwise`_` or stop highlighting                   $****`
`|v_V|``      ``V``          highlight `_`linewise`_` or stop highlighting                        $****`
`|v_Ctrl-v|`` ``Ctrl-v``     highlight `_`blockwise`_` or stop highlighting                       $****``
`

--------------------

**## Text objects****##  **## (only in Visual mode or after an operator)**## 
**

`|v_aw|``  N  ``aw``         select "`_`a`_` `_`w`_`ord"                                                $****`
`|v_iw|``  N  ``iw``         select "`_`i`_`nner `_`w`_`ord"                                            $****`
`|v_aW|``  N  ``aW``         select "`_`a`_` |`_`W`_`ORD|"                                              $****`
`|v_iW|``  N  ``iW``         select "`_`i`_`nner |`_`W`_`ORD|"                                          $****`
`|v_as|``  N  ``as``         select "`_`a`_` `_`s`_`entence"                                            $****`
`|v_is|``  N  ``is``         select "`_`i`_`nner `_`s`_`entence"                                        $****`
`|v_ap|``  N  ``ap``         select "`_`a`_` paragraph"                                           $****`
`|v_ip|``  N  ``ip``         select "`_`i`_`nner `_`p`_`aragraph"                                       $****`
`|v_ab|``  N  ``ab``         select "`_`a`_` `_`b`_`lock" (from "``[(``" to "``])``")                           $****`
`|v_ib|``  N  ``ib``         select "`_`i`_`nner `_`b`_`lock" (from "``[(``" to "``])``")                       $****`
`|v_aB|``  N  ``aB``         select "`_`a`_` `_`B`_`lock" (from "``[{``" to "``]}``")                           $****`
`|v_iB|``  N  ``iB``         select "`_`i`_`nner `_`B`_`lock" (from "``[{``" to "``]}``")                       $****`
`|v_a>|``  N  ``a>``         select "`_`a`_` <`_`>`_` block"                                            $****`
`|v_i>|``  N  ``i>``         select "`_`i`_`nner <`_`>`_` block"                                        $****`
`|v_at|``  N  ``at``         select "`_`a`_` `_`t`_`ag block" (from ``<``aaa``>`` to ``<``/aaa``>``)                    $****`
`|v_it|``  N  ``it``         select "inner `_`t`_`ag block" (from ``<``aaa``> ``to ``<``/aaa``>``)                $****`
`|v_a'|``  N  ``a'``         select "`_`a`_` single quoted `_`s`_`tring"                                $****`
`|v_i'|``  N  ``i'``         select "`_`i`_`nner `_`single quoted`_` `_`s`_`tring"                            $****`
`|v_aquote|`` N  ``a"``      select "`_`a`_` `_`double quoted`_` string"                                $****`
`|v_iquote|`` N  ``i"``      select "`_`i`_`nner `_`double quoted`_` string"                            $****`
`|v_a`|``  N  ``a```         select "`_`a`_` `_`backward quoted`_` string"                              $****`
`|v_i`|``  N  ``i```         select "`_`i`_`nner `_`backward quoted`_` string"                          $****``
`

--------------------

**## Repeating commands****## 
**

`|.|``     N  `**`.`**`          repeat last change (with count replaced with `*`N`*`)                $****`
`|q|``        ``q``{``a-z``}``     record typed characters into register ``{``a-z``}``                    $****`
`|q|``        ``q``{``A-Z``}``     record typed characters, appended to register ``{``a-z``}``            $****`
`|q|``        ``q``          stop recording                                                 $****`
`|@|``     N  ``@``{``a-z``}``     execute contents of register ``{``a-z``}`` (`*`N`*` times)                   $****`
`|@@|``    N  ``@@``         repeat previous ``@``{``a-z``}`` (`*`N`*` times)                               $****`
`|:@|``       ``:@``{``a-z``}``    execute contents of register ``{``a-z``}`` as an Ex command            $****`
`|:@@|``      ``:@@``        repeat previous ``:@``{``a-z``}``                                        $****`
`|:g|``       ``:``[``range``]``g``[``lobal``]``/``{``pattern``}/[``cmd``]``                                          $****`
`                      execute ``Ex`` command ``[``cmd``]`` (default: "``:p``") on lines`
`                      within [range] where ``{``pattern``}`` matches`
`|:g|``       ``:``[``range``]``g``[``lobal``]!``/``{``pattern``}/[``cmd``]``                                         $****`
`                      execute ``Ex`` command ``[``cmd``]`` (default: "``:p``") on lines`
`                      within ``[``range``]`` where ``{``pattern``}`` does NOT match`
`|:so|``      ``:so``[``urce``] {``file``}``                                                          $****`
`                      read ``Ex`` commands from ``{``file``}``                                   $****`
`|:so|``      ``:so``[``urce``]``!`` ``{``file``}``                                                         $****`
`                      read Vim commands from ``{``file``}``
`
`|:sl|``      ``:sl``[``eep``] [``sec``]``                                                            $****`
`                      don't do anything for ``[``sec``]`` seconds`
`|gs|``    N  ``gs``         `_`g`_`oto `_`s`_`leep for `*`N`*` seconds                                       $****``
`

--------------------

**## Key mapping****## 
**

`|:map|``     ``:ma``[``p``] {``lhs``} {``rhs``}``                                                        $****`
`                      map ``{``lhs``}`` to ``{``rhs``}`` in Normal-mode and Visual-mode``
`
`|:map!|``    ``:ma``[``p``]``!`` {``lhs``} {``rhs``}``                                                       $****`
`                      map ``{``lhs``}`` to ``{``rhs``}`` in Insert-mode and Cmdline-mode``
`
`|:noremap|`` ``:no``[``remap``][``!``] {``lhs``} {``rhs``}``                                                 $****`
`                      same as ":map", no remapping for this ``{``rhs``}``
`
`|:unmap|``   ``:unm``[``ap``] {``lhs``}``                                                            $****`
`                      remove mapping of ``{``lhs``}`` for `_`Normal`_`-mode`
`                      and `_`Visual`_`-mode``
`
`|:unmap!|``  ``:unm``[``ap``]``!`` {``lhs``}``                                                           $****`
`                      remove mapping of ``{``lhs``}`` for `_`Insert`_`-mode`
`                      and `_`Cmdline`_`-mode``
`
`|:map_l|``   ``:ma``[``p``] [``lhs``]``                                                              $****`
`                      list mappings (starting with ``[``lhs``]``) for `_`Normal`_`-mode`
`                      and `_`Visual`_`-mode``
`
`|:map_l!|``  ``:ma``[``p``]``!`` [``lhs``]``                                                             $****`
`                      list mappings (start w/ ``[``lhs``]``) for `_`Insert`_`-mode`
`                      and `_`Cmdline`_`-mode``
`
`|:cmap|``    ``:cmap``/``:cunmap``/``:cnoremap``                                                   $****`
`                      ``like ``"``:map!``"/"``:unmap!``"/"``:noremap!``" ``but`
`                      for `_`Cmdline`_`-mode only``
`
`|:imap|``    ``:imap``/``:iunmap``/``:inoremap``                                                   $****`
`                      ``like`` "``:map!``"/"``:unmap!``"/"``:noremap!``" ``but`
`                      for `_`Insert`_`-mode only``
`
`|:nmap|``    ``:nmap``/``:nunmap``/``:nnoremap``                                                   $****`
`                      ``like ``"``:map``"/"``:unmap``"/"``:noremap``" ``but`
`                      for `_`Normal`_`-mode only``
`
`|:vmap|``    ``:vmap``/``:vunmap``/``:vnoremap``                                                   $****`
`                      ``like`` "``:map``"/"``:unmap``"/"``:noremap``" ``but`
`                      for `_`Visual`_`-mode only``
`
`|:omap|``    ``:omap``/``:ounmap``/``:onoremap``                                                   $****`
`                      ``like`` "``:map``"/"``:unmap``"/"``:noremap``" ``but`
`                      only for when an `_`Operator`_` is pending``
`
`
`
`|:mapc|``    ``:mapc``[``lear``]   ``remove mappings for Normal-mode and Visual-mode             $****``
`
`|:mapc|``    ``:mapc``[``lear``]``!``  ``remove mappings for `_`Insert`_`-mode and `_`Cmdline`_`-mode            $****``
`
`|:imapc|``   ``:imapc``[``lear``]  ``remove mappings for Insert-mode                             $****``
`
`|:vmapc|``   ``:vmapc``[``lear``]  ``remove mappings for `_`Visual`_`-mode                             $****``
`
`|:omapc|``   ``:omapc``[``lear``]  ``remove mappings for `_`Opending`_`-mode                           $****``
`
`|:nmapc|``   ``:nmapc``[``lear``]  ``remove mappings for `_`Normal`_`-mode                             $****``
`
`|:cmapc|``   ``:cmapc``[``lear``]  ``remove mappings for `_`Cmdline`_`-mode                            $****``
`
`
`
`|:mkexrc|``  ``:mk``[``exrc``][``!``] [``file``]``                                                       $****`
`                      ``write current mappings, abbreviations, and settings`
`               ``       ``to ``[``file``]`` (default: ``"``.exrc``”``; use ``!`` to overwrite)``
`
`|:mkvimrc|`` ``:mkv``[``imrc``][``!``] [``file``]``                                                      $****`
`                      ``same as ``"``:mkexrc``"``, but with default ``"``.vimrc``"``
`
`|:mksession|`` ``:mks``[``ession``][``!``] [``file``]``                                                  $****`
`                      ``like "``:mkvimrc``", but store current files, windows, etc. too,`
`                      to be able to continue this session later``
`

--------------------

**## Abbreviations****## 
**

`|:abbreviate|``   ``:ab``[``breviate``] {``lhs``} {``rhs``}``                                            $****`
`                      add abbreviation for ``{``lhs``}`` to ``{``rhs``}``
`
`|:abbreviate|``   ``:ab``[``breviate``] {``lhs``}``                                                  $****`
`                      show abbr's that start with ``{``lhs``}``
`
`|:abbreviate|``   ``:ab``[``breviate``]``                                                        $****`
`                      show all abbreviations``
`
`|:unabbreviate|`` ``:una``[``bbreviate``] {``lhs``}``                                                $****`
`                      remove abbreviation for ``{``lhs``}``
`
`|:noreabbrev|``   ``:norea``[``bbrev``] [``lhs``] [``rhs``]``                                            $****`
`                      like ``"``:ab``"``, but don't remap ``[``rhs``]``
`
`|:iabbrev|``      ``:iab``/``:iunab``/``:inoreab``                                                 $****`
`                      ``like ``"``:ab``"``, but only for `_`Insert`_`-mode``
`
`|:cabbrev|``      ``:cab``/``:cunab``/``:cnoreab``                                                 $****`
`                      like ``"``:ab``"``, but only for `_`Cmdline`_`-mode``
`
`|:abclear|``      ``:abc``[``lear``]``                                                           $****`
`                      remove all abbreviations``
`
`|:cabclear|``     ``:cabc``[``lear``]``                                                          $****`
`                      remove all abbr's for `_`Cmdline`_` mode``
`
`|:iabclear|``     ``:iabc``[``lear``]``                                                          $****`
`                      remove all abbr's for `_`Insert`_`-mode``
`

--------------------

**## Options**## 

`|:set|``       ``:se``[``t``]``   ``show all modified options``                                      $****`
`|:set|``       ``:se``[``t``]`` ``all``                                                              $****``
`
`                      show all non-termcap options``
`
`|:set|``       ``:se``[``t``]`` ``termcap``                                                          $****``
`
`                      show all termcap options``
`
`|:set|``       ``:se``[``t``]`` ``{``option``}``                                                         $****`
`                      set boolean option (switch it on), show string or number option``
`
`|:set|``       ``:se``[``t``]`` ``no``{``option``}``                                                       $****`
`                      reset boolean option (switch it off)``
`
`|:set|``       ``:se``[``t``]`` ``inv``{``option``}``                                                      $****`
`                      invert boolean option``
`
`|:set|``       ``:se``[``t``]`` ``{``option``}``=``{``value``}``                                                 $****`
`                      set string/number option to ``{``value``}``
`
`|:set|``       ``:se``[``t``]`` ``{``option``}``+=``{``value``}``                                                $****`
`                      append ``{``value``}`` to string option, add ``{``value``}`` to number option``
`
`|:set|``       ``:se``[``t``]`` ``{``option``}``-=``{``value``}``                                                $****`
`                      ``remove {``value``}`` to string option, subtract ``{``value``}`` from number option``
`
`|:set|``       ``:se``[``t``]`` ``{``option``}``?``                                                        $****`
`                      show value of ``{``option``}``
`
`|:set|``       ``:se``[``t``]`` ``{``option``}``&                                                        $****`
`                      reset ``{``option``}`` to its default value``
`
`|:setlocal|``  ``:setl``[``ocal``]``                                                             $****``
`
`                      like ``"``:set``"`` but set local value for options that have one``
`
`|:setglobal|`` ``:setg``[``lobal``]``                                                            $****``
`
`                      like ``"``:set``"`` but set global value of a local option``
`
`|:fix|``       ``:fix``[``del``]``                                                               $****`
`                      set value of ``'``t_kD``'`` according to value of ``'t_kb'``
`
`|:options|``   ``:opt``[``ions``]``                                                              $****``
`
`                      open a new window to view and set options, grouped`
`                      by functionality, a one line explanation and links to help``
`

--------------------

Short explanation of each option:        *option-list*

`'``al``[``eph``]'``             'al'        ASCII code of letter Aleph (Hebrew)                $****`
`'``a``[``llow``]``r``[``ev``]``i``[``ns``]'``   'ari'       allow ``Ctrl-_`` in Insert-mode and Cmdline-mode       $****`
`'``a``[``lt``]``k``[``ey``]``m``[``ap``]'``     'akm'       obsolete option for Farsi                          $****`
`'``amb``[``i``]``w``[``idth``]'``       'ambw'      what to do with Unicode chars of `_`amb`_`iguous `_`w`_`idth   $****`
`'``anti``[``alias``]'``         'anti'      macOS: use smooth, antialiased fonts               $****`
`'``a``[``uto``]``c``[``h``]``d``[``ir``]'``     'acd'       change directory to the file in current window     $****`
`'``arab``[``ic``]'``            'arab'      for Arabic as a default second language            $****`
`'``ar``[``abic``]``shape``'``       ‘arshape’   do shaping for Arabic characters                   $****`
`'``a``[``uto``]``i``[``ndent``]'``      'ai'        take indent for new line from previous line        $****`
`'``a``[``uto``]``r``[``ead``]'``        'ar'        autom. read file when changed outside of Vim       $****`
`'``a``[``uto``]``w``[``rite``]'``       'aw'        automatically write file if changed                $****`
`'``a``[``uto``]``w``[``rite``]``a``[``ll``]'``  'awa'       as '``autowrite``', but works with more commands       $****`
`
`
`'``b``[``ack``]``g``[``round``]'``      'bg'        "dark" or "``light``", used for highlight colors       $****`
`'``b``[``ack``]``s``[``pace``]'``       'bs'        how backspace works at start of line               $****`
`'``b``[``ac``]``k``[``up``]'``          'bk'        keep backup file after overwriting a file          $****`
`'``b``[``ac``]``k``[``up``]``c``[``opy``]'``    'bkc'       make backup as a copy, don't rename the file       $****`
`'``b``[``ackup``]``dir``'``         'bdir'      list of directories for the backup file            $****`
`'``b``[``ackup``]``ex``[``t``]'``       'bex'       extension used for the backup file                 $****`
`'``b``[``ackup``]``sk``[``ip``]'``      'bsk'       no backup for files that match these patterns      $****`
`'``b``[``alloon``]``d``[``e``]``lay``'``    'bdlay'     delay in mS before a balloon may pop up            $****`
`'``b``[``alloon``]``eval``'``       'beval'     switch on balloon evaluation in the GUI            $****`
`'``b``[``alloon``]``evalterm``'``   'bevalterm' switch on balloon evaluation in the terminal       $****`
`'``b``[``alloon``]``expr``'``       'bexpr'     expression to show in balloon                      $****`
`'``b``[``ell``]``o``[``ff``]'``         'bo'        do not ring the bell for these reasons             $****`
`'``bin``[``ary``]'``            'bin'       read/write/edit file in binary mode                $****`
`'``biosk``[``ey``]'``           'biosk'     MS-DOS: use bios calls for input characters        $****`
`'``bomb``'``                'bom'       prepend a Byte Order Mark to the file              $****`
`'``br``[``ea``]``k``[``at``]'``         'brk'       characters that may cause a line break             $****`
`'``br``[``eak``]``i``[``ndent``]'``     'bri'       wrapped line repeats indent                        $****`
`'``br``[``eak``]``i``[``ndent``]``opt``'``  'briopt'    settings for '``breakindent``'                         $****`
`'``b``[``row``]``s``[``e``]``dir``'``       'bsdir'     which directory to start browsing in               $****`
`'``b``[``uf``]``h``[``idden``]'``       'bh'        what to do when buffer is no longer in window      $****`
`'``b``[``uf``]``l``[``isted``]'``       'bl'        whether buffer shows up in buffer list             $****`
`'``b``[``uf``]``t``[``ype``]'``         'bt'        special type of buffer                             $****`
`
`
`'``c``[``ase]m``[``a``]``p``'``         'cmp'       specifies how case of letters is changed           $****`
`'``cd``[``path``]'``            'cd'        list of directories searched with "``:cd``"            $****`
`'``cedit``'``               'cedit'     key used to open command-line window               $****`
`'``c``[``har``]``c``[``on``]``v``[``ert``]'``   'ccv'       expression for character encoding conversion       $****`
`'``cin``[``dent``]'``           'cin'       do C program indenting                             $****`
`'``cink``[``eys``]'``           'cink'      keys that trigger indent when '``cindent``' is set     $****`
`'``cino``[``ptions``]'``        'cino'      how to do indenting when '``cindent``' is set          $****`
`'``cinw``[``ords``]'``          'cinw'      words where '``si``' and '``cin``' add an indent           $****`
`'``c``[``lip``]``b``[``oard``]'``       'cb'        use the clipboard as the unnamed register          $****`
`'``c``[``md``]``h``[``eight``]'``       'ch'        number of lines to use for the command-line        $****`
`'``c``[``md``]``w``[``in``]``h``[``eight``]'``  'cwh'       height of the cmdline window                       $****`
`'``c``[``olor``]``c``[``olumn``]'``     'cc'        columns to highlight                               $****`
`'``co``[``lumns``]'``           'co'        number of columns in the display                   $****`
`'``com``[``ments``]'``          'com'       patterns that can start a comment line             $****`
`'``c``[``o``]``m``[``ment``]``s``[``tring``]'`` 'cms'       template for comments; used for fold-marker        $****`
`'``c``[``om``]``p``[``atible``]'``      'cp'        behave Vi-compatible as much as possible           $****`
`'``c``[``om``]``p``[``le``]``t``[``e``]'``      'cpt'       specify how Insert-mode completion works           $****`
`'``c``[``omplete``]``fu``[``nc``]'``    'cfu'       function to be used for Insert mode completion     $****`
`'``c``[``omplete``]``o``[``p``]``t``'``     'cot'       options for Insert-mode completion                 $****`
`'``c``[``omplete``]``p``[``o``]``p``[``up``]'`` 'cpp'       options for Insert-mode completion info popup      $****`
`'``c``[``omplete``]``sl``[``ash``]'``   'csl'       like '``shellslash``' for completion                   $****`
`'``co``[``nceal``]``cu``[``rsor``]'``   'cocu'      whether concealable text is hidden in cursor line  $****`
`'``co``[``nceal``]``le``[``vel``]'``    'cole'      whether concealable text is shown or hidden        $****`
`'``c``[``on``]``f``[``irm``]'``         'cf'        ask what to do about unsaved/read-only files       $****`
`'``consk``[``ey``]'``           'consk'     get keys directly from console (MS-DOS only)       $****`
`'``c``[``opy``]``i``[``ndent``]'``      'ci'        make '``autoindent``' use existing indent structure    $****`
`'``cpo``[``ptions``]'``         'cpo'       flags for Vi-compatible behavior                   $****`
`'``c``[``rypt``]``m``[``ethod``]'``     'cm'        type of encryption to use for file writing         $****`
`'``cs``[``cope``]``p``[``ath``]``c``[``omp``]'``'cspc'      how many components of path to show                $****`
`'``cs``[``cope``]``prg``'``         'csprg'     command to execute cscope                          $****`
`'``cs``[``cope``]``q``[``uick``]``f``[``ix``]'``'csqf'      use quickfix window for cscope results             $****`
`'``cs``[``cope``]``re``[``lative``]'``  'csre'      Use cscope.out path basename as prefix             $****`
`'``cs``[``cope``]``t``[``ag``]'``       'cst'       use cscope for tag commands                        $****`
`'``cs``[``cope``]``t``[``ag``]``o``[``rder``]'``'csto'      determines "``:cstag``" search order                   $****`
`'``cs``[``cope``]``verb``[``ose``]'``   'csverb'    give messages when adding a cscope database        $****`
`'``c``[``u``]``r``[``sor``]``b``[``ind``]'``    'crb'       move cursor in window as it moves in other windows $****`
`'``cu``[``rsor``]``c``[``olumn``]'``    'cuc'       highlight screen column of the cursor              $****`
`'``cu``[``rsor``]``l``[``ine``]'``      'cul'       highlight screen line of cursor                    $****`
`'``cu``[``rsor``]``l``[``ine``]``opt``'``   'culopt'    settings for '``cursorline``'                          $****`
`
`
`'``debug``'``               'debug'     set to "``msg``" to see all error messages             $****`
`'``def``[``ine``]'``            'def'       pattern to be used to find a macro definition      $****`
`'``de``[``l``]``co``[``mbine``]'``      'deco'      delete combining characters on their own           $****`
`'``dict``[``ionary``]'``        'dict'      list of file names used for keyword completion     $****`
`'``diff``'``                'diff'      use diff mode for current window.                  $****`
`'``d``[``iff``]``ex``[``pr``]'``        'dex'       expression used to obtain a diff file              $****`
`'``di``[``ffo``]``p``[``t``]'``         'dip'       options for using Diff-mode                        $****`
`'``d``[``i``]``g``[``raph``]'``         'dg'        enable entering of digraphs in Insert mode         $****`
`'``dir``[``ectory``]'``         'dir'       list of directory names for swap file              $****`
`'``d``[``ispla``]``y``'``           'dy'        list of flags for how to display text              $****`
`
`
`'``ead``[``irection``]'``       'ead'       in which direction '``equalalways``' works             $****`
`'``ed``[``compatible``]'``      'ed'        toggle flags of "``:substitute``" command              $****`
`'``emo``[``ji``]'``             'emo'       emoji characters are considered full width         $****`
`'``enc``[``oding``]'``          'enc'       encoding used internally                           $****`
`'``e``[``nd``]``o``[``f``]``l``[``ine``]'``     'eol'       write for last line in file                        $****`
`'``e``[``qual``]``a``[``lways``]'``     'ea'        windows are automatically made same size           $****`
`'``e``[``qual``]``p``[``rg``]'``        'ep'        external program to use for "``=``" command            $****`
`'``e``[``rror``]``b``[``ells``]'``      'eb'        ring bell for error messages                       $****`
`'``e``[``rror``]``f``[``ile``]'``       'ef'        name of errorfile for QuickFix-mode                $****`
`'``e``[``rror``]``f``[``or``]``m``[``at``]'``   'efm'       description of lines in error file                 $****`
`'``e``[``sc``]``k``[``eys``]'``         'ek'        recognize function keys in Insert-mode             $****`
`'``e``[``vent``]``i``[``gnore``]'``     'ei'        autocommand events that are ignored                $****`
`'``e``[``xpand``]``t``[``ab``]'``       'et'        use spaces when is inserted                        $****`
`'``ex``[``rc``]'``              'ex'        read ``.vimrc`` and ``.exrc`` in current directory         $****`
`
`
`'fileencoding'    'fenc'      file encoding for multi-byte text                      $****`
`'fileencodings'   'fencs'     automatically detected character encodings             $****`
`'fileformat'      'ff'        file format used for file I/O                          $****`
`'fileformats'     'ffs'       automatically detected values for '``fileformat``'         $****`
`'fileignorecase'  'fic'       ignore case when using file names                      $****`
`'filetype'        'ft'        type of file, used for autocommands                    $****`
`'fillchars'       'fcs'       characters to use for displaying special items         $****`
`'fixendofline'    'fixeol'    make sure last line in file has ``<``EOL``>``                  $****`
`'fkmap'           'fk'        obsolete option for Farsi                              $****`
`'foldclose'       'fcl'       close a fold when the cursor leaves it                 $****`
`'foldcolumn'      'fdc'       width of column used to indicate folds                 $****`
`'foldenable'      'fen'       set to display all folds open                          $****`
`'foldexpr'        'fde'       expression used when '``foldmethod``' is "``expr``"            $****`
`'foldignore'      'fdi'       ignore lines when '``foldmethod``' is "``indent``"             $****`
`'foldlevel'       'fdl'       close folds with a level higher than this              $****`
`'foldlevelstart'  'fdls'      '``foldlevel``' when starting to edit a file               $****`
`'foldmarker'      'fmr'       markers used when '``foldmethod``' is "``marker``"             $****`
`'foldmethod'      'fdm'       folding type                                           $****`
`'foldminlines'    'fml'       minimum number of lines for a fold to be closed        $****`
`'foldnestmax'     'fdn'       maximum fold depth                                     $****`
`'foldopen'        'fdo'       for which commands a fold will be opened               $****`
`'foldtext'        'fdt'       expression used to display for a closed fold           $****`
`'formatexpr'      'fex'       expression used with "``gq``" command                      $****`
`'formatlistpat'   'flp'       pattern used to recognize a list header                $****`
`'formatoptions'   'fo'        how automatic formatting is to be done                 $****`
`'formatprg'       'fp'        name of external program used with "``gq``" command        $****`
`'fsync'           'fs'        whether to invoke ``fsync()`` after file write             $****`
`
`
`'gdefault'        'gd'        ``"``:substitute``"`` flag '``g``'`` is default on                   $****`
`'grepformat'      'gfm'       format of ``'``grepprg``'`` output                             $****`
`'grepprg'         'gp'        program to use for ``"``:grep``"``                             $****`
`'guicursor'       'gcr'       GUI: settings for cursor shape and blinking            $****`
`'guifont'         'gfn'       GUI: Name(s) of font(s) to be used                     $****`
`'guifontset'      'gfs'       GUI: Names of multi-byte fonts to be used              $****`
`'guifontwide'     'gfw'       list of font names for double-wide characters          $****`
`'guiheadroom'     'ghr'       GUI: pixels room for window decorations                $****`
`'guioptions'      'go'        GUI: Which components and options are used             $****`
`'guipty'                      GUI: try to use a pseudo-tty for ``"``:!``"`` commands         $****`
`'guitablabel'     'gtl'       GUI: custom label for a tab page                       $****`
`'guitabtooltip'   'gtt'       GUI: custom tooltip for a tab page                     $****`
`
`
`'helpfile'        'hf'        full path name of main help file                       $****`
`'helpheight'      'hh'        minimum height of a new help window                    $****`
`'helplang'        'hlg'       preferred help languages                               $****`
`'hidden'          'hid'       don't unload buffer when it is |abandon|ed             $****`
`'highlight'       'hl'        sets highlighting mode for various occasions           $****`
`'history'         'hi'        number of command-lines that are remembered            $****`
`'hkmap'           'hk'        Hebrew keyboard mapping                                $****`
`'hkmapp'          'hkp'       phonetic Hebrew keyboard mapping                       $****`
`'hlsearch'        'hls'       highlight matches with last search pattern             $****`
`
`
`'icon'                        let Vim set the text of the window icon                $****`
`'iconstring'                  string to use for Vim icon text                        $****`
`'ignorecase'      'ic'        ignore case in search patterns                         $****`
`'imactivatefunc'  'imaf'      function to enable/disable the X input method          $****`
`'imactivatekey'   'imak'      key that activates X input method                      $****`
`'imcmdline'       'imc'       use IM when starting to edit a command line            $****`
`'imdisable'       'imd'       do not use IM in any mode                              $****`
`'iminsert'        'imi'       use :lmap or IM in Insert mode                         $****`
`'imsearch'        'ims'       use :lmap or IM when typing a search pattern           $****`
`'imstatusfunc'    'imsf'      function to obtain X input method status               $****`
`'imstyle'         'imst'      specifies input style of input method                  $****`
`'include'         'inc'       pattern to be used to find an include file             $****`
`'includeexpr'     'inex'      expression used to process an include line             $****`
`'incsearch'       'is'        highlight match while typing search pattern            $****`
`'indentexpr'      'inde'      expression used to obtain indent of a line             $****`
`'indentkeys'      'indk'      keys that trigger indenting with 'indentexpr'          $****`
`'infercase'       'inf'       adjust case of match for keyword completion            $****`
`'insertmode'      'im'        start the edit of a file in Insert mode                $****`
`'isfname'         'isf'       characters included in file names and pathnames        $****`
`'isident'         'isi'       characters included in identifiers                     $****`
`'iskeyword'       'isk'       characters included in keywords                        $****`
`'isprint’         'isp'       printable characters                                   $****`
`
`
`'joinspaces'      'js'        two spaces after a period with a join command          $****`
`
`
`'key'                         encryption key                                         $****`
`'keymap'          'kmp'       name of a keyboard mapping                             $****`
`'keymodel'        'km'        enable starting/stopping selection with keys           $****`
`'keywordprg'      'kp'        program to use for "K" command                         $****`
`
`
`'langmap'         'lmap'      alphabetic characters for other language mode          $****`
`'langmenu'        'lm'        language to be used for menus                          $****`
`'langnoremap'     'lnr'       do not apply 'langmap' to mapped characters            $****`
`'langremap'       'lrm'       do apply 'langmap' to mapped characters                $****`
`'laststatus'      'ls'        tells when last window has status lines                $****`
`'lazyredraw'      'lz'        don't redraw while executing macros                    $****`
`'linebreak'       'lbr'       wrap long lines at a blank                             $****`
`'lines'                       number of lines in display                             $****`
`'linespace'       'lsp'       number of pixel lines to use between characters        $****`
`'lisp'                        automatic indenting for Lisp                           $****`
`'lispwords'       'lw'        words that change how lisp indenting works             $****`
`'list'                        show ``<``Tab``>`` and ``<``EOL``>``                                   $****`
`'listchars'       'lcs'       characters for displaying in list mode                 $****`
`'loadplugins'     'lpl'       load plugin scripts when starting up                   $****`
`'luadll'                      name of Lua dynamic library                            $****`
`
`
`'macatsui'                    Mac GUI: use ATSUI text drawing                        $****`
`'magic'                       changes special characters in search patterns          $****`
`'makeef'          'mef'       name of errorfile for ":make"                          $****`
`'makeencoding'    'menc'      encoding of external make/grep commands                $****`
`'makeprg'         'mp'        program to use for the ":make" command                 $****`
`'matchpairs'      'mps'       pairs of characters that "%" can match                 $****`
`'matchtime'       'mat'       tenths of a second to show matching paren              $****`
`'maxcombine'      'mco'       maximum nr of combining characters displayed           $****`
`'maxfuncdepth'    'mfd'       maximum recursive depth for user functions             $****`
`'maxmapdepth'     'mmd'       maximum recursive depth for mapping                    $****`
`'maxmem'          'mm'        maximum memory (in Kbyte) used for one buffer          $****`
`'maxmempattern'   'mmp'       maximum memory (in Kbyte) used for pattern search      $****`
`'maxmemtot'       'mmt'       maximum memory (in Kbyte) used for all buffers         $****`
`'menuitems'       'mis'       maximum number of items in a menu                      $****`
`'mkspellmem'      'msm'       memory used before |:mkspell| compresses tree          $****`
`'modeline'        'ml'        recognize modelines at start or end of file            $****`
`'modelineexpr'    'mle'       allow setting expression options from a modeline       $****`
`'modelines'       'mls'       number of lines checked for modelines                  $****`
`'modifiable'      'ma'        changes to text are not possible                       $****`
`'modified'        'mod'       buffer has been modified                               $****`
`'more'                        pause listings when the whole screen is filled         $****`
`'mouse'                       enable use of mouse clicks                             $****`
`'mousefocus'      'mousef'    keyboard focus follows the mouse                       $****`
`'mousehide'       'mh'        hide mouse pointer while typing                        $****`
`'mousemodel'      'mousem'    changes meaning of mouse buttons                       $****`
`'mouseshape'      'mouses'    shape of mouse pointer in different modes              $****`
`'mousetime'       'mouset'    max time between mouse double-click                    $****`
`'mzquantum'       'mzq'       the interval between polls for MzScheme threads        $****`
`'mzschemedll'                 name of MzScheme dynamic library                       $****`
`'mzschemegcdll'               name of MzScheme dynamic library for GC                $****`
`
`
`'nrformats'       'nf'        number formats recognized for Ctrl-A command           $****`
`'number'          'nu'        print the line number in front of each line            $****`
`'numberwidth'     'nuw'       number of columns used for line number                 $****`
`
`
`'omnifunc'        'ofu'       function for filetype-specific completion              $****`
`'opendevice'      'odev'      allow reading/writing devices on MS-Windows            $****`
`'operatorfunc'    'opfunc'    function to be called for |g@| operator                $****`
`'osfiletype'      'oft'       no longer supported                                    $****`
`
`
`'packpath'        'pp'        list of directories used for packages                  $****`
`'paragraphs'      'para'      nroff macros that separate paragraphs                  $****`
`'paste'                       allow pasting text                                     $****`
`'pastetoggle'     'pt'        key code that causes 'paste' to toggle                 $****`
`'patchexpr'       'pex'       expression used to patch a file                        $****`
`'patchmode'       'pm'        keep oldest version of a file                          $****`
`'path'            'pa'        list of directories searched with "gf" et al           $****`
`'perldll'                     name of Perl dynamic library                           $****`
`'preserveindent'  'pi'        preserve indent structure when reindenting             $****`
`'previewheight'   'pvh'       height of preview window                               $****`
`'previewpopup'    'pvp'       use popup window for preview                           $****`
`'previewwindow'   'pvw'       identifies preview window                              $****`
`'printdevice'     'pdev'      name of printer to be used for :hardcopy               $****`
`'printencoding'   'penc'      encoding to be used for printing                       $****`
`'printexpr'       'pexpr'     expression used to print PostScript for :hardcopy      $****`
`'printfont'       'pfn'       name of font to be used for :hardcopy                  $****`
`'printheader'     'pheader'   format of header used for :hardcopy                    $****`
`'printmbcharset'  'pmbcs'     CJK character set to be used for :hardcopy             $****`
`'printmbfont'     'pmbfn'     font names to be used for CJK output of :hardcopy      $****`
`'printoptions'    'popt'      controls format of :hardcopy output                    $****`
`'prompt'          'prompt'    enable prompt in Ex mode                               $****`
`'pumheight'       'ph'        maximum height of popup menu                           $****`
`'pumwidth'        'pw'        minimum width of popup menu                            $****`
`'pythondll'                   name of the Python 2 dynamic library                   $****`
`'pythonhome'                  name of the Python 2 home directory                    $****`
`'pythonthreedll'              name of the Python 3 dynamic library                   $****`
`'pythonthreehome'             name of the Python 3 home directory                    $****`
`'pyxversion'      'pyx'       Python version used for pyx* commands                  $****`
`
`
`'quoteescape'     'qe'        escape characters used in a string                     $****`
`
`
`'readonly'        'ro'        disallow writing buffer                                $****`
`'redrawtime'      'rdt'       timeout for 'hlsearch' and |:match| highlighting       $****`
`'regexpengine'    're'        default regexp engine to use                           $****`
`'relativenumber'  'rnu'       show relative line number in front of each line        $****`
`'remap'                       allow mappings to work recursively                     $****`
`'renderoptions'   'rop'       options for text rendering on Windows                  $****`
`'report'                      threshold for reporting nr. of lines changed           $****`
`'restorescreen'   'rs'        Win32: restore screen when exiting                     $****`
`'revins'          'ri'        inserting characters will work backwards               $****`
`'rightleft'       'rl'        window is right-to-left oriented                       $****`
`'rightleftcmd'    'rlc'       commands for which editing works right-to-left         $****`
`'rubydll'                     name of Ruby dynamic library                           $****`
`'ruler'           'ru'        show cursor line and column in status line             $****`
`'rulerformat'     'ruf'       custom format for ruler                                $****`
`'runtimepath'     'rtp'       list of directories used for runtime files             $****`
`
`
`'scroll'          'scr'       lines to scroll with Ctrl-u and Ctrl-d                 $****`
`'scrollbind'      'scb'       scroll in window as other windows scroll               $****`
`'scrollfocus'     'scf'       scroll wheel applies to window under pointer           $****`
`'scrolljump'      'sj'        minimum number of lines to scroll                      $****`
`'scrolloff'       'so'        minimum nr. of lines above and below cursor            $****`
`'scrollopt'       'sbo'       how 'scrollbind' should behave                         $****`
`'sections'        'sect'      nroff macros that separate sections                    $****`
`'secure'                      secure mode for reading .vimrc in current dir          $****`
`'selection'       'sel'       what type of selection to use                          $****`
`'selectmode'      'slm'       when to use Select mode instead of Visual mode         $****`
`'sessionoptions'  'ssop'      options for |:mksession|                               $****`
`'shell'           'sh'        name of shell to use for external commands             $****`
`'shellcmdflag'    'shcf'      flag to shell to execute one command                   $****`
`'shellpipe'       'sp'        string to put output of ":make" in error file          $****`
`'shellquote'      'shq'       quote character(s) for around shell command            $****`
`'shellredir'      'srr'       string to put output of filter in a temp file          $****`
`'shellslash'      'ssl'       use forward slash for shell file names                 $****`
`'shelltemp'       'stmp'      whether to use a temp file for shell commands          $****`
`'shelltype'       'st'        Amiga: influences how to use a shell                   $****`
`'shellxescape'    'sxe'       characters to escape when 'shellxquote' is (           $****`
`'shellxquote'     'sxq'       like 'shellquote', but include redirection             $****`
`'shiftround'      'sr'        round indent to multiple of shiftwidth                 $****`
`'shiftwidth'      'sw'        number of spaces to use for (auto)indent step          $****`
`'shortmess'       'shm'       list of flags, reduce length of messages               $****`
`'shortname'       'sn'        Filenames assumed to be 8.3 chars                      $****`
`'showbreak'       'sbr'       string to use at start of wrapped lines                $****`
`'showcmd'         'sc'        show (partial) command in status line                  $****`
`'showfulltag'     'sft'       show full tag pattern when completing tag              $****`
`'showmatch'       'sm'        briefly jump to matching bracket if insert one         $****`
`'showmode'        'smd'       message on status line to show current mode            $****`
`'showtabline'     'stal'      tells when tab pages line is displayed                 $****`
`'sidescroll'      'ss'        minimum number of columns to scroll horizontal         $****`
`'sidescrolloff'   'siso'      min. nr. of columns to left and right of cursor        $****`
`'signcolumn'      'scl'       when to display sign column                            $****`
`'smartcase'       'scs'       no ignore case when pattern has uppercase              $****`
`'smartindent'     'si'        smart autoindenting for C programs                     $****`
`'smarttab'        'sta'       use 'shiftwidth' when inserting                        $****`
`'softtabstop'     'sts'       number of spaces that uses while editing               $****`
`'spell'                       enable spell checking                                  $****`
`'spellcapcheck'   'spc'       pattern to locate end of a sentence                    $****`
`'spellfile'       'spf'       files where |zg| and |zw| store words                  $****`
`'spelllang'       'spl'       language(s) to do spell checking for                   $****`
`'spellsuggest'    'sps'       method(s) used to suggest spelling corrections         $****`
`'splitbelow'      'sb'        new window from split is below current one             $****`
`'splitright'      'spr'       new window is put right of current one                 $****`
`'startofline'     'sol'       commands move cursor to first non-blank in line        $****`
`'statusline'      'stl'       custom format for status line                          $****`
`'suffixes'        'su'        suffixes that are ignored with multiple match          $****`
`'suffixesadd'     'sua'       suffixes added when searching for a file               $****`
`'swapfile'        'swf'       whether to use a swapfile for a buffer                 $****`
`'swapsync'        'sws'       how to sync swap file                                  $****`
`'switchbuf'       'swb'       sets behavior when switching to another buffer         $****`
`'synmaxcol'       'smc'       maximum column to find syntax items                    $****`
`'syntax'          'syn'       syntax to be loaded for current buffer                 $****`
`
`
`'tabline'         'tal'       custom format for console tab pages line               $****`
`'tabpagemax'      'tpm'       maximum number of tab pages for |-p| and "tab all"     $****`
`'tabstop'         'ts'        number of spaces that in file uses                     $****`
`'tagbsearch'      'tbs'       use binary searching in tags files                     $****`
`'tagcase'         'tc'        how to handle case when searching in tags files        $****`
`'tagfunc'         'tfu'       function to get list of tag matches                    $****`
`'taglength'       'tl'        number of significant characters for a tag             $****`
`'tagrelative'     'tr'        file names in tag file are relative                    $****`
`'tags'            'tag'       list of file names used by tag command                 $****`
`'tagstack'        'tgst'      push tags onto tag stack                               $****`
`'tcldll'                      name of Tcl dynamic library                            $****`
`'term'                        name of terminal                                       $****`
`'termbidi'        'tbidi'     terminal takes care of bi-directionality               $****`
`'termencoding'    'tenc'      character encoding used by terminal                    $****`
`'termguicolors'   'tgc'       use GUI colors for terminal                            $****`
`'termwinkey'      'twk'       key that precedes a Vim command in a terminal          $****`
`'termwinscroll'   'twsl'      max number of scrollback lines in a terminal window    $****`
`'termwinsize'     'tws'       size of a terminal window                              $****`
`'termwintype'     'twt'       MS-Windows: type of pty to use for terminal window     $****`
`'terse'                       shorten some messages                                  $****`
`'textauto'        'ta'        obsolete, use 'fileformats'                            $****`
`'textmode'        'tx'        obsolete, use 'fileformat'                             $****`
`'textwidth'       'tw'        maximum width of text that is being inserted           $****`
`'thesaurus'       'tsr'       list of thesaurus files for keyword completion         $****`
`'tildeop'         'top'       tilde command "~" behaves like an operator             $****`
`'timeout'         'to'        time out on mappings and key codes                     $****`
`'timeoutlen'      'tm'        time out time in milliseconds                          $****`
`'title'                       let Vim set title of window                            $****`
`'titlelen'                    percentage of 'columns' used for window title          $****`
`'titleold'                    old title, restored when exiting                       $****`
`'titlestring'                 string to use for Vim window title                     $****`
`'toolbar'         'tb'        GUI: which items to show in toolbar                    $****`
`'toolbariconsize' 'tbis'      size of toolbar icons (for GTK 2 only)                 $****`
`'ttimeout'                    time out on mappings                                   $****`
`'ttimeoutlen'     'ttm'       time out time for key codes in milliseconds            $****`
`'ttybuiltin'      'tbi'       use built-in termcap before external termcap           $****`
`'ttyfast'         'tf'        indicates a fast terminal connection                   $****`
`'ttymouse'        'ttym'      type of mouse codes generated                          $****`
`'ttyscroll'       'tsl'       maximum number of lines for a scroll                   $****`
`'ttytype'         'tty'       alias for 'term'                                       $****`
`
`
`'undodir'         'udir'      where to store undo files                              $****`
`'undofile'        'udf'       save undo information in a file                        $****`
`'undolevels'      'ul'        maximum number of changes that can be undone           $****`
`'undoreload'      'ur'        max nr of lines to save for undo on a buffer reload    $****`
`'updatecount'     'uc'        after this many characters flush swap file             $****`
`'updatetime'      'ut'        after this many milliseconds flush swap file           $****`
`
`
`'varsofttabstop'  'vsts'      a list of number of spaces when typing                 $****`
`'vartabstop'      'vts'       a list of number of spaces for s                       $****`
`'verbose'         'vbs'       give informative messages                              $****`
`'verbosefile'     'vfile'     file to write messages in                              $****`
`'viewdir'         'vdir'      directory where to store files with :mkview            $****`
`'viewoptions'     'vop'       specifies what to save for :mkview                     $****`
`'viminfo'         'vi'        use .viminfo file upon startup and exiting             $****`
`'viminfofile'     'vif'       file name used for viminfo file                        $****`
`'virtualedit'     've'        when to use virtual editing                            $****`
`'visualbell'      'vb'        use visual bell instead of beeping                     $****`
`
`
`'warn'                        warn for shell command when buffer was changed         $****`
`'weirdinvert'     'wiv'       for terminals that have weird inversion method         $****`
`'whichwrap'       'ww'        allow specified keys to cross line boundaries          $****`
`'wildchar'        'wc'        command-line character for wildcard expansion          $****`
`'wildcharm'       'wcm'       like 'wildchar' but also works when mapped             $****`
`'wildignore'      'wig'       files matching these patterns are not completed        $****`
`'wildignorecase'  'wic'       ignore case when completing file names                 $****`
`'wildmenu'        'wmnu'      use menu for command line completion                   $****`
`'wildmode'        'wim'       mode for 'wildchar' command-line expansion             $****`
`'wildoptions'     'wop'       specifies how command line completion is done          $****`
`'winaltkeys'      'wak'       when the windows system handles ALT keys               $****`
`'wincolor'        'wcr'       window-local highlighting                              $****`
`'window'          'wi'        nr of lines to scroll for Ctrl-b and Ctrl-b            $****`
`'winheight'       'wh'        minimum number of lines for the current window         $****`
`'winfixheight'    'wfh'       keep window height when opening/closing windows        $****`
`'winfixwidth'     'wfw'       keep window width when opening/closing windows         $****`
`'winminheight'    'wmh'       minimum number of lines for any window                 $****`
`'winminwidth'     'wmw'       minimal number of columns for any window               $****`
`'winptydll'                   name of winpty dynamic library                         $****`
`'winwidth'        'wiw'       minimal number of columns for current window           $****`
`'wrap'                        long lines wrap and continue on next line              $****`
`'wrapmargin'      'wm'        chars from right where wrapping starts                 $****`
`'wrapscan'        'ws'        searches wrap around the end of file                   $****`
`'write'                       writing to a file is allowed                           $****`
`'writeany'        'wa'        write to file with no need for "!" override            $****`
`'writebackup'     'wb'        make a backup before overwriting a file                $****`
`'writedelay'      'wd'        delay this many msec for each char (for debug)         $****`

--------------------

**## Undo/Redo commands****## 
**

`|u|      N ``u``        undo last N changes                                              $****`
`|Ctrl-r| N ``Ctrl-r``   redo last N undone changes                                       $****`
`|U|        ``U``        restore last changed line                                        $****`

--------------------

**## External commands****## 
**

`|:shell|   ``:sh``[``ell``]``   start a shell                                                  $****`
`|:!|       ``:!``{``command``}``
`
`                      execute {command} with a shell                                 $****`
`|K|        ``K``          lookup keyword under cursor with                               $****`
`                      'keywordprg' program (default: "man")                          $****``
`

--------------------
**Lastedit 20210722**

**## Quickfix commands****## 
**

`|:cc|          ``:cc`` [``nr``]``                                                              $****`
`                      display error ``[``nr``]`` (default is same again)`
`|:cnext|       ``:cn``    display `_`next`_` error                                             $****`
`|:cprevious|   ``:cp``    display `_`previous`_` error                                         $****`
`|:clist|       ``:cl``    list all errors                                                $****`
`|:cfile|       ``:cf``    read errors from file 'errorfile'                              $****`
`|:cgetbuffer|  ``:cgetb`` like :cbuffer but don't jump to first error                    $****`
`|:cgetfile|    ``:cg``    like :cfile but don't jump to first error                      $****`
`|:cgetexpr|    ``:cgete`` like :cexpr but don't jump to first error                      $****`
`|:caddfile|    ``:caddf`` add errors from error file to current quickfix list            $****`
`|:caddexpr|    ``:cad``   add errors from an expression to current quickfix list         $****`
`|:cbuffer|     ``:cb``    read errors from text in a buffer                              $****`
`|:cexpr|       ``:cex``   read errors from an expression                                 $****`
`|:cquit|       ``:cq``    quit without writing and return error code (to compiler)       $****`
`|:make|        ``:make`` [``args``]``                                                          $****``
`
`                  ``    start make, read errors, and jump to first error`
`|:grep|        ``:gr``[``ep``] [``args``]``                                                        $****``
`
`                    ``  execute 'grepprg' to find matches and jump to first one        ``
`

--------------------

**## Various commands****## 
**

`|Ctrl-l|       ``Ctrl-l``    clear and redraw screen                                     $****`
`|Ctrl-g|       ``Ctrl-g``    show current file name (with path) and cursor position      $****`
`|ga|           ``ga``        show ascii value of character under cursor in decimal,      $****`
`                         hex, and octal`
`|g8|           ``g8``        for utf-8 encoding: show byte sequence for character        $****`
`                         under cursor in hex`
`|g_Ctrl-g|     ``g Ctrl-g``  show cursor column, line, and character position            $****`
`|Ctrl-c|       ``Ctrl-c``    during searches: Interrupt search                           $****`
`|dos-Ctrl-Break|  ``Ctrl-Break``                                                         $****`
`                         MS-Windows: during searches: Interrupt search`
`|<Del>|        ``<``Del``>``     while entering a count: delete last character               $****`
`|:version|     ``:ve``[``rsion``]``                                                            $****`
`                         show version information`
`|:mode|        ``:mode N``   set screen mode to `*`N`*` (obsolete)                             $****`
`|:normal|      ``:norm``[``al``][``!``] {``commands``}``                                               $****`
`                         execute Normal mode commands`
`|Q|            ``Q``         switch to "Ex" mode                                         $****`
`
`
`|:redir|       ``:redir`` ``>``{``file``}``                                                        $****`
`                         redirect messages to ``{``file``}``
`
`|:silent|      ``:silent``[``!``] {``command``}``                                                  $****`
`                         execute ``{``command``}`` silently`
`|:confirm|     ``:confirm`` ``{``command``}``                                                    $****`
`                         quit, write, etc., asking about unsaved changes or`
`                         read-only files`
`|:browse|      ``:browse`` ``{``command``}``                                                     $****`
`                         open/read/write file, using a/ file selection dialog``
`

--------------------

**## Ex - Command-line editing****## 
**

`|c_<Esc>|     ``<``Esc``>``    abandon command-line (if 'wildchar’ is , type it twice)       $****`
`
`
`|c_Ctrl-v|    ``Ctrl-v`` {``char``}``                                                          $****`
`                       insert ``{``char``}`` literally`
`|c_Ctrl-v|    ``Ctrl-v`` {``number``}``                                                        $****`
`                       enter decimal value of character (up to three digits)`
`|c_Ctrl-k|    ``Ctrl-k`` {``char1``} {``char2``}``                                                 $****`
`                       enter digraph (See |Q_di|)`
`|c_Ctrl-r|    ``Ctrl-r`` {``register``}``                                                      $****`
`                       insert contents of a register`
`
`
`|c_<Left>|    ``<``Left``>/<``Right``>``                                                         $****`
`                       cursor one `_`character`_` left/right`
`|c_<S-Left>|  ``<``S-Left``>/<``S-Right``>``                                                     $****`
`                       cursor one `_`word`_` left/right`
`|c_Ctrl-b|    ``Ctrl-b``/``Ctrl-e``                                                          $****`
`                       cursor to beginning/end of command-line`
`
`
`|c_<BS>|      ``<``BS``>``     delete `_`character`_` `_`in front`_` of cursor                           $****`
`|c_<Del>|     ``<``Del``>``    delete `_`character`_` `_`under`_` cursor                                 $****`
`|c_Ctrl-w|    ``Ctrl-w``   delete `_`word`_` in front of cursor                                $****`
`|c_Ctrl-u|    ``Ctrl-u``   remove `_`all`_` characters                                         $****`
`
`
`|c_<Up>|      ``<``Up``>/<``Down``>``                                                            $****`
`                       recall older/newer command-line that starts`
`                       with current command`
`|c_<S-Up>|    ``<``S-Up``>/<``S-Down``>``                                                        $****`
`                       recall older/newer command-line from history`
`|c_Ctrl-g|    ``Ctrl-g``   `_`next`_` match when 'incsearch' is active                         $****`
`|c_Ctrl-t|    ``Ctrl-t``   `_`previous`_` match when 'incsearch' is active                     $****`
`|:history|    ``:his``[``tory``]``                                                             $****`
`                       show older command-lines`
`
`
`Context-sensitive completion on command-line:`
`
`
`|c_wildchar|  '``wildchar``' (default: ``<``Tab``>``)                                            $****`
`                       do completion on pattern in front of cursor; if there are`
`                       multiple mathes, beep and show first one; further`
`                       'wildchar' will show next ones`
`|c_Ctrl-d|    ``Ctrl-d``   list all names that match pattern in front of cursor          $****`
`|c_Ctrl-a|    ``Ctrl-a``   insert all names that match pattern in front of cursor        $****`
`|c_Ctrl-l|    ``Ctrl-l``   insert longest common part of names that match pattern        $****`
`|c_Ctrl-n|    ``Ctrl-n``   after 'wildchar' with multiple matches: go to `_`next`_` match      $****`
`|c_Ctrl-p|    ``Ctrl-p``   after 'wildchar' with multiple matches: go to `_`prev`_` match      $****``
`

--------------------

**## Ex - Ranges****## 
**

`|:range|      ``,``        separates two line numbers                                    $****`
`|:range|      ``;``        idem, set cursor to first line number                         $****`
`                       before interpreting second one                                $****`
`
`
`|:range|      ``{``number``}`` an absolute line number                                       $****`
`|:range|      ``.``        current line                                                  $****`
`|:range|      ``$``        last line in file                                             $****`
`|:range|      ``%``        equal to 1,$ (the entire file)                                $****`
`|:range|      ``*``        equal to '<,'> (visual area)                                  $****`
`|:range|      ``'t``       position of mark `*`t`*`                                            $****`
`|:range|      ``/``{``pattern``}[``/``]``                                                          $****`
`                       next line where {pattern} matches`
`|:range|      ``?``{``pattern``}[``?``]``                                                          $****`
`                       previous line where {pattern} matches`
`|:range|      ``+``[``num``]``   add [num] to preceding line number (default: 1)               $****`
`|:range|      ``-``[``num``]``   subtract [num] from preceding line number (default: 1)        $****``
`

--------------------

**## Ex - Special characters****## 
**

`|:bar|        ``|``        separates two commands (not for ":global" and ":!")           $****`
`|:quote|      ``"``        begins comment                                                $****`
`
`
`|:_%|         ``%``        current file name (only where a file name is expected)        $****`
`|:_#|         ``#``[``num``]``   alternate file name [num] (only where a file name is          $****`
`                       expected). Note: next seven are typed literally;`
`                       these are not special keys!`
`|:<abuf>|     ``<``abuf``>``   buffer number, for use in an autocommand (only where a        $****`
`                       file name is expected)`
`|:<afile>|    ``<``afile``>``  file name, for use in an autocommand (only where a            $****`
`                       file name is expected)`
`|:<amatch>|   ``<``amatch``>`` what matched with pattern, for use in an                      $****`
`                       autocommand (only where a file name is expected)`
`|:<cword>|    ``<``cword``>``  word under cursor (only where a file name is expected)        $****`
`|:<cWORD>|    ``<``cWORD``>``  WORD under cursor (only where a file name is expected)        $****`
`|:<cfile>|    ``<``cfile``>``  file name under cursor (only where a file name is expected)   $****`
`|:<sfile>|    ``<``sfile``>``  file name of a ":source"d file, within that file (only        $****`
`                       where a file name is expected)`
`
`
`        After "%", "#", "", "" or ""`
`        |::p|        ``:p``        full path                                             $****`
`        |::h|        ``:h``        head (file name removed)                              $****`
`        |::t|        ``:t``        tail (file name only)                                 $****`
`        |::r|        ``:r``        root (extension removed)                              $****`
`        |::e|        ``:e``        extension                                             $****`
`        |::s|        ``:s/``{``pat``}/{``repl``}``/``                                                $****`
`                               substitute ``{``pat``}`` with ``{``repl``}``
`

--------------------

**## Starting Vim****## 
**

`|-vim|   ``vim`` [options]``             start editing with an empty buffer                $****`
`|-file|  ``vim`` [options]`` ``{``file``}`` ..   start editing one or more files                   $****`
`|--|     ``vim`` [options]`` ``-``           read file from stdin                              $****`
`|-tag|   ``vim`` [options]`` ``-t`` ``{``tag``}``    edit the file associated with {tag}               $****`
`|-qf|    ``vim`` [options]`` ``-q`` ``[``fname``]``  start editing in QuickFix mode,                   $****`
`                                   display first error`
`
`
`    Most useful Vim arguments (for full list see |startup-options|)`
`
`
`|-gui|  ``-g``              start GUI (also allows other options)                        $****`
`
`
`|-+|    ``+``[``num``]``          put cursor at line [num] (default: last line)                $****`
`|-+c|   ``+``{``command``}``      execute {command} after loading file                         $****`
`|-+/|   ``+/``{pat} {file} ..   put cursor at first occurrence of {pat}                  $****`
`|-v|    ``-v``              Vi-mode, start ex in Normal-mode                             $****`
`|-e|    ``-e``              Ex-mode, start vim in Ex-mode                                $****`
`|-R|    ``-R``              Read-only mode, implies -n                                   $****`
`|-m|    ``-m``              modifications not allowed (resets 'write' option)            $****`
`|-d|    ``-d``              diff mode |diff|                                             $****`
`|-b|    ``-b``              binary mode                                                  $****`
`|-l|    ``-l``              lisp mode                                                    $****`
`|-A|    ``-A``              Arabic mode ('arabic' is set)                                $****`
`|-F|    ``-F``              Farsi mode ('fkmap' and 'rightleft' are set)                 $****`
`|-H|    ``-H``              Hebrew mode ('hkmap' and 'rightleft' are set)                $****`
`|-V|    ``-V``              Verbose, give informative messages                           $****`
`|-C|    ``-C``              Compatible, set 'compatible' option                          $****`
`|-N|    ``-N``              Nocompatible, reset 'compatible' option                      $****`
`|-r|    ``-r``              give list of swap files                                      $****`
`|-r|    ``-r`` ``{``file``}`` ..    recover aborted edit session                                 $****`
`|-n|    ``-n``              do not create a swap file                                    $****`
`|-o|    ``-o`` ``[``num``]``        open [num] windows (default: one for each file)              $****`
`|-f|    ``-f``              GUI: foreground process, don't fork                          $****`
`                        Amiga: do not restart Vim to open a window (for`
`                        e.g., mail)`
`|-s|    ``-s`` ``{``scriptin``}``   first read commands from file ``{``scriptin``}``                     $****`
`|-w|    ``-w`` ``{``scriptout``}``  write typed chars to file ``{``scriptout``}`` (append)               $****`
`|-W|    ``-W`` ``{``scriptout``}``  write typed chars to file ``{``scriptout``}`` (overwrite)            $****`
`|-T|    ``-T`` ``{terminal}``   set terminal name                                            $****`
`|-d|    ``-d`` ``{``device``}``     Amiga: open ``{``device``}`` to be used as a console                 $****`
`|-u|    ``-u`` ``{``vimrc``}``      read inits from ``{``vimrc``}`` instead of other inits               $****`
`|-U|    ``-U`` ``{``gvimrc``}``     idem, for when starting GUI                                  $****`
`|-i|    ``-i`` ``{``viminfo``}``    read info from ``{``viminfo``}`` instead of other files              $****`
`|---|   ``--``              end of options, other arguments are file names               $****`
`|--help|    ``--help``      show list of arguments and exit                              $****`
`|--version| ``--version``   show version info and exit                                   $****`
`|--|    ``-``               read file from stdin                                         $****`

--------------------

**## Editing a file****## 
**

`       Without !: Fail if changes have been made to the current buffer.`
`          With !: Discard any changes to the current buffer.`
`|:edit_f|  ``:e``[``dit``][``!``] {``file``}`` edit ``{``file``}``                                             $****`
`|:edit|    ``:e``[``dit``][``!``]``        reload current file                                     $****`
`|:enew|    ``:ene``[``w``][``!``]``        edit a new, unnamed buffer                              $****`
`|:find|    ``:fin``[``d``][``!``] {``file``}`` find ``{``file``}`` in 'path' and edit it                       $****`
`
`
`|Ctrl-^| N ``Ctrl-^``            edit alternate file N (equivalent to "``:e #N``")           $****`
`|gf|       ``gf``  or ``]f``         edit file whose name is under cursor                    $****`
`|:pwd|     ``:pwd``              print current directory name                            $****`
`|:cd|      ``:cd`` [``path``]``        change current directory to ``[``path``]``                      $****`
`|:cd-|     ``:cd`` ``-``             back to previous current directory                      $****`
`|:file|    ``:f``[``ile``]``           print current file name and cursor position             $****`
`|:file|    ``:f``[``ile``] {``name``}``    set current file name to ``{``name``}``                         $****`
`|:files|   ``:files``            show alternate file names                               $****`

--------------------

**## Using the argument list****## 
**

`|:args|    ``:ar``[``gs``]``           print argument list, with current file in "[]"          $****`
`|:all|     ``:all``  or ``:sall``    open a window for every file in arg list                $****`
`|:wn|      ``:wn``[``ext``][``!``]``       write file and edit next file                           $****`
`|:wn|      ``:wn``[``ext``][``!``] {``file``}``
`
`                             write to {file} and edit next file, unless              $****`
`                             ``{``file``}`` exists; With !, overwrite existing file`
`|:wN|      ``:wN``[``ext``][``!``] [``file``]``                                                        $****`
`                             write file and edit previous file`
`
`
`         in current window   in new window     ~`
`|:argument|  ``:argu``[``ment``] ``N``   ``:sar``[``gument``]`` N    edit file N                           $****`
`|:next|    ``:n``[``ext``]``           ``:sn``[``ext``]``          edit next file                        $****`
`|:next_f|  ``:n``[``ext``]`` ``{``arglist``}`` ``:sn``[``ext``]`` ``{``arglist``}``  define new arg list                 $****`
`                              and edit first file`
`|:Next|    ``:N``[``ext``]``           ``:sN``[``ext``]``          edit previous file                    $****`
`|:first|   ``:fir``[``st``]``          ``:sfir``[``st``]``         edit first file                       $****`
`|:last|    ``:la``[``st``]``           ``:sla``[``st``]``          edit last file                        $****`

--------------------

**## Writing and quitting****## 
**

`|:w|       ``:``[``range``]``w``[``rite``][``!``]``                                                        $****``
`
`                    ``         write to current file`
`|:w_f|     ``:``[``range``]``w``[``rite``] {``file``}``                                                    $****``
`
`                    ``         write to {file}, unless it already exists`
`|:w_f|     ``:``[``range``]``w``[``rite``]``!`` {``file``}``                                                   $****``
`
`                    ``         write to ``{``file``}``, overwrite an existing file`
`|:w_a|     ``:``[``range``]``w``[``rite``][``!``]`` ``>>``                                                     $****``
`
`                    ``         append to current file`
`|:w_a|     ``:``[``range``]``w``[``rite``][``!``]`` ``>>`` ``{``file``}``                                              $****``
`
`                    ``         append to ``{``file``}``
`
`|:w_c|     ``:``[``range``]``w``[``rite``]`` ``!``{``cmd``}``                                                    $****`
`                    ``         execute {cmd} with [range] lines as standard input`
`|:up|      ``:``[``range``]``up``[``date``][``!``]``                                                       $****``
`
`                    ``         write to current file if modified`
`|:wall|    ``:wa``[``ll``][``!``]``        write all changed buffers                               $****`
`|:q|       ``:q``[``uit``]``           quit current buffer, unless changes have been made;     $****`
`                             Exit Vim when there are no other non-help buffers`
`|:q|       ``:q``[``uit``]``!``          quit current buffer always, discard any changes         $****`
`                             Exit Vim when there are no other non-help buffers       $****`
`|:qa|      ``:qa``[``ll``]``           exit Vim, unless changes have been made                 $****`
`|:qa|      ``:qa``[``ll``]``!``          exit Vim always, discard any changes                    $****`
`|:cq|      ``:cq``               quit without writing and return error code              $****`
`
`
`|:wq|      ``:wq``[``!``]``            write current file and exit                             $****`
`|:wq|      ``:wq``[``!``]`` ``{``file``}``     write to {file} and exit                                $****`
`|:xit|     ``:x``[``it``][``!``] [``file``]``  like "``:wq``" but write only when changes have been made   $****`
`|ZZ|       ``ZZ``                same as "``:x``"                                            $****`
`|ZQ|       ``ZQ``                same as "``:q!``"                                           $****`
`|:xall|    ``:xa``[``ll``][``!``]``  ``or`` ``:wqall``[``!``]``                                                  $****`
`                             write all changed buffers and exit`
`
`
`|:stop|    ``:st``[``op``][``!``]``        suspend Vim or start new shell; if 'aw' option          $****`
`                             is set and [!] not given write buffer`
`|Ctrl-z|   ``Ctrl-z``            same as "``:stop``"                                         $****`

--------------------

**## Automatic Commands****## 
**

`|viminfo-file|    read registers, marks, history at startup, save when exiting`
`
`
`|:rviminfo|  ``:rv``[``iminfo``] [``file``]``    read info from viminfo file ``[``file``]``                $****`
`|:rviminfo|  ``:rv``[``iminfo``]``!`` ``[``file``]``   --idem-- overwrite existing info                  $****`
`|:wviminfo|  ``:wv``[``iminfo``]`` ``[``file``]``    add info to viminfo file ``[``file``]``                   $****`
`|:wviminfo|  ``:wv``[``iminfo``]``!`` ``[``file``]``   write info to viminfo file ``[``file``]``                 $****`
`
`
`|modeline|   Automatic option setting when editing a file`
`
`
`|modeline|   ``vim:``{``set-arg``}``:`` ..    In first and last lines of file                    $****`
`                         (see 'ml' option), {set-arg} is given as an argument`
`                         to ":set"`
`
`
`|autocommand|     Automatic execution of commands on certain events`
`
`
`|:autocmd|   ``:au``             list all autocommands                                   $****`
`|:autocmd|   ``:au`` ``{``event``}``     list all autocommands for ``{``event``}``                       $****`
`|:autocmd|   ``:au`` ``{``event``}`` ``{``pat``}`
`                        ``     list all autocommands for ``{``event``} ``with ``{``pat``}``            $****`
`                      `
`|:autocmd|   ``:au`` ``{``event``}`` ``{``pat``}`` ``{``cmd``}``                                                 $****``
`
`                             enter new autocommands for ``{``event``} ``with ``{``pat``}``
`
`|:autocmd|   ``:au!``            remove all autocommands                                 $****`
`|:autocmd|   ``:au!`` ``{``event``}``    remove all autocommands for ``{``event``}``                     $****`
`|:autocmd|   ``:au!`` ``*`` ``{``pat``}``    remove all autocommands for ``{``pat``}``                       $****`
`|:autocmd|   ``:au!`` ``{``event``}`` ``{``pat``}`
`                             remove all autocommands for ``{``event``}`` with ``{``pat``}``          $****`
`|:autocmd|   ``:au!`` ``{``event``}`` ``{``pat``}`` ``{``cmd``}``                                                $****`
`                             remove all autocommands for ``{``event``}`` with ``{``pat``}`
`                             and enter new one`

--------------------

**## Multi-window commands****## 
**

`|Ctrl-w_s|       ``Ctrl-w`` ``s``  ``or``  ``:split``  split window into two parts                   $****`
`|:split_f|       ``:split`` ``{``file``}``         split window and edit {file} in one of them   $****`
`|:vsplit|        ``:vsplit`` ``{``file``}``        same, but split vertically                    $****`
`|:vertical|      ``:vertical`` ``{``cmd``}``       make {cmd} split vertically                   $****`
`
`
`|:sfind|         ``:sf``[``ind``] {``file``}``       `_`s`_`plit window, `_`f`_`ind {file} in 'path'           $****`
`                                       and edit it      `
`|:terminal|      ``:ter``[``minal``]`` ``{``cmd``}``     open a terminal window                        $****`
`|Ctrl-w_]|       ``Ctrl-w ]``              split window and jump to `_`tag`_` under cursor     $****`
`|Ctrl-w_f|       ``Ctrl-w f``              split window and edit `_`filename`_` under cursor   $****`
`|Ctrl-w_^|       ``Ctrl-w ^``              split window and edit `_`alternate`_` file          $****`
`|Ctrl-w_n|       ``Ctrl-w n`` ``or`` ``:new``      create `_`n`_`ew empty window                       $****`
`|Ctrl-w_q|       ``Ctrl-w q`` ``or`` ``:q``[``uit``]``   quit editing and close window                 $****`
`|Ctrl-w_c|       ``Ctrl-w c`` ``or`` ``:cl``[``ose``]``  make buffer hidden and `_`c`_`lose window           $****`
`|Ctrl-w_o|       ``Ctrl-w o`` ``or`` ``:on``[``ly``]``   make current window `_`o`_`nly `_`o`_`ne on screen        $****`
`
`
`|Ctrl-w_k|       ``Ctrl-w k``              move cursor to window `_`above`_`                   $****`
`|Ctrl-w_j|       ``Ctrl-w j``              move cursor to window `_`below`_`                   $****`
`|Ctrl-w_w|       ``Ctrl-w w``              move cursor to `_`w`_`indow `_`above`_` (wrap)            $****`
`|Ctrl-w_Ctrl-w|  ``Ctrl-w Ctrl-w``         move cursor to `_`w`_`indow `_`below`_` (wrap)            $****`
`|Ctrl-w_t|       ``Ctrl-w t``              move cursor to `_`t`_`op window                     $****`
`|Ctrl-w_b|       ``Ctrl-w b``              move cursor to `_`b`_`ottom window                  $****`
`|Ctrl-w_p|       ``Ctrl-w p``              move cursor to `_`p`_`revious active window         $****`
`
`
`|Ctrl-w_r|       ``Ctrl-w r``              rotate windows `_`downwards`_`                      $****`
`|Ctrl-w_r|       ``Ctrl-w R``              rotate windows `_`upwards`_`                        $****`
`|Ctrl-w_x|       ``Ctrl-w x``              `_`exchange`_` current window with next one         $****`
`
`
`|Ctrl-w_=|       ``Ctrl-w =``              make all windows `_`equal`_` height and width       $****`
`|Ctrl-w_-|       ``Ctrl-w -``              `_`decrease`_` current window `_`height`_`                $****                       `
`|Ctrl-w_+|       ``Ctrl-w +``              `_`increase`_` current window height                $****`
`|Ctrl-w__|       ``Ctrl-w _``              `_`set`_` current window `_`height`_`                     $****`
`                                       (default: very high)`
`
`
`|Ctrl-w_<|       ``Ctrl-w <``              `_`decrease`_` current window `_`width`_`                 $****`
`|Ctrl-w_>|       ``Ctrl-w >``              `_`increase`_` current window width                 $****`
`|Ctrl-w_bar|     ``Ctrl-w |``              `_`set`_` current window `_`width`_`                      $****`
`                                       (default: widest possible)``
`

--------------------

**## Buffer list commands****## 
**

`|:buffers|     ``:buffers``  ``or``  ``:files``     list all known buffer and file names         $****`
`
`
`|:ball|        ``:ba``[``ll``]``   ``or``  ``:sba``[``ll``]``   edit all args/buffers                        $****`
`|:unhide|      ``:unh``[``ide``]`` ``or``  ``:sun``[``hide``]`` edit all loaded buffers                      $****`
`
`
`|:badd|        ``:bad``[``d``]`` ``{``fname``}``          add file name {fname} to list                $****`
`|:bunload|     ``:bun``[``load``][``!``] [``N``]``        unload buffer [N] from memory                $****`
`|:bdelete|     ``:bd``[``elete``][``!``] [``N``]``        unload buffer [N] and delete it from         $****`
`                                        buffer list`
`
`
**`               `****_`in current window`_****`   `****_`in new window`_****`        `****_`~`_**`                            $****`
`|:buffer|      ``:``[``N``]``buffer`` [``N``]``      ``:``[``N``]``sbuffer`` [``N``]``      to arg/buf N                 $****`
`|:bnext|       ``:``[``N``]``bn``[``ext``]`` ``[``N``]``     ``:``[``N``]``sbn``[``ext``] [``N``]``     to Nth next arg/buf          $****`
`|:bNext|       ``:``[``N``]``bN``[``ext``] [``N``]``     :``[``N``]``sbN``[``ext``] [``N``]``     to Nth previous arg/buf      $****`
`|:bprevious|   ``:``[``N``]``bp``[``revious``] [``N``]`` :``[``N``]``sbp``[``revious`` [``N``]``  to Nth previous arg/buf      $****`
`|:bfirst|      ``:bf``[``irst``]``           ``:sbf``[``irst``]``           to first arg/buf             $****`
`|:blast|       ``:bl``[``ast``]``            ``:sbl``[``ast``]``            to last arg/buf              $****`
`|:bmodified|   ``:``[``N``]``bm``[``odified``]`` ``[``N``]`` ``:``[``N``]``sbm``[``odified``] [``N``]`` to Nth modified buf          $****``
`

--------------------

**## Syntax Highlighting****## 
**

`|:syn-on|      ``:syntax`` ``on``      ``start using syntax highlighting``                       $****`
`|:syn-off|     ``:syntax`` ``off``     ``stop using syntax highlighting``                        $****`
`
`
`|:syn-keyword| ``:syntax`` ``keyword`` ``{``group-name``} {``keyword``} ``..``                             $****`
`                               ``add a syntax keyword item``
`
`|:syn-match|   ``:syntax`` ``match`` {``group-name``} {``pattern``} ``...``                              $****`
`                               add syntax match item``
`
`|:syn-region|  ``:syntax`` ``region`` ``{``group-name``} {``pattern``} ``...``                             $****`
`                               add syntax region item``
`
`|:syn-sync|    ``:syntax`` ``sync`` ``[``ccomment`` | ``lines`` {``N``} | ``...``]``                             $****`
`                               ``tell syntax how to sync``
`
`|:syntax|      ``:syntax`` ``[``list``]``  ``list current syntax items``                             $****`
`|:syn-clear|   ``:syntax`` ``clear``   ``clear all syntax info``                                 $****`
`
`
`|:highlight|   ``:highlight`` ``clear``  clear all highlight info``                            $****`
`|:highlight|   ``:highlight`` ``{``group-name``} {``key``}={``arg``} ``..``                                $****`
`                               ``set highlighting for {group-name}``
`
`
`
`|:filetype|    ``:filetype`` ``on``    ``switch on file type detection, without``                $****``
`
`                               ``syntax highlighting``
`
`|:filetype|    ``:filetype plugin indent`` ``on``                                            $****`
`                               ``switch on file type detection, with``
`
`                               ``automatic indenting and settings``
`

--------------------

**## GUI commands****## 
**

`|:gui|         ``:gui``                       UNIX: start the GUI                        $****`
`|:gui|         ``:gui`` ``{``fname``}`` ..            idem, and edit {fname} ..                  $****`
`
`
`|:menu|        ``:menu``                      list all menus                             $****`
`|:menu|        ``:menu`` ``{``mpath``}``              list menus starting with {mpath}           $****`
`|:menu|        ``:menu`` ``{``mpath``}`` ``{``rhs``}``        add menu {mpath}, giving {rhs}             $****`
`|:menu|        ``:menu`` ``{``pri``}`` ``{``mpath``}`` ``{``rhs``}``  idem, with priorities {pri}                $****`
`|:menu|        ``:menu`` ``ToolBar``.``{``name``}`` ``{``rhs``}`` add toolbar item, giving {rhs}             $****`
`|:tmenu|       ``:tmenu`` ``{``mpath``}`` ``{``text``}``      add tooltip to menu {mpath}                $****`
`|:unmenu|      ``:unmenu`` ``{``mpath``}``            remove menu {mpath}                        $****`

--------------------

**## Folding****## 
**

`|'foldmethod'|    set foldmethod=manual   manual folding                             $****`
`                  set foldmethod=indent   folding by indent                          $****`
`                  set foldmethod=expr     folding by 'foldexpr'                      $****`
`                  set foldmethod=syntax   folding by syntax regions                  $****`
`                  set foldmethod=marker   folding by 'foldmarker'                    $****`
`
`
`|zf|        ``zf``{``motion``}``    operator: Define a fold `_`manually`_`                           $****`
`|:fold|     ``:``{``range``}``fold``  define a fold for {range} lines                            $****`
`|zd|        ``zd``            delete one fold under cursor                               $****`
`|zD|        ``zD``            delete all folds under cursor                              $****`
`
`
`|zo|        ``zo``            open one fold under cursor                                 $****`
`|zO|        ``zO``            open all folds under cursor                                $****`
`|zc|        ``zc``            close one fold under cursor                                $****`
`|zC|        ``zC``            close all folds under cursor                               $****`
`
`
`|zm|        ``zm``            fold more: decrease 'foldlevel'                            $****`
`|zM|        ``zM``            close all folds: make 'foldlevel' zero                     $****`
`|zr|        ``zr``            reduce folding: increase 'foldlevel'                       $****`
`|zR|        ``zR``            open all folds: make 'foldlevel' max                       $****`
`
`
`|zn|        ``zn``            fold none: reset 'foldenable'                              $****`
`|zN|        ``zN``            fold normal set 'foldenable'                               $****`
`|zi|        ``zi``            invert 'foldenable'                                        $****`

vim:tw=78:ts=8:noet:ft=help:norl:

--------------------
tag: #macos #vim #manual #98 #user #manual #quickref #quick #reference #guide #official
