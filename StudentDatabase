import java.util.ArrayList;
import java.util.Collections;
import java.util.Scanner;

class StudentDatabase{

    public static void main(String[] args) {

        ArrayList <Student>list = new ArrayList<Student>();
        Scanner sc = new Scanner(System.in);
        boolean continues = true;
        while (continues){
        System.out.println("Enter Student name");

        String name=sc.nextLine();
            System.out.println("Enter Student City");
            String city=sc.next();

            System.out.println("Enter Student age");
            int age=sc.nextInt();
            sc.nextLine();
            Student student = new Student(name,age,city);
            list.add(student);
            System.out.println("Want to continue??Y/N");
            char ch=sc.next().charAt(0);
            if(ch =='Y'||ch=='y'){
                continues=true;
                sc.nextLine();
            }else{
                continues=false;
            }
        }
        System.out.println("The Objects are:");
        for(Student std : list){
            System.out.println(std);
        }

        boolean continues2 = true;
        while (continues2){
            System.out.println("1. Sort by first name");
            System.out.println("2. Sort by Last name");
            System.out.println("3. Sort by Age");
            System.out.println("4. Sort by city");
            System.out.println("5. Exit");
            int ch=sc.nextInt();
            switch (ch){
                case 1:
                Collections.sort(list, new SortByFName());
                    System.out.println("The Sorted Objects are:");
                    for(Student std : list){
                        System.out.println(std);
                    }
                break;
                case 2:
                    Collections.sort(list, new SortByLName());
                    System.out.println("The Sorted Objects are:");
                    for(Student std : list){
                        System.out.println(std);
                    }
                    break;
                case 3:
                    Collections.sort(list, new SortByAge());
                    System.out.println("The Sorted Objects are:");
                    for(Student std : list){
                        System.out.println(std);
                    }
                    break;
                case 4:
                    Collections.sort(list, new SortByCity());
                    System.out.println("The Sorted Objects are:");
                    for(Student std : list){
                        System.out.println(std);
                    }
                    break;
                default:
                    continues2=false;
                    break;
            }
        }
    }
}


class Student{
    String name, city,LName="",FName="";
    int age;


    Student(String name, int age, String city){
        this.name = name;
        this.age = age;
        this.city = city;
    }

    void setLname(){
        if(name.contains(" ")){
            int index=name.indexOf(" ");
            this.LName=name.substring(index);
        }

    }
    void setFname(){
        if(name.contains(" ")){
           FName= name.substring(0, name.lastIndexOf(' '));
        }else{
            this.FName=name;
        }
    }


    public String getName() {
        return name;
    }

    public String getFName() {
        setFname();
        return FName;
    }

    public String getLName() {
        setLname();
        return LName;
    }

    Integer getAge(){
        return this.age;
    }

    String getCity(){
        return this.city;
    }


    @Override
    public String toString(){
        return "Student Object for "+ this.getName()+" : " + this.getFName()+ this.getLName() + " "+this.getAge() + ", " + this.getCity();
    }
}

// Separate class for sorting using : Comparator
class SortByFName implements java.util.Comparator<Student>{
    @Override
    public int compare(Student first, Student second){
        return first.getFName().compareTo(second.getFName());
    }
}

class SortByLName implements java.util.Comparator<Student>{
    @Override
    public int compare(Student first, Student second){
        return first.getLName().compareTo(second.getLName());
    }
}

class SortByAge implements java.util.Comparator<Student>{
    @Override
    public int compare(Student first, Student second){
        return first.getAge().compareTo(second.getAge());
    }
}

class SortByCity implements java.util.Comparator<Student>{
    @Override
    public int compare(Student first, Student second){
        return first.getCity().compareTo(second.getCity());
    }
}
