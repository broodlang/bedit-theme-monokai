# bedit-theme-monokai

A **Monokai** colour theme for the [bedit](https://github.com/broodlang/bedit)
editor — a **plugin package** for [Brood](https://broodlang.org)'s hive registry.

It declares `:enhances {bedit ">= 0.1"}` and ships pure data: a `(bedit-plugin)`
function returning a `{:themes [{:name :palette}]}` contribution the host folds
into `M-x theme-select`. No dependency on the editor itself.

## Install

Inside bedit, open the package browser and install it live — no restart:

```
C-x P            ; the *Packages* browser
i                ; install the package under point
```

or `M-x package-install RET bedit-theme-monokai RET`. **Monokai** then appears in
`M-x theme-select`.

## The contribution contract

```brood
(defn bedit-plugin ()
  {:themes [{:name "Monokai" :palette { … 16 role → "#rrggbb" … }}]})
```

The palette maps bedit's 16 semantic role names to hex colours — the same shape
as the editor's bundled themes.

## Licence

AGPL-3.0-or-later, matching bedit and Brood.
