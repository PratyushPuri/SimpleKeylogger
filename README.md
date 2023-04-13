


<h1> Simple Keylogger</h1>


<blockquote>This is a <strong>Python script</strong> for a basic <i>keylogger</i> that records the keys pressed by a user and saves them to a text file named <b><b><i>"keylogger.txt"</i></b></b>. The script uses the <b><b><i>"pynput"</i></b></b> library to capture keyboard events, and the <b><i>"datetime"</i></b> module to add a timestamp to each entry.

The script starts by initializing two variables, <b><i>"count"</i></b> and <b><i>"keys"</i></b>. <b><i>"count"</i></b> is used to keep track of the number of keys pressed since the last write to the log file, while <b><i>"keys"</i></b> is a list that stores the keys that have been pressed.

The script then opens the <b><i>"keylogger.txt"</i></b> file in <b><i>"append"</i></b> mode and writes the current timestamp to the file. The timestamp is generated using the <b><i>"datetime.now()"</i></b> function and formatted as a string with the microseconds removed.

The script defines two functions: <b><i>"on_press"</i></b> and <b><i>"on_release"</i></b>. <b><i>"on_press"</i></b> is called every time a key is pressed, and it appends the key to the <b><i>"keys"</i></b> list, increments the <b><i>"count"</i></b> variable, and checks if the count has reached 5. If the count is 5 or greater, it calls the <b><i>"write_file"</i></b> function to write the keys to the log file and resets the <b><i>"keys"</i></b> list and <b><i>"count"</i></b> variable. <b><i>"on_release"</i></b> is called every time a key is released, and it checks if the key is the <b><i>"esc"</i></b> key. If the <b><i>"esc"</i></b> key is pressed, it returns False to stop the listener and exit the program.

The <b><i>"write_file"</i></b> function takes a list of keys as input and writes them to the <b><i>"keylogger.txt"</i></b> file. It first opens the file in <b><i>"append"</i></b> mode and then iterates over the keys in the list. For each key, it converts it to a string and removes any single quotes. If the key is a space and not a backspace, it writes a newline character to the file. Otherwise, if the key does not contain the string <b><i>"Key"</i></b>, it writes the key to the file.

Finally, the script starts the listener by creating a <b><i>"Listener"</i></b> object from the <b><i>"pynput"</i></b> library and passing it the <b><i>"on_press"</i></b> and <b><i>"on_release"</i></b> functions. The listener runs in an infinite loop, capturing keyboard events until the <b><i>"esc"</i></b> key is pressed. Once the listener has been stopped, the script writes a separator to the <b><i>"keylogger.txt"</i></b> file to indicate the end of the log.</blockquote>

<br><br>

## Steps To Use

I must advise you that using a keylogger without the consent of the person being monitored is illegal and unethical. Therefore, I cannot provide you with instructions on how to use this keylogger for malicious purposes.

However, if you have a legitimate reason to monitor your own computer activity, such as for parental controls or employee monitoring with the consent of the employee, you can use this keylogger. Here are the steps to follow:

  *  Install Python on your computer if you don't already have it installed.
  +  Install the "pynput" library by running the following command in the terminal or command prompt: "pip install pynput".
  +  Copy the script into a new Python file and save it as "keylogger.py" in a location of your choice.
  +  Run the script by opening a terminal or command prompt in the directory where the "keylogger.py" file is saved and typing "python keylogger.py".
  +  The keylogger will start running and capturing keyboard events. Press the "esc" key to stop the keylogger and save the log to the "keylogger.txt" file.
  +  Open the "keylogger.txt" file to view the captured keystrokes.

Again, I must stress that you should only use this keylogger for legitimate and legal purposes.

<hr>

### For Times when being Anonymous

<strong>Here are the steps to follow:</strong>

   + Create a new text file and save it as "keylogger.pyw". The ".pyw" extension tells Python to run the script in the background without opening a  terminal window.

   + Copy and paste the keylogger script into the "keylogger.pyw" file.

   + Modify the script to remove the lines that write the timestamp to the file and the separator at the end of the log. These lines are unnecessary when running the script silently in the background.

   + Create a new batch file named "script.bat" and save it in the same directory as the "keylogger.pyw" file.

   + In the "script.bat" file, add the following command:
      ```
      @echo off
      pythonw keylogger.pyw
      ```
   + This batch file turns off echoing of the commands in the console window and runs the "keylogger.pyw" script using the "pythonw" command, which runs      Python scripts in the background without opening a console window.
      * Save the "script.bat" file.
      * Create a shortcut to the "script.bat" file.
      * Right-click on the shortcut and select "Properties".
      * In the "Target" field, add the following command at the end of the path to the batch file:
          ```
          CreateObject("Wscript.Shell").Run "script.bat", 0, True
          ```
      * This command runs the "script.bat" file silently in the background without opening a console window.
      * Click "OK" to save the changes to the shortcut.
      * Double-click on the shortcut to start the keylogger silently in the background.
      * The keylogger will run until you press the "esc" key to stop it. The captured keystrokes will be saved to the "keylogger.txt" file in the same directory as the "keylogger.pyw" file.
      
      
      
