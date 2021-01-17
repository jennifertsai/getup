# STAMP
## Inspiration
Physical inactivity has been a crisis persisting since 2012, with approximately 3.2 million deaths attributed to this unhealthy lifestyle behavior per year (source: WHO). The rapidly escalating COVID-19 pandemic has only made this matter worse; with the new digital world, people have become more and more sedentary, creating negative implications to our health, focus, and productivity.

This, along with the COVID-19 restrictions on international travel, inspired us to create a fun and interactive app that will remind people to take breaks away from the screen, while being able to explore different countries around the world.

With this problem space, we identified two separate systems that directly influenced the ideas of our product: remote learning/work and international tourism. After some user research, we determined that a major issue with remote work is that it has caused a blurred line between work and rest time; thus, breaks would be most effective when spent away from the work environment and screen. With travel, people enjoy being able to learn about new cultures and getting away from their home.

Although two different contexts, “getting away” is a common theme here. Being attached to one environment for too long isn’t the best for our personal health and development. We need change, activity, and exploration. Which is why we created Stamp.

## What it does
Stamp is a web application inspired by “Don’t Touch Your Face”, built with a customizable timer system to keep track of work and break time. Once work time is elapsed, the app will notify the user to get up and away from the screen, which is monitored using a webcam facial recognition integration. Until no face is detected, the app will continue to make sounds.

During the break, the user is encouraged to go on a walk and take a “trip around the world”. When the break ends, a postcard from a different country will pop up indicating which country the user has arrived at. The post card contains fun facts about the country, and with each successful work/break sequence, a stamp from the country will be added to their collection. The goal is to collect as many stamps as possible while learning about different cultures!

## How we built it
Frontend and design: we used Figma to create our app’s overall theme and wireframe mockups of the different screens. We then implemented this design, along with timers, buttons, and pop-up functionalities with JavaScript and HTML/CSS.

Backend: first, we utilized a facial recognition software by calling the OpenCV and Face-Recognition libraries in Python to allow us to have a direct feed from the user’s webcam. The computer vision software identifies and maps the user’s face one frame at a time, detecting if one’s face is in the camera view or not. The OpenCV library was essential in accessing the webcam and enabled visual mapping of the user’s face. The Face-Recognition library was necessary for the actual face detection. Next, we used HTML to link the software to the flask application, allowing us to connect the computer vision software to the front-end development. The back-end software would detect the presence of a face and return a JSON value to the flask application, allowing it to be used in the web application. The flask application would then be deployed via Google Cloud.

## Challenges we ran into
We faced many challenges in connecting the front end and back end components. While we had both separate pieces working, there were a few inconsistencies with the output of the Flask application.

Along with that, we had a few problems with deployment. Docker didn’t allow for web cameras to run, so we had to eventually abandon it. We then switched to Google Cloud, which had issues with the compiler.

## What we learned
We learned that the most difficult part about developing software is making it accessible for all users - while it worked on one of our local machines, it didn’t work for another person’s. This is because there are a lot of dependencies associated with each software, and we needed to ensure that we had all that was necessary for the program to run.

Overall, our team learned a lot about a variety of technologies. It was our first time doing a lot of things, like connecting the frontend and backend and deploying. We had to debug and problem-solve as we went, and sometimes there were roadblocks where we had to just abandon the plan and go with another route.
