# NUMBER_GUESSING_GAME

#DESCRIPTION

This project is an engaging and interactive **Number Guessing Game** with a graphical user interface (GUI), developed using Python and the Tkinter library. Players can choose their desired difficulty level, make guesses to find a randomly generated secret number, and earn points based on how quickly they succeed. The game enhances user experience with a scoring system, CSV-based result tracking, and a leaderboard that displays the top scores.

The setup begins with importing necessary libraries. Tkinter is used for building the GUI, while additional modules like `messagebox` and `ttk` from Tkinter support pop-up messages and table-style widgets, respectively. The `random` module is used to generate the secret number, `csv` is utilized to save game results, and both `datetime` and `timedelta` are included to fetch and convert the current time into Indian Standard Time (IST). The `os` module checks whether the CSV file already exists, ensuring the leaderboard functions correctly.

A dictionary is defined to manage the difficulty levels: **Easy** allows guesses between 1 and 10 with 5 attempts, **Medium** ranges from 1 to 50 with 7 attempts, and **Hard** expands the range to 1 to 100 with a maximum of 10 attempts. These levels not only alter the guessing range but also set the limit for the number of tries. A function is created to convert the current time to IST, returning it in the formats `DD-MM-YYYY` for date and `HH:MM:SS` for time, which are later used for timestamping game results in the CSV file.

When the game is launched, the main window is initialized with a title, and key variables such as the secret number, remaining attempts, score, and player details are set. The GUI is built using Tkinter widgets including labels, buttons, entry fields, and dropdown menus. Players must first enter their name (a required step to begin the game), select a difficulty level, and click the “Start Game” button. If no name is entered, the program prompts a warning through a pop-up message.

Upon starting the game, a random number is generated based on the chosen difficulty level. The player begins guessing, and the game provides feedback after each attempt. If the guess is too low or too high, an appropriate message is displayed. When the player correctly guesses the number, a congratulatory message appears, and the final score—starting from 100 and decreasing by 10 with each incorrect guess—is shown. The game ends either when the correct number is guessed within the allowed attempts or when the player runs out of attempts. In the latter case, the correct answer is revealed, and the game resets for a new session.

Each game session concludes with the results being written to a CSV file. If the file doesn't exist, it is created and headers are added. The stored information includes the player’s name, date, time, difficulty level, the secret number, number of attempts used, final score, and whether the player won or lost. Additionally, a leaderboard feature is implemented through a "Show Leaderboard" button. This opens a new window displaying the top 10 scores from all recorded games. The leaderboard reads the CSV file, sorts the records in descending order of scores, and presents them in a structured table format showing name, score, date, time, and result. If the file contains no data, a popup informs the user that no game data is available.

#OUTPUT

