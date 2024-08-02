## Software Development

#### Q1. Threads allow a developer to.
- [ ] have tasks to completed in the correct order
- [x] perform tasks in parallel
- [ ] deploy only certain modules of an application
- [ ] reduce the resources needed for an application
- [ ] build a less complex application

➡️ Threads enable concurrent execution, improving performance by running multiple tasks simultaneously, utilizing multiple cores efficiently.

##

#### Q2. Which process requires automated builds and testing to verify software during development?

- [x] Continuous integration
- [ ] System integration
- [ ] Agile methodology
- [ ] Deployment integration
- [ ] Integration tests

➡️ Continuous integration refers to the build and unit testing stages of the software release process. Every revision that is committed triggers an automated build and test. With continuous delivery, code changes are automatically built, tested, and prepared for a release to production.

##

#### Q3. one strategy to keep file writes atomic is to 

- [ ] configure appropriate  system settings such as KEEP_FILE_WRITE_ATOMIC
- [x] write to a temporary  file, then rename the temporary file to the  original file via the system setting
- [ ] use a write-through cache to store the file until it can be written automatically
- [ ] write a file once read it back  and then rewrite it 
- [ ] concatenate the new file to the existing file 

➡️  The option that best ensures atomicity in file writes is writing to a temporary file and then renaming it to the original file name.

##

#### Q4. You have two microservices that need to communicate with each other without holding up a thread on either end. One service will receive an ID and return a message once the job is complete. Which communication framework should be used?

- [ ] Create a third service to handle the interaction between the services
- [ ] Have a shared database that allows both applications to read and write to the tables to share the data instead of having to communicate
- [x] Use a RESTful architecture for both, send the ID through a POST, and ping the service with a GET until a response is available
- [ ] Use asynchronous messaging to send and receive messages between each microservice
- [ ] Abandon the microservice architecture so no interaction is needed

➡️ Using RESTful APIs with POST and GET allows for simple, stateless, and scalable communication. Polling with GET requests avoids blocking threads, making it suitable for non-blocking, asynchronous interactions between microservices.

##

#### Q5. you need to build out an application that will integrate with multiple third party services, each with it's own unique API. It is Possible more service  be added later.

- [x] create a separate interface for each third-party service that contains the respective configurations.
- [ ] Have a single interface where the configuration are passed as method paramenter
- [ ] Design the solution so that the only one-third party service is used 
- [ ] Create a large integration service that will handle everything
- [ ] use thid partty service that don't require configuration 

➡️ The best approach would be to create a separate interface for each third-party service that contains the respective configurations. This will allow for scalability and flexibility in accommodating future services.

##

#### Q.6 Complete the function shown below by replacing // INSERT MISSING CODE with the correct line of code. Language: C

```
      // copy a string from the original to the destination
        // and return the number of characters copied
        int mystrcpy(char *destination, char *original) {
            int count = 0;
            while (*original != '\0') {
                *destination++ = *original++;
                // INSERT MISSING CODE
            }
            *destination = *original;
            return count;
        }
```

- [ ] original++;
- [x] count++;
- [ ] destination++;

➡️ To count the number of characters copied, insert (count++;) inside the while loop. This will increment count for each character copied from original to destination.

##


#### Q.7 check string to verify it consists of only lower-case alpha characters.  Language: C

```

#include <stdbool.h>

bool is_lowercase(const char *string) {
    char *p = string;
    do {
        if ((*p < 'a' || *p > 'z')
            && *p != '\0') {
            // INSERT MISSING CODE
        }
    } while (*p++ != '\0');
    return true;
}

```
- [x] return false;
- [ ] return true;
- [ ] break;
- [ ] continue;

➡️ The if condition checks if the current character is not within the range of lowercase letters ('a' to 'z') and is not the null terminator.If the condition is met (i.e., a non-lowercase character is found), the function should immediately return false because the string does not consist only of lowercase letters.

##

#### Q.8 What value is printed out?  Language: C

```
int[,] matrix = new int[,] { { 1, 2, 3 }, { 4, 5, 6 }, { 7, 8, 0 } };
int sum = 0;
for (int i = 0; i < matrix.GetLength(0); i++) {
    int product = matrix[i, 0];
    for (int j = 1; j < matrix.GetLength(1); j++) {
        product *= matrix[i, j];
    }
    sum += product;
}
Console.WriteLine(sum);

```

- [ ] 6
- [ ] 120
- [ ] 100
- [x] 126
- [ ] 720


