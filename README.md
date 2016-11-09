# Report-Card-Calculator2
java import

import java.util.Scanner;

public class GPA4
{
	public static void main(String args[])
	{
		Scanner in = new Scanner(System.in);
		
		System.out.println("REPORT CARD CALCULATOR");
		System.out.println(" ");
		
		System.out.print("What is your first numeric grade? ");
		double gr1 = in.nextDouble(); // to the right is a method
		String let1 = letterGrade(gr1); // same here
		double pts1 = points(gr1);
					
		System.out.print("What is your second numeric grade? ");
		double gr2 = in.nextDouble();
		String let2 = letterGrade(gr2);
		double pts2 = points(gr2);

		System.out.print("What is your third numeric grade? ");
		double gr3 = in.nextDouble();
		String let3 = letterGrade(gr3);
		double pts3 = points(gr3);

		System.out.print("What is your fourth numeric grade? ");
		double gr4 = in.nextDouble();
		String let4 = letterGrade(gr4);
		double pts4 = points(gr4);

		System.out.print("What is your fifth numeric grade? ");
		double gr5 = in.nextDouble();
		String let5 = letterGrade(gr5);
		double pts5 = points(gr5);
	
		System.out.print("What is your sixth numeric grade? ");
		double gr6 = in.nextDouble();
		String let6 = letterGrade(gr6);
		double pts6 = points(gr6);

		System.out.print("What is your seventh numeric grade? ");
		double gr7 = in.nextDouble();
		String let7 = letterGrade(gr7);
		double pts7 = points(gr7);

		System.out.println("	");
		System.out.println("      " + "Class" + "	" + "Numeric Grade" + "		" + "Letter Grade" + "		" + "GPA");	
		System.out.println("Grade: 1 "	+ "	" + gr1	+ "			" + let1 + "			" + pts1);
		System.out.println("Grade: 2 "	+ "	" + gr2	+ "			" + let2 + "			" + pts2);
		System.out.println("Grade: 3 "	+ "	" + gr3	+ "			" + let3 + "			" + pts3);
		System.out.println("Grade: 4 "	+ "	" + gr4	+ "			" + let4 + "			" + pts4);
		System.out.println("Grade: 5 "	+ "	" + gr5	+ "			" + let5 + "			" + pts5);
		System.out.println("Grade: 6 "	+ "	" + gr6	+ "			" + let6 + "			" + pts6);
		System.out.println("Grade: 7 "	+ "	" + gr7	+ "			" + let7 + "			" + pts7);
		
		System.out.println(" ___________________________________________________________________"); //aesthetics 

		double average = averageAll(gr1, gr2, gr3, gr4, gr5, gr6, gr7);
		System.out.printf("Overall Average " + "%2f", average); //ask why this isn't working

		String letavg = averageLet(average);
		System.out.print("		" + letavg);

		double gpaavg = averageGpa(average);
		System.out.print("			" + gpaavg);
		
	}
	public static String letterGrade(double grade)
	{
		if ((grade >= 97) && (grade <= 100))
			return "A+";
		else if ((grade >= 93) && (grade <= 96))
			return "A";
		else if ((grade >= 90) && (grade <= 92)) 				
			return "A-";
		else if ((grade >= 87) && (grade <= 89))
			return "B+";
		else if ((grade >= 83) && (grade <= 86))
			return "B";
		else if ((grade >= 80) && (grade <= 82))
			return "B-";
		else if ((grade >= 77) && (grade <= 79))
			return "C+";
		else if ((grade >= 73) && (grade <= 76))
			return "C";
		else if ((grade >= 70) && (grade <= 72))
			return "C-";
		else if ((grade >= 67) && (grade <= 69))
			return "D+";	
		else if ((grade >= 63) && (grade <= 66))
			return "D";
		else if ((grade >= 60) && (grade <= 62))
			return "D-";
		else return "F";
	}
	public static double points(double gpa)
	{
		if ((gpa >= 97) && (gpa <= 100))
			return 4.0; // no quotes around "4.0"
		else if ((gpa >= 93) && (gpa <= 96))
			return 4.0;
		else if ((gpa >= 90) && (gpa <= 92)) 				
			return 3.7;
		else if ((gpa >= 87) && (gpa <= 89))
			return 3.3;
		else if ((gpa >= 83) && (gpa <= 86))
			return 3.0;
		else if ((gpa >= 80) && (gpa <= 82))
			return 2.7;
		else if ((gpa >= 77) && (gpa <= 79))
			return 2.3;
		else if ((gpa >= 73) && (gpa <= 76))
			return 2.0;
		else if ((gpa >= 70) && (gpa <= 72))
			return 1.7;
		else if ((gpa >= 67) && (gpa <= 69))
			return 1.3;	
		else if ((gpa >= 63) && (gpa <= 66))
			return 1.0;
		else if ((gpa >= 60) && (gpa <= 62))
			return 1.0;
		else return 0.0;
	}
	public static double averageAll(double gr1, double gr2, double gr3, double gr4, double gr5, double gr6, double gr7)
	{
		double allavg = ((gr1 + gr2 + gr3 + gr4 + gr5 + gr6 + gr7) / 7);
		return allavg;
	}
	public static String averageLet(double average)
	{
		if ((average >= 97) && (average <= 100))
			return "A+";
		else if ((average >= 93) && (average <= 96))
			return "A";
		else if ((average >= 90) && (average <= 92)) 				
			return "A-";
		else if ((average >= 87) && (average <= 89))
			return "B+";
		else if ((average >= 83) && (average <= 86))
			return "B";
		else if ((average >= 80) && (average <= 82))
			return "B-";
		else if ((average >= 77) && (average <= 79))
			return "C+";
		else if ((average >= 73) && (average <= 76))
			return "C";
		else if ((average >= 70) && (average <= 72))
			return "C-";
		else if ((average >= 67) && (average <= 69))
			return "D+";	
		else if ((average >= 63) && (average <= 66))
			return "D";
		else if ((average >= 60) && (average <= 62))
			return "D-";
		else return "F";
	}
	public static double averageGpa(double average)
	{
		if ((average >= 97) && (average <= 100))
			return 4.0; // no quotes around "4.0"
		else if ((average >= 93) && (average <= 96))
			return 4.0;
		else if ((average >= 90) && (average <= 92)) 				
			return 3.7;
		else if ((average >= 87) && (average <= 89))
			return 3.3;
		else if ((average >= 83) && (average <= 86))
			return 3.0;
		else if ((average >= 80) && (average <= 82))
			return 2.7;
		else if ((average >= 77) && (average <= 79))
			return 2.3;
		else if ((average >= 73) && (average <= 76))
			return 2.0;
		else if ((average >= 70) && (average <= 72))
			return 1.7;
		else if ((average >= 67) && (average <= 69))
			return 1.3;	
		else if ((average >= 63) && (average <= 66))
			return 1.0;
		else if ((average >= 60) && (average <= 62))
			return 1.0;
		else return 0.0;
	}
}
