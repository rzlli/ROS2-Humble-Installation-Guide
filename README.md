# Installation Report: Linux Ubuntu and ROS 2 Humble

## 1. Installation Steps
The working environment and ROS 2 Humble were successfully set up on Ubuntu 22.04 LTS by following these steps:

1. Configuring Repositories:
   - Updated system packages and ensured repository access.
   - Added the official Open Robotics repository for ROS 2.

2. Adding the GPG Key:
   - Imported the authorized repository key to ensure package security and verification using the command:
         sudo apt-key adv --keyserver keyserver.ubuntu.com --recv-keys F42ED6FBAB17C654
     
3. Updating the System and Installing ROS 2:
   - Updated the package list using: 
         sudo apt update
        - Installed the full desktop version of ROS 2 via:
         sudo apt install ros-humble-desktop -y
     
4. Environment Setup:
   - Activated the ROS 2 workspace environment in the terminal using:
         source /opt/ros/humble/setup.bash
     
---

## 2. Challenges Encountered and Troubleshooting

* Initial Issue (Missing Key Error - NO_PUBKEY):
  - Description: While running sudo apt update, an error occurred stating that the public key was not available (`NO_PUBKEY F42ED6FBAB17C654`).
  - Cause: The repository key was not properly downloaded initially due to terminal line wrapping or server timeout.
  - Solution: Successfully fetched and imported the key directly from the official Ubuntu keyserver using the command:
       sudo apt-key adv --keyserver keyserver.ubuntu.com --recv-keys F42ED6FBAB17C654
        Afterwards, ran sudo apt update successfully to proceed with the installation.
