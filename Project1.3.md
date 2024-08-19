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

 DMux.hdl 

 CHIP DMux {
    IN in, sel;
    OUT a, b;

    PARTS:
    And(a=in,b=sel,out=b);
    Not(in=sel,out=notsel);
    And(a=in,b=notsel,out=a);
}
