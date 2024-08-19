Mux.hdl

CHIP Mux {
    IN a, b, sel;
    OUT out;

    PARTS:
    Not(in=sel,out=notsel);
    And(a=a,b=notsel,out=anotsel);
    And(a=b,b=sel,out=bsel);
    Or(a=anotsel,b=bsel,out=out);
}
![image](https://github.com/user-attachments/assets/ef717144-ea87-4314-9481-1e8e783fa9fc)


 DMux.hdl 

 CHIP DMux {
    IN in, sel;
    OUT a, b;

    PARTS:
    And(a=in,b=sel,out=b);
    Not(in=sel,out=notsel);
    And(a=in,b=notsel,out=a);
}
![image](https://github.com/user-attachments/assets/e2cea7d4-8ec1-433e-b691-961f04b59b94)

