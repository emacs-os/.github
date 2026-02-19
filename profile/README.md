<div align="center">

<img src="../el-init-branding-2.png" alt="EL-INIT" width="450">

# Emacs Operating System

[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-purple.svg)](LICENSE)

</div>

---

Emacs-OS is the home of **[el-init](https://github.com/emacs-os/el-init)** (coming soon), spiritual successor to [systemE](https://github.com/emacs-os/systemE) (archived). A proper full-send — Emacs-OS aims to be a Linux distribution where Emacs runs as PID 1.

The base system consists of Grub, a Linux kernel built for a no-initrd boot path, static GNU coreutils, and static Emacs with the `--pid1` patchset running **el-init** - the process supervisor and init system at its core.

The rootfs is intended to be git-tracked by policy (base-owned paths; runtime state excluded). Emacs-OS is technically a fork of [KISS Linux](https://kisscommunity.org/), similar in approach to [stali](http://sta.li) and [Oasis](https://github.com/oasislinux/oasis), but with different goals. An unashamedly glibc-bloated system. The goal is not small binaries - it is a system where Emacs runs everything, from boot to shutdown.

## Base

- Grub
- Linux kernel (initramfs may become default for user friendliness)
- Static GNU coreutils
- Static Emacs with `--pid1` patchset
- el-init (process supervisor / init system)
- GNU toolchain (gcc, glibc, binutils)
- Bash (many scripts may be rewritten in Gauche Scheme)
- Package manager (rewrite of KISS package manager in Gauche Scheme) for managing the static base
- [Guix](https://guix.gnu.org/) as a secondary package manager for additional userland software not packaged by Emacs-OS, and as a dev tool. Guix Home provides declarative, reproducible user environment management with rollback support

In general, Emacs-OS trusts the decisions made by the KISS Linux community and aims to develop tooling to automate the repetitive parts of their package build files, only forking where necessary to shift for Emacs-OS goals.

el-init may also be run standalone as a pid2+ userland supervisor with a non-patched Emacs - for example, managing an EXWM/Xorg session startup, or local dev project daemons. The "init" in el-init is optional - it makes a fine supervisor. It can also serve as a drop-in replacement for a service supervisor such as perp on a distro like Oasis or similar (leaving zombie reaping to a shim pid1 such as sinit).

<div align="center">
<br>
<img src="../EOS.png" alt="EOS" width="200">
<br>
<sub>Reap what you code.</sub>
</div>
