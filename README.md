# Firefox-userChrome

This repository contains my customizations for Firefox’s chrome. Currently, they are:

- Changes Developer Tools font to _Victor Mono Medium_ 12px.

## Installation

### Windows

Clone this repository:

```powershell
git clone git@github.com:Nurdoidz/Firefox-userChrome.git $Path
```

Change `$Path` to a new, empty directory.

Find your Firefox profile directory:

1. Open Firefox.
2. Open `about:support` in the address bar.
3. Click the “Open Folder” button next to “Profile Folder”.

To make developing easier, create a symlink in PowerShell:

```powershell
New-Item -Path $FirefoxProfile\chrome -ItemType SymbolicLink -Value $LocalRepo\chrome
```

Change the following strings to match your environment:

- `$FirefoxProfile`: The path to your Firefox profile.
- `$LocalRepo`: The path to your local git repository. 

If you chose **not** to create a symlink, copy the `chrome` directory from the local repository to your Firefox profile directory. Note that a new installation of Firefox will not have a `chrome` directory by default.

Finally, enable custom chrome stylesheets in Firefox:

1. Open Firefox.
2. Open `about:config` in the address bar.
3. Click the “Accept the Risk and Continue” button if you are prompted.
4. Search or find the `toolkit.legacyUserProfileCustomizations.stylesheets` key.
5. Set the value to `true`.
