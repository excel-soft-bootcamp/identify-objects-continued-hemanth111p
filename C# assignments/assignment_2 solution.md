|functional requirements|objects|Role|Responsibilities|
|----|-----|------|------|
|model Employee data| EmployeeData|information holder| includes name,age,address,employee id,department,basic salary,band,join date|
|model customer data| CustomerData| information holder| includes name.age,address,customer id,date of birth,contact number,registration fees|
|model special customer data|PreviligedCustomerData|information holder|in addition with customer data, includes fees,date of registration,type,discount of special previliges|
|calculate employee salary| EmployeeSalary|calculation|calculate actual salary of employees based on band|
|calculate incentive of salesperson| incentive| calculation| calculate incentive of salesperson based on sales and target|
|calculate total employee salary|TotalEmployeeSalary|calculation|combine both employee salary and incentives of salesperson|
|calculate total registration fees|RegistrationFees|calculation|calculate the total collected registration fees from customer except customer who takes special previliges|
|get total customer| TotalcustomerData|count|combine customer and special previliges customer and get total customers data|
