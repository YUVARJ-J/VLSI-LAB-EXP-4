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
![image](https://github.com/Udayabharathim/VLSI_EXPERIMENT_4/assets/160568654/3fffb34d-7636-45a0-b810-153a2a9e4937)

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
                   
![image](https://github.com/Udayabharathim/VLSI_EXPERIMENT_4/assets/160568654/b1415dba-d407-4604-9e71-950ce0278cb2)



## JK FLIPFLOP:
![image](https://github.com/Udayabharathim/VLSI_EXPERIMENT_4/assets/160568654/974ee6ec-6df1-4d94-bef6-e30b805ff7b8)
 

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

![image](https://github.com/Udayabharathim/VLSI_EXPERIMENT_4/assets/160568654/8a3c0832-15af-4481-b653-fe9d78f204d9)




## T FLIPFLOP
	

![image](https://github.com/Udayabharathim/VLSI_EXPERIMENT_4/assets/160568654/634ea0d3-4c4d-47cb-8e2a-97d8e4b4b31f)


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

  ![image](https://github.com/Udayabharathim/VLSI_EXPERIMENT_4/assets/160568654/bbf94095-1cdb-4d94-bcc2-6f1dd591ddfa)
                

## D FLIPFLOP:
 ![image](https://github.com/Udayabharathim/VLSI_EXPERIMENT_4/assets/160568654/1be6a3f8-91a4-4b35-bccc-2fd8e29a90cf)

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
![image](https://github.com/Udayabharathim/VLSI_EXPERIMENT_4/assets/160568654/e80b0a85-ba38-4673-b7e2-15acc056fe51)



## RESULT:
	The simulate and synthesis SR, JK, T, D - FLIPFLOP, COUNTER DESIGN using VIVADO is successfully verified.

