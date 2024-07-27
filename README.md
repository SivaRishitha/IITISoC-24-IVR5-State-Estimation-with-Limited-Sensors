# IITISoC-24-IVR5-State-Estimation-with-Limited-Sensors

## Goal:
To Implement a robust State Estimation algorithm that keeps computational efficiency in mind and could be deployed on NVIDIA Jetson Xavier Board or even a Raspberry Pi board.

People Involved : 

Mentors:
- [Arjun S Nair](https://github.com/arjun-593)
- [Soham Pandit](https://github.com/Scav6411)
- [Ampady B R](https://github.com/ampady06)

Members:
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

 
## Test 1: normal case

First of all, testing the performance of the estimation with normal sensor measurements. The model is able to provide accurate estimate within error range.
## Test 2: wrong extrinsic calibration

In orfer to test out the reliability of the state estimation, an intentional error is applied on the rotational matrix when transforming the reference frame of the LIDAR, resulting unreliable LIDAR measurements. By increasing the variance of the LIDAR estimated error, the model adapts and still performs well.



## Test 3: sensor measurement dropout

A portion of the GNSS and LIDAR data is intentionally erased to test the performance of the estimation when only IMU is available. (like vehicle entering a tunnel)
Although there exists a small shift in height estimation due to the wrong estimation of pitch angle, the model quickly adjusted state estimation of pitch angle and can perform as expected within a reasonable time and error range.

## Reference:


https://github.com/Vinohith/Self_Driving_Car_specializations
