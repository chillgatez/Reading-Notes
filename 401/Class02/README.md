# Class 02 Reading: Unit Testing and Documentation

## Unit Testing Best Practices

    Unit testing ensures the correctness and reliability of the code. It is important for this lab assignment because it is literally a part of the lab. However it goes implementing in this assignment unit testing helps validate the functionality of each method in the ATM console application, ensuring that the balance calculation, withdrawal, and deposit operations work as expected.
    
    Unit testing is like quality control in a manufacturing process. Just as each component or unit of a product undergoes rigorous testing to ensure it meets the required specifications, unit testing in software development verifies that each method or unit of code functions correctly. It helps identify and catch bugs early, ensuring that the final application works as intended. Just as faulty components can affect the overall quality and functionality of a product, bugs in individual code units can impact the performance and reliability of a software application. Unit testing plays a vital role in maintaining code quality and reducing the cost of fixing issues later in the development cycle.

## The Art of ReadMe

    A well-crafted README is crucial for documenting the functionality and usage of your project or application. Writing a good README is basically creating a user manual for a product. Just as a user manual provides clear instructions, illustrations, and explanations to guide users in using a product, a README serves a similar purpose for a software application. It acts as a one-stop shop for users, offering an overview of the program, demonstrating its functionality, explaining how to use it, and providing any other relevant details. Just as a well-written user manual enhances the user experience, a comprehensive README improves the usability of a software application by making it easier for users to understand, evaluate, and utilize the features of the program.


          //insert the value into the middle of the array
      int middleIndex = arr.Length / 2;
      int[] newArray = new int[arr.Length + 1];

      for (int i = 0; i < newArray.Length; i++)
      {
        if (i < middleIndex)
        {
          newArray[i] = arr[i];
        }
        else if (i == middleIndex)
        {
          newArray[i] = value;
        }
        else
        {
          newArray[i] = arr[i - 1];
        }
      }

      return newArray;