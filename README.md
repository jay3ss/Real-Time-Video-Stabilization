# Real-Time-Video-Stabilization

This is a basic implementation of a real time video stabilization algorithm based on Lakshya Kejriwal's paper: <br>
http://www.sciencedirect.com/science/article/pii/S1877050916314624

### Prerequisites

The code requires the following 3rd Party Libraries

- opencv-2.4.9
- CMake


### How to Run

- Clone the repository `git clone https://github.com/jay3ss/Real-Time-Video-Stabilization`
- Create a `build` folder: `mkdir build && cd build`
- Compile: 
    1. `cmake ..`
    2. `make`
- Change the parameters of Kalman Filter in `videostab.cpp`. (optional)
- Run the program (you have two options)
    1. Use `stabilize_video <filename>`
    2. Use `main` which will use your webcam


### License

- For academic and non-commercial purposes only

