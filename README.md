# UnityCarML-Agent

This is a released version of my thesis work. It is a custom environment, in which a car needs to
manoeuvre among obstacles to find the checkerboard patterned cube.

[![Demo](assets/unity_car_ml_agent.gif)]



## Training Environment

- The environment was developed using the Unity ML-Agents SDK.
- The agent was trained using the PPO (Proximal Policy Optimization) algorithm over several days in a multi-environment setup.

### Tech stack
- The Unity environment was developed with C#
- The PPO algorithm was develoepd with Python

### Episode Conditions

- The agent's objective is to locate the checkerboard-patterned cube. Successfully finding the cube provides positive feedback. The agent receives two types of input:
  - The red blinking raycast serves as a 1D distance sensor.
  - The black window represents an onboard camera that streams the processed image received by the agent. The image is filtered to highlight white regions and rectangular shapes.
- If the agent fails to find the cube within the allotted time, it receives negative feedback.
- If the agent collides with any object or a wall, it receives negative feedback.
- The agent is constrained to avoid unusual maneuvering, which also results in negative feedback.
- Any of the above conditions terminates the episode and restarts the simulation. The cube is placed at a random location at the start of each new episode.

    
- Go to the releases to download a video or the program.zip
- The program can be started with the Unity Environment.exe

2.     Download program.zip
3.     Unzip program.zip
4.     Start the Unity Environment.exe.
4.     Allow the app to use both private and public networks.
5.     Press and hold the left button of your mouse, so that you can adjust your view.
6.     Observe the car as it tries to find the checkerboard patterned cube.

