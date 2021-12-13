# Example 

The following command fails:

```sh
nix-build -A haskellnixdockerrepro.components.exes.haskellnixdockerrepro
```

with

```
Preprocessing executable 'haskellnixdockerrepro' for haskellnixdockerrepro-0.1.0.0..
Building executable 'haskellnixdockerrepro' for haskellnixdockerrepro-0.1.0.0..
[1 of 1] Compiling Main             ( app/Main.hs, dist/build/haskellnixdockerrepro/haskellnixdockerrepro-tmp/Main.o )

app/Main.hs:5:12: error:
    Not in scope: type constructor or class ‘Year’
  |
5 | someYear:: Year
  |            ^^^^

error: builder for '/nix/store/dh504qk02l3p5vfg0pkb7kjfdfjh8qic-haskellnixdockerrepro-exe-haskellnixdockerrepro-0.1.0.0.drv' failed with exit code 1;
       last 10 log lines:
       > Preprocessing executable 'haskellnixdockerrepro' for haskellnixdockerrepro-0.1.0.0..
       > Building executable 'haskellnixdockerrepro' for haskellnixdockerrepro-0.1.0.0..
       > [1 of 1] Compiling Main             ( app/Main.hs, dist/build/haskellnixdockerrepro/haskellnixdockerrepro-tmp/Main.o )
       >
       > app/Main.hs:5:12: error:
       >     Not in scope: type constructor or class ‘Year’
       >   |
       > 5 | someYear:: Year
       >   |            ^^^^
       > 
       For full logs, run 'nix log /nix/store/dh504qk02l3p5vfg0pkb7kjfdfjh8qic-haskellnixdockerrepro-exe-haskellnixdockerrepro-0.1.0.0.drv'.
```

