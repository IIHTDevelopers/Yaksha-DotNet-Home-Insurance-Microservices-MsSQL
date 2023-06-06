* On command prompt, cd into your project folder (cd <Your-Project-folder>).On command prompt, cd into your project folder (cd <Your-Project-folder>).
	- Service Project Folders :
		(cd CustomerServices/Customer)
		(cd AdminServices/Admin)

	- API Gateway:
		(cd OcelotGateway)

* To connect SQL  server from terminal:
	(CustomerServices/Customer/sqlcmd -S localhost -U sa -P pass@word1)
	
	-To create database from terminal - 
	1> Create Database HomeInsurance_Db
	2> Go

* Steps to Apply Migration(Code first approach):
	Press Ctrl+C to get back to command prompt
	Run following command to apply migration-
             (CustomerServices/Customer/dotnet-ef database update)

*  To check whether migrations are applied from terminal:
	(CustomerServices/Customer/sqlcmd -S localhost -U sa -P pass@word1)
	1> Use HomeInsurance_Db 
	2> Go
	1> Select * From __EFMigrationsHistory
	2> Go

* Run one of the Service and API Gateway.
	Open two terminals and use the "dotnet run" command to start them.
	- (<Service-Project-Folder>/dotnet run)
	- (OcelotGateway/dotnet run)

* To test any Restful application, the last option on the left panel of IDE, you can find ThunderClient, which is the lightweight equivalent of POSTMAN.

(NOTE: Copy URL of API Gateway to test Rest End Points - https://localhost:5001)

* To run the test cases in CMD, Run the following command to test the application:

	( <Service-Project-Folder>/dotnet test --logger "console;verbosity=detailed")
  (You can run this command multiple times to identify the test case status,and refactor code  to make maximum test cases passed before final submission)

* To ensure your code is saved and available for later use, remember to use the CTRL+Shift+B command on your code IDE.
   This will push or save the updated contents in the internal git/repository.
   It is also important to use CTRL+Shift+B before the final submission to evaluate the code quality.