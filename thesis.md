
# Argus
https://docs.nvidia.com/jetson/l4t-multimedia/group__LibargusAPI.html

Argus is a camera API that's developed by Nvidia. Argus runs only on Nvidia
hardware, such as the Jetson Orin Nano Developer Kit. This device is what will
be used in experiments and measurements for this thesis.

Argus is roughly based on V4L2 though effectively a re-implementation. At the
time Argus was created, V4L2 was still in an early stage. It di not supporting
a variety of features such as multicamera setups etc. hence Argus was created
in order to add the missing features easily. These days V4L2 and Argus are very
close though in later chapters we'll give an overview of what pros and cons
each has.

# libcamera
libcamera is an open-source (with binary blobs for some cameras) C++ embedded
camera framework that supports a large number of complex cameras such as the
IMX 219, 477 and many more. It supports multiple encoders to receive images in
for example PNGs/raw images.The primary target for libcamera is Arm processors
in the form of Raspberry PI's, Chrome OS and Android though many other
architectures are also supported.

Before libcamera, the way to use camera sensors was very complex, often
requiring it's own MCU. libcamera moved this almost completely to userspace,
trivializing many applications. libcamera supports a variety of Image Processing
Algorithms (IPA's) for 3A (Auto focus, Auto exposure, Auto white balancing). Camera
configuration is done using V4L2, libcamera being essentially an extension for
it.

# HAL 3
Hardware Abstraction Layer 3 (HAL3) is probably the most well known one that
will be discussed in this thesis. It's included in each Android phone, it has
remarkable features for a mobile phone camera. Both libcamera and Argus are
based around HAL3. It was created to bridge the gap between the higher level
the API camera2 and the lower level hardware API's. It allows for more
modification than camera2, while requiring more work to manage.


