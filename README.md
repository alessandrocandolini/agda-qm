# agda-qm

Exploration in Agda of some basic mathematical abstraction used in QM (and not just in QM!) 

## Install Agda

If using `nix`, there's a `shell.nix` file provided in the top folder for an ephemeral nix shell, just run
```bash
nix-shell
```
Be careful, it installs GHC. Agda is ~100k lines of Haskell code! A proof assistant is a lot of work :) 

This will also install the Agda standard library. To use the standard library, place a file `~/.agda/defaults` with the following content
```
standard-library
```

Alternatively, on macos it's possible to install agda via homebrew:
```bash
brew install agda
``` 

## Compile
Run
```bash
agda --compile qm.agda
```
will generate a `./Talk` executable that should print `green` as output. 


If it cannot find the standard library, try to provide it explicitly, eg, 
```bash
agda --include-path=/opt/homebrew/Cellar/agda/2.6.2.2_1/lib/agda/src --compile qm.agda
```

To run the generated executable, `./Qm` 
