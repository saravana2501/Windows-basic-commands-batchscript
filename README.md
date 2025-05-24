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
mkdir my-folder

rmdir my-folder

![Screenshot 2025-05-24 215253](https://github.com/user-attachments/assets/8f413fef-2214-400e-8a62-986ae7639336)

## COMMAND AND OUTPUT
COPY CON Rose.txt
A clock in a office can never get stolen
Too many employees watch it all the time
^Z
1 file(s) copied
dir Rose.txt

![Screenshot 2025-05-24 220209](https://github.com/user-attachments/assets/efb73e03-2a8a-46ee-b63a-aeaee598030a)

## COMMAND AND OUTPUT
echo “hello world” > hello.txt
type hello.txt

![Screenshot 2025-05-24 220351](https://github.com/user-attachments/assets/14bd1387-e3c4-482c-b469-d7b052a7f529)

## COMMAND AND OUTPUT
copy hello.txt hello1.txt

![Screenshot 2025-05-24 220442](https://github.com/user-attachments/assets/aea92769-e545-4697-a7e8-37ddb70bb426)

## COMMAND AND OUTPUT
del hello1.txt
dir hello1.txt

![Screenshot 2025-05-24 220625](https://github.com/user-attachments/assets/43775296-18e0-4f37-b1a8-cae8c9ca987a)

## COMMAND AND OUTPUT
assoc | more

![Screenshot 2025-05-24 220716](https://github.com/user-attachments/assets/6dc88484-4948-4cf4-8824-588a27ea7e6b)

## COMMAND AND OUTPUT
fc hello.txt Rose.txt

![Screenshot 2025-05-24 220807](https://github.com/user-attachments/assets/c0c45d4e-7e9f-4387-b2ca-c28ac75b8cee)

## COMMAND AND OUTPUT

## Exercise 2: Advanced Batch Scripting
Create a batch file named on the desktop. The batch file need to have a variable assigned with a desired name for ex. name="John" and display as "Hello, John".

Open Notepad with filename 1.bat and type the following batch script
```
@echo off
set name=John
echo Hello, %name%!
pause
```
Execute the batch file 1.bat

## OUTPUT

![Screenshot 2025-05-24 221207](https://github.com/user-attachments/assets/34d6d25e-1c15-4d7b-80c7-ba49bbde05dd)

![Screenshot 2025-05-24 221424](https://github.com/user-attachments/assets/e4eb38e6-3815-4609-b17a-c16e19d5838c)


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
rem Calculate remainder when divided by 2
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

![Screenshot 2025-05-24 221652](https://github.com/user-attachments/assets/cf7cf321-29b7-41d2-b3d8-9208c2e37ae0)



Write a batch file that uses a FOR loop to iterate over a sequence of numbers (1 to 5) and displays each number with the label Number:. The output should pause at the end.

```
@echo off
for %%i in (1 2 3 4 5) do (
    echo Number: %%i
)
pause
```
## OUTPUT

![Screenshot 2025-05-24 221841](https://github.com/user-attachments/assets/507647cf-6fe1-4846-9aad-30b6cdfeb6ad)



Write a batch script to check whether a file named sample.txt exists in the current directory. If the file exists, display the message sample.txt exists. Otherwise, display sample.txt does not exist. Pause the script at the end to view the result.

```
@echo off
if exist sample.txt (
    echo sample.txt exists.
) else (
    echo sample.txt does not exist.
)
pause
Instructions:
Use the IF EXIST conditional statement.
Make sure the script works for files located in the same directory as the batch file.
Use pause to keep the command window open after displaying the message.
Expected Output (if the file exists):
```

## OUTPUT

![Screenshot 2025-05-24 222057](https://github.com/user-attachments/assets/99deb1c1-610f-4580-ada3-3f37395c3e3c)

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

![Screenshot 2025-05-24 222228](https://github.com/user-attachments/assets/9fa97c62-d619-4a29-bc1b-32ac1581eb06)

# RESULT:
The commands/batch files are executed successfully.

