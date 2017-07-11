Replication:

```
git clone git@github.com:markhibberd/mafia-resolve-error-replication
cd mafia-resolve-error-replication
rm example.lock-8.0.2
./mafia lock
echo $?  # appears to work, although lockfile looks light on
./mafia build  # bombs or just running ./mafia lock again for that matter
```


Error:

```
Installing dependencies...
Resolving dependencies...
cabal: Could not resolve dependencies:
next goal: entropy (dependency of scrypt-0.5.0)
rejecting: entropy-0.3.8 (constraint from command line flag requires ==0.3.7)
trying: entropy-0.3.7
trying: entropy-setup.base~>base-4.9.1.0/installed-4.9... (dependency of
entropy-0.3.7)
trying: entropy-setup.process~>process-1.6.0.0 (dependency of entropy-0.3.7)
trying: entropy-setup.time~>time-1.6.0.1/installed-1.6... (dependency of
entropy-setup.unix-2.7.2.1/installed-2.7...)
trying: entropy-setup.directory~>directory-1.3.0.0/installed-1.3...
(dependency of entropy-0.3.7)
next goal: entropy-setup.Cabal (dependency of entropy-0.3.7)
rejecting: entropy-setup.Cabal-1.24.2.0/installed-1.2... (conflict:
entropy-setup.process==1.6.0.0, entropy-setup.Cabal =>
entropy-setup.process==1.4.3.0/installed-1.4...)
rejecting: entropy-setup.Cabal-1.24.2.0 (conflict:
entropy-setup.process==1.6.0.0, entropy-setup.Cabal =>
entropy-setup.process>=1.1.0.1 && <1.5)
rejecting: entropy-setup.Cabal-1.24.0.0 (conflict:
entropy-setup.directory==1.3.0.0/installed-1.3..., entropy-setup.Cabal =>
entropy-setup.directory>=1.1 && <1.3)
rejecting: entropy-setup.Cabal-1.22.8.0, entropy-setup.Cabal-1.22.7.0,
entropy-setup.Cabal-1.22.6.0, entropy-setup.Cabal-1.22.5.0,
entropy-setup.Cabal-1.22.4.0, entropy-setup.Cabal-1.22.3.0,
entropy-setup.Cabal-1.22.2.0 (conflict:
entropy-setup.directory==1.3.0.0/installed-1.3..., entropy-setup.Cabal =>
entropy-setup.directory>=1 && <1.3)
rejecting: entropy-setup.Cabal-1.22.1.1, entropy-setup.Cabal-1.22.1.0,
entropy-setup.Cabal-1.22.0.0 (conflict: entropy-setup.directory =>
entropy-setup.filepath==1.4.1.1/installed-1.4..., entropy-setup.Cabal =>
entropy-setup.filepath>=1 && <1.4)
rejecting: entropy-setup.Cabal-1.20.0.4, entropy-setup.Cabal-1.20.0.3,
entropy-setup.Cabal-1.20.0.2, entropy-setup.Cabal-1.20.0.1,
entropy-setup.Cabal-1.20.0.0 (conflict: entropy-setup.time =>
entropy-setup.deepseq==1.4.2.0/installed-1.4..., entropy-setup.Cabal =>
entropy-setup.deepseq>=1.3 && <1.4)
rejecting: entropy-setup.Cabal-1.18.1.7, entropy-setup.Cabal-1.18.1.6
(conflict: entropy-setup.directory =>
entropy-setup.filepath==1.4.1.1/installed-1.4..., entropy-setup.Cabal =>
entropy-setup.filepath>=1 && <1.4)
rejecting: entropy-setup.Cabal-1.18.1.5, entropy-setup.Cabal-1.18.1.4,
entropy-setup.Cabal-1.18.1.3, entropy-setup.Cabal-1.18.1.2,
entropy-setup.Cabal-1.18.1.1, entropy-setup.Cabal-1.18.1,
entropy-setup.Cabal-1.18.0 (conflict: entropy-setup.time =>
entropy-setup.deepseq==1.4.2.0/installed-1.4..., entropy-setup.Cabal =>
entropy-setup.deepseq>=1.3 && <1.4)
rejecting: entropy-setup.Cabal-1.16.0.3, entropy-setup.Cabal-1.16.0.2,
entropy-setup.Cabal-1.16.0.1, entropy-setup.Cabal-1.16.0,
entropy-setup.Cabal-1.14.0 (conflict: entropy-setup.directory =>
entropy-setup.filepath==1.4.1.1/installed-1.4..., entropy-setup.Cabal =>
entropy-setup.filepath>=1 && <1.4)
rejecting: entropy-setup.Cabal-1.12.0, entropy-setup.Cabal-1.10.2.0,
entropy-setup.Cabal-1.10.1.0, entropy-setup.Cabal-1.10.0.0 (conflict:
entropy-setup.directory => entropy-setup.filepath==1.4.1.1/installed-1.4...,
entropy-setup.Cabal => entropy-setup.filepath>=1 && <1.3)
rejecting: entropy-setup.Cabal-1.8.0.6, entropy-setup.Cabal-1.8.0.4,
entropy-setup.Cabal-1.8.0.2, entropy-setup.Cabal-1.6.0.3,
entropy-setup.Cabal-1.6.0.2, entropy-setup.Cabal-1.6.0.1,
entropy-setup.Cabal-1.4.0.2, entropy-setup.Cabal-1.4.0.1,
entropy-setup.Cabal-1.4.0.0, entropy-setup.Cabal-1.2.4.0,
entropy-setup.Cabal-1.2.3.0, entropy-setup.Cabal-1.2.2.0,
entropy-setup.Cabal-1.2.1, entropy-setup.Cabal-1.1.6 (conflict: entropy =>
entropy-setup.Cabal>=1.10 && <2.2)
rejecting: entropy-setup.Cabal-1.24.1.0 (conflict:
entropy-setup.base==4.9.1.0/installed-4.9..., entropy-setup.Cabal =>
entropy-setup.base<0)
Dependency tree exhaustively searched.

Note: when using a sandbox, all packages are required to have consistent
dependencies. Try reinstalling/unregistering the offending packages or
recreating the sandbox.
Process failed: cabal install --reorder-goals --max-backjumps=-1 --avoid-reinstalls --dry-run --enable-tests --enable-benchmarks --enable-profiling --constraint ansi-terminal == 0.6.3.1 --constraint async == 2.1.1.1 --constraint base16-bytestring == 0.1.1.6 --constraint base64-bytestring == 1.0.0.1 --constraint concurrent-output == 1.10.0 --constraint cryptonite == 0.23 --constraint entropy == 0.3.7 --constraint exceptions == 0.8.3 --constraint foundation == 0.0.10 --constraint haskell-lexer == 1.0.1 --constraint hedgehog == 0.2.2 --constraint lifted-base == 0.2.3.11 --constraint memory == 0.14.6 --constraint mmorph == 1.0.9 --constraint monad-control == 1.0.1.0 --constraint mtl == 2.2.1 --constraint pretty-show == 1.6.13 --constraint primitive == 0.6.2.0 --constraint process == 1.6.0.0 --constraint random == 1.1 --constraint resourcet == 1.1.9 --constraint scrypt == 0.5.0 --constraint stm == 2.4.4.1 --constraint terminal-size == 0.3.2.1 --constraint text == 1.2.2.2 --constraint th-lift == 0.7.7 --constraint transformers-base == 0.4.4 --constraint transformers-compat == 0.5.1.4 --constraint wl-pprint-annotated == 0.1.0.0 (exit code: 1)
```
