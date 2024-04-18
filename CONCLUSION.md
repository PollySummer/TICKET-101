# Conclusion about TICKET-101
## Advantages
<i>To be honest, I haven't worked with Flutter and Dart before, so I've highlighted such pros that are important in every programming language and are common.</i>


## Disadvantages
* LoanPeriod shows 6 months instead of 12 months. The image is attached below.

![6 moths bug](images/img_6_months.png)

* The next bug that I found and fixed was: "Another exception was thrown: Incorrect use of ParentDataWidget". It shows in console every time when I changed screen size.
It was found in <b> main.dart </b> file. 

<b>Solution:</b>

I removed the Expanded widget from the SizedBox and directly set the height of the SizedBox based on bodyHeight.

* The next one is "Another exception was thrown: A RenderFlex overflowed by 44 pixels on the bottom." In <b>loan_form.dart</b> file.
  
<b>Solution:</b>
I added SingleChildScrollView and wrapped in Expanded, this helped avoid overflow.

* And also "Use 'const' with the constructor to improve performance. Try adding the 'const' keyword to the constructor invocation.". Was recomendation from VS code, so I added it in the main.dart and loan_form.dart

That's all the disadvatages I found and fixed.