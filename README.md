# A-Generative-Method-for-Producing-Distractors-for-Cloze-Questions

# API url:
http://173.48.132.117:8633/api/question-generation

# Post data structure:


```javascript
data={
      'key': a timestamp string, 
      'text':content_html_text_data,
      'question_type': ['cloze'] }
```
each sentence used for generate cloze question should be labled with <p></p>
# Returned data structure:


```javascript
result={
      'key': a timestamp string, 
      'data': a list of questions, each element is a dict
      }
```

# cloze question structure
 # cloze: 
            {"type": "cloze",
             "question":[{"answer":"this is right answer",
                          "options":["option one", "option two", "option three"],
                          "question_id": "0"},
                        
                         {"answer":"this is right answer",
                          "options":["option one", "option two", "option three"],
                          "question_id": "1"},
                          
 	                     {"answer":"this is right answer",
                          "options":["option one", "option two", "option three"],
                          "question_id": "2"}],
             "html":"
                    <p>
                        <span>
                            Church-key
                            <span question_id="0"></span>
                            pitchfork knausgaard, meh fashion 
                            <span question_id="1"></span>
                            kale chips organic meditation enamel pin tilde kogi.
                        </span>
                        <span>
                            Paleo forage yr glossier pug
                            <span question_id="1"></span>
                            photo booth locavore waistcoat 8-bit roof party activated charcoal.
                        </span>
                    </p>
                    <p>
                        <span>
                            Truffaut DIY
                            <span question_id="2"></span>
                            charcoal enamel pin freegan hella flexitarian knausgaard pug.
                        </span>
                    </p>"
            }
