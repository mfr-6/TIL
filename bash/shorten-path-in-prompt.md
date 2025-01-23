## Shortening Path Displayed in Bash Prompt

Usually if you work in nested structure of directories, you might end up with a very long prompt that limits your visibility.

`@mfr-6 ➜ /workspaces/TIL/test/test1/test2/test3/test4 (main) $`

To avoid that, you can set `PROMPT_DIRTRIM` to shrink amount of directories being display.

```bash
@mfr-6 ➜ /workspaces/TIL/test/test1 (main) $ PROMPT_DIRTRIM=1
@mfr-6 ➜ .../test1 (main) $ 
```

If `PROMPT_DIRTRIM` is set to `1` - it means ONE trailing directory will be displayed.

```bash
@mfr-6 ➜ .../test1 (main) $ PROMPT_DIRTRIM=1
@mfr-6 ➜ .../test1 (main) $ 
```

```bash
@mfr-6 ➜ .../test1 (main) $ PROMPT_DIRTRIM=2
@mfr-6 ➜ .../test/test1 (main) $
```

```bash
@mfr-6 ➜ .../test/test1 (main) $ PROMPT_DIRTRIM=3
@mfr-6 ➜ .../TIL/test/test1 (main) $ 
```

#### Reference
1. [GNU.org Bash Variables](https://www.gnu.org/software/bash/manual/html_node/Bash-Variables.html#index-PROMPT_005fDIRTRIM)