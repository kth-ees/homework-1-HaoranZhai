[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/GdI-uXRc)
[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-2e0aaae1b6195c2367325f4f02e2d04e9abb55f0b24a779b69b11b9e10269abc.svg)](https://classroom.github.com/online_ide?assignment_repo_id=20360264&assignment_repo_type=AssignmentRepo)

module decoder (
  input logic [3:0] binary,
  output logic [15:0] one_hot
);
  // …
  // Add your description here
  always_comb begin
    one_hot = '0;              
    one_hot[binary] = 1'b1;    
  end
  // …
endmodule

module bin2bcd (
  input logic [3:0] binary,
  output logic [3:0] bcd,
  output logic carry
);
  // …
  // Add your description here
  always_comb begin
    if (binary >= 4'd10) begin
      carry = 1'b1;
      bcd   = binary - 4'd10;  
    end else begin
      carry = 1'b0;
      bcd   = binary;          
    end
  end
  // …
endmodule

module count_ones_4_simple (
  input  logic [3:0] a,
  output logic [2:0] out
);
  // …
  // Add your description here
  assign out = a[0] + a[1] + a[2] + a[3];
  // …
endmodule
