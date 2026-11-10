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
| `uname -a` | Linux 1e637795d670 6.12.76-linuxkit aarch64 | My container's ID, its kernel, and ARM (Apple Silicon) | here is shows the kernel is not Ubuntu's own, but a "linuxkit" kernel which is a lightweight Linux kernel for containers |
| `echo hello platform` | hello platform | Prints text back to the screen |

## What broke
- Running `docker run` a second time failed: "container name /linux-lab is already in use"
- Why: `docker run` creates a NEW container — the name was already taken by my existing one
- Fix: don't recreate it, just reopen it with `docker start -ai linux-lab`

## What I still don't get
- Why the container uses a "linuxkit" kernel instead of Ubuntu's own kernel
- What most of those root folders (bin, etc, usr, var) are actually for


## 1. Why linuxkit instead of Ubuntu's own kernel?
Your answer to Q1 is the reason: containers share a kernel, they don't bring one. Ubuntu in your container is only the tools and folders — not a kernel. And a Mac has no Linux kernel at all, so Docker Desktop quietly runs a tiny Linux VM whose kernel is called linuxkit, and all your containers share it. Your uname -a was showing you that hidden VM.

## 2. What are those root folders for? The simple map:

bin / usr — programs and apps (the commands you run live here)
etc — configuration files (settings for the system and apps)
var — things that vary: logs, caches, data that changes
home — users' personal folders (root's own home is /root)
tmp — throwaway files

## Done when ✅
- [x] Repo exists
- [x] Lab shell opens
- [x] Day 1 note committed
