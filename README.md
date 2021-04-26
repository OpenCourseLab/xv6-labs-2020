# xv6-labs-2020
Labs of 2020 MIT 6.S081

## Set up & Preparation

This set up guide for macOS is from [mit 6.S081 Tools](https://pdos.csail.mit.edu/6.828/2020/tools.html), but the setup may be different on different macOS  because of different locations which installed packages or tools in. So it's my tools setup guides. And may it help beginners

First, install developer tools:

```shell
xcode-select --install
```

Next, install Homebrew, a package manager for macOS:

```shell
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

Next, install the RISC-V compiler toolchain: (notice this may not work with your homebrew or os, but it's easy to find the way works)

```shell
brew tap riscv/riscv
brew install riscv-tools
```

The brew formula may not link into `/usr/local`. You will need to update your shell's rc file (e.g. [~/.bashrc](https://www.gnu.org/software/bash/manual/html_node/Bash-Startup-Files.html)) to add the appropriate directory to [$PATH](http://www.linfo.org/path_env_var.html). And then you should run source ~/.bashrc

```
PATH=$PATH:/usr/local/opt/riscv-gnu-toolchain/bin
```

Finally, install QEMU:

```shell
brew install qemu
```

On my mac mojave 10.14.6, these qemu tools and vms are in the /user/local/Cellar/qemu/5.2.0_1/bin, don't forget to add the directory to [$PATH](http://www.linfo.org/path_env_var.html) and run the source command. Otherwise you may not boot your xv6 using qemu.

## Progress

Each lab's exercise codes are in the branch which shares the same name. 

- [ ] util: Unix utilities
- [ ] syscall: System calls
- [ ] pgtbl: Page tables
- [ ] traps: Traps
- [ ] lazy: lazy allocation
- [ ] cow: Copy-on-write
- [ ] thread: Multithreading
- [ ] lock: Lock
- [ ] fs: File System
- [ ] mmap: mmap
- [ ] net: Network driver

