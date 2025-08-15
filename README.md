# Minjun-s-Garbage-Classification-Model
This garbage classification model is an AI made with Resnet34 that detects different types of garbage (trash, battery, plastic, metal, etc.).It is meant to help people find out what they can recycle and what they can’t. It is built to run on the Jetson Orin Nano but can run on many modern systems or mini computers built for AI such as the Jetson Developer Kits. You must be using linux or be using a VM that has linux for this to work. 

Instructions:
    You have to download all of the files. Then, you can run the command "python3 -m http.server" without the quotation marks in your terminal. Afterwards, visit http://localhost:8000 on your browser (Google Chrome is prefered but most browsers will most likely work!). Lastly, import an image of your trash and the AI will classify it.


Progress Report:
    *1 An epoch can be described as a round of training, where it trains an AI model on a dataset, recording the accuracy and improving the AI every “round.”
(I wasn’t able to take consistent measurements due to having to have breaks such as meals and sleep which made it impossible for me to take measurements every 10 or so epochs. A total of 75 epochs were run.)

After 10 epochs of training, the accuracy achieved was: 52.75%
After 15 epochs of training, the accuracy achieved was: 54.57%
After 35 epochs of training, the accuracy achieved was: 74.99%
After 50 epochs of training, the accuracy achieved was: 81.32%
After 75 epochs of training, the accuracy achieved was: 85.59%


How I made it:
    To make this classification model, I combined two datasets I found at Kaggle, and used them to run a training program in python called train.py that used the Resnet34 CNN via Pytorch and Torchvision that would train them on all of the images in my dataset. Then, I would export my model into a file called resnet34.onnx. Afterward, with the help of some AI for fixing bugs and classmates to help with my code, I made an HTML file that would allow me to run my model with a frontend so it would run on a webpage. Now, using a file (labels.txt), the model can now label each image imported into the webpage and show how confident it is in which type of garbage it is! Enjoy! :D

Deeper Explanation:
https://youtu.be/JjSOKV4HNyQ
