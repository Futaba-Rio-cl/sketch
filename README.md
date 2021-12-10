# sketch
#include <arduino.h>
int ledPin = 3;
void setup (){
  pinMode(ledPin,OUTPUT);
}
void loop(){
  for (int a=0; a<=255;a++) { //循环语句，控制PWM亮度的增加
    analogWrite(ledPin,a);
        delay(5); //当前亮度级别维持的时间,单位毫秒            
  }
  for (int a=255; a>=0;a--) { //循环语句，控制PWM亮度减小
    analogWrite(ledPin,a);
        delay(5); //当前亮度的维持的时间,单位毫秒  
  }
}
