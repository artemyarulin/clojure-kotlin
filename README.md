# clojure-kotlin

Example how to call Kotlin from Clojure

## Why

Idea is to use Kotlin as a main development language, but use Clojure as a connected REPL for playing with code.

## How

- Build kotlin. **IMPORTANT** If you are using Spring then because of a custom loader it wouldn't be possible to import classes from final JAR in Clojure
- In Clojure project add local JAR as a reference. **IMPORTANT** `org.jetbrains.kotlin/kotlin-stdlib` has to be added as a dependency as well, otherwise it woudn't be possible to instantiate Kotlin classes
- Call Kotlin from Clojure. For referencing Kotlin use `import [package].[class]` like:
``` bash
$ clj --eval "(import example.App) (.ping (example.App.))"
example.App
"pong"
```

## Alternative

https://github.com/seancorfield/boot-kotlinc - A Boot task that provides compilation of Kotlin source files.
