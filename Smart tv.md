#include<iostream>
#include<string.h>
#include<stdlib.h>
using namespace std;
class Modem{
  private:
    string nomi, modeli,
    qabul_qilish_tezligi, uzatish_tezligi,
    funksiyasi, diapazonni, ulanishlar_soni;
    int narxi;  
    float ishlab_chiqarilgan_davlati;

  public:
    void show(){
      static int k=0;
      cout<<++k<<" - modem: "<<endl<<endl;
      cout<<"Nomi: "<<nomi<<endl;
      cout<<"Modeli: "<<modeli<<endl;
      cout<<"qabul_qilish_tezligi: "<<qabul_qilish_tezligi<<endl;
      cout<<"uzatish_tezligi: "<<uzatish_tezligi<<endl;
      cout<<"funksiyasi: "<<funksiyasi<<endl;  
      cout<<"diapazonni: "<<diapazonni<<endl;
      cout<<"Narxi: "<<narxi<<endl;
      cout<<"Ishlab_chiqarilgan_davlati: "<<ishlab_chiqarilgan_davlati<<endl;      
    };
    void input(){
      static int k=0;
      cout<<++k<<" - Modem: "<<endl;
      cout<<"Nomi: "; cin>>nomi;
      cout<<"Modeli: "; cin>>modeli;
      cout<<"qabul_qilish_tezligi: "; cin>> qabul_qilish_tezligi;
      cout<<"uzatish_tezligi: "; cin>> uzatish_tezligi;  
      cout<<"funksiyasi: "; cin>>funksiyasi;
      cout<<"diapazonni: "; cin>>diapazonni;
      cout<<"Narxi: "; cin>>narxi;
      cout<<"Ishlab_chiqarilgan_davlati: "; cin>>ishlab_chiqarilgan_davlati;
      cout<<endl;
    };
    void qidir(string s){
      int k;cout<<"Modem"<<endl;
      cout<<"Nomi: "<<nomi<<endl;
      cout<<"Modeli: "<<modeli<<endl;
      cout<<"qabul_qilish_tezligi: "<<qabul_qilish_tezligi<<endl;
      cout<<"uzatish_tezligi: "<<uzatish_tezligi<<endl;
      cout<<"funksiyasi: "<<funksiyasi<<endl;  
      cout<<"diapazonni: "<<diapazonni<<endl;
      cout<<"Narxi: "<<narxi<<endl;
      cout<<"Ishlab_chiqarilgan_davlati: "<<ishlab_chiqarilgan_davlati<<endl;  
        cout<<"Bunday mahsulot mavjud: "<<endl;
        show();  
    };  
};
int main(){
   Modem t[100];
   int N; cout<<" Modem nomini kiriting: "; cin>>N;
   for(int i=0; i<N; i++){
    t[i].input();
   }
   string s;
   cout<<endl<<"Qidirilayotgan modem nomini kiriting: "; cin>>s;
   for(int i=0; i<N; i++){
    t[i].qidir(s);
   }   
}
