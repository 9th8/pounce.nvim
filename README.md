## Usage

The `:Pounce` command starts the motion. Type the character at the destination
and Pounce will highlight all matches on screen. Next, refine the matches by
typing more characters (in order) that are present after the destination. The
first letter of the match will be replaced with an uppercase "accept key". You
can hit that key to jump to the match, or continue refining the search. Enter
accepts the best match (highlighted in blue). Escape cancels the motion and
leaves the cursor at its previous position.

The `:PounceRepeat` command works the same way but is initialized with the
input from the previous Pounce command.

Configuration is done with the `setup` function. It's optional to call `setup`.
Here are the defaults:

```lua
require'pounce'.setup{
  accept_keys = "JFKDLSAHGNUVRBYTMICEOXWPQZ",
  accept_best_key = "<enter>",
  multi_window = true,
  debug = false,
}
```
Note that `accept_keys` allows you to configure the order in which accept keys display – closest proximity match gets the first letter in the `accept_keys` string. Users of alternative keyboard layouts may wish to amend that string. Colemak DHm might start with `NTESIROA...` for example.
