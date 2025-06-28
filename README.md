# Cruise-Controller-using-PID-on-Matlab
A simple cruise control system with PID controller; design done in Simulink.

The cruise control system design is for a Compact Sedan (system parameters for modelling such as weight of the car, dimensions, drag coefficient, rolling resistance, max torque and so on has been for a Honda City 1.5L)

System is first-order mass damper model, the modeling has been done in simulink in both discrete and continuous modes, with and without a PID controller. The tuning of the PID parameters has been done using the matlab pid tuner tool. The system objective was to maintain the speed of the car at 100 km/h (27.78 m/s). System stability was checked by applying disturbance similar to that of a car running from a plain road to an inclined terrain. Rise time is designed to be less than 12 seconds, as the car in modelling (honda city 1.5l) can do 0-100km/h in 10.8 seconds.

## Simulink model for the controller and plant are as follows :
- `cruise_model_open_loop.slx` – Open loop system in s-domain  
- `cruise_model.slx` – Closed loop system with PID controller in s-domain  
- `cruise_open_loop_discrete.slx` – Open loop system in z-domain  
- `cruise_discrete.slx` – Closed loop system with PID controller in z-domain

## Matlab file for analysis :
- `system_analyis.m` – Contains system parameters and response analysis  
- `discrete_transfer_function_analysis.m` – Performs system transfer function analysis

## Mathematical Model and parameters :
![image](https://github.com/user-attachments/assets/85945e5b-a0f1-485e-8ba6-ee078e3c6552)

## First Order mass damper model :
![image](https://github.com/user-attachments/assets/d6a2ba5b-1b74-4055-8f9b-8259dedb1664)

## Contol systems model :
![image](https://github.com/user-attachments/assets/cbf9da40-c1bd-4743-92d9-02f631d55fc6)


## Results from the simulation can be found in the `Results` folder.
