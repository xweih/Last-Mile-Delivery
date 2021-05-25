# Last Mile Delivery 
# A practical solution to a schedule optimization problem using Gurobi

![alt text](https://leighdavid.com/wp-content/uploads/2019/03/final-mile-home-delivery-bg.png)


## Story
Furniture Co’s logistic department of is responsible for the last mile delivery from store to customers’ homes. The company has stores in many cities across the country. Each store is responsible for delivering customers’ items in the region. Every store has several one-furniture trucks, which are used to transport furniture from the store to each customer. There are a number of employees who can drive the trucks to deliver furniture. A one-furniture truck can take one furniture at a time, as shown in the following photo. A one-furniture truck takes one Furniture Co’s employee to drive and operate. For now, let’s assume each store always has the same number of one-furniture trucks and employees.

Each employee has his/her shift start/end time, i.e., not all employees start/end at the same time. An employee can do multiple deliveries a day. For example, an employee can start the day by first driving the one-furniture truck with the purchased furniture to customer 1, delivering the furniture and coming back to the store; then move onto the second delivery - take the 2nd customer’s furniture, drive it to Customer 2, and come back, and move to the third delivery. 

## Data
The excel file has three tabs, each tab is a table. In this dataset, the store in City X has 19 employees working tomorrow. There are 49 customer furnitures to be delivered tomorrow. You can find the deliveries data in events tab; and resources tab for employees shift start/end time in the excel file; and driving duration in duration tab.

For example, EventId 8366991 is a customer’s delivery. The address of this customer is A1, the driving time from hub to A1 is 30min, as shown in the duration tab. We assume the driving time from the store to address A1 is the same as the driving time from A1 to the store. The total driving time to/from A1 is one hour (30min one way). Together with the time needed to spend with the customer on paperworks and test drive, this delivery event is going to take 2 hours. The time window from the start of the trip to the end of the trip is fixed, i.e. from 8:15 to 10:15, as shown in the events tab. In resources tab, each row is a Furniture Co’s employee with his/her shift time, e.g. ResourceId 9454310 is an employee who works from 7:00am to 19:00pm.

## Mission
Let us generate an assignment schedule for tomorrow by showing "who delivers which furniture". 
