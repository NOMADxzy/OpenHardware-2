# -18030100013xzy-
void setup()
{
  pinMod# -1
char MORSE[][4] = {
  {'.','-','*','*'}, //A
  {'-','.','.','.'}, //B
  {'-','.','-','.'}, //C
  {'-','.','.','*'}, //D
  {'.','*','*','*'}, //E
  {'.','.','-','.'}, //F
  {'-','-','.','*'}, //G
  {'.','.','.','.'}, //F
  {'.','.','*','*'}, //I
  {'.','-','-','-'}, //J
  {'-','.','-','*'}, //K
  {'.','-','.','.'}, //L
  {'-','-','*','*'}, //M
  {'-','.','*','*'}, //N
  {'-','-','-','*'}, //O
  {'.','-','-','.'}, //P
  {'-','-','.','-'}, //Q
  {'.','-','.','*'}, //R
  {'.','.','.','*'}, //S
  {'-','*','*','*'}, //T
  {'.','.','-','*'}, //U
  {'.','.','.','-'}, //V
  {'.','-','-','*'}, //W
  {'-','.','.','-'}, //X
  {'-','.','-','-'}, //Y
  {'-','-','.','.'}  //Z
};
void setup() 
{
  Serial.begin(9600);     
}

void loop() 
{
   String str = "";
   String morse = "";
   int i,t,temp = 0;
   int n = 0;
   while (Serial.available() > 0) {
    temp = 1;
    str += char(Serial.read());
    delay(2);
    n++;
   }
   if(temp){
    for(i=0;i<n;i++)
    {
      for(t=0;t<4;t++)
      {
        morse += ' ';
      }
      Serial.println(morse);
    }
    delay(2);
   }
   
