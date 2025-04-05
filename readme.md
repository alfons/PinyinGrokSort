## Installation

# PinyinGrokSort

## Description

A fast sorting algorithm to sort words in Hànyǔ Pīnyīn in alphabetical order, inspired by the "ABC Chinese-English Dictionary" by John DeFrancis.

Hànyǔ Pīnyīn is the romanised writing form of modern, spoken, standard Chinese. The sorting algorithm is intended for Pīnyīn with diacritics (no fall-back to tone numbers.) It is assumed that words are written letter by letter, not by pre-defined syllable blocks.

## The Rules

    1. Sort by base characters (ignoring tones, case, and separators) alphabetically.
    2. Sort by tones: no tone, 1st tone (ā), 2nd tone (á), 3rd tone (ǎ), 4th tone (à).
    3. Sort u before ü.
    4. Sort lowercase/mixed case before all uppercase.
    5. Sort by separators: no separator < space < hyphen.


## Credits

    - John DeFrancis: Original Pinyin sorting rules from "ABC Chinese-English Dictionary".
    - Mark Swofford of Banqiao, Taiwan: Explaining the rules on the pinyin.info blog.
    - Grok (xAI): Coding the implementation with flair and precision.
    - Alfons Grabher: Idea, prompting, testing, and driving the development.

## Usage

### For an array of strings: 
    
```python
from PinyinGrokSort import pinyin_grok_sort

sorted_list = pinyin_grok_sort(["shíshī", "shíshì", "shǐshī", "shìshī", "shīshi", "shīshī", "shīshí", "shīshǐ", "shīshì"])
```

### For an array of dictionaries:

```python
from PinyinGrokSort import pinyin_grok_sort

sorted_list = pinyin_grok_sort([{"pinyin": "shíshī"}, {"pinyin": "shīshi"}], key="pinyin")
```


### For an array of dictionaries (descending order Z-A):

```python
from PinyinGrokSort import pinyin_grok_sort

sorted_entries = pinyin_grok_sort(entries_list, key="pinyin", reverse=True)
```
