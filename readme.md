ScaffoldingManagement-InvoiceExtract
===

CLI to extract data from MongoDB and create a file to be used for invoicing


Command line parameters 

The email to send the extracted data to

	-e / --email

	
The connectionstring to the database

	-c / --connectionstring


The year to extract data from 	

	-y / --year

	
The month in the year to extract data from

	-m / --month
	
	
Functionality:	

- Extract data from Activity for the given year/month
- For each company 
  - For each gateway
    - Sum number of days in activity stream
	- Write invoice line: "Gateway" / [Serial number] / count days"
	- Find all sensors attached to gateway
      - Sum number of days in activity stream
	  - Write invoice line: "Sensor" / [Serial number] / count days"
	  
	