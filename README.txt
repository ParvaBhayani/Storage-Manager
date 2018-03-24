STORAGE MANAGER
_______________

 
TEAM MEMBERS (GROUP 3)
______________________

1. Parva Udaykumar Bhayani(A20396637)
2. Shringa Bais(A20382937)
3. Monali Vijaykumar Balani(A20410147)
4. Helly Nileshbhai Modi(A20398173)


HOW TO EXECUTE THE SCRIPT
_________________________

1. Open terminal 

2. Go to the path where files are extracted

3. Run the below command: make

4. Run the below command for testing test_assign1_1.c: make run 

5. To remove object files, run following command: make clean


FUNCTIONS IMPLEMENTED
_____________________


1. initStorageManager()

 - This function is used to initialize the storage manager.


2. createPageFile()

 - This function is used to create a  new page file.
 - If the file exists, it is overwritten else, a new file is created.


3. openPageFile()

 - This function is used to open a file. We open the file in read only mode using the fopen() function.


4. closePageFile()
 
 - This function sets the file pointer to NULL.


5. destroyPageFile()

 - This function checks if the file is present in memory. If it is present, the file is deleted from the memory using remove() function.


6. readBlock()

 - This function is used to read a block of file using the parameter pageNum passed in the function call.
 - Various conditions are checked before reading the file :
 	- The pointer to the file should be available.
 	- The page number should be valid i.e., we have to ensure that it is present in the file and greater than 0.
 - If all the above conditions are true, the file is read using fseek() and fread() functions. 


7. getBlockPos()

 - This function is used to return the position of the current page in the file.
 - It uses curPagePos, an attribute of File Handle which is used to store the current position of page in file.


8. readFirstBlock()
 
 - This function is used to retrieve first page from the file.


9. readLastBlock()

 - This function is used to retrieve last page from the file.


10. readPreviousBlock()

 - This function is used to fetch a block from the file that is one block before the current page position.


11. readCurrentBlock()

 - This function is used to fetch a block from the file that is pointed by the current page position.


12. readNextBlock()

 - This function is used to fetch a block from the file that is one block after the current page position.


13. writeBlock()

 - This function is used to write new content into the file in the location specified by the pageNum variable in the function call.
 - Various conditions are checked before writing into the file :
 	- The file is open and the file pointer points to it correctly.
 	- The page number should be valid i.e., we have to ensure that it is present in the file and greater than 0.
 - If the conditions are true, then we write the contents into the file using fseek() and fwrite() functions.


14. writeCurrentBlock()

 - This function is similar to the writeBlock() function except the fact that the content is written to the current page position.


15. appendEmptyBlock()

 - This function is used to add one block at the end of the file with a size of one block.
 - The new page is filled with zero bytes.
 - The total number of pages is incremented with 1.


16. ensureCapacity()

 - This function is used to check if the file has the number of pages we require. If the total number of pages in the file is less than the required number of pages, calculate the remaining number of pages to be added to the file. Then, append new empty pages in the file at the end of the file.


TEST CASES
__________

This program verifies that all the test cases mentioned in the file "test_assign1_1.c" execute correctly.
