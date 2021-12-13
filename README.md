# Example 

The following command fails:

```sh
docker build -t haskellnixdockerrepro -f nix/Dockerfile .
```

with

```
#9 1223.0 Builder called die: Cannot wrap '/nix/store/lbbi4f8nvsr66m11035mf02whj5bkm63-nix-tools/bin/stack-to-nix' because it is not an executable file
#9 1223.0 Backtrace:
#9 1223.0 7 assertExecutable /nix/store/7cf7m6l4s9y22zasqclqc1vda8z3z57w-hook/nix-support/setup-hook
#9 1223.0 136 wrapProgram /nix/store/7cf7m6l4s9y22zasqclqc1vda8z3z57w-hook/nix-support/setup-hook
#9 1223.0 6 source /tmp/nix-build-nix-tools.drv-0/.attr-0
#9 1223.0 1306 genericBuild /nix/store/c6h9qrn88g5vv5zdvn2813al9j0r7dpa-stdenv-linux/setup
#9 1223.0 2 main /nix/store/9krlzvny65gdc8s7kpb6lkx8cd02c25b-default-builder.sh
#9 1223.0 
#9 1223.1 builder for '/nix/store/6j4kvjpm4wc75kn7jp0p1sdpkgwcxyk0-nix-tools.drv' failed with exit code 1
#9 1223.1 cannot build derivation '/nix/store/58p2i48rkwzgmbcwjw9y2wmhhwdmn04b-haskell-project-plan-to-nix-pkgs.drv': 1 dependencies couldn't be built
#9 1223.5 error: build of '/nix/store/58p2i48rkwzgmbcwjw9y2wmhhwdmn04b-haskell-project-plan-to-nix-pkgs.drv' failed
#9 1223.5 (use '--show-trace' to show detailed location information)
```