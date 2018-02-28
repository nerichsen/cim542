# WEEK 3
## Space Ship Interface

### This project took me a little because I had trouble with the switch when it came to connecting it to bread board. I realized it was a simple thing like rotating the switch around to ensure that it was securely plugged in.


int switchstate = 0;

void setup() {
  pinMode(3, OUTPUT);
  pinMode(4, OUTPUT);
  pinMode(5, OUTPUT);
  pinMode(2, INPUT);
}

void loop() {
  switchstate = digitalRead(2);

  if (switchstate == LOW) {
    digitalWrite(3, HIGH);
    digitalWrite(4, LOW);
    digitalWrite(5, LOW);
  }

  else {
    digitalWrite(3, LOW);
    digitalWrite(4, LOW);
    digitalWrite(5, HIGH);

    delay(250);
    digitalWrite(4, HIGH);
    digitalWrite(5, LOW);
    delay(250);
  }
}

[Watch the video yourself!](https://vimeo.com/257621926)
