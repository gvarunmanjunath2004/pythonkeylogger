SIMPLE PYTHON KEYLOGGER
EXPLANATION :
 1.pynput.keyboard:  
       ### This external library provides the necessary functionalities for interacting with the keyboard. It allows the program to detect and respond to key press events.
 2.Listener Class:  
       ### This core class from pynput.keyboard creates a persistent listener that continuously monitors keyboard input.
 3.write_to_file(key) Function :
       ### Extracts the character corresponding to the pressed key.
 4.with open("log.txt", 'a') as f:
    f.write(letter)
       ### Opens the "log.txt" file in append mode ('a'), which adds new content to the end of the file without overwriting existing data.
       ### Writes the processed character to the file.
 5.with Listener(on_press=write_to_file) as l: 
      ## 
      # This with statement creates an instance of the Listener class and associates the write_to_file function with the on_press event.
      # The with statement ensures proper resource management by automatically closing the listener when the code exits the with block, even if an error occurs.
      # The l.join() method starts the listening process, initiating an infinite loop that continuously waits for key presses and executes the write_to_file function for each detected key.
HOW THE CODE WORKS:
  ##
  # Import: The code imports the necessary Listener class from the pynput.keyboard library.
  # Function Definition: The write_to_file function is defined to handle key press events and write them to the log file.
  # Listener Creation: A Listener object is created, and the write_to_file function is assigned to handle key press events.
  # Start Listening: The l.join() method starts the listener, initiating continuous monitoring of keyboard input.
  # Key Press Handling: Whenever a key is pressed:
     * The write_to_file function is called.
     * The function processes the key, handles special cases, and writes the corresponding character to the "log.txt" file.
  # Continuous Monitoring: The listener continues to monitor keyboard input indefinitely until the program is stopped.
