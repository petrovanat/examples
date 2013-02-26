#include <iostream>
#include <vector>
#include <cmath>

using namespace std;

class GeometricalFigures
{
   public:

    virtual void display(){};

   virtual float area()
   {
       return 0;
   }

};

class Circle:public GeometricalFigures
{
    public:
    Circle()
    {
        rad_of_circle=0;
    }
    float rad_of_circle;

   virtual float area()
   {
       float surface=0;
       float p=3.14;
       surface=p*pow(rad_of_circle,2);
       return surface;

   }
   virtual void display()
   {
       cout<<"circle: "<<"radius= "<<rad_of_circle<<" "<<"surface= "<<area()<<endl;
   }

};

class Cube:public GeometricalFigures
{
    public:
    Cube()
    {
    s_of_cube=0;
    }
    float s_of_cube;

    virtual float area()

   {
       float surface=0;
       surface=pow(s_of_cube,3);
       return surface;

   }
  virtual void display()
   {
       cout<<"cube: " <<"side= "<<s_of_cube<<" "<<"surface= "<<area()<<endl;
    }

};

class Rhombus:public GeometricalFigures
{
    public:
    Rhombus()
    {
        length_rhombus=0;
        height_rhombus=0;
    }

    float length_rhombus;
    float height_rhombus;

  virtual float area()
   {
       float surface=0;
       surface=length_rhombus*height_rhombus;
       return surface;

   }
  virtual void display()
  {

      cout<<"rhombus: "<<"length= "<<length_rhombus<<" "<<"height= "<<height_rhombus<<" "<<"surface= "<<area()<<endl;
  }


};

class Triangle:public GeometricalFigures
{
    public:
    Triangle()
    {
        base_triangle=0;
        height_triangle=0;
    }
    float base_triangle;
    float height_triangle;

   virtual float area()
   {

       float surface=0;
       surface=0.5*base_triangle*height_triangle;
       return surface;
   }
  virtual void display()
   {
       cout<<"triangle: "<<"base= "<<base_triangle<<" "<<"height= "<<height_triangle<<" surface: "<<area()<<endl;
   }


};


int main()
{

    vector<GeometricalFigures*>myarray;
    int number_of_figures=0;
    float total_area=0;
    int count=0;
    cout << "How many figures do you want to enter?"<< endl;
    cin>>number_of_figures;

    int type=0;
    while(count<number_of_figures)
    {
    cout<<"Please, enter the type of your figure and parameters. Press 1 for a circle, 2 for a cube, 3 for a rhombus, 4 for a triangle :"<<endl;
    cin>>type;

        if(type==1)
        {
            float rad=0;
            cout<<"please, enter the radius of your circle:"<<endl;
            cin>>rad;
  		Circle * myCirclePtr = new Circle();
            myCirclePtr->rad_of_circle=rad;
            myCirclePtr->area();
            myarray.push_back(myCirclePtr);


        }
        if(type==2)
        {
            float side=0;
            cout<<"please, enter the side of your cube:"<<endl;
            cin>>side;
            Cube * myCubePtr = new Cube();
  		myCubePtr->s_of_cube=side;
            myCubePtr->area();
            myarray.push_back(myCubePtr);


        }
        if(type==3)
        {
            float length=0;
            float height=0;
            cout<<"please, enter the lengt and the height:"<<endl;
            cin>>length>>height;
  		Rhombus * myRhombusPtr = new Rhombus();

            myRhombusPtr->length_rhombus=length;
            myRhombusPtr->height_rhombus=height;
            myRhombusPtr->area();
            myarray.push_back(myRhombusPtr);


        }
        if(type==4)
        {
            float base=0;
            float height=0;
            cout<<"please, enter the base and the height:"<<endl;
            cin>>base>>height;
  		Triangle * myTrianglePtr = new Triangle();
  		myTrianglePtr->base_triangle=base;
            myTrianglePtr->height_triangle=height;
            myTrianglePtr->area();
            myarray.push_back(myTrianglePtr);


        }


        count++;
    }
    for(int i=0;i<myarray.size();i++)
    {

  	myarray[i]->display();
    }

    for(int i=0;i<myarray.size();i++)
    {
        total_area+=myarray[i]->area();

    }
    cout<<"TOTAL AREA IS:"<<total_area<<endl;
    return 0;
}
