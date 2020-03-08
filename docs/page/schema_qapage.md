---
layout: page
---

### 説明

Q＆A

### タイプ

| タイプ名 | 説明     |
| -------- | -------- |
| QAPage   | Q&A要素 |
| Question | 質問     |
| Answer   | 回答     |

### プロパティ

#### QAPage

| プロパティ名     | 説明       |
| ---------------- | ---------- |
| mainEntity(必須) | メイン要素 |

#### Question

| プロパティ名         | 説明                   |
| -------------------- | ---------------------- |
| answerCount(必須)    | 質問に対する回答の総数 |
| acceptedAnswer(必須) | 回答                   |
| name(必須)           | 質問                   |
| author               | 質問者                 |
| dateCreated          | 追加日(ISO8601形式)   |
| text ｜質問文        |
| upvoteCount          | 質問に対する投票の総数 |

#### Answer

| プロパティ名 | 説明                   |
| ------------ | ---------------------- |
| text(必須)   | 回答の全文             |
| author       | 回答者                 |
| dateCreated  | 追加日(ISO8601形式)   |
| upvoteCount  | 回答に対する投票の総数 |
| url          | URL                    |

### 例

    <script type="application/ld+json">
    {
      "@context": "https://schema.org",
      "@type": "QAPage",
      "mainEntity": {
        "@type": "Question",
        "name": "How many ounces are there in a pound?",
        "text": "I have taken up a new interest in baking and keep running across directions in ounces and pounds. I have to translate between them and was wondering how many ounces are in a pound?",
        "answerCount": 3,
        "upvoteCount": 26,
        "dateCreated": "2016-07-23T21:11Z",
        "author": {
          "@type": "Person",
          "name": "New Baking User"
        },
        "acceptedAnswer": {
          "@type": "Answer",
          "text": "1 pound (lb) is equal to 16 ounces (oz).",
          "dateCreated": "2016-11-02T21:11Z",
          "upvoteCount": 1337,
          "url": "https://example.com/question1#acceptedAnswer",
          "author": {
            "@type": "Person",
            "name": "SomeUser"
          }
        },
        "suggestedAnswer": [
          {
            "@type": "Answer",
            "text": "Are you looking for ounces or fluid ounces? If you are looking for fluid ounces there are 15.34 fluid ounces in a pound of water.",
            "dateCreated": "2016-11-02T21:11Z",
            "upvoteCount": 42,
            "url": "https://example.com/question1#suggestedAnswer1",
            "author": {
              "@type": "Person",
              "name": "AnotherUser"
            }
          }, {
            "@type": "Answer",
            "text": " I can't remember exactly, but I think 18 ounces in a lb. You might want to double check that.",
            "dateCreated": "2016-11-06T21:11Z",
            "upvoteCount": 0,
            "url": "https://example.com/question1#suggestedAnswer2",
            "author": {
              "@type": "Person",
              "name": "ConfusedUser"
            }
          }
        ]
      }
    }
    </script>
