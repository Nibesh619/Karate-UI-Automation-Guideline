# Karate-UI-Automation-Guideline

Solution for error that i faced during Karate UI Automation. 


You inspect the css file using the css selector. Css selector can be used to know the XPath of the desired element. To check if the desired XPath is present or not use “Ctrl+F”. Here you can search the desired Xpath location. 

1) If all you need to do is check if a button exists, use exists() like this:
 Then def flag = exists('#myButton')
 # now you can use the value of flag to perform logic

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


7) For dropdown button, use this code
Given select("select[name='adminTable_length']","20")

8) To match the message after any action, use this code
Then match text('#eg02DivId') == '16'


9)  fail test if element does not exist
 * assert exists('#foo')

10)  click if element actually exists else do nothing
* optional('#foo').click()

11) Get element without any wait and fail if it does not exist
* def btn = locate('#foo')
* btn.click()

12)  To select scroll the page, use this code. 
* scroll('#myInput')

13) To scroll and click(), use this code. 
*scroll(‘#myInput’).click()
I also use this code when I have to scroll the page and there is only text available. So this code scrolls the desired text and clicks the text which does not do anything. So you can scroll pages more easily. 


14) To locate exact path of certain element use, this code
Then assert locate("//span[text()='Report']").present

15)  To upload file, first keep your desired uploading file in the path where the .feature file is present then, use this code.
When driver.inputFile("input”'] ","FileName")

16) Condition to check or validate, use these steps 

* def flag = exists("button[id='adminlistbtnhover']")
Then def flag = false? 'Sample.feature' : 'Sample2.feature'
* def result = call read(flag)
* delay(1000)
Then close()

Here  * def flag = exists("button[id='adminlistbtnhover']") returns either true or false boolean. Then Then def flag = false? 'Sample.feature' : 'Sample2.feature'  checks the returned value.  I have made two sample features which are sample and sample2. Which prints what value to print(I made two sample feature file where one prints positive return value and another prints negative which can be seen on below code) -  So if flag  is false it will print Sample2.feature and if it is true it will print Sample.Feature. 
demo code for Sample.feature and Sample2.feature-


@ignore
Feature: Call scenario from another scenario

Scenario: Result
Then print 'It was not found'


                                                 






