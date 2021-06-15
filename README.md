# Object detection

## Abstract

`object_detection` is a ROS node that provide an interface to detect object in an image using tensorflow. It takes as input:
  * A network file (`.pb`),
  * A label file (`.pbtxt`),
  * An input image topic,
  * An output object detection topic.

Each object is represented in the image by:
  * A score (float32) in the range [0, 1] that indicate the probability that this detection belongs to the given category,
  * A category (string),
  * A 2d bounding box in opencv image coordinate system.

Here is a small example for person detection.

![Example](https://github.com/bcrobo/object_detection/blob/main/doc/img/object_detection.gif)

## Further improvments

We could accelerate the detection pipeline by using a dedicated TPU such as Google Coral that would allow to develop a Kalman Filter to track the object.
