# Java-EE-Group-Project

The theme for the Group Project is to bring together everything you have learned:
1. JPA – for model objects
2. Session beans – for business logic
3. REST – representation of back-end resources
4. JEE security roles – controls who can invoke which operation
5. Testing using JUnit – a series of test cases that demonstrate the operation and correctness of the system

- Task One – Finish Custom Authentication Mechanism
- Task Two – Relationship Between SecurityUser and Student
- Task Three and Lesson 1 – Building a REST API
- Task Four and Lesson 2 – Securing REST Endpoints
- Task Five and Lesson 3 - Building JUnit Tests

Requirement Summary
1. Make a resource for all tables.
a. Student is given as an example.
b. Each resource needs to support CRUD operations.
i. Update is optional.
c. Resource is not needed for security_user, security_role, and user_has_role.
d. Resource is needed for the following classes/entities:
i. ClubMembership
ii. Course
iii. PeerTutorRegistration
iv. MembershipCard
v. PeerTutor
vi. Student
vii. StudentClub
e. Import and use the provided Postman collection REST-ACMECollege-
Sample.postman_collection.json to test your REST endpoints. (Note: Feel
free to add and modify the REST requests/messages. Please include only those
REST requests that are working properly for your REST API system and
remove those REST requests that are not working or not supported by your
REST API system. When submitting your completed work, please include only
those REST requests that are working properly for your REST API system and
remove those REST requests that are not working or not supported by your
REST API system. Your work will be graded based on the REST requests
included in your Postman collection.)
2. Update your entities with appropriate Jackson annotations similar to Lab 4.
a. Examples of all you need is in the code already.
b. Use @JsonIgnore if you need to remove a field from being processed by Jackson. For
example, student club does not to display all the club memberships.
c. Use @JsonSerialize if you like to create a custom serialization of your entity. For example,
when creating JSON for student club we just need to see the count.
d. If you need access to your lazy fetched objects, you need to create a namedQuery with
join. For example, we need all student clubs with their club membership counts.
"SELECT distinct sc FROM StudentClub sc left JOIN FETCH sc.clubMemberships".
e. What exactly needs to be displayed is up to you. Display enough meaningful information
in your JSON.
3. Create JUnit tests for your REST APIs.
a. Minimum of 40 JUnit tests.
b. Use the Client API to test your code.
c. Remember to run your server first as the REST API needs to be running first.
d. Tests the roles and CRUD operations.
e. Optionally, you may want to generate a Maven surefire report that summarizes your test
results (see Assignment 3 on how to generate the Maven surefire report).
