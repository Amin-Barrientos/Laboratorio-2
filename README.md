#include <iostream>
using namespace std;
float potencia(float x, float num, float &result);
int factorial(int x);
float serie(float x, float n);
int main()
{
    int op, Factorial;
    float base, exponente, x, n, r;
    do{
        cout<<"MENU"<<endl;
        cout<<"1. Potencia"<<endl;
        cout<<"2. Factorial"<<endl;
        cout<<"3. Serie"<<endl;
        cout<<"0. SALIR"<<endl;
        cin>>op;
        switch(op)
        {
        case 1: cout<<"Digite la base"<<endl; cin>>base;
                cout<<"Digite el exponente"<<endl; cin>>exponente; 
                cout<< "La potencia es"<<potencia(base, exponente, r)<<endl;
                break;
        case 2: cout<<"Factorial de:"<<endl; cin>>Factorial;
                cout<<"El factorial de: "<< Factorial <<" es: "<< factorial(Factorial)<<endl;
                break;
        case 3: cout<<"Digite el valor de x: "<<endl; cin>>x;
                cout<<"Digite el valor de n: "<<endl; cin>>n;
                cout<<"EL resultado de la serie es: "<<serie(x, n)<<endl;
        break;
        case 0: cout<<"SALIENDO...";
                break;
        default:cout<<"Opcion no valida, seleccione las que se muestran en pantalla";
                break;
        }
    }while(op!=0);
    

    return 0;
}
float potencia(float x, float num, float&n)
{
    n=1;
    for(int i=1; i<=num; i++)
    n=n*i;
    
    return n;
}
int factorial(int x)
{
    float fact=1;
    for(int i=1; i<=x; i++)
    
    fact=fact*i;
    
    return fact;
}
float serie(float x, float n)
{
    int total = 0;
    float z;
    for(int i=0; i<=n; i++)
    {
        potencia(x, i, z);
        total=total + (z / factorial(i));
    }
   
    total = total + 3;
    return total;
}
-------------------------------------------------------------------------
#include <iostream>
using namespace std;

void s(float a, float b);
void r(float a, float b);
void m(float a, float b);

int main()
{
    float num1, num2;
    int op;
    do{
        cout<<"MENU DE OPERACIONES"<<endl;
        cout<<"1. SUMA"<<endl;
        cout<<"2. RESTA"<<endl;
        cout<<"3. MULTIPLICAR"<<endl;
        cout<<"0. SALIR"<<endl;
        cin>>op;
        switch(op)
        {
            case 1: cout<<"Digite el primer numero"; cin>>num1;
            cout<<"Digite el segundo numero"; cin>>num2;
            s(num1, num2);
            break;
             case 2: cout<<"Digite el primer numero"; cin>>num1;
            cout<<"Digite el segundo numero"; cin>>num2;
            r(num1, num2);
            break;
             case 3: cout<<"Digite el primer numero"; cin>>num1;
            cout<<"Digite el segundo numero"; cin>>num2;
            m(num1, num2);
            break;
            case 0: cout<<"SALIENDO DEL PROGRAMA...";
            break;
            default: cout<<"Opcion no valida, ingrese una de las opciones que se muestran en pantalla";
            break;
        }
    }while (op!=0);
    

    return 0;
}

void s(float a, float b)
{
    cout<<"La suma de"<< a << "y"<< b <<"es: " <<   (a+b)<<endl;
}
void r(float a, float b)
{
    cout<<"La resta de"<< a << "y"<< b << "es:"<<   (a-b)<<endl;
}
void m(float a, float b)
{
    cout<<"La multiplicacion de"<< a << "y"<< b << "es:"<<   (a*b)<<endl;
}
    
