# A-Generative-Method-for-Producing-Distractors-for-Cloze-Questions

# Post data structure:


```javascript
data={
      'key': a timestamp string, 
      'text':content_html_text_data,
      'question_type': ['cloze'] }
```
# Returned data structure:


```javascript
result={
      'key': a timestamp string, 
      'data': a list of questions, each element is a dict
      }
```
# API url:
http://173.48.132.117:8633/api/question-generation
