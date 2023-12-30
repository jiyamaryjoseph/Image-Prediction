#  Data Science Project: This marks my initial step into image prediction.
Reference : @codebasics

IMAGE CLASSIFICATION:
           

I'm excited to showcase my image classification project, influenced by a celebrity face recognition project. It aided me in recalling all the project components, such as the client, model, and UI. This project marks the beginning of my data science journey, and I'm eager to see where it takes me next.                  


![image](https://github.com/jiyamaryjoseph/Image-Prediction/assets/83010684/6ea792c5-7a24-4d7a-aab8-b9814ba6f088)

              
##               Model  
consists of:
                        
#####              : Dataset  (dont misunderstand me..I just took all the positive things of these confident personalities..I like them somehow or someway..let it be for my project..)
               1. Kalpana Chawla
               2. Micheal Obama
               3. Nita Ambani
               4. Opera Winfrey
               5. Priyanka Chopra
 source: google image (webscrapping with the help of fatkun-batch)
              
#####               :myrole_model_predic.ipynb
 This is the model for predicting the faces of my favourate rolemodels.After reading,changing to two diamention(i.e:from color to grey),detect the eyes and frontal face through cascadeclassifier.after detecting face and eyes,we cropped the image and make a folder in dataset and save.
      Then images go through wavelet transformation and combain the raw image and wavelet image  and keep it as X for training.And y is took as corresponding number of personality.. 
 On traing we took SVM for training by the method of gridsearching..we got 98% accuracy score.save this model as pickle file.
 
##              Server
consists of

####             :server.py
 This the server file for running the project..  Flask is a small and lightweight Python web framework that provides useful tools and features that make creating web applications in Python easier. It gives developers flexibility and is a more accessible framework for new developers since you can build a web application quickly using only a single Python file.
####             :utils.py
Whenever a common block of code needs to be used from multiple places, we can create utils class.Here we are doing classifying image..and loading artifacts..etc..     

#####             : wavelet.py
It another class specially for changing raw image into wavelet.
#####             : opencv
Haar Cascade is a machine learning-based approach where a lot of positive and negative images are used to train the classifier. Positive images – These images contain the images which we want our classifier to identify. Negative Images – Images of everything else, which do not contain the object we want to detect.The pretrained models are located in the data folder in the opencv.
#####             : artifacts
consists of pickle file and class dictionary.

##             UI
consists of
#####             :app.css
As you’ve seen, browsers render certain HTML elements with distinct styles (for example, headings are large and bold, paragraphs are followed by a blank line, and so forth). These styles are very basic and are primarily intended to help the reader understand the structure and meaning of the document.

To go beyond this simple structure-based rendering, you use Cascading Style Sheets (CSS). CSS is a stylesheet language that you use to define the visual presentation of an HTML document. You can use CSS to define simple things like the text color, size, and style (bold, italic, etc.), or complex things like page layout, gradients, opacity, and much more.It has the stylesheet of webpage.
#####             :app.html
The text in a typical web page is wrapped in HTML tags, which tell your browser about the structure of the document. With this information, the browser can decide how to display the information in a way that makes sense.
#####             :app.js
JavaScript is a scripting language that you can add to an HTML page to make it more interactive and convenient for the user. For example, you can write some JavaScript that will inspect the values typed in a form to make sure they are valid. Or, you can have JavaScript show or hide elements of a page depending on where the user clicks. JavaScript can even contact the web server to execute database changes without refreshing the current web page.


                    
                    
                    
                    
                    
                    
              
              
              


       

