# Bitcoin dot

This is a fairly simple project that aims to provide a basic set up in order to get you up to speed with building, reviewing and even contributing to [bitcoin](https://github.com/bitcoin/bitcoin) in a simple but efficient way.

It is comprised by a just a limited set of text files that can be used either independently or together. 

## Summary

To the rescue of a developer that wants to onboard bitcoin, there is an abundance of resources included into the Bitcoin Core documentation as well as other sources mostly offered by long term contributors, see [references](#references) below. However, the whole process may seem intimidating to a newcomer! 

With that in mind, and to streamline commands and processes that are essential to set up, run and debug bitcoin, I offer the included dot file named [bitcoin](https://github.com/itornaza/btc-dot/blob/main/bitcoin). I have been updating it in constant time ever since I started my bitcoin journey and it seems very obvious to me that I will never stop. So, if you find a TODO anywhere, you have been warned.

Its usage should be as simple as sourcing it to `.zshrc` in order to get the included commands available to your own shell. The `.zshrc` file is nothing more than a configuration file for the zsh - or otherwise known as the z shell. It is a script that runs every time a you start a new interactive shell and is typically located in your home directory `~/.zshrc`.

What is more, this file can also be used as a reference, or even better a checklist, to assist with procedures such how to build the project, how to set up your system to do a pr review, or how to initiate a debugging session. In my case, I find it handy to have it open (as read only!) on the side of my basic terminal arrangement during development for quick look ups.

## System requirements

The Intended use is for computers running macos with zsh shell available and visual studio code installed mostly for more interactive and visual debugging. Otherwise just using vm or any other editor is also fine.

- [macos](https://support.apple.com/en-us/102662)
- [zsh](https://www.zsh.org/)
- [vscode](https://code.visualstudio.com/)

The project also assumes that you have your own fork of [bitcoin](https://github.com/bitcoin/bitcoin) on your machine.

## Installation

You just have to clone this repository to a directory on your machine using:

`% git clone https://github.com/itornaza/btc-dot.git`

## Documentation

For a quick intro just read the next two sections [Bitcoin dot file](#bitcoin-dot-file) and [Visual Studio Code configuration file](#visual-studio-code-configuration-file) which very brief on purpose because I just want the project files to be self-contained. 

For more relevant and detailed documentation please refer to the respective comment sections within each project file.

## Bitcoin dot file

[bitcoin](https://github.com/itornaza/btc-dot/blob/main/bitcoin) is the main dot file that defines exports, aliases, commands and functions in order to simplify and streamline the bitcoin building, testing and development process. 

It is divided into the following two main sections.

- `Checklists` for procedures grouped together in order to help you get through with regular tasks within the bitcoin project. 

- `zsh` which contains the actual commands that do the job. Feel free to add you own commands, rename the existing ones or do whatever you deem appropriate to suit your needs. This section is also divided to logical groupings like, `Installations`, `Git`, `Build`, `Tests`, etc to further guide you through the process or help you locate desired commands more easily. 

- The `git difftool` can also be easily integrated with vscode as well for a more visual spot of the differences.

### How to use

To include the [bitcoin](https://github.com/itornaza/btc-dot/blob/main/bitcoin) configuration in your shell environment include the following line in `~/.zshrc` like.

`source <path-to-bitcoin-file>`

Then, you only have to restart the terminal for the file to get sourced.

**Caution!** Please read through the file before sourcing it to avoid any unintentional behavior of your system. It shouldn't be that bad, but please check it out first.

## Visual Studio Code configuration file

[bitcoin.code-workspace](https://github.com/itornaza/btc-dot/blob/main/bitcoin.code-workspace)  which is a visual studio code file, is included as well for anyone who wants to run debugging sessions with the added convenience of an IDE. 

### How to use

Assuming you have visual studio code installed, you just need to open vscode and from the top menu select `File > Open workspace from file`. Then select this project's `bitcoin.code-workspace` from wherever you have cloned it. 

After doing that, if you want to open the `bitcoin.code-workspace` file from within the workspace to check the documentation, select the `Run and Debug` button on the top left of the screen and then click on the settings symbol next to the debug configurations on the topmost part of the left pane. 

Please, read the file for more on the debug configurations and how to use them.

## References

The main sources for the compilation of this file comes straight from Bitcoin Core:

- [macOS Build Guide](https://github.com/bitcoin/bitcoin/blob/master/doc/build-osx.md)

- [Contributing to Bitcoin Core](https://github.com/bitcoin/bitcoin/blob/master/CONTRIBUTING.md)

- [Developer Notes](https://github.com/bitcoin/bitcoin/blob/master/doc/developer-notes.md)

- [Productivity](https://github.com/bitcoin/bitcoin/blob/master/doc/productivity.md)

- [Benchmark](https://github.com/bitcoin/bitcoin/blob/master/doc/benchmarking.md)

and Jon Atack's blog: 

- [How to compile Bitcoin Core and run the unit and functional tests](https://jonatack.github.io/articles/how-to-compile-bitcoin-core-and-run-the-tests)

- [How to Review Pull Requests in Bitcoin Core](https://jonatack.github.io/articles/how-to-review-pull-requests-in-bitcoin-core)

- [Onboarding to Bitcoin Core](https://bitcoincore.academy/bin/onboarding-to-bitcoin-core.html)

On debugging with Visual Studio code or not:

- [Debugging](https://code.visualstudio.com/Docs/editor/debugging)

- [Debugging Bitcoin Core](https://github.com/fjahr/debugging_bitcoin)

- [lldb tutorial](https://lldb.llvm.org/use/tutorial.html)

Misc external tools references

- [Vim](https://www.vim.page/vim-commands-cheat-sheet)

## License

[Bitcoin dot](#bitcoin-dot) is released under the terms of the [MIT license](https://opensource.org/licenses/MIT)
