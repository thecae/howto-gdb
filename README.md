# Mastering GDB

`gdb` is the most commonly used debugger. The base installation is super user-friendly and offers a rich feature set. It is also very easy to extend with plugins.

Nearly every challenge dissected in this guide used `gdb`, with a few exceptions.

{% hint style="info" %}
`gdb` has a _LOT_ of features. This guide covers the ones that are most commonly used in everyday settings. If you want to read more, check out [this summary guide](https://gist.github.com/integeruser/0c436a64e087b1c43b278761434cbbfa).
{% endhint %}

## Installation

Installation of `gdb` is extremely simple:

```nasm
pip install gdb
```

To extend its feature set, we will also install the `gdb-gef` extension. More information can be found [here](https://github.com/hugsy/gef). GEF allows live previews of the instruction set, the registers, and the stack. This allows us to easily do a dynamic analysis of the binary.

To install GEF, use the following command:

```nasm
$ bash -c "$(wget https://gef.blah.cat/sh -O -)"
```

{% hint style="info" %}
Other plugins out there are equally effective. Notable plugins are [`pwndbg`](https://github.com/pwndbg/pwndbg) and [`peda`](https://github.com/longld/peda).

They all offer very similar feature sets. I personally like GEF the best, but feel free to use whichever one you like. Read [this](https://infosecwriteups.com/pwndbg-gef-peda-one-for-all-and-all-for-one-714d71bf36b8) article if you want to install more than one and build a local version manager.
{% endhint %}

## Usage

We run `gdb` on the binary that we want to analyze. The plugin will automatically run when we run the binary.

```nasm
gdb <binary>
```
