# SIGN-LANGUAGE-TRANSLATOR
Objective: To develop a wearable glove solution for speech-impaired individuals that translates sign language into speech and text.
#Description:
Designed and developed a wearable glove prototype for converting sign language into speech and text.
Incorporated sensors and technology to accurately detect hand movements and gestures.
Developed algorithms to analyze and interpret the captured sign language data.
Implemented a speech synthesis system to convert the interpreted sign language into audible speech.
Integrated a text generation feature to provide real-time text representation of the sign language.
Conducted extensive testing and fine-tuning to ensure high accuracy and reliability of the translation.
Collaborated with a multidisciplinary team to optimize the glove's design, functionality, and user experience.
Demonstrated the prototype's effectiveness in enabling effective communication for speech-impaired individuals.
Actively sought user feedback to further refine and improve the system's performance.
#



#define asd 8 
#define add 7 
#define adds 6
//#define adds A0
char temp = '0';

void setup()
{
  pinMode(asd, INPUT);
  pinMode(add, INPUT);
 pinMode(adds, INPUT);
  
   Serial.begin(9600);
  
}
  void printfun(char cp) //to avoid printing repeating symbols
{
if(cp!=temp)
{
Serial.print(cp);
temp=cp;
}
}
void loop()
{
  int var=digitalRead(asd);
  int varr=digitalRead(add);
 int varrs=digitalRead(adds);

if(varrs == HIGH)
{
printfun("im done");
Serial.println("im done");
}
if(var==HIGH)
{
printfun('A');
Serial.println('A');
}
if(varr==HIGH)
{
printfun('B');
Serial.println('B');
}
delay(1000); 
}


//if((var==HIGH)&&(varr==HIGH))
//{
//Serial.println('F');
//printfun('F');
//}


//  if (var==HIGH)
//  {
//     Serial.println("im done");
//  }
//    if (varr==HIGH)
//     {
//      Serial.println("WET");
//  }
//  if ((var & varr) == HIGH)
// {
//    Serial.println("WET and dry");
// }
  
