# EXPT 1: Computation-of-DFT-using-direct-method

## AIM
To perform and verify DFT using direct method by SCILAB.
## APPARATUS REQUIRED
PC installed with SCILAB
## PROGRAM 
### DFT DIRECT METHOD
clc;

clear;
xn=[1 2 3 4 4 3 2 1];
n1=0:1:length(xn)-1;
subplot(3,1,1);
plot2d3(n1,xn);
xlabel('Time n');
ylabel('Amplitude xn');
title('Input Sequence');
j=sqrt(-1);
N=length(xn);
Xk=zeros(1,N);
for k=0:N-1
for n=0:N-1
Xk(k+1)=Xk(k+1)+xn(n+1)*exp((-j*2*%pi*k*n)/N);
end
end
disp(Xk)
K1=0:1:length(Xk)-1;
magnitude=abs(Xk)
subplot(3,1,2);
plot2d3(K1,magnitude);
xlabel('frequency(Hz)');
ylabel('magnitude(gain)');
title('magnitude spectrum');
angle = atan(imag(Xk),real(Xk))
subplot(3,1,3);
plot2d3(K1,angle);
xlabel('frequency(Hz)');
ylabel('Phase');
title('Phase spectrum')
### CALCULATIONS:
<img width="900" height="1600" alt="image" src="https://github.com/user-attachments/assets/bdc4ec1d-1091-43a2-b119-c6d8aa9d75e6" />
<img width="900" height="1600" alt="image" src="https://github.com/user-attachments/assets/4f98c915-b5dd-4d8c-803b-d27a9f6d1294" />
<img width="900" height="1600" alt="image" src="https://github.com/user-attachments/assets/f0c7a95c-653a-4dfc-b634-f243026d00bf" />
### SAMPLE OUTPUT:
<img width="1600" height="745" alt="image" src="https://github.com/user-attachments/assets/78a8f01a-213a-4b24-acf3-2a3108209e5c" />


## RESULT:
Thus,  DFT using direct method for two given sequences were performed and its result was verified.

