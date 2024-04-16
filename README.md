# BOOLEAN_FUNCTION_MINIMIZATION

**AIM:**

To implement the given logic function verify its operation in Quartus using Verilog programming.

F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D 

F2=xy’z+x’y’z+w’xy+wx’y+wxy

**Equipment Required:**

Hardware – PCs, Cyclone II , USB flasher

**Software – Quartus prime**

**Theory**

**Logic Diagram**

**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**
//Program to compute the function f1=a'b'c'd'+ac'd'+b'cd'+a'bcd+bc'd
//f2=xy'z+x'y'z+w'xy+wx'y+wxy
// simplify the logic using Boolean minimization/k map 
//compute f2 and write verilog code for f2 as like f1
module BMf1f2(a,b,c,d,w,x,y,z,f1,f2);
input a,b,c,d,w,x,y,z;
output f1,f2;
wire adash,bdash,cdash,ddash,ydash,p,q,r,s,t,u;
not(adash,a);
not(bdash,b);
not(cdash,c);
not(ddash,d);
and(p,bdash,ddash);
and(q,adash,b,d);
and(r,a,b,cdash);
or(f1,p,q,r);
//type code for f2 as like f1
not(ydash,y);
and(s,x,y);
and(t,ydash,z);
and(u,w,y);
or(f2,s,t,u);
endmodule


Developed by:B.SANDHIYA SREE
RegisterNumber:212223220093


**RTL realization**
![Screenshot 2024-04-16 101303](https://github.com/Sandhniya/BOOLEAN_FUNCTION_MINIMIZATION/assets/151395890/d6fb0d81-1ea9-46bb-9acd-df454505545d)



**Output:**
![Screenshot 2024-04-16 101320](https://github.com/Sandhniya/BOOLEAN_FUNCTION_MINIMIZATION/assets/151395890/df2575cc-9386-4552-990d-f1ce1759623c)



**RTL**

![Screenshot 2024-04-16 101344](https://github.com/Sandhniya/BOOLEAN_FUNCTION_MINIMIZATION/assets/151395890/694ff67d-5de3-44f8-b1ad-8f1f20120c68)


**Timing Diagram**

**Result:**

Thus the given logic functions are implemented using and their operations are verified using Verilog programming.

