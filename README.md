# VLSI_EXPERIMENT_4
## AIM: 
  To simulate and synthesis SR, JK, T, D - FLIPFLOP, COUNTER DESIGN using VIVADO.

 ## APPARATUS REQUIRED:
 VIVADO 2023.2

## PROCEDURE:
 STEP:1 Start the Vivado, Select and Name the New project.<br>
 STEP:2 Select the device family, device, package and speed. <br>
STEP:3 Select new source in the New Project and select Verilog Module as the Source type.<br>
STEP:4 Type the File Name and Click Next and then finish button. Type the code and save it.<br>
STEP:5 Select the Behavioural Simulation in the Source Window and click the check syntax.<br>
 STEP:6 Click the simulation to simulate the program and give the inputs and verify the outputs as per the truth table.<br>











                

## SR FLIPFLOP:

![image](https://github.com/Udayabharathim/VLSI-LAB-EXP-4/assets/160568654/9bc25f0c-eacc-48f2-a0a9-d8eb5b90711d)


## PROGRAM:
module sr_ff(clk,q,rst,s,r);<br>
input s,r,clk,rst;<br>
output reg q;<br>
always@(posedge clk)<br>
begin<br>
if(rst==1)<br>
q=1'b0;<br>
else<br>
begin<br>
case({s,r})<br>
2'b00:q=q;<br>
2'b01:q=1'b0;<br>
2'b10:q=1'b1;<br>
2'b11:q=1'bx;<br>
endcase<br>
end<br>
end<br>
endmodule<br>



## OUTPUT:               
                   
![image](https://github.com/Udayabharathim/VLSI-LAB-EXP-4/assets/160568654/c3b77772-5456-497c-9382-8db273e9448e)


## JK FLIPFLOP:

![image](https://github.com/Udayabharathim/VLSI-LAB-EXP-4/assets/160568654/f836cdf2-8f95-403b-b4b7-ed1a1fb8aec4)


## PROGRAM:
module jk_ff(clk,q,rst,j,k);<br>
input j,k,clk,rst;<br>
output reg q;<br>
always@(posedge clk)<br>
begin<br>
if(rst==1)<br>
q=1'b0;<br>
else<br>
begin<br>
case({j,k})<br>
2'b00:q=q;<br>
2'b01:q=1'b0;<br>
2'b10:q=1'b1;<br>
2'b11:q=~q;<br>
endcase<br>
end<br>
end<br>
endmodule<br>

## OUTPUT:

![image](https://github.com/Udayabharathim/VLSI-LAB-EXP-4/assets/160568654/76d60cab-41f8-4e76-bc5c-2b9abb6eb335)


## T FLIPFLOP
	
![image](https://github.com/Udayabharathim/VLSI-LAB-EXP-4/assets/160568654/af11bd82-5024-4f61-b501-94e2e9e5c93c)


## PROGRAM: 
module t_ff(clk,q,rst,t);<br>
input t,clk,rst;<br>
output reg q;<br>
always@(posedge clk)<br>
begin<br>
if(rst==1)<br>
q=1'b0;<br>
else<br>
if(t==0)<br>
q=q;<br>
else<br>
q=~q;<br>
end<br>
endmodule


## OUTPUT

 ![image](https://github.com/Udayabharathim/VLSI-LAB-EXP-4/assets/160568654/4dd88f8c-dd4e-4dc8-82ba-68f30dc35ddd)

                

## D FLIPFLOP:

![image](https://github.com/Udayabharathim/VLSI-LAB-EXP-4/assets/160568654/35cf7925-dc51-40b1-9e61-abef0abebf67)


## PROGRAM:
module d_ff(clk,q,rst,d);<br>
input d,clk,rst;<br>
output reg q;<br>
always@(posedge clk)<br>
begin<br>
if(rst==1)<br>
q=1'b0;<br>
else<br>
q=d;<br>
end<br>
endmodule<br>

## OUTPUT:

![image](https://github.com/Udayabharathim/VLSI-LAB-EXP-4/assets/160568654/5e737a39-bbf3-47b8-8597-b02e386c3145)



## RESULT:
	The simulate and synthesis SR, JK, T, D - FLIPFLOP, COUNTER DESIGN using VIVADO is successfully verified.

