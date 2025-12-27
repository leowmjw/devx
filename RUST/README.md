# Modern UNIX w/ Rust

## Objective

Simple way to experiment with newer UNIX tools written in Rust; easy way + clean way to judge tools without too messy; by leveraging modern tooling like mise (which is even more of a superset of direnv, Make, go-task, just ..)

Use mise to demonstrate and try out common patterns per categories.
If available in mise registry; highest preference as it is universally available across MacOS + Linux / Ubuntu ..

Keep mise update once in a while to get new registry ...
```shell
$ mise update 
```

We have all core languages like below available; common CLI agents, universal dev tools (like ripgrep,  overmind, watchexec) and also a few other common tooling like: bun (Typescript), uv (Python)

```shell
$ mise ls

Tool                        Version                 Source                      Requested
amp                         0.0.1766634431-g578c41  ~/.config/mise/config.toml  latest
aqua:BurntSushi/ripgrep     15.1.0                  ~/.config/mise/config.toml  latest
aqua:astral-sh/uv           0.9.18                  ~/.config/mise/config.toml  latest
codex                       0.77.0                  ~/.config/mise/config.toml  latest
crush                       0.29.1                  ~/.config/mise/config.toml  latest
github:MoonshotAI/kimi-cli  0.68                    ~/.config/mise/config.toml  latest
github:block/goose          1.18.0                  ~/.config/mise/config.toml  latest
go                          1.23.12
go                          1.25.5                  ~/.config/mise/config.toml  latest
node                        24.12.0                 ~/.config/mise/config.toml  lts
opencode                    1.0.200                 ~/.config/mise/config.toml  latest
overmind                    2.5.1                   ~/.config/mise/config.toml  latest
python                      3.14.2                  ~/.config/mise/config.toml  latest
rust                        1.92.0 (symlink)        ~/.config/mise/config.toml  latest
watchexec                   2.3.2                   ~/.config/mise/config.toml  latest

```

To activate; just run below in your zsh session ..

```shell
$ eval "$(mise activate zsh)"

# If wanted to add local .. it creates a mise.toml file in the dir
$ mise use bat <-- cat replacement using Rust ..
```

Notice that the local mise files will overlap ... mise.toml and mise.local.toml will overwrite ) if needed ..
 
To expand more, read through below for suggested path ...

Available core languages covers my common used: Go, Rust, Python, typescript ..

```shell
$ mise registry | grep -i core:
bun                           core:bun
deno                          core:deno
elixir                        core:elixir
erlang                        core:erlang
go                            core:go
java                          core:java
node                          core:node
python                        core:python
ruby                          core:ruby
rust                          core:rust asdf:code-lever/asdf-rust
swift                         core:swift
zig                           core:zig

# Example if wanted to add deno for Global ..
$ mise use -g deno
```

; it has modern signed binaries ..

