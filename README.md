# Personal Project: A program for a hospital
This project is to facilitate the process of registering the data of new patients at a hospital and the process of checking the total amount and changing the patient payment status.
## Functionality
The program displays a menu that has 3 options: 1. Save the patient information 2. Check the total patient amount and change the patient payment status 3. Exit. To register patient data, you must log in by entering the user id and password as a doctor and then save the data in the text file called "userId_pacientes.txt" (userId refers to the userId of that doctor) and save the patient ID, the total amount and the doctor's user ID of each patient in the text file called "infoDePago.txt". To check the total amount and change the payment status, you must log in by entering the user ID and password as administrative and you must enter the patient ID. Then, if the patient has paid, save the payment status change in the text file called "userId_pago.txt" (userId refers to the userId of that adminstrative). The last option is to exit the program. In the Hospital class you have the Employee objects as pointers for polymorphism and they create the employee data (Doctor/Administrativo). Doctor has PatientData and its own attributes and its data is saved in text files. From that text file (infoDePago.txt) the patient ID is searched from the Administrative class and if it is there, depending on what the patient has paid, the change is applied and saved in the text file.

## Considerations
To log in, you must enter certain userIds and passwords. For option 1, you have to use the doctor ones, and for option 2, you have to use the administrative ones. The program does not offer this information, since in real life it is the login information of doctors and administrators, I cannot show it directly in the program. The following data is the userIds and passwords of the doctors and administrators. :

- Doctor
userId: dmltk01 | password: qlqjsdlf | servicio: 1

userId: dmltk02 | password: qlqjsdl | servicio: 2

userId: dmltk03 | password: qlqjstka | servicio: 3

userId: dmltk04 | password: qlqjstk | servicio: 4

userId: dmltk05 | password: qlqjsdh | servicio: 5

userId: dmltk06 | password: qlqjsdbr | servicio: 6

- Administrativo
userId: rufwp01 | password: alfghclf

userId: rufwp02 | password: alfghvkf

userId: rufwp03 | password: alfghrn

userId: rufwp04 | password: alfghtlq

For option 3, you must enter the text file called "infoDePago.txt" to obtain the patient ID, and then you must enter that ID into the program. In real life, these data are kept by administrators in a file that has all the information on patient payments.

You have to be very careful with the data you enter. When choosing the options, you must enter only these three numbers: 1, 2, 3 (or others if allowed). If you enter a character, the program will crash. This applies to entering the service value or bed number as well. Additionally, if the program asks for between 'm' and 'f', you must enter 'm' or 'f' (lowercase). If the program asks for 'Y' or 'N', you must enter 'Y' or 'N' (upper case). If the program asks for "DD/MM/YY" form, you must enter, for example, "24/05/2024". If one of them does not meet, in the text file, it will save a garbage value and so the program will not run properly until you delete the garbage values ​​manually and run the program again.

For option 2 of the program, to enter the patient ID, you must open the text file "infoDePago.txt" to check the new data just saved. If not, the program will not run. The first letters that are separated from the other data in the text file are the ids.

The program only runs in the console and is made with standard c++ so it runs on all operating systems

compile with on window and mac/linux:

                          "g++ main.cpp Hospital.cpp Empleado.cpp Doctor.cpp Administrativo.cpp DatoDePaciente.cpp -o main"

                          
                          "main" - window

                          
                          "./main" - mac/linux
