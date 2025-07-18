
This is a sample Automation Test Framework to test the endpoints of the minimal API application - ToDo APIS.
Framework is built using Xunit, .Net JSON in C#.
Test Scenarios are written as test code with the failed scenarios as bugs found during testing.
This framework has both Integration Level tests and E2E tests to support a test pyramid.

Limitations: 
Not advisable to run tests at once as this does not support parallel runs due to the use of Entity Framework DB context as application can only be run locally (Development mode).  This can be supported by creating a sophisticated test fixture to support all setup configuration, which I have not done.

To run the tests:
1. Clone branch/repo into VS
2. Install Xunit v3 - https://www.nuget.org/packages/xunit.v3#supportedframeworks-body-tab
3. Install Microsoft.AspNetCore.Mvc.Testing via Managet NuGet package in VS or here -https://www.nuget.org/packages/Microsoft.AspNetCore.Mvc.Testing/8.0.10
4. Add package JsonSchema.Net - https://www.nuget.org/packages/JsonSchema.Net
5. Open Test Explorer in VS.  View tab > Test Explorer
6. Run tests per test class to avoid EF DBContext conflict in parallel runs or run per test to understand the test clearly.
