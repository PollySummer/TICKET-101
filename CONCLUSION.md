# Conclusion about TICKET-101
## Advantages
* Short and clear comments;
* Try-catch for handling possible errors;
* Clear variable and file names;
* Handling user errors, e.g. when isikukood is shorter than 11 digits or it is entered in an incorrect format;
* Adaptation for phones and tablets;
* The code is structured into separate files and classes, promoting code organization and reusability.

## Disadvantages
* LoanPeriod shows 6 months instead of 12 months. The image is attached below.
<p align="center">
<img src="https://github.com/PollySummer/TICKET-101/blob/master/images/img_6_months.png" alt="6 moths bug" width="500"/>
</p>

* The next bug that I found and fixed was: "Another exception was thrown: Incorrect use of ParentDataWidget". It shows in console every time when I changed screen size.
It was found in <b> main.dart </b> file. 

<b>Solution:</b>

I removed the Expanded widget from the SizedBox and directly set the height of the SizedBox based on bodyHeight.

* The next one is "Another exception was thrown: A RenderFlex overflowed by 44 pixels on the bottom." In <b>loan_form.dart</b> file. 
  
<b>Solution:</b>

I added SingleChildScrollView and wrapped in Expanded, this helped avoid overflow.


* And also "Use 'const' with the constructor to improve performance. Try adding the 'const' keyword to the constructor invocation.". Was recomendation from VS code, so I added it in the main.dart and loan_form.dart

That's all the disadvatages I found and fixed.

<i>To be honest, I don't have much experience with Flutter and Dart, so my notes may seem general for all programming languages, but I tried to find as many pros and cons as possible.</i>