### Mission-driven to maximize decision intelligence.

#### Army Career &#10230;&#10230;&#10230;&#10230;&#10230;&#10230;&#10230;&#10230;&#10230;&#10230;&#10230;&#10230; More Recently

<img src="Wordclouds_Combined.png" alt="Work Experience Wordclouds" width="685" height="241" style="vertical-align: middle;"/>

<details>
  <summary>Wordcloud code</summary>  
  <pre style="white-space: pre-wrap;"><code>
&#35; Import necessary libraries/modules      
import textract
from nltk.corpus import stopwords
from nltk.tokenize import word_tokenize, sent_tokenize
import re
from wordcloud import WordCloud<br><br>

&#35; Extract text from the document
text = textract.process('/Users/chris/Desktop/Army.docx')

&#35; Filter out character codewords
cleaned_text = re.sub(r'\\(n|xe2|x80|x99)', '', str(text))

&#35; Tokenize the words in the text
tokens = word_tokenize(cleaned_text)

&#35; Tokenizing the sentences in the text
sentences = sent_tokenize(cleaned_text)

&#35; Remove stopwords and create 'filtered_tokens' variable
stop_words = set(stopwords.words('english'))
filtered_tokens = [word for word in tokens if word not in stop_words]

&#35; Create wordcloud with filtered tokens
wordcloud = WordCloud(width=1400, height=1000).generate(' '.join(filtered_tokens))
plt.imshow(wordcloud, interpolation='bilinear')
plt.axis('off')
plt.show()
for i in range(10):
    print(i)
  </code></pre>
</details>


<table style="border-collapse: collapse; border-spacing: 0; margin: 0; padding: 0;">
  <tr style="margin: 0; padding: 0;">
    <td style="margin: 0; padding: 0; border: none; align: left;">
      <img src="https://github.com/chrisaguirre3/chrisaguirre3/blob/main/tm_cm_gb_profile.png" alt="Hobbies Treemap and Confusion Matrix" width="685" height="241" style="width:4000px;margin: 0; padding: 0; display: block;"/>
    </td>
    <td style="vertical-align: top; margin: 0; padding: 0;">
      Welcome!<br><br> I predicted you'd be visiting today.<br><br>
      Looks like my Accuracy, Recall, Precision, and F1 scores are all at <strong>100%!</strong>
    </td>
  </tr>
</table>

<table>
  <tr>
    <td style="padding-right: 20px;"> <!-- Add padding to create space -->
      Open to collaboration on data science / data analysis projects.
    </td>
    <td>
      <a href="mailto:christophermiguelaguirre@gmail.com">
    <img src="gmail_hero.jpg" alt="Gmail" width="30" height="30" style="vertical-align: bottom; margin: 20px;"/>
 </a><a href="https://www.linkedin.com/in/christopher-aguirre7/">
    <img src="linkedin_logo2.jpg" alt="LinkedIn" width="30" height="30" style="vertical-align: bottom;"/>
</a>
    </td>
  </tr>
</table>


<!---
chrisaguirre3/chrisaguirre3 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
