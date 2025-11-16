# Stability-Analysis-using-Bode-Plot
## Aim:
To analyse the stability of the system having open loop transfer function, G(S)=1/(S(1+0.5S)(1+0.1S)) using bode plot and verify it using MATLAB. 
## Apparatus Required:
Computer with MATLAB software

## Theory:

![WhatsApp Image 2025-11-16 at 23 01 56_073dbfdc](https://github.com/user-attachments/assets/a55dd979-fc4e-4551-8375-5cedcc61d564)
![WhatsApp Image 2025-11-16 at 23 01 57_c96d2f9c](https://github.com/user-attachments/assets/aa12a8fe-21de-4c7b-99a2-f40f8a706f64)



## Procedure:
	Open MATLAB software
	Open a new script file.
	Type the program.
	Save and Execute the program.
	Determine the gain crossover frequency, phase cross over frequency, gain margin and phase margin.
	Also determine the stability.

## Program: 
```
num=[1];
den=[0.05 0.6 1 0];
sys=tf(num,den)
bode(sys)
grid on;
[gm pm wpc wgc]=margin(sys)
gmindb=20*log10(gm)
if(wpc>wgc)
    disp('stable')
elseif(wpc==wgc)
    disp('marginally stable')
else
    disp('unstable')
end
```
## Output:

<img width="1910" height="897" alt="Screenshot 2025-11-16 224650" src="https://github.com/user-attachments/assets/3411f70c-b796-4234-ba31-a4944c163f99" />

## Result:
Thus the bode plot for the given transfer function was drawn and verified using MATLAB. 

Gain margin = 12 dB.

Phase Margin = 60 degree.

Gain crossover frequency = 0.9070 rad/s.

Phase crossover frequency = 4.4721.

The system is  stable.
