CS 210 Project Three - Corner Grocer app
Created by Daniel Gorelkin
April 15, 2024
  
Run program.
Try to read data from .txt file.											// (Function: readSoldProducts())
If the file was successfully opened
	Read the file line by line and capitalize every product name.							// (Function: capitilize())
	Push the read product into a storage vector.									// (Function: addSoldProduct())
		If the product doesn’t yet exist in the vector:
			Set object, and add to the vector.
		Else, increment the object’s quantity by one.								// (Class Function: AddItemsSold())
	If encounter error while writing file, Throw runtime error (#2) and quit app, else close file.
Else: If the file cannot be opened, throw a runtime error (#1) and quit the app.
 
Try to write (back up) data from the storage vector to a .dat file.							// (Function: backUpSoldProducts())
  
If a writing error is encountered, throw a runtime error (#3) and quit the app; otherwise, close the file for writing.
Set while loop:
Get and Validate user input.												// (Function: getAction())
If the input is unrecognized, Print the prompt and repeat the loop.
 
Print the main menu.													// (Function: printMenu())
If input is “1”:													// (Function: searchSoldProduct())
	Get user input.
		If item found in the storage vector: Output object’s itemsSold Quantity.
		Else: Output item not found prompt.
	Return and repeat while loop
 
If input is “2”: 													// (Function: printSoldProducts())
	Print a table of all the products sold and the items in the sold quantity for each product.
Return and repeat while loop.
 
If input is “3”: 													// (Function: printProductsHistogram())
	Print a table of all the sold products and a sales graph (histogram) for each product.
Return and repeat while loop.
 
If the input is “Q”: 
End while loop.
Clear allocated memory													// (Function: clearVector())
End program.
