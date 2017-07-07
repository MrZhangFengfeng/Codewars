### The following examples all return 15:

      parseInt(' 0xF', 16);
      parseInt(' F', 16);
      parseInt('17', 8);
      parseInt(021, 8);
      parseInt('015', 10);   // parseInt(015, 10); will return 15
      parseInt(15.99, 10);
      parseInt('15,123', 10);
      parseInt('FXX123', 16);
      parseInt('1111', 2);
      parseInt('15 * 3', 10);
      parseInt('15e2', 10);
      parseInt('15px', 10);
      parseInt('12', 13);
      
 - - -
 
 ### The following examples all return NaN:
 
    parseInt('Hello', 8); // Not a number at all
    parseInt('546', 2);   // Digits are not valid for binary representations
          
 - - -
 
 ### The following examples all return -15:
 
    parseInt('-F', 16);
    parseInt('-0F', 16);
    parseInt('-0XF', 16);
    parseInt(-15.1, 10)
    parseInt(' -17', 8);
    parseInt(' -15', 10);
    parseInt('-1111', 2);
    parseInt('-15e1', 10);
    parseInt('-12', 13);
    
 - - -
 
 ### The following examples all return 4:
 
    parseInt(4.7, 10);
    parseInt(4.7 * 1e22, 10); // Very large number becomes 4
    parseInt(0.00000000000434, 10); // Very small number becomes 4
   
- - -
 
 ### The following examples all return 0:
 
    parseInt('0e0'); // 0
    parseInt('08'); // 0, '8' is not an octal digit.(octal digit:八进制)
