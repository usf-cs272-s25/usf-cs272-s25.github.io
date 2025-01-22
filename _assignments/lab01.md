---
layout: assignment
due: 2025-01-22 17:00
github_url: https://classroom.github.com/a/SS2VPKUZ
published: true
---

## Step 1: Set up your terminal environment

1. For this course, you will develop software locally on your laptop. If you are not familiar with the Unix shell, please review my [Shell Basics](https://github.com/usfca-cs-tools/docs/blob/main/shell-basics.md) document.
1. Terminal setup (<a onclick="toggle_display('terminal_mac')">Mac</a>, <a onclick="toggle_display('terminal_win')">Windows</a>)

    <div id="terminal_mac" class="div-toggle" style="display:none" markdown=1>
    For Mac:
    - Apple's Terminal app should work ok
    - I prefer [iTerm2](https://iterm2.com/) because it works well with my preferred terminal-mode editor, [micro](https://iterm2.com/)
    </div>

    <div id="terminal_win" class="div-toggle" style="display:none" markdown=1>
    For Windows:
    - I recommend using [Git For Windows](https://gitforwindows.org/). Git Bash offers a Unix-like shell environment.
    - If you already have [Windows Subsystem for Linux](https://learn.microsoft.com/en-us/windows/wsl/install), that's also fine
    </div>

1. You may use the terminal-mode editor of your choice (e.g. micro, nano, vim, emacs)

## Step 2: Use github on USF's network

1. In order to use `github.com` you'll want to somehow store credentials on your laptop. Traditionally, we used [`ssh`](https://cs221-03-f23.github.io/docs/ssh-local-setup.html) to authenticate to github, where credentials are stored using `ssh-agent`. 
1. However, USF has made it difficult to use `ssh` on the USF Connect Wi-Fi network. Therefore, I recommend switching to using `http` and [Git Credential Manager](https://github.com/git-ecosystem/git-credential-manager/blob/release/docs/install.md)
1. I recommend that you clone repos using the http URL. Git will use the credential manager, and communicate over `https`, which is permitted on USF Connect.

## Step 3: Set up your Go toolchain

1. Install the [Go toolchain](https://go.dev/dl/). Be careful to choose the right build for your laptop (<a onclick="toggle_display('go_mac')">Mac</a>, <a onclick="toggle_display('go_win')">Windows</a>)

    <div id="go_mac" class="div-toggle" style="display:none" markdown=1>
    For Mac:
    - Newer Apple laptops with M1 or M2 processors need the `darwin-arm64` build
    - Older Apple laptops with Intel processors need the `darwin-amd64` build
    - The Go toolchain installs into `/usr/local/` and is automatically added to the `PATH` (by installing itself into `/etc/path.d/`)
        ```sh
        phil@Phils-MacBook-Pro:~ % which go
        /usr/local/go/bin/go

        phil@Phils-MacBook-Pro:~ % go version
        go version go1.23.0 darwin/arm64
        ```
    </div>

    <div id="go_win" class="div-toggle" style="display:none" markdown=1>
    For Windows Git Bash:
    - Windows laptops need the `windows-amd64` build
    - The Go toolchain installs into `C:\Program Files\Go` and is added to the `PATH` automatically
        ```sh
        phil@PHILPETERSO43DB MINGW64 /
        $ which go
        /c/Program Files/Go/bin/go

        phil@PHILPETERSO43DB MINGW64 /
        $ go version
        go version go1.23.0 windows/amd64
        ```
    </div>

1. Install the `dlv` ([delve](https://github.com/go-delve/delve)) debugger.
    ```sh
    go install github.com/go-delve/delve/cmd/dlv@latest
    ```

1. Edit your shell config file (<a onclick="toggle_display('dlv_mac')">Mac</a>, <a onclick="toggle_display('dlv_win')">Windows</a>)

    <div id="dlv_mac" class="div-toggle" style="display:none" markdown=1>
    For Mac:
    1. Edit `~/.zshrc`
    1. At the bottom of the file, add `export PATH=~/go/bin:$PATH`
    1. Apply the change to your shell: `source ~/.zshrc`
    </div>

    <div id="dlv_win" class="div-toggle" style="display:none" markdown=1>
    For Windows Git Bash:
    1. Edit `~/.bashrc`
    1. At the bottom of the file, add `export PATH=~/go/bin:$PATH`
    1. Apply the change to your shell: `source ~/.bashrc`
    </div>

1. Check to see that `dlv` is on the path
    ```sh
    phil@Phils-MBP:~ % which dlv
    /Users/phil/go/bin/dlv
    ```

1. If you want to use an Integrated Development Environment (IDE), I recommend [VS Code](https://code.visualstudio.com/). VS Code will offer to install extensions for `go` and `gopls`. You should accept both. 

1. Unsupported: There is a Go-specific IDE called [GoLand](https://www.jetbrains.com/go/) that you're welcome to try. I won't be supporting it.

## Given

1. Clone the lab01 repo using the link above and `cd` into that directory
1. Use your preferred editor to enter this `go` program, which prints `Hello, World` into the terminal
    ```go
    package main

    import "fmt"

    func main() {
        fmt.Println("Hello, World")
    }
    ```
1. To run the program
    ```sh
    $ go run main.go
    Hello, World
    ```

## Rubric

1. 100 pts
    1. Commit and push your Hello World
    1. Show me your environment working during the Week 1 lab section.

<script>
    function toggle_display(id_name) {
        var e = document.getElementById(id_name);
        if (e.style.display === "none") {
            e.style.display = "block";
        } else {
            e.style.display = "none";
        }
    }
</script>

