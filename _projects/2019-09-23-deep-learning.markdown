---
layout: project
title:  "Deep Learning Level Generation"
date:   2019-05-02 13:44:00
author: Alex Stroud
categories:
- project
img: BuildingGeneratorThumbnail.png
thumb: BuildingGeneratorThumbnail.png
carousel:
- DeepLearning1.png
- DeepLearning2.png
- DeepLearning3.png
- DeepLearning4.png
tagged: C++, Programming, Development

---

#### Deep Learning Level Generation

This project was the final of three tasks under the "Advanced Technologies" module during year three of my degree. The task was to use deep learning and Python to train a model using satellite imagery in order to produce 'realistic' game levels.


#### Project Summary

This task resulted in a Python file that was used to train a model using deep learning on a large number of satellite image tiles. The data was gathered through a group effort of saving multiple areas of map data, and splitting each image into individual 50x50 pixel tiles. Once the group had collectively gathered all the tile data and separated the different types of environment into different folders, this information could be fed into the Python program.

After the program had ran the training dataset, another file was used for producing a model that would test a previously unused map area and run it against the trained dataset. As the evaluation data is tested, it writes to a text file and guesses what type of environment is represented by each tile. This information is then used inside a Unity project that reads in from the text file.

The Unity project then uses prefabs to assign to each different type of environment, in order to create a semi-realistic representation of the satellite data image.

To read about this project further, please follow the link below to find the project report and also take a look at the short showreel video for all of the projects within this module.


#### Report Download Link
[![Open World Report Download](https://i.gyazo.com/e3c24f39b688d6e4bff152deaeeaedd1.png)](https://drive.google.com/open?id=1A5f1Wtz4nCcDa7yuIf4Hph_E3RayPSjL "Deep Learning Report PDF")

#### Deep Learning Level Generation Demonstration Video: Youtube
<iframe width="560" height="315" src="https://www.youtube.com/embed/YU6iP-LFMeE" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

#### Advanced Technologies - Showreel Video: Youtube
<iframe width="560" height="315" src="https://www.youtube.com/embed/dm-c4ovVGrQ" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
