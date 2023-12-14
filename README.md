# SQL Insights: Uni-Database Showcase

This project demonstrates my ability in fundamental SQL queries. I initially learned these skills during the 'Datenbanken Grundlagen' lecture at TUM Munich, led by Professor Alfons Kemper. I will use Professor Kemper's University Database, originally in German. I'll translate the table names into English and create a small database using **PostgreSQL 16**. After that, I'll apply the basic SQL queries I've learned

--> Here is a graphic illustrating the Uni-Database in German


![Uni-database-German](https://github.com/Janet-Cajavilca/SQL/assets/93542752/605ad936-6b97-49df-a61c-fcd714658eef)


--> This is how the Uni-Database appears after translating the German terminology into English:

![Uni-Database-english](https://github.com/Janet-Cajavilca/SQL/assets/93542752/289b2647-8bb3-4f59-9c03-2b499f1f1a5b)

# SQL Task List

1. **Create Tables:**
   - students
   - professors
   - assistants
   - lectures
   - attend
   - prerequisites
   - test
   
   Using PostgreSQL in the UniDatabase.

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

- Entering Data into the **student's Table**
  
![CreateStudentTable](https://github.com/Janet-Cajavilca/SQL/assets/93542752/1be3e13b-da99-4b0b-a8db-63c49a9b0454)

-> Check the table:
  
![CheckCreatedStudentTable](https://github.com/Janet-Cajavilca/SQL/assets/93542752/03617462-fe17-4f2a-ab5e-c39bd2b21e13)


- Entering Data into the **professor's Table**
  
![CreateProfessorsTable](https://github.com/Janet-Cajavilca/SQL/assets/93542752/f050062d-24a2-4dcc-9b8b-a54854ce3d99)

  
-> Check the table:

![CheckCreatedProfessorsTable](https://github.com/Janet-Cajavilca/SQL/assets/93542752/2976ca30-8cd5-4b57-8344-7772e2b2a692)

- Entering Data into the **assistant's Table**
  
![CreateAssistantsTable](https://github.com/Janet-Cajavilca/SQL/assets/93542752/7002a63c-154d-409e-a2d9-a3ccb9f12ddf)

-> Check the table:

![CheckCreatedAssistantsTable](https://github.com/Janet-Cajavilca/SQL/assets/93542752/67fdfc88-21c3-4463-b385-485b48e2a076)


- Entering Data into the lectures Table
- Check the table:
- Entering Data into the attend Table
- Check the table:
- Entering Data into the prerequisites Table
- Check the table:
- Entering Data into the test Table
- Check the table:
