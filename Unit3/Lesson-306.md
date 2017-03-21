Objectives Students will be able to…

-   **Write** programs that accept user input using a scanner object.

Assessments Students will...

-   **Complete** Practice-It problems

Homework Students will...

-   **Outline** Chapter 3, except for HW 3.4

Materials & Prep
================

-   **Projector and computer**

-   **Whiteboard and** **markers**

Pacing Guide
============

| Section                                 | Total Time |
|-----------------------------------------|------------|
| Bell-work and attendance                | 5min       |
| Introduction to interactive programming | 15min      |
| Student practice                        | 35min      |

Procedure
=========

Bell-work and Attendance \[5 minutes\]
--------------------------------------

Introduction to Interactive Programming \[10 minutes\]
------------------------------------------------------

1. Hook the students with a brief discussion about Pokemon. Be sure that the following points come up during discussion (either you bring them up, or you guide the students to bring these points up themselves):

-   EV (experience values) are gained through combat. When one Pokemon wins against another, they win EV points to raise your stats.

-   These stats are private, the trainer (user) cannot see them.

-   If you want to know what your EV value is (so you can determine strategy and gain the most points), you need to compute it yourself given the values that you can see.

-   The formula for calculating HP is on Bulbepedia, and if we do some algebra we can calculate EV. Let’s write a program that will help us calculate EV for any Pokemon stats a trainer enters.

2. Have a student (or sequential students) come to the board to write the console output as you work through the example below. You should have students write and label this sample program as you write it. While discussing the different parts of the program, circle the room, checking to make sure students are keeping up with the notes.

-   Write a method that reads user input for known Pokemon stats to determine EV (effort value).

> **import java.util.\*;**

-   Anytime you’re getting user input, start with this import declaration (highlighted).

> public class GetEV {
>
> public static void main(String\[\] args) {
>
> **Scanner userInput = new Scanner (System.in);**

-   So far, the headers look familiar. When constructing the scanner (highlighted):

> 1. You always capitalize Scanner
>
> 2. Name the scanner something useful (scanner, console, userInput)
>
> 3. Construct with the NEW keyword, and System.in.
>
> System.out.println(“This program calculates user EV.”);
>
> System.out.println(“Input your Pokemon’s stats below:”);

-   This outputs to the console a message explaining the program to the user.

> System.out.print(“Hit points: ”);
>
> int hp = **userInput**.nextInt();

-   This pairs a user prompt with a variable hp that holds the information the user inputted.

> System.out.print(“Level: “);
>
> int level = userInput.nextInt();

-   Again, we pair the prompt for the user input with the scanner that accepts and stores that data as a variable for later use.

> System.out.print(“IV: “); This is for initial value of the hit point stat
>
> int iv = userInput.nextInt();
>
> System.out.print(“Base HP: “);
>
> int base = userInput.nextInt();

-   Next we need to write the formula that will calculate EV from the user input, then return a value (otherwise the scanner has no function!) You should have the students build as much of this formula as possible:

EV = (((HP – 10) \* 100) / Level – 2\*Base – IV – 100) \* 4

> int ev = (((hp – 10) \* 100)/level – 2 \* base – iv – 100) \* 4;
>
> System.out.println(“You have ” + ev + “ effort value points for your HP stat.”);
>
> }

}

-   If students need another example, work through the book example for mortgage payments, having students write more of the code than in the previous example.

Student Practice \[35 minutes\]
-------------------------------

1. Have students complete the following Practice-It self-check questions:

a. promptMultiplyBy2

b. SumNumbers

c. RobertPaulson

2. Have students complete the following Practice-It example questions:

a. scientific

b. cylinderSurfaceArea

c. sphereVolume

Accommodation and Differentiation
=================================

In ELL classrooms, you should distribute a handout diagramming the parts of a program with all vocabulary words included on the sample code or screenshot. Turning the pictures on the worksheet into classroom posters will be helpful in helping students remember syntax.