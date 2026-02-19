<div align="center">

<img src="../el-init-branding-2.png" alt="EL-INIT" width="450">

# Emacs Operating System

[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-purple.svg)](LICENSE)

</div>

---

Emacs-OS is the home of **[el-init](https://github.com/emacs-os/el-init)** (coming soon), spiritual successor to [systemE](https://github.com/emacs-os/systemE) (archived). A proper full-send Emacs-OS aims to be a Linux distribution where Emacs runs as PID 1.

## The base system shall consist of:

- Grub
- Static Linux kernel (initramfs may become default for user friendliness)
- Static Emacs with `--pid1` patchset
- el-init (process supervisor / init system)
- Static GNU coreutils
- Static Bash (many scripts may be rewritten in Gauche Scheme)
- GNU toolchain (gcc, glibc, binutils)
- Package manager written in Scheme (Gauche)
- Git (rootfs is git-tracked by policy; base-owned paths versioned, runtime state excluded)

el-init may also be run standalone as a pid2+ userland supervisor with a non-patched Emacs - for example, managing an EXWM/Xorg session startup, or local dev project daemons. The "init" in el-init is optional - it makes a fine supervisor. It can also serve as a drop-in replacement for a service supervisor such as perp on a distro like Oasis or similar (leaving zombie reaping to a shim pid1 such as sinit).

<div align="center">
<br>
<img src="../EOS.png" alt="EOS" width="200">
<br>
<sub>Reap what you code.</sub>
</div>
