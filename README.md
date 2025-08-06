# 4_alu_using-verilog
designed alu using verilog
#top_module
module alu(input [3:0]op,input [7:0]a,b, output reg [7:0] out);#input output ports decleration
always@(*)#it run the always block whenever input changes
begin
case(op)#case with statment #various operation define
4'b0000:out=a+b;
4'b0001:out=a+1;
4'b0010:out=b-a;
4'b0011:out=a-1;
4'b0100:out=a*b;
4'b0101:out=a/b;
4'b0110:out=a>>1;
4'b0111:out=a<<1;
4'b1000:out=a&&b;
4'b1001:out=a||b;
4'b1010:out=~a;
4'b1011:out=a^b;
default:out=4'b0000;
endcase
end
endmodule
