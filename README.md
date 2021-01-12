# 0105
void setup() {  
  // put your setup code here, to run once:  
pinMode(3, OUTPUT);  
pinMode(4, OUTPUT);  
pinMode(5, OUTPUT);  
pinMode(6, OUTPUT);  
Serial.begin(9600);  
}  
void loop() {  
  // put your main code here, to run repeatedly:  
int x =analogRead(A1);   
int y =analogRead(A2);   
int z =analogRead(A3);   
Serial.println("x     y     z");  
Serial.print(x);  
Serial.print("   ");  
Serial.print(y);  
Serial.print("   ");  
Serial.println(z);  
delay(500);  
  
if(x<370&x>300)  
{  
  digitalWrite(3, HIGH);      
  digitalWrite(4, HIGH);  
  }  
if(x>370)  
{                           
  digitalWrite(3, LOW);     
  digitalWrite(4, HIGH);  
  }       
if(x<320)  
{  
  digitalWrite(4, LOW);     
  digitalWrite(3, HIGH);  
 }  
  if(y<360&y>330)  
{  
  digitalWrite(5, HIGH);     
  digitalWrite(6, HIGH);  
  }  
if(y>370)  
{  
  digitalWrite(5, LOW);     
  digitalWrite(6, HIGH);  
  }  
if(y<320)  
{  
  digitalWrite(6, LOW);     
  digitalWrite(5, HIGH);  
  }  
}  
  
