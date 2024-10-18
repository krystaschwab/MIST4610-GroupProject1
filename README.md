# MIST4610-GroupProject1

Team 6

## Team Members:
1. Nico Espinel [@nicoespinel](https://github.com/gne74937/MIST4610GroupProject1)
2. Evan Mahathirath [@evanmahathirath](https://github.com/emahathirath/MIST4610GroupProject1) 
3. Tarita Jakobs [@taritajakobs](https://github.com/TaritaJakobs/MIST4610GroupProject1Zoo)
4. Mia Townsend [@miatownsend](https://github.com/MiaGTownsend/MIST4610-GroupProject1-Zoo) 
5. Krysta Schwab [@krystaschwab](https://github.com/krystaschwab/MIST4610-GroupProject1)


## Problem Description:

The objective is to design and model a relational database that captures the essential operations of a zoo. The Employee table serves as the central entity in this model, as it is interconnected with several other entities, including Department, Exhibit, FoodCourt, TicketPurchases, and EmployeeVehicleAssignment. Additionally, the data model encompasses other entities such as Transportation, Visitors, Suppliers, Animals, Tickets, and AnimalDiet. Our primary focus is on effectively managing various operations, including guest services, ticketing processes, and animal welfare. To validate the database design, we generated sample data and populated the entities. This allows us to execute a range of simple and complex queries, simulating how the zoo would utilize this database in real-world scenarios.



## Data Model:

Our model is based on a zoo. The Department entity is at the top of our data model and consists of departments like zookeepers, vets, drivers, sales, and foodcourt. Each department has many employees, but an employee can only work in one department. 
The Employee entity is the central part of our data model. This entity contains information about each employee’s ID, first and last name, salary, contact information, and which department they belong to. For instance, an employee with the zookeeper department ID or vet department ID will have an exhibit ID where they work, but will not have a food court ID since they do not work in the food court department. Each employee is assigned to one exhibit where they will work with the animal that is assigned to that exhibit. However, the exhibit has many employees, such as a zookeeper and a vet. Exhibits will have multiple animals in them but the animals will not be placed in another exhibit. The Animals entity keeps track of their information such as their size or date of birth. Inside the Animals entity, there are two foreign keys from the exhibits entity. With the exhibit's key, it denotes the location of the animal and what exhibit they are in.

The Animals entity also has the FK dietNumber from the animal diet entity. Animal diet has a one-to-one relationship with animals to show that each animal has a special diet with specific instructions, like what time of day they eat and what kind of food they eat (herbivore, carnivore, omnivore).

Additionally, the Employee entity also has a one-to-many relationship with the food court, indicating that one food court stall has many employees but employees belong to one entity. The food court entity connects to the supplier entity, in which the supplier supplies both the food court with food and the animal diet entity with animal food. One supplier supplies many food stalls and animal diets, but each food stall and animal diet has one supplier.

The Employees entity also branches out into the TicketPurchases entity, as employees who are in the sales department are in charge of administering ticket sales, therefore each ticket purchase is associated with a sales employee. The TicketPurchases entity also keeps track of the purchase number, which is the unique identifier, as each purchase has a different purchase number, the cost of the ticket, the number of tickets purchased, and the date the tickets were purchased. The TicketPurchases entity branches off into the Tickets entity, as one purchase can be composed of multiple tickets. The Tickets entity tracks the individual ticket number, the visitor ID, as well as the purchase ID that is associated with the ticket. This entity is connected to the Visitors entity through a one to many relationship, as in each visitor could have many tickets. The Visitor entity contains information such as the visitorID, visitor first and last name, and visitor age, which is stored as their date of birth. Together, the Tickets, Visitors, and TicketPurchases entities would allow the zoo to track the number of tickets purchased, as well as information about the visitors and the sales employee that sold them the tickets. 

Finally, the Employee entity branches out into the EmployeeVehicleAssignment entity, as each employee in the transportation department can have many vehicle assignments. The EmployeeVehicleAssignment entity would keep track of the license plate of the assigned vehicle, the employee ID of the assigned employee, as well as their shift date. The EmployeeVehicleAssignment entity is branched from the Transportation entity, which contains more details about the vehicles. The Transportation entity contains information about the license plate of the vehicle, the make, model and capacity of the vehicle. Together, these entities would allow for the zoo to track which employees are assigned to which vehicles, as many employees can be assigned to many vehicles, representing a many to many relationship.


![348F32CC-704F-4266-B777-49821B0C0129_1_201_a](https://github.com/user-attachments/assets/93677c0c-2b18-4ffc-beab-95f91c1476c7)



**Data Dictionary:**
![2DF7CC14-2652-4E80-A406-1A58B3A0FD9B_1_201_a](https://github.com/user-attachments/assets/05dbb295-cc26-4802-8adc-98def991d325)
![5ED319CD-3F11-4B5D-8D17-76D7A85D397B_1_201_a](https://github.com/user-attachments/assets/abb1a76f-a901-4012-8587-01c7c695cc3f)
![D8E23A45-5836-4978-97F0-6EC019A9F6B4_1_201_a](https://github.com/user-attachments/assets/b9437e2e-e739-4e54-a392-ee8758d941b4)
![9DEE78DF-E29D-41B4-9D6A-4E08918BCAEF_1_201_a](https://github.com/user-attachments/assets/12cb4a5f-c8f9-4680-b81e-a45fc7d0eb4f)
![54C298C2-FD8F-4C6E-A327-0679C4518830_1_201_a](https://github.com/user-attachments/assets/5bced662-1ded-4745-941f-8e06d7342b98)
![D4057175-D9AC-4AB0-AF14-9486D3FBF12F_1_201_a](https://github.com/user-attachments/assets/8122226d-6725-44dc-a362-0cd4b74d2029)
![63D1EDFF-B75A-43D2-8696-883655EF99F2_1_201_a](https://github.com/user-attachments/assets/7f6a50d3-4224-4693-af86-8ab7a8c09c7c)
![1CD0275D-1D44-42E3-9F2C-EEAF2AB65BFC_1_201_a](https://github.com/user-attachments/assets/f7d90182-d82f-4444-a507-fd68287839df)
![E54B5679-EDED-46DC-89DA-EBF8EA81A807_1_201_a](https://github.com/user-attachments/assets/388e9cdc-1415-4f5b-8ed3-01c85864ce19)
![613762CA-1406-4A4F-A55A-E484BDB4E34B_1_201_a](https://github.com/user-attachments/assets/faa613c6-67b9-4455-a9d1-6f8a7ce8c97c)
![46E1F529-9417-4B19-A959-DAC09104783E_1_201_a](https://github.com/user-attachments/assets/697901fb-6565-4bbc-9d45-6b2993f90f73)
![6036993E-719B-45BD-A42E-7312435B0BF2_1_201_a](https://github.com/user-attachments/assets/fc40af98-b0f4-4955-902c-30bb13fcd8a5)



## Queries:

![BBEDDA19-D941-4737-9075-38CFF7142F37_1_201_a](https://github.com/user-attachments/assets/e00f3b83-944e-4e63-906e-a07bc34692ea)




1. Query 1 (Simple)
![DD5B49C8-2003-4F4B-B121-7F9896778B94_4_5005_c](https://github.com/user-attachments/assets/255b2eff-44aa-4daf-a4f5-7da3925406ed)
![5B1AC2AA-311A-4A6D-8E1A-AFF71A81E23E_4_5005_c](https://github.com/user-attachments/assets/7784e0ee-82a7-4ede-9e0a-8eb019b30aa2)

This would be important for the zookeepers to keep track of what animals they have to feed during the evening, who have a particular diet type, such as omnivore. They could use this information to create a feeding schedule as well, to increase the operational efficiency of the zoo.

2. Query 2 (Simple)
![FACC3F4D-B3E3-46BE-9FB4-6254CD5E5733_4_5005_c](https://github.com/user-attachments/assets/cd775df9-cb79-4c80-9efa-e8c7d923ce98)
![0A8B374E-2101-4702-9C70-4102878C17B3](https://github.com/user-attachments/assets/a504cca3-94ff-4572-9774-ae864b73feb3)

This would highlight to the zoo the amount of their visitors who are part of the older generation, in order for them to create marketing campaigns that aligns with the age group demographic that frequents the zoo the most, or to entice a group of people that are not frequent visitors. 

3. Query 3 (Simple)
![5DD6FD7D-5806-4E15-B891-4F32099CB36F_4_5005_c](https://github.com/user-attachments/assets/6d5bd505-b3b8-4b66-9087-01988ebbafb9)
![EAAEF291-DFA4-4CD3-8B35-F9588D36E3AA_4_5005_c](https://github.com/user-attachments/assets/2f57e0c9-4337-484e-baf7-63565eb618f4)

Creating a list of all the animals who are male and in the Safari exhibit would be helpful for both the zookeepers and the vets to create schedules to care for the animals according to their needs, as male and female animals have different needs.

4. Query 4 (Simple)
![196EEE73-AE7D-4ECA-A1F7-A3A4C742AD26_4_5005_c](https://github.com/user-attachments/assets/3bfede05-ae8c-4c3e-9b04-34cd41716ce7)
![737D6DD0-ED66-443E-9114-EA90ADCC1ABD_4_5005_c](https://github.com/user-attachments/assets/bb9d5b81-44ad-4f80-9ae5-b6137adc8665)

This would be helpful to keep track of the restaurants and their suppliers, and with this information, the zoo would be able to streamline shipments from the suppliers and allocate the supplies to each restaurant efficiently. 

5. Query 5 (Complex)
![C7DB5B23-617F-46FE-A130-9897E1B9F436_4_5005_c](https://github.com/user-attachments/assets/91d23b32-8489-4407-a0ee-2991d095918a)
![D81F8125-A5A3-45E3-8172-384759981B6C_4_5005_c](https://github.com/user-attachments/assets/2542f7e1-588b-4b16-8482-972d49e768e7)

Keeping track of how many animals that the zoo has in each exhibit is important for the goal of animal welfare. The zoo needs to be aware of how many animals in each exhibit need to be taken care of, fed, and looked at by the zookeepers. 

6. Query 6 (Complex)
![C9E445E8-8715-4CE9-980B-190DDB5DD7F0_4_5005_c](https://github.com/user-attachments/assets/110b9abf-ba31-492d-8a83-4774a99c45d6)
![4865C8E4-81DD-4E0E-AD8D-8C9E90D0B826](https://github.com/user-attachments/assets/1326b976-3617-441c-bc4e-54415b835022)

This query is important to the zoo’s management because food court employees have schedules managed by individual restaurants. As a result, when creating the zoo-wide employee schedule, it is necessary to separate employees who do not work in the food court. By identifying these employees, the zoo can efficiently create a general schedule for the rest of the staff, ensuring better organization and improved operational efficiency.

7. Query 7 (Complex)
![DA9CC26E-757A-412E-A2B8-76FC15C4BA49](https://github.com/user-attachments/assets/fb3007f6-feb8-4c25-8036-8fd58fc7338c)
![135F103C-4C64-4887-9653-3BF549DDEFF1_4_5005_c](https://github.com/user-attachments/assets/e5a751de-1d69-45bf-8403-d84e7ea8eac9)

This query is important for identifying high-performing employees with names starting with "L" who exceed the average sales, which could help recognize patterns in employee success or performance. It may also aid in targeted recognition or resource allocation for staff who contribute significantly to sales, which may be done in alphabetical order.

8. Query 8 (Complex)
![2B0516D3-A122-4270-BE4A-BDC599A9CBBC_4_5005_c](https://github.com/user-attachments/assets/3b881eef-ec08-4013-9ae3-a2b51a2984e7)
![E50F2820-808F-4251-9800-93B89136CE2E](https://github.com/user-attachments/assets/ad611052-888a-42a3-883f-6afb00eabde1)

This query is important to the zoo because they can ensure that each employee is making their fair share, and if pay cuts or raises need to be distributed. Furthermore, they can use this information to compare co-workers that hold the same title, and the discrepancies in the salaries. 

9. Query 9 (Complex)
![5A91975C-595E-4D7E-83A6-15A0F8A218BE](https://github.com/user-attachments/assets/5679af34-e399-4024-9a0a-ab38ec349999)
![E64C34DE-C5C3-4A0F-9C45-8D0F44A6AC3E_4_5005_c](https://github.com/user-attachments/assets/6b0988a5-90d7-44cf-841a-d2c2874495e6)

Listing exhibits that have the same number of employees as animals helps identify where the balance between employees and animals is equal. This information can be used to ensure that there are enough employees to care for the animals. If additional employees are needed to maintain proper care, they can be reassigned to those exhibits where the number of employees may be insufficient relative to the number of animals.

10. Query 10 (Complex)
![E86C1387-EFE4-4334-8946-72DFCBAF98EC_4_5005_c](https://github.com/user-attachments/assets/f8a61c01-c461-45d9-bc54-72b78fb56187)
![78C3F540-B56E-49D5-A7CF-1A48B84F3CF9](https://github.com/user-attachments/assets/d901dfe0-4899-4adf-b569-a0b4d8878302)

This query would be important to the zoo management, specifically the sales department, because they would be able to use targeted marketing programs to entice these customers to visit the zoo again. This would be important because it would also allow the zoo to create relationships with their customers and build customer loyalty.



## Database Information
Name of the database: ns_4610Fa24Group6
## Additional information: Each query listed above is marked in the database using stored procedures which can be called using the following format: CALL TP_Q1();

## Slide Presentation 

[Presentation](https://docs.google.com/presentation/d/1ffQU4eKNTn2uIhKbh5l6qyVmpCS3tuCLsDjraL5XGHQ/edit?usp=sharing)











