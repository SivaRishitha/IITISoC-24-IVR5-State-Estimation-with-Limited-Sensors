# IITISoC-24-IVR5-State-Estimation-with-Limited-Sensors

## Goal:
To Implement a robust State Estimation algorithm that keeps computational efficiency in mind and could be deployed on NVIDIA Jetson Xavier Board or even a Raspberry Pi board.

People Involved : 

Mentors:
- [Arjun S Nair](https://github.com/arjun-593)
- [Soham Pandit](https://github.com/Scav6411)
- [Ampady B R](hgitttps://github.com/ampady06)

Members:
<br>
- [Inturi Siva Rishitha](https://github.com/SivaRishitha)
- [Varikuti Reethika Prasanna](https://github.com/Reethika1115)

  
# State-Estimation-with-Limited-Sensors

## Estimating State of an Autonomous Vehicle

In this project, we have estimated the state of our autonomous vehicle by fusing the data from the sensors IMU, GNSS reciever, and a LiDAR. These sensors provide measurements of varying reliability and at different rates. We have fused the data from these sensors using EXTENDED KALMAN FILTER(EKF). 

The KALMAN FILTER includes a motion model that tells us how the state evolves over time. It updates a state estimate through two stages:



- Prediction using the motion model.
- Correction using the measurement model.



EKF uses linearization to adapt the Kalman Filter to non linear systems.

 Linearization works by computing a local linear approximation to a non linear function about a chosen operating point. It relies on computing Jacobian matrices, which contain all the first order partial derivatives of a function.
 ![image alt](https://github.com/SivaRishitha/IITISoC-24-IVR5-State-Estimation-with-Limited-Sensors/blob/96a6fe895f0cd75679560f4cfb5a50b5650e198a/ekf%202.jpg) ![image alt](https://github.com/SivaRishitha/IITISoC-24-IVR5-State-Estimation-with-Limited-Sensors/blob/bc2d59ddabce6dab9268a22aacb298e7393e41b1/ekf%201.jpg)

