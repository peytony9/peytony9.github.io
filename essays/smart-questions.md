---
layout: essay
type: essay
title: "Smart Question? What's a Smart Question?"
# All dates must be YYYY-MM-DD format!
date: 2026-01-29
published: True
labels:
  - Questions
  - Answers
  - StackOverflow
---

<img width="300px" class="rounded float-start pe-4" src="../img/smart-questions/rtfm.png">

## The Importance of a Smart Question

Everyone has their own questions and in a complicated line of work like software engineering, questions constantly show up so it's crucial that these questions are smart questions. You may ask, what in the world is a "smart question"? A smart question consists of many different aspects such as effort, context, clarity, precision, and respect. Smart questions are just as if not more important for software engineering because coding languages can be complicated and problems can have many different solutions. The ability to ask smart questions is a crucial skill for collaboration, productivity, and learning in the software engineering work space and community.

## What’s a smart question?

In search of a smart question, I explored through Stack Overflow which is a really useful question and answer website for software engineers. Stack Overflow is a great way for programmers to find answers to the issues they face in their coding and learn from their questions and answers of those around them. While most questions are smart questions, I searched through and found both a smart question and a "bad" question.

The first example I found was of a smart question and I'd like to believe that this question being a good question is the reason it has the most votes on Stack Overflow. The asker was trying to figure out why a sorted array processes faster than an unsorted one.

```
Q: Why is processing a sorted array faster than processing an unsorted array?

In this C++ code, sorting the data (before the timed region) makes the primary loop ~6x faster:

    // After Data Generated
    // Test
    clock_t start = clock();
    long long sum = 0;
    for (unsigned i = 0; i < 100000; ++i)
    {
        for (unsigned c = 0; c < arraySize; ++c)
        {   // Primary loop.
            if (data[c] >= 128)
                sum += data[c];
        }
    }

    double elapsedTime = static_cast<double>(clock()-start) / CLOCKS_PER_SEC;

    std::cout << elapsedTime << '\n';
    std::cout << "sum = " << sum << '\n';
}

- Without std::sort(data, data + arraySize);, the code runs in 11.54 seconds.
- With the sorted data, the code runs in 1.93 seconds.

(Sorting itself takes more time than this one pass over the array, so it's not actually worth doing if we needed to calculate this for an unknown array.)

Initially, I thought this might be just a language or compiler anomaly, so I tried Java:

    // After Date Generated
    // Test
      long start = System.nanoTime();
      long sum = 0;
      for (int i = 0; i < 100000; ++i)
      {
          for (int c = 0; c < arraySize; ++c)
          {   // Primary loop.
                if (data[c] >= 128)
                    sum += data[c];
            }
        }

        System.out.println((System.nanoTime() - start) / 1000000000.0);
        System.out.println("sum = " + sum);
    }
}
With a similar but less extreme result.

My first thought was that sorting brings the data into the cache, but that's silly because the array was just generated.

- What is going on?
- Why is processing a sorted array faster than processing an unsorted array?

The code is summing up some independent terms, so the order should not matter.
```
[Link to Stack Overflow Question](https://stackoverflow.com/questions/11227809/why-is-processing-a-sorted-array-faster-than-processing-an-unsorted-array)
The asker received 26 answers to their question that brought a lot of insight about the reasoning they were encountering this bizzare "issue" and the reason they were receiving good answers was due to their good question. The question is straightforward as to what the asker's goal was and it's clear that they put it in time trying to figure it out on their own and since they made it precise and informative, they received precise and informative responses back.

## What's an un-smart question?

While it may seem like realistically a question could never be bad, there are cases. Some questions can be difficult to answer, not very insightful, not precise on what the goal of the question is, etc. It's hard to find not so smart questions on Stack Overflow so I asked ChatGPT to help me look for one and here's what I found:

```
Q: Is a sudden occurence of an unbearable desire to write some comments, a symptom of a bad design?

Imagine... You have written some code; implemented some interfaces, used some design patterns, passed many unit tests, extracted many methods for sake of refactoring and so. You developed, developed, developed... But at some mysterious point, for some reason you, something inside you started to whisper you that you should write a comment now. Something pokes you that if you don't write a comment something will be missing or something can be not exactly clear...

Then you comment your code! :(

Can this be a secret sign of a bad design?
```
[Link to the Stack Overflow Question](https://stackoverflow.com/questions/4450048/is-a-sudden-occurence-of-an-unbearable-desire-to-write-some-comments-a-symptom)
This question and even the description are noticiably different from the first one. The question is ambiguous and has no clear goal leaving the responses left up purely to how the responder feels which isn't very precise and the asker probably didn't get very useful answers as the question is so open ended. The question is also not super related to the coding part of software engineering and instead focuses on just comments which is typically a personalized part of projects.

## Conclusion

Questions answers are often in correlation with how "smart" the question is. I've realized the importance of smart questions and that questions should be very precise on what its goal is and it's important that the question is also clear and valid so that the answers can equally portray a clear precise answer to the question. Questions are one of the most important things in life as they often provide us with a lot of information so it's important to make our questions smart so that we can gain the most and the best answers for what we want to know.
