# Ansi color codes

2025-05-07 19:24:59

All color codes start like this:
```bash
\033[XXXm
```

Clear styles:
```bash
\033[0m
```

Example:
```bash
\033[31;1;4m
```

| 0 |    Reset / Normal | all attributes off |
| 1 |    Bold or increased intensity  | _ |
| 2 |    Faint (decreased intensity) | Not widely supported. |
| 3 |    Italic  | Not widely supported. Sometimes treated as inverse. |
| 4 |    Underline    | _ |
| 5 |    Slow Blink  | less than 150 per minute |
| 6 |    Rapid Blink | MS-DOS ANSI.SYS; 150+ per minute; not widely supported |
| 7 |    reverse video | swap foreground and background colors |
| 8 |    Conceal | Not widely supported. |
| 9 |    Crossed-out | Characters legible, but marked for deletion. Not widely supported. |
| 10 |   Primary(default) font    | _ |
| 11–19 |   Alternate font |  Select alternate font n-10 |
| 20 |   Fraktur | hardly ever supported | 
| 21 |   Bold off or Double Underline |    Bold off not widely supported; double underline hardly ever supported. |
| 22 |   Normal color or intensity  | Neither bold nor faint | 
| 23 |   Not italic, not Fraktur  | _ |
| 24 |   Underline off  | Not singly or doubly underlined |
| 25 |   Blink off    | _ |
| 27 |   Inverse off  | _ |
| 28 |   Reveal |  conceal off |
| 29 |   Not crossed out  | _ |
| 30–37 |   Set foreground color |    See color table below | 
| 38 |   Set foreground color  |   Next arguments are 5;<n> or 2;<r>;<g>;<b>, see below |
| 39 |   Default foreground color  |  implementation defined (according to standard) |
| 40–47 |   Set background color  |  See color table below | 
| 48 |   Set background color  |  Next arguments are 5;<n> or 2;<r>;<g>;<b>, see below |
| 49 |   Default background color |    implementation defined (according to standard) | 
| 51 |   Framed   | _ |
| 52 |   Encircled    | _ |
| 53 |   Overlined    | _ |
| 54 |   Not framed or encircled  | _ |
| 55 |   Not overlined    | _ |
| 60 |   ideogram underline | hardly ever supported |
| 61 |   ideogram double underline |   hardly ever supported |
| 62 |   ideogram overline  | hardly ever supported | 
| 63 |   ideogram double overline |   hardly ever supported | 
| 64 |   ideogram stress marking | hardly ever supported | 
| 65 |   ideogram attributes off | reset the effects of all of 60-64 | 
| 90 | –97   Set bright foreground color | aixterm (not in standard) |
| 100 | –107 Set bright background color | aixterm (not in standard) |
