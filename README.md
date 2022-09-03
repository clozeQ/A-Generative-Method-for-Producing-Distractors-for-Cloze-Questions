# A-Generative-Method-for-Producing-Distractors-for-Cloze-Questions

# Web API for generating distractors:
URL: http://wangserver.ddns.net:8633/api/question-generation

# Example post request:


```javascript
data={
      'key': any timestamp string, 
      'text':"<p>Virchow was the first scientist to discover that leukiemia is caused by rapid production of abnormal white blood cells.</p>",
      'question_type': ['cloze'] }
Each sentence used for generate cloze question should be labled with "<p></p>" tag
```

# Returned data structure:


```javascript
result={
      'key': a timestamp string, 
      'data': a list of questions, each element is a dict.
      }
```

# Data structure of cloze question

      {"type": "cloze",
       "question":[{"answer":"abnormal white blood cells",
                    "options":["healthy white blood cells", "immature neurons", "useless tissues"],
                    "question_id": "0"}
                    ],
       "html": "<p>
                  Virchow was the first scientist to discover that leukiemia is caused by rapid production of <span question_id="0">abnormal white blood cells</span>.
               </p>"
      }
