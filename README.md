# Readability

## Background

According to Scholastic, E.B. White’s Charlotte’s Web is between a second- and fourth-grade reading level, and Lois Lowry’s The Giver is between an eighth- and twelfth-grade reading level. What does it mean, though, for a book to be at a particular reading level?

Well, in many cases, a human expert might read a book and make a decision on the grade (i.e., year in school) for which they think the book is most appropriate. But an algorithm could likely figure that out too!

## Instructions

In a file called `readability.py`, you’ll implement a program that calculates the approximate grade level needed to comprehend some text. Your program should print as output “Grade X” where “X” is the grade level computed, rounded to the nearest integer. If the grade level is 16 or higher (equivalent to or greater than a senior undergraduate reading level), your program should output “Grade 16+” instead of giving the exact index number. If the grade level is less than 1, your program should output “Before Grade 1”.

* To calculate the grade level of a text, you can calculate the "Coleman-Liau" index: `0.0588 * L - 0.296 * S - 15.8`, where `L` is the average number of letters per 100 words in the text, and `S` is the average number of sentences per 100 words in the text.

* Your program should count the number of letters, words, and sentences in the text. You may assume that a letter is any lowercase character from `a` to `z` or any uppercase character from `A` to `Z`, any sequence of characters separated by spaces should count as a word, and that any occurrence of a period, exclamation point, or question mark indicates the end of a sentence.

* Your program should print as output `Grade X` where `X` is the grade level computed by the Coleman-Liau formula, rounded to the nearest integer.

* If the resulting index number is 16 or higher (equivalent to or greater than a senior undergraduate reading level), your program should output `Grade 16+` instead of giving the exact index number. If the index number is less than 1, your program should output `Before Grade 1`.

## Sample Checkpoints

### Sample Checkpoint 1

**Sample Input**

```
One fish. Two fish. Red fish. Blue fish.
```

**Sample Output**

```
Before Grade 1
```

### Sample Checkpoint 2

**Sample Input**

```
Would you like them here or there? I would not like them here or there. I would not like them anywhere.
```

**Sample Output**

```
Grade 2
```

### Sample Checkpoint 3

**Sample Input**

```
A large class of computational problems involve the determination of properties of graphs, digraphs, integers, arrays of integers, finite families of finite sets, boolean formulas and elements of other countable domains.
```

**Sample Output**

```
Grade 16+
```
