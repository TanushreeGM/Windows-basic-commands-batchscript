# Windows-basic-commands-batchscript
Ex08-Windows-basic-commands-batchscript

# AIM:
To execute Windows basic commands and batch scripting

# DESIGN STEPS:

### Step 1:

Navigate to any Windows environment installed on the system or installed inside a virtual environment like virtual box/vmware 

### Step 2:

Write the Windows commands / batch file . Save each script in a file with a .bat extension. Ensure you have the necessary permissions to perform the operations. Adapt paths as needed based on your system configuration.
### Step 3:

Execute the necessary commands/batch file for the desired output. 




# WINDOWS COMMANDS:
## Exercise 1: Basic Directory and File Operations
Create a directory named "my-folder"

## COMMAND AND OUTPUT

Remove the directory "my-folder"
<img width="348" height="84" alt="image" src="https://github.com/user-attachments/assets/f6636c59-5528-4c66-9e8f-681d287b14ea" />

## COMMAND AND OUTPUT


Create the file Rose.txt
<img width="553" height="300" alt="image" src="https://github.com/user-attachments/assets/1fbd0bc2-c1b9-46f8-88c5-0de4786134a4" />

## COMMAND AND OUTPUT


Create the file hello.txt using echo and redirection
<img width="454" height="104" alt="image" src="https://github.com/user-attachments/assets/1c90fc15-d8e4-4446-a48c-08dced4012f2" />

## COMMAND AND OUTPUT

Copy the file hello.txt into the file hello1.txt
<img width="451" height="110" alt="image" src="https://github.com/user-attachments/assets/f7bd251d-19f4-4eab-9d99-b58d6ed74b9a" />

## COMMAND AND OUTPUT

Remove the file hello1.txt
<img width="400" height="186" alt="image" src="https://github.com/user-attachments/assets/91dd8bfa-9333-4c69-b0ab-ea2dc4e05fde" />

## COMMAND AND OUTPUT

List out the file hello1.txt in the current directory
<img width="400" height="186" alt="image" src="https://github.com/user-attachments/assets/f8ecea9f-1a58-4eb4-8964-2040aaf85e40" />

## COMMAND AND OUTPUT

List out all the associated file extensions 
<img width="419" height="334" alt="image" src="https://github.com/user-attachments/assets/6250c54e-a6ef-4deb-bc43-c66b68b416d6" />

## COMMAND AND OUTPUT
<img width="450" height="166" alt="image" src="https://github.com/user-attachments/assets/41d03d6a-ea2e-42ef-b68e-6a60de0bbd9f" />


Compare the file hello.txt and rose.txt

## COMMAND AND OUTPUT

## Exercise 2: Advanced Batch Scripting
Create a batch file named on the desktop. The batch file need to have a variable assigned with a desired name for ex. name="John" and display as "Hello, John".
```
@echo off
set name=John
echo Hello, %name%!
pause
```




## OUTPUT
<img width="398" height="68" alt="image" src="https://github.com/user-attachments/assets/a3287f3c-0c66-4f8a-820e-4db0be5de29b" />



Create a batch file  on the desktop that checks whether a user-input number is odd or not. The script should:
Prompt the user to enter a number.
Calculate the remainder when the number is divided by 2.
Display whether the number is odd or not.
Ask the user if they want to check another number.
Repeat the process if the user enters Y, and exit with a thank-you message if the user enters N.
Handle invalid inputs for the continuation prompt (Y/N) gracefully.

```
@echo off
:main
set /p number=Enter a number:
set /a remainder=%number% %% 2

if %remainder%==1 (
    echo %number% is an odd number.
) else (
    echo %number% is not an odd number.
)

:choice
set /p continue=Do you want to check another number? (Y/N):
if /i "%continue%"=="Y" goto main
if /i "%continue%"=="N" goto end
echo Invalid choice, please enter Y or N.
goto choice

:end
echo Thank you for using the odd number checker!
pause
```


## OUTPUT
<img width="503" height="182" alt="image" src="https://github.com/user-attachments/assets/deddb838-4db5-4142-b42a-f4fcf0a74d23" />




Write a batch file that uses a FOR loop to iterate over a sequence of numbers (1 to 5) and displays each number with the label Number:. The output should pause at the end.
```
@echo off
for %%i in (1 2 3 4 5) do (
    echo Number: %%i
)
pause
```



## OUTPUT
<img width="442" height="145" alt="image" src="https://github.com/user-attachments/assets/87bca1df-5704-490f-87ae-5a2c631db2b9" />




Write a batch script to check whether a file named sample.txt exists in the current directory. If the file exists, display the message sample.txt exists. Otherwise, display sample.txt does not exist. Pause the script at the end to view the result.

Instructions:
Use the IF EXIST conditional statement.
Make sure the script works for files located in the same directory as the batch file.
Use pause to keep the command window open after displaying the message.
Expected Output (if the file exists):
```
@echo off
if exist sample.txt (
    echo sample.txt exists.
) else (
    echo sample.txt does not exist.
)
pause
```

## OUTPUT
<img width="498" height="185" alt="image" src="https://github.com/user-attachments/assets/76b51168-e257-42b4-901b-c0e73d50f585" />


Write a batch script that displays a simple menu with three options:
Say Hello – Displays the message Hello, World!
Create a File – Creates a file named newfile.txt with the content This is a new file
Exit – Exits the script with a goodbye message
The script should repeatedly display the menu until the user chooses to exit. Use goto statements to handle menu navigation.
```
@echo off
:menu
echo 1. Say Hello
echo 2. Create a File
echo 3. Exit

set /p choice=Choose an option:

if "%choice%"=="1" goto hello
if "%choice%"=="2" goto createfile
if "%choice%"=="3" goto end
goto menu

:hello
echo Hello, World!
goto menu

:createfile
echo Creating a file...
echo This is a new file > newfile.txt
goto menu

:end
echo Goodbye!
pause
```

## OUTPUT
<img width="461" height="334" alt="image" src="https://github.com/user-attachments/assets/ac3b7c9c-323b-4fd5-8f23-29fb3df1812b" />



# RESULT:
The commands/batch files are executed successfully.

