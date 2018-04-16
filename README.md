# Week8

1) Username Enumeration:
This challenge was from the green site.
Here the user can enter in random usernames and try to log in, if the username exists then the error message will desplay "Login was unsuccessful" in bold, but if the user doesn't exist then it won't be bolded. I used usernames that exist (jmonroe99, and pperson) and usernames that don't exist (personExists, and hey I'm a user), after I enter in random passwords that don't match, the site gives me the error message, and it only becomes bold when a user exists.

2) IDOR (Insecure Direct Object Reference):
This challenge was from the red site.
Here I am first logged in, so I can see which accounts are on the site, I see that Testy McTesterton, which is a user that is not public until September 1 (as it says) and I check to see the ID in the url is 10. I log out and check to see the other staff members and check to find Testy in the list, but Testy isn't there. I click a random staff member and change the ID to 10, which is Testy's ID, and I can see the member change to Testy.

3) SQL Injection:
This challenge was from the blue site.
Here the blue site isn't sanitized properly, so when someone tries to go to a user, they can inject some SQL into the url. Here I enter the characters: ' OR SLEEP(4)=0--', this makes it so that the SQL injected can make the page wait 4 seconds while loading, this can be done on other parts of the site and for longer than 4 seconds, the user just has to enter in a high number. The time it waits just confirms that the SQL works.

4) XSS (Cross Site Scripting):
This challenge was from the green site.
Here an attacker can insert some script in a comment, and after a victim views the comment, the script is then executed and can cause harm. Here I have the script display the message that says "YOU GOT HACKED!" as soon as the comment is opened by the user.

5) XSRF (Cross Site Request Forgery):
This challenge is from the red site.
Here an attacker can submit a form that uses the permissions of a user who opens it and can change databsae info. Here I send a message as feedback, linking in an html file that I made to change a user's information, once the user who's logged in opens it, the site takes the changes submitted and implements them. In this case Sherry Trevino's info got changed, after having the user click on a file named "IDORPAGE", this can be named whatever, I linked it into the comment so that the user can open it and I can use their permissions to apply the changes I specified in the file to make changes to Sherry's info.

6) Session Hijacking:
This challenge was from the blue site.
Here I use two browsers, one in which I am logged in (victim) and one another in which I need to log in (attacker). I check the logged-in site's session (by using the script to change the sessionID) and copy it, go to the other browser (the one that isn't logged in) and gain access to the site. An attacker can gain access to the site by using a victim user's session and take advantage of how the site allows their user to stay on for longer periods of time (in this case a year) compared to the other two sites.
