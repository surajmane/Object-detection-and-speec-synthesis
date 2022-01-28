# Object-detection-and-speech-synthesis
A project to detect objects in a given image and have the system speak those results out for the user.
Given an image, we run object detection module using YOLO trained on COCO dataset in the backend and detect and return all those objects in the form of a CSV. This CSV contains output like anchor points, x and y coordinates, area occupied by that object, etc.
This CSV is then imported to Observable where most important functions work. We provide user the choices to see or listen to the object in the following 4 ways:
  1. By relevance - If the user wants to see objects that are most relevant.
  2. By order - See the objects in a order, in which they were detected.
  3. By Uniqueness - Images could be cluttered with a lot of objects, that too similar kind, here we provide a list of distinct objects detected in the scene.
  4. By Count - This gives count of each objects in the image.
This all is then given to a speech Utterance API which converts the text to speech and the user, if with impaired vision, could hear the results.

There are two modules, first which detects the objects and returns a CSV, the second is the Observable part which basically is our front end of the project with certain interactivity.
