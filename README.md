# termcode

Edit code and review Git changes in a Linux terminal. Open a project to browse its files,
search across them, and see edits side by side with the last commit. You can also open the
editor as a Code tab in herdr.

> This repository is where termcode is published, and where you report problems and ask
> for features. It holds no source code.

**Contents** · [Install on Debian or Ubuntu](#install-on-debian-or-ubuntu) · [Edit a file](#edit-a-file) · [Review changes](#review-changes) · [Help and settings](#help-and-settings) · [License and credits](#license-and-credits)

![termcode showing the file explorer, editor and integrated terminal](doc/screenshots/editor.png)

## Install on Debian or Ubuntu

Run `dpkg --print-architecture` to find your architecture (`amd64` or `arm64`).
Download the matching `.deb` from the [latest release](https://github.com/JonasAtelier/termcode-releases/releases/latest).
In the folder containing that package, install it and check the version.

```sh
sudo apt install ./termcode_*.deb
termcode --version
```

The release notes also explain how to add the signed apt repository for updates.
For a Code tab in herdr 0.9.1+, run `herdr plugin link /usr/share/termcode`.

<a id="open-your-first-file"></a>

## Edit a file

From a project folder, run `termcode .` (or `termcode --tab .` in herdr). Press
**Ctrl+P**, type part of a filename and select it. **Ctrl+S** saves, **F1** lists
commands, and **Ctrl+Q** returns to the shell.

| Task | How to do it |
| --- | --- |
| Open a file at a known line | Run `termcode README.md:12` from the folder containing that file. |
| Find a function | Press **Ctrl+P** in the editor and type `@` to browse functions in the current file. |
| Preview Markdown | Open a Markdown file and press **Ctrl+Shift+V** to switch between source and preview. |

## Review changes

Save an edit, press **Ctrl+G** to open **Source Control**, and select the changed
file. Read the old and new versions side by side.

When a repository’s Git settings can start external programs, Source Control asks you
to trust the repository before enabling Git. Only grant trust if you know its origin.

## Help and settings

**Ctrl+,** opens Settings. The Debian package includes `man termcode`. The
[0.4.0 user guide](https://github.com/JonasAtelier/termcode-releases/blob/6fcfc0078c2f0a48eac95b96a0446457dde30b53/README.md)
covers shortcuts, previews, optional tools and troubleshooting. To report a problem,
run **Help: Report Issue** from F1 and review the copied diagnostics before posting
to the [issue tracker](https://github.com/JonasAtelier/termcode-releases/issues/new/choose).

## License and credits

For packaged releases, see the terms shipped in `/usr/share/doc/termcode/copyright` and the dependency licenses in `/usr/share/doc/termcode/THIRD-PARTY-LICENSES`. Default colors come from Microsoft’s
VS Code and file icons from Jesse Weed’s Seti UI, both under MIT.
