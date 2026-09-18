# EXPT-6-Simulation-of-Multirate-DSP-using-Decimation-and-Interpolation

# AIM: 

# To perform and verify Multirate-DSP-using-Decimation-and-Interpolation.

# APPARATUS REQUIRED: 
PC installed with SCILAB. 

# PROGRAM: 
clear;
clc;
close;

// Generate the original signal
n = 0:%pi/50:2*%pi;
x = sin(%pi * n);

// Input factors
M = input("Enter the Downsampling Factor (M): ");
L = input("Enter the Upsampling Factor (L): ");

//-------------------------
// Downsampling
//-------------------------
downsampling_x = x(1:M:length(x));

disp(x, "Input Signal x(n) = ");
disp(downsampling_x, "Downsampled Signal = ");

// Plot Original and Downsampled Signals
figure(1);

subplot(2,1,1);
plot2d3(1:length(x), x);
xtitle("Original Signal");

subplot(2,1,2);
plot2d3(1:length(downsampling_x), downsampling_x);
xtitle("Downsampled Signal by a Factor of M");

//-------------------------
// Upsampling
//-------------------------
upsampling_x = zeros(1, L * length(x));

for i = 1:length(x)
    upsampling_x(1, L*i) = x(i);
end

disp(x, "Input Signal x(n) = ");
disp(upsampling_x, "Upsampled Signal = ");

// Plot Original and Upsampled Signals
figure(2);

subplot(2,1,1);
plot2d3(1:length(x), x);
xtitle("Original Signal");

subplot(2,1,2);
plot2d3(1:length(upsampling_x), upsampling_x);
xtitle("Upsampled Signal by a Factor of L");


# OUTPUT: 
<img width="768" height="592" alt="image" src="https://github.com/user-attachments/assets/e7621bb5-7e5d-4ae9-be6b-fe00adacd6d8" />
<img width="758" height="581" alt="image" src="https://github.com/user-attachments/assets/11c209d5-8b60-4dd8-951a-09dea8c81e04" />
<img width="1866" height="932" alt="image" src="https://github.com/user-attachments/assets/6e43f2e9-3383-441b-b5da-ce3e754c9952" />


# RESULT: 
Thus the Multirate-DSP-using-Decimation-and-Interpolation using python was performed and verified.
