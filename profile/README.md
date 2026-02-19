<div align="center">

<img src="../el-init-branding.png" alt="EL-INIT" width="600">

# Emacs Operating System

[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-purple.svg)](LICENSE)

</div>

---

Emacs-OS is the home of **el-init**. Emacs-OS is a Linux distribution where Emacs is PID 1.

The base system consists of Grub, a static Linux kernel, static GNU coreutils, and static Emacs with the `--pid1` patchset running **el-init** - the process supervisor and init system at its core.

The rootfs is to be git-tracked, similar in approach to [stali](http://sta.li), but with different goals. Emacs-OS is to be an unashamedly full-send glibc-bloated Emacs OS. The goal is not small binaries - it is a system where Emacs runs everything, from boot to shutdown.

## Base

- Grub
- Static Linux kernel (initramfs may become default for user friendliness)
- Static GNU coreutils
- Static Emacs with `--pid1` patchset
- el-init (process supervisor / init system)

el-init may also be run with a non-patched Emacs for supervision only, as a drop-in replacement for a service supervisor such as perp on a distro like Oasis or similar (leaving zombie reaping to a shim pid1 such as sinit).

## Userland

- glibc toolchain
- Bash (many scripts may be rewritten in Gauche Scheme)
- Package manager (Scheme/Lisp)

<div align="center">
<br>
<img src="../EOS.png" alt="EOS" width="200">
<br>
<sub>Reap what you code.</sub>
</div>
