# SIMULATION-OF-AUTOCORRELATION-AND-PSD-USING-SCILAB-1

__AIM:__

Write a program for Autocorrelation and PSD of signals in SCILAB and verify Wiener-Khinchin relation. 


__EQUIPMENTS Needed:__

.Computer with i3 Processor 

.SCI LAB


__THEORY:__

The Wiener-Khinchin theorem states that the power spectral density of a wide sense stationary random process is the 
Fourier transform of the corresponding autocorrelation function.

__Algorithm:__

 1.Load or Define the Signal: Input your time-domain signal. 

 2.Compute Autocorrelation: Calculate the autocorrelation function of the signal.

3.Compute Power Spectral Density (PSD): Estimate the PSD of the signal, either directly using a method like
Welch’s periodogram or by using the Fourier transform of the autocorrelation.

4.Plot Results: Visualize the autocorrelation function and PSD. 

__PROCEDURE:__


Refer Algorithms and write code for the experiment. 

Open SCILAB in System 

Type your code in New Editor 

Save the file 

Execute the code 

If any Error, correct it in code and execute again 

Verify the generated waveform using Tabulation and Model Waveform 

__PROGRAM:__
```
clear all;
close;

t = 0:0.01:%pi*2;
x = sin(2*t);


subplot(3,2,1);
plot(t, x);
title('Original Signal');

au = xcorr(x, x);
subplot(3,2,2);
plot(au);
title('Autocorrelation');


v = fft(au);
subplot(3,2,3);
plot(abs(v));
title('FFT of Autocorrelation');


fw = fft(x);
subplot(3,2,4);
plot(abs(fw));
title('FFT of Original Signal');


fw2 = (abs(fw)).^2;
subplot(3,2,5);
plot(fw2);
title('Power Spectrum');
```

__OUTPUT:__

<img width="1915" height="1078" alt="image" src="https://github.com/user-attachments/assets/aa77167e-96b7-4330-b301-073fa734d5dd" />

__RESULT:__
The autocorrelation function of the signal was successfully computed and plotted. The Power Spectral Density (PSD) obtained from the FFT of the autocorrelation verified the Wiener-Khinchin relation.
<img width="899" height="1599" alt="image" src="https://github.com/user-attachments/assets/286a6066-8aa4-46bf-b9c6-fc552ad3b9ba" />
