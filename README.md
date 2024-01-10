int l1green = 5; int l2green = 6;
int l1red = 7; int l2red = 4;
int buzzer = 9;
void setup ()
{
Serial. begin (9600);
Pin Mode (l1green, OUTPUT);
pin Mode (l2green, OUTPUT);
pin Mode (l1red, OUTPUT);
pin Mode (l2red, OUTPUT);
pin Mode (buzzer, OUTPUT);
digital Write (buzzer, LOW);
}
void normal ()
{
If (Serial. available ()>0)
{ int pc_ data = Serial. Parse Int ();
If (pc_ data== 1)
{
Digital Write (buzzer, HIGH); lane1();
}
else if (pc_ data == 2)
{
Digital Write (buzzer, HIGH); lane2();
}
}
else
{
Digital Write (buzzer, LOW);
Digital Write (l1green, HIGH);
Digital Write (l2green, LOW);
digital Write (l1red, LOW);
digital Write (l2red, HIGH);
delay (2000);
digital Write (l1green, LOW);
digital Write (l2green, HIGH);
digital Write (l1red, HIGH);
digital Write (l2red, LOW);
delay (2000);
