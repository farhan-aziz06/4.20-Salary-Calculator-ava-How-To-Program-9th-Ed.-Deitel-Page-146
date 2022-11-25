# 4.20-Salary-Calculator-ava-How-To-Program-9th-Ed.-Deitel-Page-146
Java Program To Find The Salary of Three Employee 

(Salary Calculator) Develop a Java application that determines the gross pay for each of
        three employees.

The company pays straight time for the first 40 hours worked by each employee
and time and a half for all hours worked in excess of 40.


You’re given a list of the employees, their number of hours worked last week and their hourly rates.

Your program should input this information for each employee,

then determine and display the employee’s gross pay. Use class Scanner to input the data.



import java.util.Scanner;

public class Main {
    public static void main(String[] args){
     
        Scanner console = new Scanner(System.in);

        int HourlyRate;
        double WorkingHours;

        System.out.println("Enter Hourly Pay Rate: ");
        HourlyRate = console.nextInt();


        int Employee;

        Employee=1;

        while (Employee< 4){

            System.out.println("Enter Working Hour of Employee "+ Employee);
            WorkingHours = console.nextInt();

            if (WorkingHours <= 40){
                double Pay = HourlyRate*WorkingHours;
                System.out.println(" Pay of Employee " + Employee + " is: "+ Pay);
            } else if (WorkingHours>40) {
                double ExtraHours = WorkingHours - 40;

                double Pay = (HourlyRate*40)+(ExtraHours*(int)(HourlyRate/2));
                System.out.println(" Pay of Employee " + Employee + " is: "+ Pay);
            }
            Employee++;
        }
    }
}
