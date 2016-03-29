# flycheck-liquidhs.el

[LiquidHaskell](https://github.com/ucsd-progsys/liquidhaskell) Flycheck integegration.

## Usage

To enable, add this to your `init.el`

```
(require 'flycheck-liquidhs)
(add-hook 'haskell-mode-hook
          '(lambda () (flycheck-select-checker 'haskell-liquid)))

(add-hook 'literate-haskell-mode-hook
          '(lambda () (flycheck-select-checker 'haskell-liquid)))
```

## Use stack ghci

In the .el file, change

```
:command ("liquid" source-inplace)
```

to

```
:command ("stack ghci liquid" source-inplace)
```

Non-hacky stack integration coming soon.