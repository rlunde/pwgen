# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a simple XKCD-style password generator implementation as a single HTML file. The project generates human-readable passwords using common English words rather than random character strings, inspired by the XKCD comic about password entropy.

## Project Structure

The repository contains only two files:
- `README.md` - Project description and TODO list
- `pwgen.html` - Complete password generator implementation

## Architecture

### Single-File Implementation
The entire application is contained in `pwgen.html` with:
- Embedded JavaScript for password generation logic
- Inline HTML for the user interface
- No external dependencies or build process

### Key Components

#### Password Generation (`pwgen.html:444-504`)
- `xkcd_pw_gen()` - Original XKCD-style generator (4 words separated by spaces)
- `ron_pw_gen()` - Customized generator with 2 words, capitalization, punctuation, and digits
- Uses a predefined wordlist of 404 common English words

#### Entropy Sources (`pwgen.html:414-441`)
- System clock timing measurements
- Browser/system information (user agent, screen dimensions)
- Math.random() combined with SHA-1 hashing
- Server-provided hash value for additional entropy

#### Word Selection (`pwgen.html:447-451`)
- Combines JavaScript Math.random() with SHA-1 hash
- XOR operation for additional randomness
- Modulo operation to select from wordlist

## Development Notes

### No Build System
This is a standalone HTML file with no build, test, or lint commands. Development workflow is simply:
1. Edit `pwgen.html` directly
2. Open in browser to test
3. No compilation or preprocessing required

### Current Implementation Status
The active password generator is `ron_pw_gen()` which creates passwords with:
- 2 words from the wordlist
- One word capitalized (first letter only)
- One punctuation character (!@#$%^&*)
- One digit (0-9)
- Format: `Word1[punct]word2[digit]` or `Word1[digit]word2[punct]`

### Author's Memory Considerations (from README)
- Avoid uppercase letters (hard to remember which word/letter is capitalized)
- Use more words to compensate for no uppercase
- Can remember digits or special characters as word separators or terminators

### Future Enhancements (from README)
The author plans to modernize this into a Hugo-based website with:
- Multiple password choices at once
- Clipboard copy functionality
- User controls for length and special characters
- Better visual design
- Accommodation for password length limits