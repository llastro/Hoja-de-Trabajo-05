
#include <iostream>
#include <string>
#include <fstream>
#include <cctype>

using namespace std;

struct zonas{
  string descripcion;
  string codigo;
  float precio;
  int cantidad;
  float totalde;
} zona[3];

struct compras{
  string zona;
  int cantidad;
  bool miembro;
  float total;
};


void inicio_variables(){

  zona[0]={"VIP","V",350.00,0,0};
  zona[1]={"PLATEA","P",130.00,0,0};
  zona[2]={"POPULAR","E",50.00,0,0};
};

float calculo(string codigo, int cantidad, bool miembro){
  float total=0, descuento;
  int intzona=0;
  if ((codigo=="V") || (codigo=="v" )){
    intzona=0;
  } else if ((codigo=="P") || (codigo=="p")) {
    intzona=1;
  } else if ((codigo=="E") || (codigo=="e")) {
    intzona=2;
  } else {
    cout << "no hay nada" << endl;
  }

  total=cantidad*zona[intzona].precio;
  
  if ((cantidad>=3) and (cantidad<=6)){
    descuento=0.05;
  } else if ((cantidad>=7) and (cantidad<=9)){
    descuento=0.075;
  } else if (cantidad>9){
    descuento=0.10;
  } else {
    descuento=0;
  }
  total=total-(total*descuento);

  if (miembro==true) {
    total=total-(total*0.08);
  }

  return total;
};

void ingreso(){
    compras x;
  string var1;

  cout << "Ingrese la zona selecionada: ";
  cin >> x.zona;

  cout << "Ingrese la cantidad de boletas a comprar: ";
  cin >> x.cantidad;

  cout << "Es miembro : ";
  cin >> var1;

    if ((var1=="si") or (var1=="SI")) {
    x.miembro=true;
  } else {
    x.miembro=false;
  }

  x.total=calculo(x.zona, x.cantidad, x.miembro);

  string miem;
  if (x.miembro==true) {
    miem="s";
  } else {
    miem="n";
  }

  ofstream archivo("venta_boletos.txt", ios::app);

  archivo<<x.zona<< "\t" << x.cantidad << "\t" <<  miem << "\t" << x.total << "\n";

  archivo.close();

};

void leer(){
    inicio_variables();

    float totalde=0;
    int grancantidad=0;
    string miem;


    ifstream archivo;
    
    compras x;
  
      
   
        }

        
     totalde=totalde+x.total;
        grancantidad=grancantidad+x.cantidad;
      }

      string empty;
      getchar();
      getline(cin, empty);
      return;
    }
    catch (exception X){    
      cout<<"Error para abrir archivo"<<endl;     
      
      exit(1);
    }
};

void menu(){
  char tecla;
  string empty;
  bool bandera=false;
  
  do
    {
        system("clear");
        cin.clear();
        cout << "Venta de boletos" << endl;
        cout << "-----------" << endl << endl;
        cout << "\t1 .- Vender Boletos" <<endl;
        cout << "\t2 .- Mostrar Venta Global" <<endl;
        cout << "\t3 .- Salir" << endl << endl;
        cout << "Elije una opcion: ";
 
        cin >> tecla;
 
    
int main(){
  inicio_variables();
  menu();
  return 0;
}



