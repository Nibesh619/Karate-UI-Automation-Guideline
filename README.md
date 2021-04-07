# Karate-UI-Automation-Guideline

Error that i faced during Karate UI Automation. 


You inspect the css file using the css selector. Css selector can be used to know the XPath of the desired element. To check if the desired XPath is present or not use “Ctrl+F”. Here you can search the desired Xpath location. 

1) If all you need to do is check if a button exists, use exists() like this:
* def flag = exists('#myButton') # now you can use the value of flag to perform logic

2) Always see which method is used in css selector for example 
<input><span> <button> 

3) To click a hyperlink use this set of instructions.
Then click("//span[text()='Admin']")

4) To click login button, use this set of instruction
When submit().click("button[type='submit']") 

5) To select div class use this set of instruction
"//div[text()='* Invalid email address']"

6) To clear the anything in textfield, use this code
Then clear("input[id='email']")
