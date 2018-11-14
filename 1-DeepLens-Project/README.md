# Create and deploy DeepLens object detection project

In this lab your will create and deploy object detection project on DeepLens.

## Create DeepLens Project

1. Using your browser, open the AWS DeepLens console at https://console.aws.amazon.com/deeplens/.
2. Choose Projects, then choose Create new project.
3. On the Choose project type screen
  - Choose Use a project template, then choose Object detection.
  - Scroll to the bottom of the screen, then choose Next.
4. On the Specify project details screen
   - In the Project information section:
      - Project name: Object-Detection
      - Description: Detect persons not wearing safety hats.
  - Scroll to the bottom of the screen, then click Create.

This returns you to the Projects screen where the project you just created is listed with your other projects.

## Deploy DeepLens Project

Next you will deploy the Object Detection project you just created.

1. From Deeplens console, On the Projects screen, choose the radio button to the left of your project name, then choose Deploy to device.

2. On the Target device screen, from the list of AWS DeepLens devices, choose the radio button to the left of the device where you want to deploy this project.

3. Choose Review.

   This will take you to the Review and deploy screen.

   If a project is already deployed to the device, you will see a warning message
   "There is an existing project on this device. Do you want to replace it?
   If you Deploy, AWS DeepLens will remove the current project before deploying the new project."

4. On the Review and deploy screen, review your project and click Deploy to deploy the project.

   This will take you to to device screen, which shows the progress of your project deployment.

## Viewing a Device Stream on Your AWS DeepLens Device

To view an unprocessed device stream on your AWS DeepLens device, start your terminal and run the following command:

- mplayer -demuxer lavf /opt/awscam/out/ch1_out.h264

To stop viewing the video stream and end your terminal session, press Ctrl+C.

## Viewing a Project Stream on Your AWS DeepLens Device
To view a project stream on your AWS DeepLens device, start your terminal and run the following command:

- mplayer -demuxer lavf -lavfdopts format=mjpeg:probesize=32 /tmp/results.mjpeg

To stop viewing the video stream and end your terminal session, press Ctrl+C.
