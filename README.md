#include<iostream>
#include<string.h>
#include<stdlib.h>
using namespace std; 
class Car{ 
 private : 
 string nomi,avtosaloni,diskasi; 
 int yili; 
 int baloni; 
 int saloni; 
 float narxi; 
 public : 
  void show() 
  { 
   static int k=0; 
   cout<<++k<<" - mashina"<<endl<<endl; 
   cout<<"Avtosaloni: "<<avtosaloni<<endl;
   cout<<"Nomi: "<<nomi<<endl;  
   cout<<"Yili: "<<yili<<endl; 
   cout<<"Diskasi: "<<diskasi<<endl; 
   cout<<"Baloni: "<<baloni<<endl; 
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
