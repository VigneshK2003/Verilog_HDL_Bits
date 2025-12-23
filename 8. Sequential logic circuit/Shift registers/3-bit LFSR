module top_module (
	input [2:0] SW,      
	input [1:0] KEY,
    output [2:0]LEDR );  
    
    wire clk;
    wire L;
    wire [2:0]R;
    wire [2:0]Q;
    
    assign R = SW;
    assign clk = KEY[0];
    assign L = KEY[1];
    
    always@(posedge clk)
       begin
           if( L )
               Q <= R;
           else if( ~L)
               Q <= { Q[1]^Q[2], Q[0] , Q[2] } ;
       end
    
       assign LEDR = Q ;
endmodule
