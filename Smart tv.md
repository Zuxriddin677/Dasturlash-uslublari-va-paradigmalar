#include<iostream>
#include<string.h>
#include<stdlib.h>
using namespace std; 
class printerlar{ 
 private : 
 string nomi,brendi,modeli; 
 int chop_etish_tezligi; 
 int ishlash_funksiyasi; 
 int chop_etish_turi; 
 float narxi; 
 public : 
  void show() 
  { 
   static int k=0; 
   cout<<++k<<" - nomi"<<endl<<endl; 
   cout<<"Brend nomi: "<<brendi<<endl;
   cout<<"Nomi: "<<nomi<<endl;  
   cout<<"Siz chopetish tezligini tanlang"<<chop_etish_tezligi<<endl; 
   cout<<"ishlash funksiyasi: "<<ishlash_funksiyasi<<endl; 
   cout<<"chop etish turi: "<<chop_etish_turi<<endl; 
   cout<<"Pozitsiyasi: "<<saloni<<endl; 
   cout<<"Narxi: "<<narxi<<endl; 
  }; 
  void input(){ 
   static int k=0; 

   cout<<++k<<" - mashina"<<endl<<endl; 
   cout<<"Avtosaloni: ";cin>>avtosaloni;
   cout<<"Nomi: ";cin>>nomi;  
   cout<<"Yili: ";cin>>yili; 
   cout<<"Diskasi: ";cin>>diskasi; 
   cout<<"Baloni: ";cin>>baloni; 
   cout<<"Pozitsiyasi: ";cin>>saloni; 
   cout<<"Narxi: ";cin>>narxi;
   cout<<endl; 
  }; 
  void qidir(string s){ 
   if(nomi.compare(s)==0) 
   { 
    cout<<"Bunday nomli mashina yuk"; 
    show(); 
   } 


}; 
void qidir1(string d){ 
   if(avtosaloni.compare(d)==0) 
   { 
    cout<<"Bunday avtosaloni mashina yuk"; 
    show(); 
   } 
  }; 
}; 
int main() 
{ 
 Car t[100]; 
 int N;cout<<"Mashina sonni kriting";cin>>N;  
 for(int i=0;i<N;i++) 
 { 
  t[i].input(); 
 } 
 string s; 
 cout<<endl<<"Qidiriliyotgan mashina nomini kriting";cin>>s; 
 for(int i;i<N;i++) 
 { 
  t[i].qidir(s); 
 } 
 string d; 
 cout<<endl<<"Qidiriliyotgan avtosaloni  kiriting";cin>>d; 

 for(int i;i<N;i++) 
 { 
  t[i].qidir1(d); 
 } 
}
