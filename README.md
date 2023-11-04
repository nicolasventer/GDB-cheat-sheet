| <h3>GDB commands by function - simple guide</h3> |                                                     |
| ------------------------------------------------ | --------------------------------------------------- |
| <h4>Breakpoints</h4>                             |                                                     |
| **(gdb) break main**                             | **set a breakpoint on a function**                  |
| (gdb) break 101                                  | set a breakpoint on a line number                   |
| (gdb) break basic.c:101                          | set breakpoint at file and line (or function)       |
| (gdb) info breakpoints                           | show breakpoints                                    |
| (gdb) disable 2                                  | turn a breakpoint off, but don't remove it          |
| (gdb) enable 2                                   | turn disabled breakpoint back on                    |
| (gdb) condition break-no expression              | break only if condition is true                     |
| (gdb) condition 2 i == 20                        | example: break on breakpoint 2 if i equals 20       |
| (gdb) watch expression                           | set software watchpoint on variable                 |
| (gdb) info watchpoints                           | show current watchpoints                            |
| <h4>Running the program</h4>                     |                                                     |
| **(gdb) run**                                    | **run the program with current arguments**          |
| (gdb) run args redirection                       | run with args and redirection                       |
| **(gdb) cont**                                   | **continue the program**                            |
| **(gdb) step**                                   | **single step the program; step into functions**    |
| (gdb) step count                                 | **single step `count` times**                       |
| **(gdb) next**                                   | **step but step over functions**                    |
| (gdb) next count                                 | **next `count` times**                              |
| **(gdb) finish**                                 | **finish current function's execution**             |
| **(gdb) kill**                                   | **kill current executing program**                  |
| <h4>Stack backtrace</h4>                         |                                                     |
| **(gdb) bt**                                     | **print stack backtrace**                           |
| (gdb) frame                                      | show current execution position                     |
| (gdb) up                                         | move up stack trace (towards main)                  |
| (gdb) down                                       | move down stack trace (away from main)              |
| **(gdb) info locals**                            | **print automatic variables in frame**              |
| **(gdb) info args**                              | **print function parameters**                       |
| <h4>Browsing source</h4>                         |                                                     |
| (gdb) list 101                                   | list 10 lines around line 101                       |
| (gdb) list 1,10                                  | list lines 1 to 10                                  |
| (gdb) list main                                  | list lines around function                          |
| (gdb) list -                                     | list previous 10 lines                              |
| (gdb) search regexpr                             | forward current for regular expression              |
| (gdb) reverse-search regexpr                     | backward search for regular expression              |
| <h4>Browsing Data</h4>                           |                                                     |
| **(gdb) print expression**                       | **print expression, added to value history**        |
| (gdb) info functions regexp                      | print function names                                |
| (gdb) info variables regexp                      | print global variable names                         |
| **(gdb) ptype name**                             | **print type definition**                           |
| (gdb) ptype class                                | print class members                                 |
| (gdb) whatis expression                          | print type of expression                            |
| (gdb) display expression                         | display expression result at stop                   |
| (gdb) undisplay                                  | delete displays                                     |
| (gdb) info display                               | show displays                                       |
| <h4>Miscellaneous</h4>                           |                                                     |
| (gdb) RETURN                                     | repeat last command                                 |
| (gdb) shell command args                         | execute shell command                               |
| (gdb) quit                                       | quit gdb                                            |
| gdb -x file                                      | execute gdb commands from `file`                    |
| gdb -tui                                         | use gdb's text user interface                       |
| (ctrl-x) (a)                                     | enter/leave TUI mode                                |
| (gdb) set substitute-path from to                | look for source in directory `to` instead of `from` |

Original from [rkubik](https://gist.github.com/rkubik): https://gist.github.com/rkubik/b96c23bd8ed58333de37f2b8cd052c30
