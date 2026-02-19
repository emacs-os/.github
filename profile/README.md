<div align="center">

<img src="../el-init-branding.png" alt="EL-INIT" width="600">

# Emacs Operating System

[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-purple.svg)](LICENSE)

</div>

---

EOS is a Linux distribution where Emacs is PID 1. The entire rootfs is git-tracked.

The base system consists of Grub, a static Linux kernel, static GNU coreutils, and static Emacs with the `--pid1` patchset running **el-init** — the process supervisor and init system at its core.

The rootfs is git-tracked, similar in approach to [stali](http://sta.li), but with different goals. EOS is an unashamedly full-send glibc-bloated Emacs OS. The goal is not small binaries — it is a system where Emacs runs everything, from boot to shutdown.

## Base

- Grub
- Static Linux kernel
- Static GNU coreutils
- Static Emacs with `--pid1` patchset
- el-init (process supervisor / init system)

## Userland

- glibc toolchain
- Package manager (Scheme/Lisp)

<div align="center">
<br>
<img src="../EOS.png" alt="EOS" width="200">
<br>
<sub>Reap what you code.</sub>
</div>
