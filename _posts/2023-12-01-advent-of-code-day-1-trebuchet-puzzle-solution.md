---
layout: post
title: "Advent of Code - Day 1: Trebuchet Puzzle Solution"
tags: [AoC, Advent of Code, Python, Puzzle, Solution]
description: "Explanation of my Python based solution to the AoC Puzzle of Day 1 in 2023."
---


# Advent of Code - Day 1: Trebuchet Puzzle Solution

## Unraveling the Trebuchet Mystery

Welcome to my solution walk-through for [Day 1 of the Advent of Code](https://adventofcode.com/2023/day/1) challenge, titled "Trebuchet?!". This year, you are tasked with restoring global snow production, which requires getting fifty stars marked on a map by December 25th.

The elves are loading you onto a [trebuchet](https://en.wikipedia.org/wiki/Trebuchet), ready to shoot you into the sky, because that's where the snow comes from.
But here's the catch: the calibration document needed for the trebuchet has been creatively altered by a young Elf, making the values hard to read. This sets the stage for our two-part programming challenge:

1. **Extract and Sum Calibration Values:** The first part of the puzzle requires us to extract calibration values from each line of text by combining the first and last digits into a two-digit number and summing these numbers.
2. **Incorporate Spelled-out Digits:** The second part complicates things a bit. Some digits are spelled out (like 'one', 'two', 'three', etc.), and these also count as valid digits. The task is to find the real first and last digit (numeric or spelled out) on each line and sum them as before.

This puzzle tests our ability to manipulate strings, regular expressions, and map data structures. It's an excellent exercise in parsing and transforming textual data.

## My Solution: Step-by-Step

### Part One: Simplified Digit Extraction

```python
def solve():
    """Solve first part of the puzzle"""
    # only keep the digits of each line
    numbers = input(convert_fn=lambda s: "".join(filter(str.isdigit, s)))
    #  concat first and last digit, convert to int, calculate sum
    return sum(map(int, [n[0]+n[-1] for n in numbers if n]))
```

1. **Filtering Digits:** For each line of the input, I used a lambda function to filter out all non-digit characters, leaving only the numeric ones.
2. **Concatenation and Summation:** I then concatenated the first and last digit of each processed line, converted it into an integer, and computed the sum of these integers.

### Part Two: Including Spelled-out Digits with Overlapping Characters

```python
def solve2():
    """Solve second part of the puzzle"""

    # produce a map for different string representations to ints (e.g. 'one': 1, '1': 1)
    str_digit_map = ['one', 'two', 'three', 'four', 'five', 'six', 'seven', 'eight', 'nine']
    str_digit_map = {s: str(i) for i, s in enumerate(str_digit_map, start=1)}
    str_digit_map.update({str(i): str(i) for i in range(1, 10)})

    result = 0
    for line in input():
        # in each line find the starting indices for each number string
        findings = {}
        for s, v in str_digit_map.items():
            findings.update({i: v for i in substring_idx(line, s)})
        # the minimum and maximum indices correspond to the first and last digit in the string
        min_idx, max_idx = min(findings), max(findings)
        # concat digits and sum up
        result += int("".join((findings[min_idx], findings[max_idx])))

    return result
```

1. **Challenges with Overlapping Characters:** An intriguing aspect of this puzzle is handling cases where spelled-out numbers are joined together, sharing some letters, like in 'eightwothree' which translates to '823'. This scenario poses a unique challenge since using simple string replacement methods or standard regex find operations would consume the shared letters ('t' in this example) in the first finding or replacement, making it impossible to correctly identify subsequent numbers.
2. **Maintaining Character Integrity:** To overcome this, I employed a strategy that involves finding the starting indices of all occurrences of each digit representation in the string, without consuming the characters. This way, the shared characters between adjoining numbers are preserved for subsequent matches.
3. **Mapping and Concatenating Digits:** After identifying the starting indices, I used a dictionary (findings) to map these indices to their corresponding digit values. The first and last digits in the text are then identified by the minimum and maximum indices, ensuring that even in joined representations like 'eightwothree', each digit is correctly identified and translated.
4. **Final Computation:** The first and last digit representations are concatenated and summed across all lines to give the final result.

The function to find all starting indices of a substring can be easily implemented using the re module:
{% raw %}
<script src="https://gist.github.com/gboeer/b3efdd765c8edf8568d76ee4f086b8cd.js"></script>
{% endraw %}


## Conclusion

Reflecting on this year's Advent of Code, Day 1's "Trebuchet?!" puzzle stands out as a notch more challenging compared to the puzzles of previous years. Particularly, the second part of the challenge brought an intriguing twist that compelled me to rethink my initial approach.

My first instinct was to employ simple string replacements to extract and process the digits. While this method seemed straightforward initially, it quickly became apparent that it wasn't sufficient for the task at hand, especially when dealing with concatenated digit words like 'eightwothree'.

### &#x21A7; &#x21A7; &#x21A7; 
[Code for all my solutions for this year](https://github.com/gboeer/advent_of_code/blob/main/2023/)

