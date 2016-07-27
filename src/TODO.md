Initial Release
---------------

This is the minimum required to prove that this is a worthwhile
use of my time, and this work should not be published until these
minimum features work.

NOTE: All of this stuff MUST work with UTF-8 characters.


[x] Make Editor a singleton.
[x] Move lua code to lua_primitives.cc + lua_primitives.h
[x] Make main.cc instantiate the singleton.
[x] Draw status-bar
[x] Draw status-bar in reverse
[x] Prompt for input for status-bar
[x] Implement eval.
[x] Implement loading a file.
[x] Implement saving a file.
[x] Implement is_dirty flag
[x] Implement file/buffer-name for buffer-struct.
[x] Sort out navigation:
    [x] Sort out up - moves past end of row if cur is longer than prev
    [x] Sort out down - moves past end of row if cur is longer than next
    [x] sort out left
    [x] sort out right
    [x] HOME + END -> start of line / end of line
    [x] M-HOME + M-END -> start of file / end of file
[x] Get character at point.
[x] Get/Set point.
[x] sort out insertion:
    [x] insert char in middle of row
    [x] insert char at end of row.
    [x] insert newline at end of row
    [x] insert newline in middle of row.
[x] sort out deletion
    [x] delete at end of line
    [x] delete at start of line
    [x] delete in middle of line.
[ ] Buffers
    [x] Count buffers (`buffers()`
    [x] Get/Set the active buffer (`buffer()` vs. `buffer(N)`).
    [x] create_buffer([name])
    [ ] choose_buffer() - For interactive usage.
    [x] kill_buffer()
    [x] select_buffer( "*Messages*")
[x] prompt() should handle wide-characters.
[x] M-x goto_line() should work.
    -> TODO: Can we bind `goto-line` to `goto_line` via _G ?
[~] "M-x foo" and "M-x foo()" should do the same thing.
[x] Sort out keymap lookup for operations
[x] Move primitives into separate groups.
[ ] Release as 0.0.1


Future Stuffs
-------------

* mark() - use inverse drawing for region between point & mark.
   - Should be much simpler with ncurses.
* syntax highlighting
* regexp search