➡️ First row: {1, 2, 3} Initial product = 1 Product after multiplying by 2 = 1 * 2 = 2 Product after multiplying by 3 = 2 * 3 = 6 Sum after first row = 0 + 6 = 6
Second row: {4, 5, 6} Initial product = 4 Product after multiplying by 5 = 4 * 5 = 20 Product after multiplying by 6 = 20 * 6 = 120 Sum after second row = 6 + 120 = 126
Third row: {7, 8, 0} Initial product = 7 Product after multiplying by 8 = 7 * 8 = 56 Product after multiplying by 0 = 56 * 0 = 0 Sum after third row = 126 + 0 = 126
So, the value printed out by the program is 126.

##

#### Q.9 What's wrong with this code? Language: Java

```
 public int doThings(String numberString) {
            try {
                int i = Integer.parseInt(numberString);
            } catch(Exception e) {
                System.out.println(e);
            }
            return i;
        }

```
- [ ] numberString should be null checked
- [ ] Nothing's wrong
- [x] i isn't in scope to be returned
- [ ] Integer can't cast to int
- [ ] parseInt() can't produce Exception

➡️ we will get compilation errr as i is declared inside the try block, so it is not accessible outside of that block.

##

#### Q.10 What value is printed? Language: JavaScript

```
function f(x) {
    x = "x-" + x;
    return function(y) {
        y = "y-" + x;
        return function(z) {
            return "z-" + y;
        }
    }
}

let g = f("a")("b")("c");
console.log(g);

```

- [x] z-y-x-a
- [ ] z-y-b-x-a
- [ ] z-y-a
- [ ] z-y-b

➡️ first call x become x-a return updated x.  second call y become y-x-a return updated y and in third call z becomes z-y-x-a.So, the value printed is "z-y-x-a".

##

#### Q.11 What does the function someFunction() perform? Language: Java

    ```
        public Node someFunction(Node root, int key) {
            if (root == null || root.key == key) {
                return root;
            }

            if (root.key > key) {
                return someFunction(root.left, key)
            }

            return someFunction(root.right, key)
        }
    ```

- [x] Searches through a binary tree for a value
- [ ] Checks to find null values in a binary tree
- [ ] Sorts values of a binary tree
- [ ] Builds out a binary tree
- [ ] Throws an uncaught exception on all calls

 ➡️ This code performs a binary search on a binary search tree (BST) to find and return the node with the specified key. It recursively traverses the left or right subtree based on the comparison of the current node's key with the target key.

 ##  

 #### Q.12 Complete the function shown below by replacing // INSERT MISSING CODE with the correct line of code. Language: JavaScript

    ```
        function findLargestIndex(theArray) {
            index = 0;
            largestValue = theArray[0];
            for (i = 0; i < theArray.length; i++) {
                if (theArray[i] > largestValue) {
                    index = i;
                    // INSERT MISSING CODE
                }
            }
            return index;
        }
    ```

- [x] largestValue = theArray[i];
- [ ] continue;
- [ ] i = largestValue;
- [ ] largestValue = i;
- [ ] break;

➡️ The missing code should update the largestValue to the current largest element found in the array. This ensures that the comparison in subsequent iterations is always against the largest value encountered so far

##

#### Q.13 What does this method return? Language: Java

```
 public List<Integer> someFunction(final List<Integer> numbers) {
            List<Integer> result = new ArrayList<Integer>();
            for (int i = numbers.size() - 1; i >= 0; i--) {
                result.add(numbers.get(i));
            }
            return result;
        }
```

- [ ] An incrementally sorted list
- [ ] A decrementally sorted list
- [ ] Throws ArrayIndexOutOfBoundsException
- [x] A reverse ordered list
- [ ] The same list

➡️ This code reverses a given list of integers. It iterates through the list from the end to the beginning and adds each element to a new list, which is then returned.

##

#### Q.14 Complete the function shown below by replacing # INSERT MISSING CODE with the correct line of code. Language: Python

```
 # find the count of odd numbers and
        # the smallest odd number in a list
        def get_smallest_odd(numlist):
            oddcount = 0
            smallest = float('inf')
            for num in numlist:
                if (num % 2) != 0:
                    oddcount += 1
                    if num < smallest:
                        # INSERT MISSING CODE
            return oddcount, smallest
```
- [ ] break
- [x] smallest = num
- [ ] num = smallest
- [ ] smallest = smallest + 1
- [ ] smallest = oddcount

➡️ The function checks if the number is odd (num % 2 != 0).If the number is odd, it increments the oddcount.It then compares the odd number (num) with smallest. If num is smaller, it updates smallest with this value. so the missing code will be smallest  = num.

##

#### Q.15 
