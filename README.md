# EXPT-6-Simulation-of-Multirate-DSP-using-Decimation-and-Interpolation

# AIM: 

 To perform and verify Multirate-DSP-using-Decimation-and-Interpolation.

# APPARATUS REQUIRED: 
 PC installed with SCILAB. 

# PROGRAM: 
 clear;
 
clc;

close;

n = 0:%pi/50:2*%pi;

x = sin(%pi*n); //original signal

M=input('Enter the downsampling factor');

L=input('Enter the upsampling factor');

//Down Sampling

downsampling_x = x(1:M:length(x));

disp(x,'Input signal x(n)=');

disp(downsampling_x,'Downsampled Signal');

figure(1);

subplot(2,1,1)

plot2d3(1:length(x),x);

xtitle('original singal')

subplot(2,1,2)

plot2d3(1:length(downsampling_x),downsampling_x);

xtitle('Downsampled Signal by a factor of M');

//Upsampling

upsampling_x=[];

for i=1:length(x)

upsampling_x(1,L*i)=x(i);

end

disp(x,'Input signal x(n)=');

disp(upsampling_x,'Upsampled Signal');

figure(2);

subplot(2,1,1);

plot2d3(x);

title('original signal');

subplot(2,1,2);

plot2d3(upsampling_x);

title('Upsampled Signal by a factor of L');


# OUTPUT: 
<img width="932" height="691" alt="image" src="https://github.com/user-attachments/assets/e3ae6888-18fd-49e0-a87c-fd15ac2a5371" />


# RESULT: 
Thus the Multirate-DSP-using-Decimation-and-Interpolation using python was performed and verified.
