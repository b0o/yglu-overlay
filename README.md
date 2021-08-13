# yglu-overlay

A wrapper for [yglu](https://github.com/lbovet/yglu) that enables importing and
merging documents into the root node.

#### Dependencies

- [Yglu](https://github.com/lbovet/yglu)

#### Example usage

From [alacritty-conf](https://github.com/b0o/alacritty-conf):

```yaml
---
_merge_skip: !-
  - shell
_import: !()
  - !? $import('base.yml')
  - !? $import('themes/base16-greenscreen-256.yml')

window:
  padding:
    x: 20
    y: 20

font:
  size: 20.0

shell:
  program: /usr/bin/zsh
  args:
    - -i
    - -c
    - while true; do
      clear;
      echo "Press any key to start a Pomodoro";
      read -srk1;
      clear;
      pomodoro;
      clear;
      done
```

## License

[MIT](https://www.mit-license.org/)
