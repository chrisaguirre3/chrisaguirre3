# Mission-driven to maximize decision intelligence.

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

#### <span style="color: #F0EAD6;">&nbsp;&nbsp; Army Career &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; More Recently</span>

<img src="wordclouds_v2.png" alt="Work Experience Wordclouds" width="685" height="330" style="vertical-align: middle;"/>

<table>
  <tr>
    <!-- First Code Dropdown -->
    <td>
      <details>
        <summary>Wordcloud code</summary>
        <pre><code>
          
&#35; Import necessary libraries/modules      
import textract
from nltk.corpus import stopwords
from nltk.tokenize import word_tokenize, sent_tokenize
import re
from wordcloud import WordCloud
          
&#35; Extract text from the document
text = textract.process('/Users/chris/Desktop/Army.docx')

&#35; Filter out character codewords
cleaned_text = re.sub(r'\\(n|xe2|x80|x99|t|xc2)', '', str(text))

&#35; Tokenize the words in the text
tokens = word_tokenize(cleaned_text)

&#35; Tokenizing the sentences in the text
sentences = sent_tokenize(cleaned_text)

&#35; Remove stopwords and create 'filtered_tokens' variable
stop_words = set(stopwords.words('english'))
filtered_tokens = [word for word in tokens if word not in stop_words]

&#35; Create wordcloud with filtered tokens
fig, ax = plt.subplots()
fig.patch.set_facecolor('black')

wordcloud = WordCloud(width=1400, height=1000).generate(' '.join(filtered_tokens))
plt.imshow(wordcloud, interpolation='bilinear')
plt.axis('off')
plt.show()
        </code></pre>
      </details>
    </td>
    
  <td>
      <details>
        <summary>Tree Map/Confusion Matrix code</summary>
        <pre style="white-space: pre-wrap;"><code>
          
&#35; Import necessary libraries/modules 
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
import squarify

&#35; Plot hobbies treemap
categories = ['Piano', 'Hiking in the Mountains', 'Snowboarding', 'Tennis','CrossFit',
              'AI Generated Art','Learning New Skills','Going on Adventures!']
sizes = [20, 20, 10, 10, 20, 5, 15, 15] 
colors = ['#dfe318', '#2db27d', '#38598c', '#0b101b']

&#35; Create a figure and a set of subplots
fig, ax = plt.subplots(figsize=(12, 8))

&#35; Set the background color of the axes and the figure
ax.set_facecolor('#1e2327')  # for the axes
fig.patch.set_facecolor('#1e2327')  # for the figure background

squarify.plot(sizes=sizes, label=categories, color=colors, alpha=0.7, pad=0.01, ax=ax)

plt.title('Some of my Hobbies',fontweight='bold',fontsize=20, color='#F0EAD6')
plt.axis('off')  # Disable the axis

&#35; Adjust label formatting
for i, label in enumerate(plt.gca().texts):
    label.set_fontsize(13.5)  
    label.set_weight('bold')
    if categories[i] == 'Going on Adventures!':  
        label.set_rotation(90)
        label.set_color('#2db27d')
    if categories[i] == 'Tennis': 
        label.set_color('#2db27d') 

plt.show()

&#35; Create list of predictions and transform into 2x2 numpy array
predictions_list = [0,0,0,1]
predictions_matrix = np.array(predictions_list).reshape(2,2)

&#35; Change background color
fig, ax = plt.subplots(figsize=(5,4))
fig.patch.set_facecolor('#1e2327')
ax.set_facecolor('#1e2327')
    
&#35; Plot confusion matrix using seaborn heatmap
plt.figure(figsize=(5,4))
ax = sns.heatmap(predictions_matrix, vmin=0, vmax=1, annot=True, 
                    cmap = sns.color_palette("mako", as_cmap=True), fmt='g')
plt.title('Confusion Matrix', fontsize=16, fontweight='bold', color='#F0EAD6')
plt.xlabel('Predicted Label', color='#F0EAD6')
plt.ylabel('True Label', color='#F0EAD6')
ax.tick_params(axis='both', colors='#F0EAD6')

&#35; Access the color bar
cbar = ax.collections[0].colorbar

&#35; Change the color of the color bar's tick labels
cbar.ax.yaxis.set_tick_params(color='#F0EAD6')  # Change tick label colors
plt.setp(plt.getp(cbar.ax.axes, 'yticklabels'), color='#F0EAD6') # Change tick text colors
    
plt.show()
        </code></pre>
      </details>
    </td>
  </tr>
</table>

<table style="border-collapse: collapse; border-spacing: 0; margin: 0; padding: 0;">
  <tr style="margin: 0; padding: 0;">
    <td style="margin: 0; padding: 0; border: none; align: left;">
      <img src="https://github.com/chrisaguirre3/chrisaguirre3/blob/main/tm_cm_v2.png" alt="Hobbies Treemap and Confusion Matrix" width="685" height="241" style="width:4000px;margin: 0; padding: 0; display: block;"/>
    </td>
    <td style="vertical-align: top; margin: 0; padding: 0;">
      Welcome!<br><br> I predicted you'd be visiting today.<br><br>
      Looks like my Accuracy, Recall, Precision, and F1 scores are all at <strong>100%!</strong>
    </td>
  </tr>
</table>


<!---
chrisaguirre3/chrisaguirre3 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
