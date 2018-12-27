---
title: Designing Tests
page_title: Load Testing - Designing Your Test
description: "Test Studio is an innovative and easy-to-use automated web, WPF and load testing solution. Test Studio tests support essential technologies like ASP.NET AJAX, Silverlight, PHP and MVC. HTML5, Testing framework, functional testing, performance testing, load testing, exploratory testing, manual testing."
position: 2
---

# Load Testing: Designing Your Test

Getting started with Test Studio Load Testing is a snap. Do you have existing functional tests in Test Studio? You can set up powerful profiles by using those tests without having to modify them. You can also quickly tailor “think time” delays to simulate the pauses real users make as they navigate your site.

Have you been capturing Fiddler traces of site activity during troubleshooting or monitoring? Use this invaluable data directly by importing it into Test Studio as a user profile!
 
To get the most out of your Load Test, it is best if you follow a few simple guidelines:

1.&nbsp; Make sure you have think times with deviations. Think Times with deviations have a random duration. By having some users at different intervals sitting out of the test (thinking) it not only mimics real world usage better, but it allows for your agents I/O to not be as congested. It may be counter intuitive, but having your virtual users stop to think for a time will actually increase the number of users and requests that your agent can complete.

2.&nbsp; Use ramp times to build up your users from a small number to larger numbers. Again, if you start with a large consistent load, without any ramping, you will likely clog the I/O. By ramping up from lower numbers you give your think times better chances to get involved.

There are six steps to create and fully define a load test: 

1.&nbsp; Add a new Load test to your project:

  a. Click the **Record** button.
  b. Select **Load Test**.
  c. Enter a name for your new load test.
  d. Click **OK**.

![Load test][1]

2.&nbsp; <a href="/features/testing-types/load-testing/adding-user-profiles" target="_blank">Add user profiles to the load test</a>. A "user profile" is a specific sequence of HTTP traffic that represents how one user is interacting with your web applications. A load test must have at least one user profile. Your load test may contain as many user profiles as you like. There are four possible sources for the HTTP traffic representing a user profiles. 

- Imported from an existing load test.
- Imported from a <a href="http://fiddler2.com/fiddler2/" target="_blank">Fiddler</a> trace.
- Manually capture new traffic from a selected web browser.
- Capture HTTP traffic generated by executing an existing Telerik functional web test in a selected browser.

3.&nbsp; <a href="/features/testing-types/load-testing/dynamic-targets" target="_blank">Select the dynamic targets</a>. A "Dynamic Target" is a unique parameter or variable used by the application to generate information like a unique user ID or session ID. These values are generated by the web server, sent to the browser which then later returns that value back to the server so that the application can match the new request to a previous HTTP transaction. To accurately simulate users via virtual users it is important to correctly return these Dynamic Targets during the load test execution.

4.&nbsp; Optionally configure the <a href="/features/testing-types/load-testing/think-times" target="_blank">think times</a>. "Think Time" is the time it takes a person to process the information received from the application and decide what to do next. It is also the amount of time spent filling in a form before clicking on Submit or Next. Because every user is different, to have accurate load tests it is important to use a good Think Time range. Some users take longer to read and/or enter data into a form than others. Test Studio can automatically vary the Think Time based a deviation time specified with the Think Time. This will more accurately replicate the length of time from when a person receives a response (a webpage) from your server to the time that person requests a new page.

5.&nbsp; <a href="/features/testing-types/load-testing/test-settings" target="_blank">Configure the work load distribution of your user profiles</a>. You may not want all the HTTP traffic hitting your application under test equally. You may configure some of the user profiles to be much more frequent than the other user profiles.

6.&nbsp; <a href="/features/testing-types/load-testing/test-settings" target="_blank">Configure the number of virtual users and the time length of the test.</a>

[1]: /img/features/testing-types/load-testing/designing-tests/fig1.png