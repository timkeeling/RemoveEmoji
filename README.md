macOS Emoji Remover

A lightweight macOS Quick Action that automatically strips emojis from filenames directly from Finder.

It uses native macOS tools (Perl), requiring no external dependencies or installations (no Python/Xcode required).

Features

Zero Dependencies: Runs on stock macOS.

Safe: Uses a "Dry Run" logic internally to handle collisions (e.g., if File🔥.txt and File.txt both exist, it renames to File_1.txt).

Comprehensive: Removes modern 4-byte emojis and legacy symbols (Dingbats, etc).

Clean: Automatically removes double spaces left behind by deletions.

Installation

This tool works as a Finder Quick Action. You must create it once in Automator.

Open Automator on your Mac.

Select New Document > Quick Action.

Configure the top workflow settings:

Workflow receives current: files or folders

in: Finder

Search for and add the action: Run Shell Script.

Configure the script settings:

Shell: /bin/zsh

Pass input: as arguments

Delete any default text in the script box.

Copy the code from the remove_emojis_automator.sh file in this repository and paste it into the Automator box.

Save the file (Cmd+S) as Remove Emojis.

Usage

Select any file(s) or folder(s) in Finder.

Right-click (or Control-click).

Navigate to Quick Actions > Remove Emojis.

The filenames will update instantly.

License

MIT****
