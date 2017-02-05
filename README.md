# lights
Heartfelt Connections
int buttonPin1 = 3;
int buttonPin2 = 2;
int buttonPin3 = 4;

int yellowPin1 = 9;
int bluePin1 = 8;
int redPin1 = 7;
int yellowPin2 = 6;
int bluePin3 = 10;
int redPin2 = 11;
int bluePin2 = 12;
int redPin3 = 13;
int yellowPin3 = 5;

void setup() {
  // put your setup code here, to run once:
  //or pinMode(2,OUTPUT);
  //or ledPin = 2
  pinMode(bluePin1,OUTPUT);
  pinMode(yellowPin2,OUTPUT);
  pinMode(yellowPin1,OUTPUT);
  pinMode(yellowPin3,OUTPUT);
  pinMode(redPin1,OUTPUT);
  pinMode(bluePin3,OUTPUT);
  pinMode(bluePin2,OUTPUT);
  pinMode(redPin2,OUTPUT);
  pinMode(redPin3,OUTPUT);
  
  pinMode(buttonPin1,INPUT);
  pinMode(buttonPin2,INPUT);
  pinMode(buttonPin3,INPUT);
  
  Serial.begin(9600);
}

void loop() {
  // put your main code here, to run repeatedly:
  
  int buttonState1 = digitalRead(buttonPin1);
  int buttonState2 = digitalRead(buttonPin2);
  int buttonState3 = digitalRead(buttonPin3);
  
//  Serial.println(buttonState1);
  Serial.println(buttonState2);
  

  bool pattern1 = false;
  bool pattern2 = false;
  bool pattern3 = false;
  bool pattern4 = false;
  bool pattern5 = false;
  bool pattern6 = false;
  bool pattern7 = false;
  bool nothing = false;
  bool pattern8 = false;
  
  if (buttonState1 == HIGH && buttonState2 == LOW && buttonState3 == LOW){
    pattern1 = true;
    pattern2 = false;
    pattern3 = false;
    pattern4 = false;
    pattern5 = false;
    pattern6 = false;
    pattern7 = false;
    pattern8 = false;
  } 
  
  else if (buttonState2 == HIGH && buttonState1 == LOW && buttonState3 == LOW){
    pattern1 = false;
    pattern2 = true;
    pattern3 = false;
    pattern4 = false;
    pattern5 = false;
    pattern6 = false;
    pattern7 = false;
  }

  else if (buttonState1 == HIGH && buttonState2 == HIGH && buttonState3 == LOW){
    pattern1 = false;
    pattern2 = false;
    pattern3 = true;
    pattern4 = false;
    pattern5 = false;
    pattern6 = false;
    pattern7 = false;
  }

  else if (buttonState3 == HIGH && buttonState1 == LOW && buttonState2 == LOW){
    pattern1 = false;
    pattern2 = false;
    pattern3 = false;
    pattern4 = true;
    pattern5 = false;
    pattern6 = false;
    pattern7 = false;
  }

  else if (buttonState3 == HIGH && buttonState1 == HIGH && buttonState2 == LOW){
      pattern1 = false;
      pattern2 = false;
      pattern3 = false;
      pattern4 = false;
      pattern5 = true;
      pattern6 = false;
      pattern7 = false;
    }

  else if (buttonState3 == HIGH && buttonState1 == LOW && buttonState2 == HIGH){
      pattern1 = false;
      pattern2 = false;
      pattern3 = false;
      pattern4 = false;
      pattern5 = false;
      pattern6 = true;
      pattern7 = false;
    }

  else if (buttonState3 == HIGH && buttonState1 == HIGH && buttonState2 == HIGH){
      pattern1 = false;
      pattern2 = false;
      pattern3 = false;
      pattern4 = false;
      pattern5 = false;
      pattern6 = false;
      pattern7 = true;
    }
    
  else if (buttonState1 == LOW && buttonState2 == LOW && buttonState3 == LOW){
    pattern1 = false;
    pattern2 = false;
    pattern3 = false;
    pattern4 = false;
    pattern5 = false;
    pattern6 = false;
    pattern7 = false;
    nothing = true;
   }

  if (nothing == true){
    digitalWrite(yellowPin1,LOW);
    digitalWrite(bluePin1,LOW);
    digitalWrite(redPin1,LOW);
    digitalWrite(yellowPin2,LOW);
  }
  
  else if (pattern1 == true){
    digitalWrite(yellowPin1,HIGH);
    digitalWrite(yellowPin2,HIGH);
    digitalWrite(yellowPin3,HIGH);
    delay(200);
    digitalWrite(yellowPin1,LOW);
    digitalWrite(yellowPin2,LOW);
    digitalWrite(yellowPin3,LOW);
    delay(200);
    digitalWrite(yellowPin1,HIGH);
    digitalWrite(yellowPin2,HIGH);
    digitalWrite(yellowPin3,HIGH);
    delay(130);
    digitalWrite(yellowPin1,LOW);
    digitalWrite(yellowPin2,LOW);
    digitalWrite(yellowPin3,LOW);
    delay(570);  
    }
    
   else if (pattern2 == true){
    digitalWrite(redPin1,HIGH);
    digitalWrite(redPin2,HIGH);
    digitalWrite(redPin3,HIGH);
    delay(200);
    digitalWrite(redPin1,LOW);
    digitalWrite(redPin2,LOW);
    digitalWrite(redPin3,LOW);
    delay(200);
     digitalWrite(redPin1,HIGH);
    digitalWrite(redPin2,HIGH);
    digitalWrite(redPin3,HIGH);
    delay(130);
    digitalWrite(redPin1,LOW);
    digitalWrite(redPin2,LOW);
    digitalWrite(redPin3,LOW);
    delay(570);  
   }

  else if (pattern3 == true){
    digitalWrite(redPin1,HIGH);
    digitalWrite(redPin2,HIGH);
    digitalWrite(redPin3,HIGH);
    digitalWrite(yellowPin1,HIGH);
    digitalWrite(yellowPin2,HIGH);
    digitalWrite(yellowPin3,HIGH);
    delay(150);
    digitalWrite(redPin1,LOW);
    digitalWrite(redPin2,LOW);
    digitalWrite(redPin3,LOW);
    digitalWrite(yellowPin1,LOW);
    digitalWrite(yellowPin2,LOW);
    digitalWrite(yellowPin3,LOW);
    delay(150);
     digitalWrite(redPin1,HIGH);
    digitalWrite(redPin2,HIGH);
    digitalWrite(redPin3,HIGH);
    digitalWrite(yellowPin1,HIGH);
    digitalWrite(yellowPin2,HIGH);
    digitalWrite(yellowPin3,HIGH);
    delay(80);
    digitalWrite(redPin1,LOW);
    digitalWrite(redPin2,LOW);
    digitalWrite(redPin3,LOW);
    digitalWrite(yellowPin1,LOW);
    digitalWrite(yellowPin2,LOW);
    digitalWrite(yellowPin3,LOW);
    delay(520);  
  }

  else if (pattern4 == true){
    digitalWrite(bluePin1,HIGH);
    digitalWrite(bluePin2,HIGH);
    digitalWrite(bluePin3,HIGH);
    delay(200);
    digitalWrite(bluePin1,LOW);
    digitalWrite(bluePin2,LOW);
    digitalWrite(bluePin3,LOW);
    delay(200);
    digitalWrite(bluePin1,HIGH);
    digitalWrite(bluePin2,HIGH);
    digitalWrite(bluePin3,HIGH);
    delay(130);
    digitalWrite(bluePin1,LOW);
    digitalWrite(bluePin2,LOW);
    digitalWrite(bluePin3,LOW);
    delay(570);  
  }

  else if (pattern5 == true){
    digitalWrite(bluePin1,HIGH);
    digitalWrite(bluePin2,HIGH);
    digitalWrite(bluePin3,HIGH);
    digitalWrite(yellowPin1,HIGH);
    digitalWrite(yellowPin2,HIGH);
    digitalWrite(yellowPin3,HIGH);
    delay(150);
    digitalWrite(bluePin1,LOW);
    digitalWrite(bluePin2,LOW);
    digitalWrite(bluePin3,LOW);
    digitalWrite(yellowPin1,LOW);
    digitalWrite(yellowPin2,LOW);
    digitalWrite(yellowPin3,LOW);
    delay(150);
    digitalWrite(bluePin1,HIGH);
    digitalWrite(bluePin2,HIGH);
    digitalWrite(bluePin3,HIGH);
    digitalWrite(yellowPin1,HIGH);
    digitalWrite(yellowPin2,HIGH);
    digitalWrite(yellowPin3,HIGH);
    delay(80);
    digitalWrite(bluePin1,LOW);
    digitalWrite(bluePin2,LOW);
    digitalWrite(bluePin3,LOW);
    digitalWrite(yellowPin1,LOW);
    digitalWrite(yellowPin2,LOW);
    digitalWrite(yellowPin3,LOW);
    delay(520);  
  }

  else if (pattern6 == true){
    digitalWrite(bluePin1,HIGH);
    digitalWrite(bluePin2,HIGH);
    digitalWrite(bluePin3,HIGH);
    digitalWrite(redPin1,HIGH);
    digitalWrite(redPin2,HIGH);
    digitalWrite(redPin3,HIGH);
    delay(150);
    digitalWrite(bluePin1,LOW);
    digitalWrite(bluePin2,LOW);
    digitalWrite(bluePin3,LOW);
    digitalWrite(redPin1,LOW);
    digitalWrite(redPin2,LOW);
    digitalWrite(redPin3,LOW);
    delay(150);
    digitalWrite(bluePin1,HIGH);
    digitalWrite(bluePin2,HIGH);
    digitalWrite(bluePin3,HIGH);
    digitalWrite(redPin1,HIGH);
    digitalWrite(redPin2,HIGH);
    digitalWrite(redPin3,HIGH);
    delay(80);
    digitalWrite(bluePin1,LOW);
    digitalWrite(bluePin2,LOW);
    digitalWrite(bluePin3,LOW);
    digitalWrite(redPin1,LOW);
    digitalWrite(redPin2,LOW);
    digitalWrite(redPin3,LOW);
    delay(520);  
  }

  else if (pattern7 == true){
    digitalWrite(bluePin1,HIGH);
    digitalWrite(bluePin2,HIGH);
    digitalWrite(bluePin3,HIGH);
    digitalWrite(redPin1,HIGH);
    digitalWrite(redPin2,HIGH);
    digitalWrite(redPin3,HIGH);
    digitalWrite(yellowPin1,HIGH);
    digitalWrite(yellowPin2,HIGH);
    digitalWrite(yellowPin3,HIGH);
    delay(120);
    digitalWrite(bluePin1,LOW);
    digitalWrite(bluePin2,LOW);
    digitalWrite(bluePin3,LOW);
    digitalWrite(redPin1,LOW);
    digitalWrite(redPin2,LOW);
    digitalWrite(redPin3,LOW);
    digitalWrite(yellowPin1,LOW);
    digitalWrite(yellowPin2,LOW);
    digitalWrite(yellowPin3,LOW);
    delay(120);
    digitalWrite(bluePin1,HIGH);
    digitalWrite(bluePin2,HIGH);
    digitalWrite(bluePin3,HIGH);
    digitalWrite(redPin1,HIGH);
    digitalWrite(redPin2,HIGH);
    digitalWrite(redPin3,HIGH);
    digitalWrite(yellowPin1,HIGH);
    digitalWrite(yellowPin2,HIGH);
    digitalWrite(yellowPin3,HIGH);
    delay(50);
    digitalWrite(bluePin1,LOW);
    digitalWrite(bluePin2,LOW);
    digitalWrite(bluePin3,LOW);
    digitalWrite(redPin1,LOW);
    digitalWrite(redPin2,LOW);
    digitalWrite(redPin3,LOW);
    digitalWrite(yellowPin1,LOW);
    digitalWrite(yellowPin2,LOW);
    digitalWrite(yellowPin3,LOW);
    delay(490);  
  }

  else if (pattern8 == true){
    digitalWrite(yellowPin1,HIGH);
    digitalWrite(yellowPin2,HIGH);
    digitalWrite(yellowPin3,HIGH);
    delay(200);
    digitalWrite(yellowPin1,LOW);
    digitalWrite(yellowPin2,LOW);
    digitalWrite(yellowPin3,LOW);
    delay(200);
    digitalWrite(yellowPin1,HIGH);
    digitalWrite(yellowPin2,HIGH);
    digitalWrite(yellowPin3,HIGH);
    delay(130);
    digitalWrite(yellowPin1,LOW);
    digitalWrite(yellowPin2,LOW);
    digitalWrite(yellowPin3,LOW);
    delay(570);

  }
  
  else{  
    digitalWrite(yellowPin1,LOW);
    digitalWrite(bluePin1,LOW);
    digitalWrite(redPin1,LOW);
    digitalWrite(yellowPin2,LOW);
  }
  
}
