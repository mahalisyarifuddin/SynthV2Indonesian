**English** | [Bahasa Indonesia](README-id.md)

# SynthV2Indonesian
Indonesian vocal creation made easier.

## Introductions
SynthV2Indonesian adds Indonesian pronunciation support and a Bahasa Indonesia interface translation to Synthesizer V Studio 2 Pro.

Earlier attempts at Indonesian singing required splitting notes and mixing note languages to get the right sounds. With [Synthesizer V Studio 2 Pro 2.3.0](https://dreamtonics.com/synthesizer-v-studio-2-pro-2-3-0-update-and-improvements/), the editor now supports language-independent X-SAMPA natively. This dictionary uses that system to define Indonesian pronunciations without the old language mix-and-match workflow.

This is community-made support, not a new official Indonesian language mode or voice database. The dictionary lives under Spanish, but its pronunciations use X-SAMPA.

The repository includes:
- **`SynthV2Indonesian.json`**: An Indonesian pronunciation dictionary with 3,821 entries.
- **`id-id.txt`**: A Bahasa Indonesia UI translation.

This will be a living, breathing repository, following Synthesizer V updates with dictionary corrections, translation changes, and compatibility fixes.

## Quick Start / Usage

### Requirements
Use **Synthesizer V Studio 2 Pro 2.3.0 or later**. Dreamtonics notes that many 2.3.0 features require **voice version 205**; update supported voices through the Product Manager and check availability for your voice provider.

### Install the dictionary
1. Download [`SynthV2Indonesian.json`](SynthV2Indonesian.json).
2. Close Synthesizer V Studio 2 and copy the file into the Spanish dictionary folder below. Create the folder if needed.

**Windows**
```text
C:\Users\<username>\AppData\Roaming\Dreamtonics\Synthesizer V Studio 2\dicts\spanish
```

**macOS**
```text
/Users/<username>/Library/Application Support/Dreamtonics/Synthesizer V Studio 2/dicts/spanish
```

Replace `<username>` with your account name.

3. Reopen Synthesizer V Studio 2. Set the relevant notes to **Spanish** and select the installed Indonesian dictionary in the Dictionary panel.
4. Enable **Use X-SAMPA symbols** in the Dictionary panel so the entries are interpreted as X-SAMPA, not simplified Spanish phonemes. The Notes panel has the same option for viewing and editing note phonemes.
5. Enter Indonesian lyrics. Check the resulting phonemes and listen back; adjust entries or note phonemes where needed.

The dictionary contains word-to-pronunciation entries, not a complete Indonesian spelling-to-sound engine. For words it doesn't cover, add an entry in the Dictionary panel or enter X-SAMPA phonemes manually. Normal musical syllable splitting is still useful when a word spans several notes; the change is that you no longer need to split notes just to borrow sounds from different languages.

### Install the UI translation (Windows)
1. Download [`id-id.txt`](id-id.txt).
2. Close Synthesizer V Studio 2 and copy the file into:

```text
C:\ProgramData\Dreamtonics\Synthesizer V Studio 2\translations
```

3. Reopen the editor and select **Bahasa Indonesia** in the interface language settings. Restart if prompted. Copying into `ProgramData` may require administrator permission.

The UI translation and pronunciation dictionary are separate. You can use either without installing the other. The UI path above is for Windows; the macOS paths in this README cover the dictionary only.

## Phoneme Inventories and Examples
The supplied dictionary uses **32 distinct X-SAMPA tokens**. These tables describe the actual entries, including glides, a glottal stop, and unreleased stop variants. Tokens are case-sensitive: `j` and `J` are different sounds. Separate tokens with spaces.

### Vowels
| Token | Sound | Dictionary example | Stored pronunciation |
| --- | --- | --- | --- |
| `a` | a | aku | `a k u` |
| `i` | i | ibu | `i b u` |
| `u` | u | aku | `a k u` |
| `e_o` | Mid e (e taling) | enak | `e_o n a k}` |
| `@` | Schwa (e pepet) | empat | `@ m p a t}` |
| `o_o` | Mid o | obat | `o_o b a t}` |

Use `e_o` and `o_o` exactly as written in the file. Don't shorten them to `e` and `o` when copying these pronunciations.

### Consonants and glides
| Token | Sound / spelling cue | Dictionary example | Stored pronunciation |
| --- | --- | --- | --- |
| `p` | p | apa | `a p a` |
| `b` | b | batu | `b a t u` |
| `t` | t | satu | `s a t u` |
| `d` | d | dua | `d u a` |
| `k` | k | kaki | `k a k i` |
| `g` | g | gigi | `g i g i` |
| `tS` | c | cinta | `tS i n t a` |
| `dZ` | j | ajak | `a dZ a k}` |
| `m` | m | mata | `m a t a` |
| `n` | n | nama | `n a m a` |
| `J` | ny | nyanyi | `J a J i` |
| `N` | ng | bunga | `b u N a` |
| `f` | f | afdal | `a f d a l` |
| `s` | s | satu | `s a t u` |
| `z` | z | zaman | `z a m a n` |
| `S` | sy | syukur | `S u k u 4` |
| `x` | kh | khusus | `x u s u s` |
| `h` | h | hari | `h a 4 i` |
| `l` | l | lama | `l a m a` |
| `4` | Tapped r | rasa | `4 a s a` |
| `w` | w / glide | waktu | `w a k} t u` |
| `j` | y / glide | yakin | `j a k i n` |

### Closure and unreleased stops
| Token | Sound | Dictionary example | Stored pronunciation |
| --- | --- | --- | --- |
| `?` | Glottal stop | berdoa | `b @ 4 d o_o ? a` |
| `p}` | Unreleased p | atap | `a t a p}` |
| `t}` | Unreleased t | alat | `a l a t}` |
| `k}` | Unreleased k | adik | `a d i k}` |

These are dictionary choices, not a claim that every Indonesian speaker uses the same realization. Final stops, vowels, and loanwords may need adjustment for your intended pronunciation and the voice you use.

### Try a phrase
The dictionary contains each word in **aku cinta indonesia**:

| Word | X-SAMPA |
| --- | --- |
| aku | `a k u` |
| cinta | `tS i n t a` |
| indonesia | `i n d o_o n e_o s i a` |

For a correction or new word, follow the dictionary's existing format:

```json
{
  "w": "nyanyi",
  "p": "J a J i"
  "phoneset": "xsampa"
}
```

Entries belong inside the JSON file's top-level `data` array. Keep the JSON valid, including commas between entries.

## License
The Indonesian support files in this repository are licensed under the [MIT License](LICENSE).

**Synthesizer V © Dreamtonics.** Synthesizer V Studio and its voice databases are separate products governed by their respective licenses. This repository does not grant rights to those products and is not an official Dreamtonics release.

## Contributions
Pronunciation corrections, translation fixes, and pull requests are welcome. For dictionary changes, include the word, proposed X-SAMPA pronunciation, and the reason for the correction. For compatibility reports, include your Synthesizer V version and voice database version.
