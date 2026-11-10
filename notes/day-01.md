# Day 1 — Linux lab setup
# Day 1 — Tue Nov 10, 2026
**Week 1: Linux I — working in the shell**

## What I did
- Created my `platform-journey` GitHub repo with a `notes/` folder
- Set up my Linux lab: an Ubuntu container in Docker Desktop named `linux-lab`
- Created it with: `docker run -it --name linux-lab ubuntu bash`
- Learned I reopen it with: `docker start -ai linux-lab`

## First commands and what they showed
| Command | Output | Meaning |
|---|---|---|
| `pwd` | `/` | I'm at the top of the filesystem |
| `whoami` | `root` | I'm the superuser (admin) |
| `ls -la` | bin, etc, home, usr, var... | The standard Linux folder layout, including hidden files |
| `uname -a` | Linux 1e637795d670 6.12.76-linuxkit aarch64 | My container's ID, its kernel, and ARM (Apple Silicon) |
| `echo hello platform` | hello platform | Prints text back to the screen |

## What broke
- Running `docker run` a second time failed: "container name /linux-lab is already in use"
- Why: `docker run` creates a NEW container — the name was already taken by my existing one
- Fix: don't recreate it, just reopen it with `docker start -ai linux-lab`

## What I still don't get
- Why the container uses a "linuxkit" kernel instead of Ubuntu's own kernel
- What most of those root folders (bin, etc, usr, var) are actually for

## Done when ✅
- [x] Repo exists
- [x] Lab shell opens
- [x] Day 1 note committed
