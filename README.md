# ROBOTICS HACKATHON (jan 2023) - Line Follower
Ten hours line follower hackathon as part of the final project for Introduction In Robotics 3rd year course.
### Task: The robot must follow the linie as accurate as possible in order to finish the track. The robot has 3 tries to get the best time.

<details>
<summary> <h2>Electronic setup :electric_plug:</h2> </summary>
<br>

### Components list
![image](https://user-images.githubusercontent.com/96074975/212561004-faaa97f3-109b-4f6d-b739-f99f38cf0c95.png)

      1.Arduino Uno
      2.Zip-ties
      3.Power source - LiPo battery
      4.2 Wheels
      5.Wires set for the line sensor (female - male)
      6.QTR-8A reflectance sensor, along with screws
      7.Ball caster
      8.Extra wires from the rest of components (male - male)
      9.3D printed Chassis
      10.Breadboard - medium (400pts)
      11.L293D motor driver
      12.2 DC motors

### Driver Connection table

![image](https://user-images.githubusercontent.com/96074975/212561232-9d6eca06-67b3-482b-acb4-5dcb3b32a5fd.png)


![image](https://user-images.githubusercontent.com/96074975/212561191-978ec6ae-f99f-4c5c-b6c9-7873e568f8b0.png)

### Motors and Sensor Connection scheme

![image](https://user-images.githubusercontent.com/96074975/212561261-3b9fd04a-e0c5-4bee-8ba6-5a4bf120d826.png)

</details>

<details>
<summary> <h2>Code details :computer:</h2> </summary>
<br>
<details>
<summary> <h3>PID</h3> </summary>

First it is better to start by changing just kp value. 

      Increase the value if the robot can not do a turn;
      
      Decrease the value if the robot do not follow the line becouse of overshooting

After finding a resonable kp value, next step is to change kd value by

      Increasing till the robot doesn't wobble to much and also takes better turns.

The final values for PID control

      float kp = 140; 
      float ki = 0;
      float kd = 180; 
 
 Other tries
 
      BEST CASES
      //Case 1:  follow the linie roughly, slow
      baseSpeed = 150;
      
      float kp = 5; 
      float ki = 0;
      float kd = 0;
      
      //Case 2:  follow the linie roughly, slow
      baseSpeed = 170;
      
      float kp = 7; 
      float ki = 0;
      float kd = 2;
      
      WORST CASES
      //Case 3:  not follow the linie
      baseSpeed = 160;
      
      float kp = 6; 
      float ki = 0;
      float kd = 0;

      //Case 4:  not follow the linie
      baseSpeed = 200;
      
      float kp = 5; 
      float ki = 0;
      float kd = 1;
      
      //Case 5:  not follow the linie
      baseSpeed = 160;
      
      float kp = 5; 
      float ki = 0;
      float kd = 0;
 </details>
 
 <details>
 <summary> <h3>Calibration(with millis)</h3> </summary>
 
       For CALIBRATION it is used autoCalibrate function where the robot moves left and right
       in order to understand the difference between black and white. 
 
 He first goes to the right, then to the left and so on.
 
 Calibration covers all sensors.
 
 - For the right move, the robot will have the following motor speeds:
      
      - right motor: -200
            
      - left motor: 200
      
 - For the left move, the robot will have the following motor speeds:
 
      - right motor: 250
      
      - left motor: -250
     
 These values were chosen after several attempts.
</details>

</details>

### :trophy: Best time: 48'
### :movie_camera: Watch the robot on the circuit in the final round: [youtube video here](https://youtu.be/fTuI3Zrmzfs)

### Final track
<img src="https://user-images.githubusercontent.com/96074975/212561679-ebe6544f-be2a-4667-8337-a04b82a55766.png" width=50% height=50%> 



### Setup

1.
<img src="https://user-images.githubusercontent.com/96074975/212561374-39e04df3-fe72-49c7-b00a-035a95a30332.png" width=50% height=50%> 

2.
<img src="https://user-images.githubusercontent.com/96074975/212561476-f946fbb6-c66c-4be6-bcd3-9b1fe347ee18.png" width=50% height=50%> 
