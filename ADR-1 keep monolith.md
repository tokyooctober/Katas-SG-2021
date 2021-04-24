# Title
Keep Monolith Backend [working name]

# Status
[proposed, ~~accepted, superseeded~~]

# Context
Monolith is the original application developed to support SysOps.  It contains all operational info (Customer, Billing info, customer's support plan,  Expert and their skillset, KB)  

However, there are reliability issues when there are spike in usgaes and the number of customers using the system.  There are 4 classes of users.  They are (in descending numbers):
1. customers
2. experts
3. administrators
4. managers 

Customers and Experts are affected when reliability issues occured because their numbers is more than administrator and managers.

# Decision
- Administrators and Managers will continue to use the Monolith for their operational work.
- Monolith will continue to be the central store for all info for SysOps to meet reporting needs.
- To relieve monolith from spike in usage, additional component (outside monolith) will be added to serve Customers and Experts.

# Consequences
- duplicate info of ticket info

