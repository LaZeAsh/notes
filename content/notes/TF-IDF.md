---
title: "Term Frequency - Inverse Document Frequency (TF-IDF)"
---

Term Frequency - Inverse Document Frequency (TF-IDF) is a weighing system that assigns a weight to each word in a document based on its term frequency (TF) and inverse document frequency (IDF). 

Formula: TF * IDF

Youtube Video Link: https://youtu.be/D2V1okCEsiE?si=RicTV_H1U5iHFfTQ

## Term Frequency

Term frequency is defined by Number of repeated words in a sentence / Number of words in a sentence

Example:

- Sentence 1 -> Good Boy

- Sentence 2 -> Good Girl

- Sentence 3 -> Boy Girl Good

Term Frequency Table:

|      | Sent 1 | Sent 2 | Sent 3 |
| ---- | ------ | ------ | ------ |
| good | 1/2    | 1/2    | 1/3    |
| boy  | 1/2    | 0      | 1/3    |
| girl | 0      | 1/2    | 1/3    |

## Inverse Document Frequency

Inverse Document Frequency is defined by log(Number of sentences / Number of sentences containing words)


IDF Table:

| Words | IDF          |
| ----- | ------------ |
| good  | log(3/3) = 0 |
| boy   | log(3/2)     |
| girl  | log(3/2)     |

## Multiply TF and IDF



|            | word 1 | word 2          | word 3          |
| ---------- | ------ | --------------- | --------------- |
|            | good   | boy             | girl            |
| Sentence 1 | 0      | 0.5 * log(3/2)  | 0               |
| Sentence 2 | 0      | 0               | 0.5 * log(3/2)  |
| Sentence 3 | 0      | 0.33 * log(3/2) | 0.33 * log(3/2) |

This table makes it possible for us to interpret the meaning of the sentence by placing emphasize on the important words:

In Sentence 1 (good boy):

The word good has a value of 0 and the word boy has a value of 0.5 * log(3/2)

$\because$ 0.5 * log(3/2) > 0 numerically the emphasize is placed on the word boy

Grammatically this would also hold true, the word "boy" in good boy is more important / relevant than the word "good"

In Sentence 2 (good girl):

Same pattern as the Sentence 1 instead of boy now we're talking about girl

In Sentence 3 (Boy Girl Good)

Boy and Girl are given equal emphasis while good is not valued as much compared to Boy and Girl

## Conclusion

This is a really cool way to mathematically give meaning to sentences by measuring which words hold more importance.

- Term Frequency (TF) = Number of repeated words in a sentence / Number of words in a sentence
- Inverse Document Frequency (IDF) = log(Number of sentences / Number of sentences containing a word)
- Multiply TF and IDF to get a vector that showcases the importance of each word in a numerical value. **The higher the value the more important it is**