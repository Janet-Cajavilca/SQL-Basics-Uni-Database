# SQL Basics: Uni-Database Practice

This small project demonstrates my ability in fundamental SQL queries. I initially learned these skills during the lecture 'Database: Fundamentals' at TUM Munich, led by Professor Alfons Kemper. I will utilize Professor Kemper's compact University Database schema, initially in German, to implement some fundamental SQL queries. First, I'll translate the table names into English and create a small database using **PostgreSQL 16**. After that, I'll apply the basic SQL queries I've learned to solve the tasks listed below

--> Here is a graphic illustrating the **Uni-Database in German**


![Uni-database-German](https://github.com/Janet-Cajavilca/SQL/assets/93542752/605ad936-6b97-49df-a61c-fcd714658eef)


--> This is how the Uni-Database appears after translating into **English**:

![Uni-Database-english](https://github.com/Janet-Cajavilca/SQL/assets/93542752/289b2647-8bb3-4f59-9c03-2b499f1f1a5b)

# SQL Task List

1. **Create Tables:**
   students, professors, assistants, lectures, attend, prerequisites, and test in the UniDatabase.

2. **Insert Values:**
   Insert values into each of the created tables.

3. **Find Lectures with No Listeners:**
   Identify the lectures that have no listeners.

4. **Find Students Attending All Lectures:**
   Find the students who attend all lectures.

5. **Find Students Knowing Professor Sokrates:**
   Find the students who know Professor Sokrates from lecture(s).

6. **Find Students Attending Lectures with Fichte:**
   Find the students who attend lectures that Fichte also attends.

7. **Find Assistants of Professors for Student Carnap:**
   Find the assistants of professors who have taught the student Carnap, potentially as supervisors for his bachelor thesis.

8. **Professors Known by Theophrastos:**
   Provide the names of professors known by Theophrastos from lectures.

9. **Lectures Attended by Bachelor's Program Students:**
   Identify which lectures are attended by students in the bachelor's program (1st – 6th semester). Provide the titles of these lectures.

10. **Number of Students Attending Each Lecture:**
    Determine, for each lecture, how many students are attending it. Include lectures without attendees. Sort the results in descending order by the number of attendees.

11. **Promotion of C3 Professors to C4:**
    All professors with the rank C3 will be promoted to the rank C4. Set the rank of all C3 professors to C4.

12. **Delete Assistants with Field of Study in Planetary Movements:**
    The movements of planets are fully researched. Delete all assistants with this field of study.

13. **Create New Lecture "Foundations: Databases":**
    Create a new lecture with the name "Foundations: Databases" and the number 5278. Professor Curie holds the lecture, and it has "Logic" as a prerequisite. The lecture lasts for 4 SWS (semester weeks). Enroll the student with the matriculation number 28106 as a listener for the lecture.

# Solution

1. **Create Tables:**
   
![CreateTable](https://github.com/Janet-Cajavilca/SQL/assets/93542752/bee28f26-b02d-4842-918c-83f91c7b81d9)

2. **Insert Values:**
   Insert values into each of the created tables.

- Entering Data into the **students** Table
  
![CreateStudentTable](https://github.com/Janet-Cajavilca/SQL/assets/93542752/1be3e13b-da99-4b0b-a8db-63c49a9b0454)

-> Check the table:
  
![CheckCreatedStudentTable](https://github.com/Janet-Cajavilca/SQL/assets/93542752/03617462-fe17-4f2a-ab5e-c39bd2b21e13)

- Entering Data into the **professors** Table
  
![CreateProfessorsTable](https://github.com/Janet-Cajavilca/SQL/assets/93542752/f050062d-24a2-4dcc-9b8b-a54854ce3d99)

  
-> Check the table:

![CheckCreatedProfessorsTable](https://github.com/Janet-Cajavilca/SQL/assets/93542752/2976ca30-8cd5-4b57-8344-7772e2b2a692)

- Entering Data into the **assistant** Table
  
![CreateAssistantsTable](https://github.com/Janet-Cajavilca/SQL/assets/93542752/7002a63c-154d-409e-a2d9-a3ccb9f12ddf)

-> Check the table:

![CheckCreatedAssistantsTable](https://github.com/Janet-Cajavilca/SQL/assets/93542752/67fdfc88-21c3-4463-b385-485b48e2a076)


- Entering Data into the **lectures** Table

![CreateLecturesTable](https://github.com/Janet-Cajavilca/SQL/assets/93542752/9d728db1-67da-4b0c-889e-a09ff90422fe)

-> Check the table:

![CheckCreatedLecturesTable](https://github.com/Janet-Cajavilca/SQL/assets/93542752/c16190e9-cb42-4471-a97a-4ccb1937556e)


I realized I made a spelling mistake; I wrote 'tittle' instead of 'title.' For that reason, I corrected this by using the query **ALTER TABLE**

![CorrectSpellingTitle](https://github.com/Janet-Cajavilca/SQL/assets/93542752/2207eeea-08b2-4355-b8f7-2a50c1f9745c)

- Entering Data into the **attend** Table
  
![CreateAttendTable](https://github.com/Janet-Cajavilca/SQL/assets/93542752/2625e477-625f-452b-9db5-5a5d26d355c9)

-> Check the table:

![CheckCreatedAttendTable](https://github.com/Janet-Cajavilca/SQL/assets/93542752/56587d88-77ee-49b7-a747-1e27174d7cf8)

- Entering Data into the **prerequisites** Table

 ![CreatePrerequisitesTable](https://github.com/Janet-Cajavilca/SQL/assets/93542752/8e0b0e61-2101-44eb-aebb-fe7faacfdb5a)
 
-> Check the table:

![CheckCreatedPrerequisitesTable](https://github.com/Janet-Cajavilca/SQL/assets/93542752/6273457e-d6b2-42a2-bda8-c778a604c16f)

- Entering Data into the **test** Table
  
![CreateTestTable](https://github.com/Janet-Cajavilca/SQL/assets/93542752/9c022584-3d0b-44a1-9d41-3fef74ec4fe8)

-> Check the table:

![CheckCreatedTestTable](https://github.com/Janet-Cajavilca/SQL/assets/93542752/2fb7e402-b901-480e-b3c9-42a29b3c74be)

3. **Find Lectures with No Listeners:**
   Identify the lectures that have no listeners.

![LecturesWithNoListeners](https://github.com/Janet-Cajavilca/SQL/assets/93542752/b625ec18-cbcd-4038-8434-715b2bf15f12)

4. **Find Students Attending All Lectures:**
   Find the students who attend all lectures.

![StudentsAttendAllLectures](https://github.com/Janet-Cajavilca/SQL/assets/93542752/e149922a-9e23-47e5-87d5-adb98062aa45)

-> The rows are empty, which means there are no students who visit all lectures.

5. **Find Students Knowing Professor Sokrates:**
   Find the students who know Professor Sokrates from lecture(s).
   
![StudentsKnowProfSokrates](https://github.com/Janet-Cajavilca/SQL/assets/93542752/29c7f08e-7d23-4d6a-8c04-d5dd32a0ce4d)


6. **Find Students Attending Lectures with Fichte:**
   Find the students who attend lectures that Fichte also attends.
   
![StudentsSameLectureFichte](https://github.com/Janet-Cajavilca/SQL/assets/93542752/7ebb15fd-eab4-401f-8367-625aa20b9551)

7. **Find Assistants of Professors for Student Carnap:**
   Find the assistants of professors who have taught the student Carnap, potentially as supervisors for his bachelor thesis.

![StudentsMayHaveCarnapSupervisor](https://github.com/Janet-Cajavilca/SQL/assets/93542752/0a402465-85f2-4cb0-8e8f-f6b2d05e3ceb)

   
8. **Professors Known by Theophrastos:**
   Provide the names of professors known by Theophrastos from lectures.

![ProfessorsKnownByTheophrastos](https://github.com/Janet-Cajavilca/SQL/assets/93542752/4df6275b-bc7b-446d-a853-568b0dbc8437)

   
9. **Lectures Attended by Bachelor's Program Students:**
   Identify which lectures are attended by students in the bachelor's program (1st – 6th semester). Provide the titles of these lectures.

![LecturesByBachelorStudents](https://github.com/Janet-Cajavilca/SQL/assets/93542752/2fee4e7a-5ab7-4ecf-9d9e-83efbc98048a)

10. **Number of Students Attending Each Lecture:**
    Determine, for each lecture, how many students are attending it. Include lectures without attendees. Sort the results in descending order by the number of attendees.

![LecturesAndNumbAttends](https://github.com/Janet-Cajavilca/SQL/assets/93542752/ee1f45b4-e8e9-4723-b8e9-bdc48fdb182c)
  

11. **Promotion of C3 Professors to C4:**
    All professors with the rank C3 will be promoted to the rank C4. Set the rank of all C3 professors to C4.

-> Before changing the rank, I checked which professors have the rank C3.

![ChangeProfessorFromC3ToC4](https://github.com/Janet-Cajavilca/SQL/assets/93542752/53a83ff6-02b6-42f0-a307-93d00f7217cb)

-> Changing the Rank from C3 to C4

![UpdatingProfessorRankC3ToC4](https://github.com/Janet-Cajavilca/SQL/assets/93542752/51e5c996-56b6-4c16-9380-be0ce6deed51)

-> see the new results: 

![UpdatedResultsRankProfessors](https://github.com/Janet-Cajavilca/SQL/assets/93542752/2ccb25a4-74f7-4733-9518-2c449ffe4d44)

-> The professors Copernicus, Popper, and Augustine have now a rank of C4.



12. **Delete Assistants with Field of Study in Planetary Movements:**
    The movements of planets are fully researched. Delete all assistants with this field of study.

    ![image](https://github.com/Janet-Cajavilca/SQL/assets/93542752/3876ac24-0ce3-4700-a42b-bf677bf5ed55)


13. **Create New Lecture "Foundations: Databases":**
    Create a new lecture with the name "Foundations: Databases" and the number 5278. Professor Curie holds the lecture, and it has "Logic" as a prerequisite. The lecture lasts for 4 SWS (semester weeks). Enroll the student with the matriculation number 28106 as a listener for the lecture.


Before solving this assignment, we need the personnel number for Professor Curie, and we also need the number of the lecture 'Logic

->  What is the personnel number for Professor Curie?

![image](https://github.com/Janet-Cajavilca/SQL/assets/93542752/86014e4e-679e-4c7f-9069-b3ca2207f5ed)

->  What is the number of the lecture 'Logic'?

![NumberOfLectureLogic](https://github.com/Janet-Cajavilca/SQL/assets/93542752/4f0ba5c3-2705-4fba-9c72-431ceeabfa89)

-> Now that we know that the personal number of Professor Curie is 2136 and the Number of the lecture 'Logic' is 4052 we can solve the assignment.

![CreateNewLectureAndUpdateData](https://github.com/Janet-Cajavilca/SQL/assets/93542752/5b24fb3b-9604-4620-a592-e486a91865da)