```shell
$ mise registry | grep -i aqua:
...
act                           aqua:nektos/act ubi:nektos/act asdf:gr1m0h/asdf-act
age                           aqua:FiloSottile/age asdf:threkk/asdf-age
aichat                        aqua:sigoden/aichat
air                           aqua:air-verse/air asdf:pdemagny/asdf-air
apko                          aqua:chainguard-dev/apko ubi:chainguard-dev/apko asdf:omissis/asdf-apko
atlas                         aqua:ariga/atlas asdf:komi1230/asdf-atlas
aws-sso                       aqua:synfinatic/aws-sso-cli asdf:adamcrews/asdf-aws-sso-cli
bat                           aqua:sharkdp/bat ubi:sharkdp/bat cargo:bat asdf:https://gitlab.com/wt0f/asdf-bat
bats                          aqua:bats-core/bats-core asdf:timgluz/asdf-bats
benthos                       aqua:redpanda-data/connect asdf:benthosdev/benthos-asdf
bitwarden                     aqua:bitwarden/clients asdf:vixus0/asdf-bitwarden
bottom                        aqua:ClementTsang/bottom asdf:carbonteq/asdf-btm cargo:bottom
btop                          aqua:aristocratos/btop ubi:aristocratos/btop
buf                           aqua:bufbuild/buf ubi:bufbuild/buf asdf:truepay/asdf-buf
caddy                         aqua:caddyserver/caddy asdf:salasrod/asdf-caddy
cfssl                         aqua:cloudflare/cfssl/cfssl asdf:mathew-fleisch/asdf-cfssl
changie                       aqua:miniscruff/changie ubi:miniscruff/changie asdf:pdemagny/asdf-changie
checkov                       aqua:bridgecrewio/checkov ubi:bridgecrewio/checkov asdf:bosmak/asdf-checkov
chisel                        aqua:jpillora/chisel ubi:jpillora/chisel go:github.com/jpillora/chisel asdf:lwiechec/asdf-chisel
choose                        aqua:theryangeary/choose ubi:theryangeary/choose cargo:choose asdf:carbonteq/asdf-choose
cloudflared                   aqua:cloudflare/cloudflared asdf:threkk/asdf-cloudflared
cocogitto                     aqua:cocogitto/cocogitto
colima                        aqua:abiosoft/colima ubi:abiosoft/colima asdf:CrouchingMuppet/asdf-colima
committed                     aqua:crate-ci/committed
conform                       aqua:siderolabs/conform asdf:skyzyx/asdf-conform
conftest                      aqua:open-policy-agent/conftest asdf:looztra/asdf-conftest
container-use                 aqua:dagger/container-use ubi:dagger/container-use
copper                        aqua:cloud66-oss/copper ubi:cloud66-oss/copper asdf:vladlosev/asdf-copper
cosign                        aqua:sigstore/cosign asdf:https://gitlab.com/wt0f/asdf-cosign
croc                          aqua:schollz/croc ubi:schollz/croc
ctop                          aqua:bcicen/ctop ubi:bcicen/ctop asdf:NeoHsu/asdf-ctop
curlie                        aqua:rs/curlie
cyclonedx                     aqua:CycloneDX/cyclonedx-cli asdf:xeedio/asdf-cyclonedx
dagger                        aqua:dagger/dagger asdf:virtualstaticvoid/asdf-dagger
dagu                          aqua:dagu-org/dagu ubi:dagu-org/dagu
dasel                         aqua:TomWright/dasel asdf:asdf-community/asdf-dasel
dbmate                        aqua:amacneil/dbmate asdf:juusujanar/asdf-dbmate
delta                         aqua:dandavison/delta ubi:dandavison/delta asdf:andweeb/asdf-delta cargo:git-delta
devspace                      aqua:devspace-sh/devspace asdf:NeoHsu/asdf-devspace
diffoci                       aqua:reproducible-containers/diffoci
difftastic                    aqua:Wilfred/difftastic ubi:Wilfred/difftastic[exe=difft] asdf:volf52/asdf-difftastic cargo:difftastic
dive                          aqua:wagoodman/dive ubi:wagoodman/dive asdf:looztra/asdf-dive
dockle                        aqua:goodwithtech/dockle asdf:mathew-fleisch/asdf-dockle
doggo                         aqua:mr-karan/doggo ubi:mr-karan/doggo
dotenvx                       aqua:dotenvx/dotenvx ubi:dotenvx/dotenvx
dt                            aqua:so-dang-cool/dt asdf:so-dang-cool/asdf-dt
dua                           aqua:Byron/dua-cli ubi:Byron/dua-cli[exe=dua] cargo:dua-cli
duckdb                        aqua:duckdb/duckdb ubi:duckdb/duckdb
duf                           aqua:muesli/duf asdf:NeoHsu/asdf-duf
dust                          aqua:bootandy/dust ubi:bootandy/dust asdf:looztra/asdf-dust cargo:du-dust
dyff                          aqua:homeport/dyff asdf:https://gitlab.com/wt0f/asdf-dyff
earthly                       aqua:earthly/earthly asdf:YR-ZR0/asdf-earthly
ejson                         aqua:Shopify/ejson asdf:cipherstash/asdf-ejson
envsubst                      aqua:a8m/envsubst asdf:dex4er/asdf-envsubst
fd                            aqua:sharkdp/fd ubi:sharkdp/fd asdf:https://gitlab.com/wt0f/asdf-fd cargo:fd-find
fission                       aqua:fission/fission asdf:virtualstaticvoid/asdf-fission
fx                            aqua:antonmedv/fx asdf:https://gitlab.com/wt0f/asdf-fx
fzf                           aqua:junegunn/fzf ubi:junegunn/fzf asdf:kompiro/asdf-fzf
gdu                           aqua:dundee/gdu
ggshield                      aqua:GitGuardian/ggshield ubi:GitGuardian/ggshield pipx:ggshield
ghalint                       aqua:suzuki-shunsuke/ghalint ubi:suzuki-shunsuke/ghalint
git-chglog                    aqua:git-chglog/git-chglog asdf:GoodwayGroup/asdf-git-chglog
git-cliff                     aqua:orhun/git-cliff asdf:jylenhof/asdf-git-cliff
gitsign                       aqua:sigstore/gitsign asdf:spencergilbert/asdf-gitsign
gitversion                    aqua:gittools/gitversion ubi:gittools/gitversion
gleam                         aqua:gleam-lang/gleam asdf:asdf-community/asdf-gleam
go-jira                       aqua:go-jira/jira asdf:dguihal/asdf-go-jira
go-jsonnet                    aqua:google/go-jsonnet asdf:https://gitlab.com/craigfurman/asdf-go-jsonnet
go-swagger                    aqua:go-swagger/go-swagger asdf:jfreeland/asdf-go-swagger
gocryptfs                     aqua:rfjakob/gocryptfs ubi:rfjakob/gocryptfs
..
```

