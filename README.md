# dronekit

DroneKit-Python helps you create powerful apps for UAVs.

⚠️ ATTENTION: MAINTAINERS NEEDED ⚠️
Hey it's true this project is not very active, but it could be with your help. We are looking for maintainers interested in keeping the project alive by keep up with CI and PRs. If you are interested in helping please apply by creating an issue and listing the reasons why you would like to help, in return we will be granting committer access to folks who are truly interested in helping.

Overview
DroneKit-Python (formerly DroneAPI-Python) contains the python language implementation of DroneKit.

The API allows developers to create Python apps that communicate with vehicles over MAVLink. It provides programmatic access to a connected vehicle's telemetry, state and parameter information, and enables both mission management and direct control over vehicle movement and operations.

The API is primarily intended for use in onboard companion computers (to support advanced use cases including computer vision, path planning, 3D modelling etc). It can also be used for ground station apps, communicating with vehicles over a higher latency RF-link.

Getting Started
The Quick Start guide explains how to set up DroneKit on each of the supported platforms (Linux, Mac OSX, Windows) and how to write a script to connect to a vehicle (real or simulated).

A basic script looks like this:

from dronekit import connect

# Connect to UDP endpoint.
vehicle = connect('127.0.0.1:14550', wait_ready=True)
# Use returned Vehicle object to query device state - e.g. to get the mode:
print("Mode: %s" % vehicle.mode.name)
Once you've got DroneKit set up, the guide explains how to perform operations like taking off and flying the vehicle. You can also try out most of the tasks by running the examples.

Resources
The project documentation is available at https://readthedocs.org/projects/dronekit-python/. This includes guide, example and API Reference material.

The example source code is hosted here on Github as sub-folders of /dronekit-python/examples.

The DroneKit Forums are the best place to ask for technical support on how to use the library. You can also check out our Gitter channel though we prefer posts on the forums where possible.

Documentation: https://dronekit-python.readthedocs.io/en/latest/about/index.html
Guides: [https://dronekit-python.readthedocs.io/en/latest/guide/index.html)
API Reference: [https://dronekit-python.readthedocs.io/en/latest/automodule.html)
Examples: /dronekit-python/examples
Forums: http://discuss.dronekit.io/
Gitter: https://gitter.im/dronekit/dronekit-python though we prefer posts on the forums where possible.
Users and contributors wanted!
We'd love your feedback and suggestions about this API and are eager to evolve it to meet your needs, please feel free to create an issue to report bugs or feature requests.

If you've created some awesome software that uses this project, let us know on the forums here!

If you want to contribute, see our Contributing guidelines, we welcome all types of contributions but mostly contributions that would help us shrink our issues list.

Licence
DroneKit-Python is made available under the permissive open source Apache 2.0 License.
