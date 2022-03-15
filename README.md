# OOPS! Pitfall Finder

This Github action offers the opportunity to check the .OWL-Files of an Pull-Request regarding the OOPS!-Pitfalls of http://oops.linkeddata.es/. 

For more Information about OOPS! compare https://www.semanticscholar.org/paper/OOPS!-(OntOlogy-Pitfall-Scanner!)%3A-An-On-line-Tool-Poveda-Villal%C3%B3n-G%C3%B3mez-P%C3%A9rez/28f692a5b6e61ab48bece1221f4e17e05a9a8139 

The **github action** script is in the file **test-action-linting/.github/workflows/main.yml**

It automatically will be used within the controll tests if you have a new pull request. 

_The OWL-Files in the pull request will be analyzed based on your personal defined pitfalls:_

In http://oops.linkeddata.es/webservice.html you can find out which OOPS!-Pitfalls you want to check the .OWL-Files in your Pull-Request. 

Although 35 pitfalls have been identified, not all of them have been implemented. List of implemented pitfalls: **2, 3, 4, 5, 6, 7, 8, 10, 11, 12, 13, 19, 20, 21, 22, 24, 25, 25, 26, 27, 28 and 29**."_ (Date of Research: 11/03/2022)

If the user just wants to analyze some pitfalls, just enter the number of the pitfall with a coma separator if more than one pitfall is entered. For instance: “4,11,21” or "P04,P11,P21".

If you dont want to have any pitfalls in minor.TXT oder major.TXT, just fill in like here:
```
no
```

In the folder test-action-linting/.github/workflows/OOPSPitfalls/ you can define **your pitfalls** you want to check during this Github action: 

- **minor.TXT** -> Single Line with Pitfalls which are MINOR for your case (e.g. minor.txt: 3,5). The output will be displayed in the command, but it has no effect if this action will be accepted or fail.  

- **major.TXT** -> Single Line with Pitfalls which are MAJOR for your case (e.g. minor.txt: 3,5). The output will be displayed in the command. If OOPS! find Major Pitfalls, then this action will fail. 

minor.TXT and major.TXT should like this example: 
```
21,22,24
```

- **positiveFeedback.TXT** -> !!! This file should NOT be changed.!!!

**For more information of the data analysis, please view the action feedback in the Github workfile view**