If all fails; look for direct from repo; or if the release

```shell
$ mise registry | grep -i github:
...
btrace                        github:btraceio/btrace asdf:mise-plugins/mise-btrace
buck2                         github:facebook/buck2[bin=buck2]
certstrap                     github:square/certstrap asdf:carnei-ro/asdf-certstrap
doppler                       github:DopplerHQ/cli[exe=doppler] asdf:takutakahashi/asdf-doppler
flatc                         github:google/flatbuffers[exe=flatc] asdf:TheOpenDictionary/asdf-flatc
infisical                     github:Infisical/cli
jwtui                         github:jwt-rs/jwt-ui[exe=jwtui] cargo:jwt-ui
localstack                    github:localstack/localstack-cli[exe=localstack]
mongosh                       github:mongodb-js/mongosh asdf:itspngu/asdf-mongosh
nsc                           github:nats-io/nsc asdf:dex4er/asdf-nsc
openbao                       github:openbao/openbao[exe=bao]
tonnage                       github:elementalvoid/tonnage asdf:elementalvoid/asdf-tonnage
traefik                       github:traefik/traefik asdf:Dabolus/asdf-traefik
trufflehog                    aqua:trufflesecurity/trufflehog github:trufflesecurity/trufflehog
tusd                          github:tus/tusd
unison                        github:unisonweb/unison asdf:susurri/asdf-unison
vespa-cli                     github:vespa-engine/vespa
yt-dlp                        github:yt-dlp/yt-dlp[rename_exe=yt-dlp] asdf:duhow/asdf-yt-dlp
zigmod                        github:nektro/zigmod asdf:mise-plugins/asdf-zigmod
...

```

Even if the LLM Agent Pi or worktree 

```shell
$ mise use -g github:badlogic/pi-mono
$ mise use -g github:camoneart/maestro
```

Example of problematic might be VictoriaLogs if they mix multiple tools in Release.  
I think APISIX also same weirdnes ..

## Categories

### DNS

- a
- b

### Disk Usage

- a
- b

### Finding files, directories ..

- fzf
- fd

### Pattern matching 

- ripgrep
- awk?
- sd <-- sed replacement ..
- runiq

### Process Management

- bottom
- procs

### Bash Testing

- bats-core
- 