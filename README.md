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


#main program
#define ina 2
#define inb 3
#define inc 4
#define ind 5
#define ine 6
#define inf 7
#define ing 8
#define inh 9
#define ini 10
#define inj 11
#define ink 12
#define inl 13
#define inm A0
#define inn A1
#define ino A2
#define inp A3
#define inq A4
#define inr A5
#define ins A6
#define inu A7
char temp = '0';

void setup()
{
  pinMode(ina,INPUT);
  pinMode(inb,INPUT);
  pinMode(inc ,INPUT);
  pinMode(ind,INPUT);
  pinMode(ine,INPUT);
  pinMode(inf,INPUT);
  pinMode(ing,INPUT);
  pinMode(inh,INPUT);
  pinMode(ini,INPUT);
  pinMode(inj,INPUT);
  pinMode(ink,INPUT);
  pinMode(inl,INPUT);
  pinMode(inm,INPUT);
  pinMode(inn,INPUT);
  pinMode(ino,INPUT);
  pinMode(inp,INPUT);
  pinMode(inq,INPUT);
  pinMode(inr,INPUT);
  pinMode(ins,INPUT);
  pinMode(inu,INPUT);
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
  int vna = digitalRead(ina);
  int vnb = digitalRead(inb);
  int vnc = digitalRead(inc);
  int vnd = digitalRead(ind);
  int vne = digitalRead(ine);
  int vnf = digitalRead(inf);
  int vng = digitalRead(ing);
  int vnh = digitalRead(inh);
  int vni = digitalRead(ini);
  int vnj = digitalRead(inj);
  int vnk = digitalRead(ink);
  int vnl = digitalRead(inl);
  int vnm = analogRead(inm);
  int vnn = analogRead(inn);
  int vno = analogRead(ino);
  int vnp = analogRead(inp);
  int vnq = analogRead(inq);
  int vnr = analogRead(inr);
  int vns = analogRead(ins);
  int vnu = analogRead(inu);

  if(vna == HIGH)
  {
    printfun("aaaaa");
    Serial.println("aaaaa");
  }
  if(vnb == HIGH)
  {
    printfun("bbbbb ");
    Serial.println(" bbbbb");
  }
   if(vnc == HIGH)
  {
    printfun("ccccc ");
    Serial.println("ccccc");
  }
   if(vnd == HIGH)
  {
    printfun(" ddddd");
    Serial.println(" ddddd");
  }
   if(vne== HIGH)
  {
    printfun("eeeee ");
    Serial.println(" eeeee");
  }
   if(vnf == HIGH)
  {
    printfun("fffff ");
    Serial.println("fffff ");
  }
   if(vng == HIGH)
  {
    printfun("ggggg ");
    Serial.println("ggggg ");
    delay(2000);
  }
   if(vnh == HIGH)
  {
    printfun("hhhhh ");
    Serial.println(" hhhhh");
  }
   if(vni == HIGH)
  {
    printfun("iiiii ");
    Serial.println("iiiii ");
  }
   if(vnj == HIGH)
  {
    printfun(" jjjjj");
    Serial.println("jjjjj ");
  }
   if(vnk == HIGH)
  {
    printfun("kkkkk ");
    Serial.println("kkkkk ");
  }
   if(vnl == HIGH)
  {
    printfun("lllll ");
    Serial.println("lllll ");
  }
}
   if(vnm >= 500)
  {
    printfun(" mmmmm");
    Serial.println("mmmmm ");
  }
  if(vnn >= 500)
  {
    printfun("nnnnn ");
    Serial.println("nnnnn ");
  }
  if(vno >= 500)
  {
    printfun(" ooooo");
    Serial.println("ooooo ");
  }
  if(vnp >= 500)
  {
    printfun("ppppp ");
    Serial.println("ppppp ");
  }
  if(vnq >= 500)
  {
    printfun("qqqqq ");
    Serial.println("qqqqq ");
  }
  if(vnr >= 500)
  {
    printfun("rrrrr ");
    Serial.println("rrrrr ");
  }
  if(vns >= 500)
  {
    printfun("sssss");
    Serial.println("sssss ");
  }
  if(vnu >= 500)
  {
    printfun("uuuuu ");
    Serial.println("uuuuu ");
  }
 delay(2000);
 }



 #calibration code
 /? Manual callibratio
while(1)
{
float flexADC5 = analogRead(FLEX_PIN5);
Serial.println(flexADC5);
delay(800);
}

