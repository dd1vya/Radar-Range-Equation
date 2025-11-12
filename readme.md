## EVALUATION OF RADAR RANGE USING PYTHON

### Aim:
To calculate the maximum range of a radar system using the Radar Range Equation and verify the results through Scilab programming.

### Theory:
The Radar Range Equation is a fundamental relation used in radar system design to determine the maximum range at which a radar can detect a target. It is expressed as:


<img width="668" height="728" alt="Screenshot 2025-10-29 081954" src="https://github.com/user-attachments/assets/1cc7b58d-a41a-4159-bad2-445992f69dec" />

### Procedure:
1)Set Up the Scilab Environment:  
Open Scilab software and create a new script file (.sce).  
2)Define the Input Parameters:  
Specify the transmitted power, transmitter and receiver gains, operating frequency, radar cross section, and minimum detectable power.  
3)Compute the Wavelength:  
Calculate wavelength using the speed of light and operating frequency.  
4)Implement the Radar Range Equation:  
Use Scilab’s mathematical functions to compute the maximum radar range based on the formula.  
5)Execute the Script:  
Run the program to obtain and display the maximum radar range.  

### Code:
```
Pt = 1000;
G = 1000;
sigma = 1;
Ae = 10;

Smin = logspace(-12, -6, 100);
Rmax = ((Pt * G * sigma * Ae) ./ (16 * %pi^2 .* Smin)).^(1/4);
subplot(3,1,1);
plot(Smin, Rmax);

Ppeak = linspace(100, 10000, 100);
Rmax2 = ((Ppeak * G * sigma * Ae) ./ (16 * %pi^2 * 1e-10)).^(1/4);
subplot(3,1,2);
plot(Ppeak, Rmax2);

Gt = linspace(100, 2000, 100);
Rmax3 = ((Pt * Gt * sigma * Ae) ./ (16 * %pi^2 * 1e-10)).^(1/4);
subplot(3,1,3);
plot(Gt, Rmax3);

```

### Output waveform:
<img width="1561" height="981" alt="image" src="https://github.com/user-attachments/assets/35eb708a-5cfd-42be-a970-09dbc885b3b0" />




### Manual Calculations: 
![WhatsApp Image 2025-11-05 at 08 43 02_f94c59c3](https://github.com/user-attachments/assets/585a17e6-ece8-4925-afda-b0bf5ab0a6aa)



### Result:
Thus, the maximum range of a radar system using the Radar Range Equation is calculated and verified through Scilab programming.
