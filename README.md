#include "Keypad.h" //4*4 keypad size
char Keys[4][4] = { //[Rows] [Columns]
{'D','#','0','*'},
{'C','9','8','7'},
{'B','6','5','4'},
{'A','3','2','1'}};
byte RP[4] = {6, 7, 8, 9};
byte CP[4] = {2, 3, 4, 5};
Keypad KP=Keypad(makeKeymap(Keys),RP,CP,4,4); // Object
void setup(){pinMode(13,OUTPUT);}
void loop(){
char x = KP.getKey();
if (x=='*'){digitalWrite(13,HIGH);}
if (x=='#'){digitalWrite(13,LOW);}}
<!---
zaidaghbar/zaidaghbar is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
