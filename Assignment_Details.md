# Cipher-Tool

In this assignment, you will create a java program for a cipher tool that:

Takes as input:
a. A message to be encoded: This message should not be empty and contains at least one letter (If the input message does not satisfy these conditions an error message should be displayed accordingly.)
b. A shiftNumber: This input should be an integer in the range (0-25) inclusive. (Similarly, if the input shift number is out of these bounds, an error message should be displayed)
c. A rotateNumber: This input should be >=0 (Similarly, if the input shift number is out of these bounds, an error message should be displayed)

Returns as output:
a. The cipher encoded text which is generated as follows:
i. All letters (a-z, A-Z) will be shifted by the number of characters specified in the shiftNumber as in Caesar Cipher (Hint: lookup on how the Caesar Cipher works) and all the other characters should remain unchanged. Additionally, Capitalization should be preserved, for example, “Cat” with shiftNumber =1 should give “Dbu”
j. All characters will be rotated right by the number of characters specified in the rotateNumber, with letters from the end wrapping around the front. For example, “Cat” with rotateNumber=1 will be “tCa”.
k. The encoded text should be displayed using the below message
“Your cipher encoded message is ………………….”. If the inputs are invalid, the output should be set to an empty string and the corresponding error message should be displayed.

Error Messages:

If the user provides an invalid input. The following error messages should be displayed.
1. “At least one letter should be provided” ---> When the message is an empty string or contains no alphabets.
2. “The Shift should be between 0 and 25” ---> When the input shift is out of the shiftNumber bounds.
3. “Rotation should be greater than or equal zero” ---> when the input rotateNumber<0
4. “No Encryption Applied” ---> when both rotate and shift equals to zero.

Test Cases:

message = “ Up with the White and Gold!”, shift=25, rotate=0 ---> To vhsg sgd Vghsd zmc Fnkc!
message = “ 123AbcCat123”, shift=0, rotate=3 ---> 123123AbcCat
message = “35505!”shift=5, rotate=0 ---> Error message : At least one letter should be provided
message = “valid message invalid shift”shift=30, rotate=0 ---> The Shift should be between 0 and 25
message = “ zero shift and rotate”, shift=0, rotate=0 ---> No Encryption Applied
message = “Cat”, shift =1, rotate=1 ---> uDb
