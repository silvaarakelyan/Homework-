#include<iostream>
#include<string>
using namespace std;

class Date{
    public:
        int day;
        string month;
        int year;
    
    public:
        Date();
        void initialize_date(int d, int m, int y);
        string get_formatted_date();
};

Date::Date(){
        day=1;
        month=1;
        year=1900;
}

void Date::initialize_date(int d, int m, int y){
    
        if((m>0)&&(m<13)){
            if(m==1){
                month="Jenuary";}
            else if(m==2){
                month="February";}
            else if(m==3){
                month="March";}
            else if(m==4){
                month="April";}
            else if(m==5){
                month="May";}
            else if(m==6){
                month="June";}
            else if(m==7){
                month="July";}
            else if(m==8){
                month="August";}
            else if(m==9){
                month="September";}
            else if(m==10){
                month="October";}
            else if(m==11){
                month="November";}
            else if(m==12){
                month="December";}
        }
        
        else {cout<<"Month is not right"<<endl;}

        
        if ((d>0)&&(d<32)){
                day=d;}
            else { cout<<"Day is not right"<<endl; 
             
             }
      
        if(y>0){
                year=y;}
            else{  cout<<"input right year"<<endl;}

        
        if ((d>0)&&(d<32)){
                day=d;}
            else { cout<<"Day is not right"<<endl; 
             
             }
      
        if(y>0){
                year=y;}
            else{  cout<<"input right year"<<endl;}
    }
    
string Date::get_formatted_date(){
    return  to_string(day)+","+ month+"_" +to_string(year);
    
}

class Student{
    private:
        string first_name;
        string last_name;
        string faculty;
        Date birth_date;
        string ID;
        string ID_number;
    
    public:
        static int ID_counter;
        Student(string name1, string name2, string faculty1);
        void set_name(string name1, string name2);
        void set_birth_date(int day1, int month1, int year1); 
        Student(Student&obj);
        string get_birth_date();
        string get_firstname();
        string get_lastname();
        string get_ID();
    

    
};

Student::Student(string name1, string name2, string faculty1){
    faculty=faculty1;
    ++ID_counter;
    ID_number=to_string(ID_counter);
    ID="AUA_"+faculty+" "+ID_number;

    set_name( name1, name2);
}

void Student::set_name(string name1, string name2){
    first_name=name1;
    last_name=name2;
}

void Student::set_birth_date(int day1, int month1, int year1){
    birth_date.initialize_date(day1, month1, year1);

    
}

Student::Student(Student &obj){
    faculty=obj.faculty;
     ++ID_counter;
    ID_number=to_string(ID_counter);
    ID="AUA_"+faculty+" "+ID_number;
    
}

string Student::get_birth_date(){
    string bd=birth_date.get_formatted_date();

    return bd;
}


string Student::get_firstname(){
    return first_name;
}

string Student::get_lastname(){
    return last_name;
}

string Student::get_ID(){
    return ID;
}
    
int Student::ID_counter=0;


int main(){
    Student S("Aram","Grigoryan","CS");
    S.set_birth_date(12,7,1995);
    
    Student D(S);
    D.set_name("Anna","Sargsyan");
    D.set_birth_date(1,5,1995);
    
    cout<<"Bellow is the information about registered students"<<endl;
    cout<<S.get_firstname()<<" "<<S.get_lastname()<<" "<<S.get_ID()<<endl;
    cout<<S.get_birth_date()<<endl;
    
     cout<<D.get_firstname()<<" "<<D.get_lastname()<<" "<<D.get_ID()<<endl;
    cout<<D.get_birth_date()<<endl;
    
}
    
