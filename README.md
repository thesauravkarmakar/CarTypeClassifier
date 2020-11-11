<p align="center">
  <img src="https://2.bp.blogspot.com/-ixZ569la3uY/VelYbxNTCyI/AAAAAAAAAnE/5-rSLNq5iPs/s1600/Your%2Bguide%2Bto%2Bhealthy%2Bliving.png"  width="512" height="256"/>
</p>

![](https://img.shields.io/badge/TensorFlow-1.14.0-%23FF6F00?style=plastic&logo=tensorflow)
![](https://img.shields.io/badge/Python-3.6.9-%233776AB?style=plastic&logo=python)

## :computer: Visit: https://cartypeclassifier.herokuapp.com/

# Table of Contents
- [About](#about)
- [Motivation](#motivation)
- [Dataset](#dataset)
- [Usage](#usage)

## About
We know that there are different types of Cars like Hatchback, Sedan, SUV,and so on. Here, I'm trying to classify only Sedan and SUV.

## Motivation
There are many challenges in Image Classfication, out of them I'm focusing on two challenges:
1. Intra-Class Variation
2. View-Point Variation

But,why?   
Because Car is _a super-class_ and there are different sub-classes under Car like Type, Make, Model, etc. I'm choosing only one "Type." Image Classification model can distinguish a Car and a Human, but to differentiate between a Sedan and an SUV is a little challenging. 
The second challenge I'm trying to solve is _View-Point Variation_ because the images could be shot in the dark or blurry; it can be clicked at different angles. So, to understand all the features and classify correctly, which is what without inputting full image, is what I want to solve.

## Dataset 
I have manually scrapped images from Google Images. There are total 100 images belonging to 2 classes _(50 in each)_ with various dimensions, as well as rotation. 

## Usage 
To run locally 
1. Clone the Repository.
```bash
    $ git clone https://github.com/thesauravkarmakar/CarTypeClassifier.git
 ```
2. Install dependencies 
```bash
    $ pip install -r requirements.txt
 ```
3. Edit app.py and change this part _(from line 35 to 37)_
```bash
    clApp = ClientApp()
    if __name__ == "__main__":
        app.run(port=8000, debug=True)
 ```	
 to 
 ```bash
    if __name__ == "__main__":
        clApp = ClientApp()
        app.run(host=0.0.0.0,port=8000, debug=True)
 ```	
 4. Run app.py
```bash
    $ python app.py
 ```
