# Project Name:- Simple Python Project

## Description:- Writing Testcases in Robot Framework using Selenium Library to search google for "python" 

### Steps to Automate:- 

    *** Settings ***
    Library  SeleniumLibrary
    *** Variables ***
    ${browser}  chrome
    ${url}   https://www.google.com/
    *** Test Cases ***
    Google
    Open Browser    ${url}   ${browser}

    Maximize Browser Window
    Press Keys   xpath://input[@name='q']    Python+ENTER
    ${AllLinksCount}=  get element count  xpath://div[@id='rso']//h3
    log to console   ${AllLinksCount}

     @{LinkItems}     create list
     FOR     ${i}  IN RANGE  1    ${AllLinksCount}+1
     ${linkText}=  get text  xpath:(//div[@id='rso']//h3)[${i}]
     log to console   ${linkText}
     END
    *** Keywords ***
    
### Execution Instructions:-

* Open Google Chrome browser by using url
* Write the testcases to find
* write a code to maximize the browser window 
* Write a xpath to enter the "python" search engine

## Output logs:-
 *    Python Tutorial - W3Schools
 *    Python (programming language) - Wikipedia
 *    Videos
 *    Python Tutorial - Tutorialspoint
 *    Top stories
 *    Python Courses & Tutorials | Codecademy
 *    Online Python Compiler (Interpreter) - Programiz



