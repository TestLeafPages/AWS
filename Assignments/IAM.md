Hi Team,

Find the below given *IAM Assignment*

1. Login as Root/admin account
2. Go to IAM service 
3. Create two users(user1 & user2) -> With Password - AWS Management Console access
4. Add *AmazonRDSFullAccess* policy to user1
5. Create a Group -(DevTeam) -> Assign a *AmazonEC2FullAccess* policy
6. Add user2 to group (DevTeam) 
7. Login with newly created IAM user1 and confirm you have access to RDS but not EC2 for user1 
8. For user2 confirm you have access to EC2 but not RDS
