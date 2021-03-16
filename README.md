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










class Vector3D{
	double x,y,z;
	public:
		Vector3D(double,double,double);
		void show();
		double abs();
		void scale(double );
		Vector3D operator+(const Vector3D &);
		bool operator||(const Vector3D &);
};

Vector3D::Vector3D(double a = 0,double b = 0,double c = 0){
	x = a; y = b; z = c; 
}

void Vector3D::show(){
	cout << "[" << x << ", " << y << ", " << z << "]\n";
}
double Vector3D::abs(){
    return sqrt(pow(x,2)+pow(y,2)+pow(z,2));
}
void Vector3D::scale(double a){
    x=x*a;
    y=y*a;
    z=z*a;
}
Vector3D Vector3D::operator+(const Vector3D &a){
    return Vector3D(a.x+x,a.y+y,a.z+z);
}
bool Vector3D::operator||(const Vector3D &a){
   Vector3D t(x,y,z);
    if((a.x==0&&a.y==0&&a.z==0)||(x==0&&y==0&&z==0)){
        return false;
    }else{
        if(a.x==t.x&&a.y==t.y&&a.z==t.z){
            return true;
        }else{
            if(a.x/t.x==a.y/t.y&&a.x/t.x==a.z/t.z&&a.y/t.y==a.z/t.z){
                return true;
            }else{
                return false;
            }
        }
    }
    
}



