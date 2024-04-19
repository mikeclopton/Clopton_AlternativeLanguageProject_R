# Clopton_AlternativeLanguageProject_R

NOTE: THE FILE HERE IS A .IPYNB BUT IT IS WRITTEN IN R. I USED GOOGLE COLAB AS MY ENVIRONMENT WHICH DEFAULTS TO A .IPYNB.

*Which programming language and version did you pick?

  -For this project, I used R. Specifically, 'R version 4.3.3 (2024-02-29)' in Google Colab.

*Why did you pick this programming language?

  -I chose R because it is a language I have not ever used yet, and I plan to heavily involve myself in the world of data science and analytics tangentially as I focus on Artificial Intelligence and Data Mining/Machine Learning. Because of that, this project was a perfect opportunity for me to dive in. However, at times, this project felt like I bit off more than I could chew, but that is the point. After working on this heavily, I am certainly not as good with R as I am with other languages like Python, but I do feel like I would be able to read it now. It was nice to be able to use R because I am very familiar with using Colab as my environment/notebook to work in, so there was at least some familiarity there. 

*How your programming language chosen handles:

Object-oriented programming

  -What I learned from this project, with much difficulty at first, was how R handles objects. It has three different object systems: S3, S4, and R6. S3 is simple and dynamic, S4 is more robust for more inheritance etc, and R6 is more similar to Java or C++. Here, we really only used S4, specifically because of the Cell class using the setClass() function. S4 allows for more formal class definitions including explicit declaration of slots (properties with defined data types)

File Ingestion

  -Can handle various file formats for data ingestion, including CSV, Excel, JSON, XML, and various database formats. Here, we only used the CSV file provided.

Conditional Statements

  -Supports standard conditional statements such as if, else, and else if and functions like ifelse() which was very helpful.

Assignment Statements

  -Uses the <- symbol as the assignment operator, though = is also commonly used in function calls. While I was familiar with both of these before in different forms from other languages, I had to really learn them here.

Loops

  -Supports loops such as for, while, and repeat. Also loop control commands like break and next. All of which was used in my program.

Subprograms

  -Functions in R are first-class objects and are created using function(). Methodsare defined within the context of S3, S4, or R6 classes, with specific ways to use them based on the class. Here we used S4.

Unit Testing

  -Supports unit testing primarily through packages like testthat, however because I chose to work in the Colab environment, I could not use testthat. Obviously, Colab is primarily used for Python, so it does not have these libraries available. I hope in the future Google will expand the environment to include these testing features.

Exception Handling

  -Handles exceptions through functions like try(), tryCatch(), and withCallingHandlers(). 

*List out 3 libraries you used from your programming language (if applicable) and explain what they are, why you chose them and what you used them for.

  -The libraries I used are "data.table" and "methods". 
      -"data.table" is an R package that offers high-performance data manipulation capabilities, particularly suited for handling large data sets efficiently such as the Cells CSV provided and used. Also it provides concise syntax for complex operations which makes data processing tasks more straightforward and less verbose than using base functions. "data.table" syntax is employed to perform data cleaning and transformation tasks such as replacing missing values and extracting numerical values from mixed data types.
      -"methods" provides for programming with classes and methods, particularly in the S4 object system.It includes functions for defining classes and methods, creating objects, and performing method dispatch based on the class of an object. I used it because it supports S4 object-oriented programming very well, and truthfully there was no other way to do this without it. For example, it was used to define the Cell class with its properties (slots) and associated methods for initializing objects and handling specific actions like converting object details to string format.
      -I did not use a third library, however I would have given the opportunity for testing. Instead, I manually wrote out 3 tests. A library I would have used I mentioned above, "testthat". "testthat" makes testing much simpler than what I had to do, it is very similar to pyunit.

*Answer the following questions (These are directly copy and pasted from the notebook, if you open the notebook in a notebook environment the outputs will be at the bottom):

-What company (oem) has the highest average weight of the phone body?

"OEM with highest average weight: Lenovo with an average weight of 5050228.93 grams"

-Was there any phones that were announced in one year and released in another? What are they? Give me the oem and models.

"Phones announced and released in different years:"
      oem           model launch_announced
     <char>          <char>           <char>
  1: Google      Pixel 4 XL 2019, October 15
  2: Google         Pixel 4 2019, October 15
  3: Google     Pixel 3a XL     2019, May 07
  4: Google        Pixel 3a     2019, May 07
  5:  Honor         8S 2020     2020, May 27
 ---                                        
549: Huawei Y9 Prime (2019)  2019, August 01
550: Huawei P20 lite (2019)       2019, June
551: Huawei       P Smart Z        2019, May
552: Huawei  Mate 20 X (5G)        2019, May
553: Huawei       Y5 (2019)   2019, April 24
                            launch_status
                                   <char>
  1: Available. Released 2019, October 22
  2: Available. Released 2019, October 22
  3:     Available. Released 2019, May 15
  4:     Available. Released 2019, May 15
  5:     Available. Released 2020, May 27
 ---                                     
549:  Available. Released 2019, August 05
550:       Available. Released 2019, July
551:       Available. Released 2019, June
552:       Available. Released 2019, July
553:   Available. Released 2019, April 24

-How many phones have only one feature sensor?

"Number of phones with only one feature sensor: 432"

-What year had the most phones launched in any year later than 1999? 

"Year with the most phones launched after 1999: 2004, Q1 with 46 launches"
      
