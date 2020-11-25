# TP-N-16-AUTITO-A-CONTROL-REMOTO


string BT_recibido = "";



void setup()
{  
  configurarPines ();
  configurar BT ();
  
  Serial.begin (9800);
  SerialsetTimeout ( 50 );
  
}



void loop()
{
  //llama al serialEvent automaticamente
  
  comunicacion ();
  
  switch ( BT_recibido )
  {
    case 'w':
        avanzar ();
        break;
    case 's': 
       retroceder ()
         break;
    case 'a': 
       girarIzq ();
       break;
    case 'd': 
       girarDer ();
       break;
    case 'f': 
       frenar ();
       break;
    case 'g': 
    detenerse ();
    break;
    case 'q': 
    girarIzqEnSuEje ();
    break;
    case 'e':
    girarDerEnSuEje ();
    break;
    
  }
  
}


void serialEvent()
{
  while (  Serial.avaible  ()  )
  {
    BT recibido = Serial.read ();
    
  }
  Serial.flush ();
}

///////////////////////////////////////////////////////////////

void configurarpines ()
{
  for ( int pin = 2 ; ??? ; pin++ ) 
  {
    pinMode (pin, OUTPUT);
  
  }
  
  pinMode ( sem_mov , INPUT );
  
}


void configurarBT()
{
  ???
}

//////////////////////////////////////////////////////////////////

void avanzar ()
{
  String motor [] = (motor1, motor2, motor2_1, motor2_2, motor1_2, motor1_1);
  int estado []   = ( 255  ,  255  ,   1     ,   0     ,   0      ,    1   );

  for (int i = 0 ; ??? ; i++ )
  {
    
    analogWrite ( motor [i] , estado [i] );
    digitalWrite ( motor [i], estado [i] );
    
  } 



}

void retroceder ()

{

//???

}

void frenar ()

{

//???

}

void detenerse ()

{


//???

}

///////////////////////////////////////////////////////////////

/* 2 ruedas giran y 2 ruedas se quedan quietas */
void girarDer ()
{
  String motor () = (motor1, motor2, motor2_1, motor2_2, motor1_2, motor1_1 );
  int motor []    = ( 170  , 170   ,  0      ,    0    ,    0    ,   1      );

  for (int i = 0 ; ??? ; i++ )
  {
    
    analogWrite ( motor [i] , estado [i] );
    digitalWrite ( motor [i], estado [i] );
    
  }

}

void girarIzq ()
{

//???

}

///////////////////////////////////////////////////////////////

/* Las ruedas giran en sentidos opuestos*/
void girarIzqEnSuEje ()
{
  
 //???
  
}

void girarDerEnSuEje ()
{
  
 //??? 
  
}

////////////////////////////////////////////////////////////////

bool movimiento ()
{
  
 // leer sensor de movimiento y devolver el dato. 
  
  
}
  
void comunicacion ()
{
  
 // enviar informacion al celular (control remoto del auto).
  leerMovimiento () ; // -> es true entonces
  
  // verificar si estamos recibiendo informacion del BT ( puerto de comunicacion del auto )
  // en cuanto no estemos recibiendo informacion le enviamos al auto
  
  Serial.write ("Hay un objeto delante.");
  
  delay (100);
  
}
  
  
  
