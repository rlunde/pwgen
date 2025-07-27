# XKCD Password Generator

A simple, memory-friendly password generator inspired by the [XKCD "Password Strength" comic](https://xkcd.com/936/). This tool creates passwords using common English words instead of confusing strings of random characters, making them both secure and memorable.

## The Problem

Traditional password generators create strings like `Tr0ub4dor&3` that are:
- Hard to remember (which word was capitalized?)
- Difficult to type accurately
- Annoying to enter on mobile devices
- Still not as secure as they could be

Meanwhile, passwords like `correct horse battery staple` are:
- Much easier to remember and type
- More secure due to higher entropy
- Perfect for WiFi passwords, mobile apps, and other situations where you actually need to type them

## The Solution

This generator creates memorable passwords using:
- **common lowercaseEnglish words** (no confusing capitalization to forget)
- **Optional separators** between words (spaces,digits or special characters)
- **Optional terminators** at the end for extra security
- **Multiple choices** so you can pick one that feels right

### Features

- 🎯 **Memory-optimized**: No mixed lowercase and uppercase letters to forget
- 🔧 **Flexible controls**: Adjust word count, separators, and character types
- 📱 **Easy copying**: One-click copy buttons for each password
- 📊 **Multiple options**: Generate 3-10 passwords at once

## How to Use

1. Open `pwgen.html` in your web browser
2. Adjust settings:
   - **Number of words**: 2-5 words (more words = more security)
   - **Number of passwords**: How many options to generate
   - **Separators**: Add characters or spacesbetween words
   - **Terminators**: Add characters at the end
   - **Character types**: Include digits (0-9) and/or special characters (!@#$%^&*)
3. Click "Generate Passwords"
4. Click "Copy" next to your favorite option

## Example Outputs

With different settings, you might get:
- `wordwordwordword` (4 words, no separators)
- `word3word!word8word` (4 words with separators)
- `wordwordwordword7` (4 words with terminator)
- `word3word!word8word#` (4 words with both)

## Security Considerations

⚠️ **Important Disclaimers:**

- **For casual use only**: This tool is designed for guest WiFi passwords, non-critical mobile apps, and other non-critical applications
- **Local only**: Runs entirely in your browser - no passwords are sent anywhere

**For important accounts** (banking, email, etc.), use:
- A proper password manager (1Password, Bitwarden, etc.)
- Hardware security keys where possible
- Two-factor authentication ***always***

## Technical Details

- **Offline capable**: Works without internet connection (with a VERY limited word list)

## Remaining TODO

- Link to educational resources about password security

## Inspiration

Based on [XKCD #936: Password Strength](https://xkcd.com/936/) by Randall Munroe, which brilliantly illustrates why `correct horse battery staple` is better than `Tr0ub4dor&3`.