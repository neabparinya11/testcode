# testcode
























class People{
    string name;
    char gender;
    int age;
    public:
        People(string ,char ,int );
        void show();
};

People::People(string nm="Tony",char ge='M',int ag=69){
    name=nm;
    gender=ge;
    age=ag;
}
void People::show(){
    cout<<"----------------------------------\n";
    cout<<"NAME: "<<name<<"\n";
    if(gender=='M'||gender=='m'){cout<<"GENDER: "<<"MALE"<<"\n";;
    }else if(gender=='F'||gender=='f'){cout<<"GENDER: "<<"FEMALE"<<"\n";;
    }else{
    cout<<"GENDER: "<<"UNKNOWN"<<"\n";;
    }
    
    cout<<"AGE: "<<age<<" years\n";
    cout<<"----------------------------------\n";
}








