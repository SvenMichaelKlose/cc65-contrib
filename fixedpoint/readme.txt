Fixed Point Library
By Steffen Goerzig

Type "fixed":
1.1 fixed point
Type "doublefixed":
1.3 fixed point
2.2 fixed point
3.1 fixed point

Macros for type "fixed":

floatStringToFixed(value, result);
fixedToFloatString(value, result);
bitStringToFixed(value, result);
fixedToBitString(value, result);
fixedToUnsignedInt(value, result);
fixedToUnsignedChar(value, result);
unsignedIntToFixed(value, result);
unsignedCharToFixed(value, result);
// result = op1+op2 
fixedAdd(op1, op2, result);
// result = op1-op2 
fixedSub(op1, op2, result);
// result = op1*op2 
fixedMul(op1, op2, result);
// result = op1/op2 
fixedDiv(op1, op2, result);
// result = op1*op2 
fixedMulUnsignedChar(op1, op2, result);

Macros for type "doublefixed"

// call this macro to change between different fixed point types
// numBytes must be in range {1,2,3}, default: 2 
// numBytes==1: 3.1 fixed point 
// numBytes==2: 2.2 fixed point 
// numBytes==3: 1.3 fixed point 
doublefixedSetNumberBytesAfterPoint(numBytes);
fixedToDoublefixed(value, result);
doublefixedToFixed(value, result);
bitStringToDoublefixed(value, result);
doublefixedToBitString(value, result);
doublefixedToUnsignedInt(value, result);
doublefixedToUnsignedLong(value, result);
doublefixedToUnsignedChar(value, result);
unsignedLongToDoublefixed(value, result);
unsignedIntToDoublefixed(value, result);
unsignedCharToDoublefixed(value, result);
// convert between different doublefixed types,
// e.g. from 1.3 fixed point to 2.2 fixed point
doublefixed13To22(value, result);
doublefixed13To31(value, result);
doublefixed22To13(value, result);
doublefixed22To31(value, result);
doublefixed31To22(value, result);
doublefixed31To13(value, result);
// result = op1+op2 
doublefixedAdd(op1, op2, result);
/* result = op1-op2 */
doublefixedSub(op1, op2, result);
// biggest cc65 data type has 4 bytes,
// so current macros for doublefixed 
// div and mul do not work properly
