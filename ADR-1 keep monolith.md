# Title
The plan is to use Strangler pattern and incrementally transform the monolithic to full microservice architecture. Keep Monolith Backend for Administrator and Manager domain services. [working name]

# Status
[proposed, ~~accepted, superseeded~~]

# Context
Monolith is the original application developed to support SysOps.  It contains all operational info (Customer, Billing info, customer's support plan,  Expert and their skillset, KB)  

However, there are reliability & elasticity issues due to spike in usgaes and the number of customers using the system.  We believe the monolith was built to a specific capability which was exceed during the spike conditions.

 We see there are 4 main classes of users.  They are (in descending order of numbers):
1. customers
2. experts
3. administrators
4. managers 

Customers and Experts are affected when there are spikes  because their numbers is more than administrator and managers.

# Decision
- 
- Monolith will continue to be the central store for all info for SysOps to continue meeting operational needs beyond ticketing issues.
- New component to be built to address and solve the elasticity and reliability issues.  This component must be scalable and elastic to meet sudden spike in usage, hence will be built outside the monolith.

# Consequences
- Administrators and Managers will continue to use the Monolith for their operational work.
- Further investigation and decision on the technology choice for the new component.  Current suggestion is the component will be using microservices style and cloud-native to take advantage of elasticity , reliability and scability.


