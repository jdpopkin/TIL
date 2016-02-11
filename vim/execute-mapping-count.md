### Execute Mapping \<count> Times

One obstacle that keeps me from diving too deep into the world of Vim plugins is that plugins tend to behave differently from Vim itself.<sup>[1](#footnote1)</sup> In particular, plugin-defined mappings rarely accept a count the way normal commands do. Custom mappings usually don't work with a provided count, either.

There's a way around this: the current count is accessible in ex commands through the `v:count` and `v:count1` variables. (The former defaults to 0 and the latter defaults to 1.) See `:h v:count` for details, and see [this Vi Stack Exchange question and answers](http://vi.stackexchange.com/questions/3182/is-it-possible-to-make-a-numerically-prefixed-hotkey-run-a-function-that-many-ti) for this example: `nnoremap <M-.> :<C-u>call MyAmazingEnhancedDot(v:count1)<cr>`

<a name="footnote1">1</a>: I think my favorite part of Vi(m) is its internal coherence - it feels less like a program and more like a set of overlapping languages. That's why it really bothers me when `2ysiw"` doesn't surround a word with double quotation marks, even if you would ever need to do this and could use `.` to accomplish the same thing.
