---
layout: page
---

### 説明

求人情報

### タイプ

| タイプ名   | 説明     |
| ---------- | -------- |
| JobPosting | 求人情報 |

### プロパティ

#### JobPosting

| プロパティ名                  | 説明                                                     |
| ----------------------------- | -------------------------------------------------------- |
| datePosted(必須)              | 求人情報を投稿した最初の日付(ISO8601形式)               |
| description(必須)             | 求人の詳細                                               |
| hiringOrganization(必須)      | 会社                                                     |
| jobLocation(必須)             | 職場                                                     |
| title(必須)                   | 職種                                                     |
| validThrough(必須)            | 募集の締め切り                                           |
| applicantLocationRequirements | 従業員がリモートワークするために所在する必要のある地域 |
| baseSalary                    | 基本給                                                   |
| employmentType                | 雇用形態                                                 |
| identifier                    | 採用側組織の一意の識別子                                 |
| jobLocationType               | 勤務場所                                                 |

### 例

    <script type="application/ld+json">
    {
      "@context" : "https://schema.org/",
      "@type" : "JobPosting",
      "title" : "Software Engineer",
      "description" : "<p>Google aspires to be an organization that reflects the globally diverse audience that our products and technology serve. We believe that in addition to hiring the best talent, a diversity of perspectives, ideas and cultures leads to the creation of better products and services.</p>",
      "identifier": {
        "@type": "PropertyValue",
        "name": "MagsRUs Wheel Company",
        "value": "1234567"
      },
      "datePosted" : "2017-01-18",
      "validThrough" : "2017-03-18T00:00",
      "employmentType" : "CONTRACTOR",
      "hiringOrganization" : {
        "@type" : "Organization",
        "name" : "Google",
        "sameAs" : "http://www.google.com",
        "logo" : "http://www.example.com/images/logo.png"
      },
      "jobLocation": {
      "@type": "Place",
        "address": {
        "@type": "PostalAddress",
        "streetAddress": "1600 Amphitheatre Pkwy",
        "addressLocality": ", Mountain View",
        "addressRegion": "CA",
        "postalCode": "94043",
        "addressCountry": "US"
        }
      },
     "baseSalary": {
        "@type": "MonetaryAmount",
        "currency": "USD",
        "value": {
          "@type": "QuantitativeValue",
          "value": 40.00,
          "unitText": "HOUR"
        }
      }
    }
    </script>
