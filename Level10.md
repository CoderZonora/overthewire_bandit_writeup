The level description mentioned the ```strings``` command. Searched what it was and knew exactly what to do.
Using ```strings``` on **data.txt** gave a few strings but doing grep for **'====='** on the standard output of strings filtered out the password.


![VirtualBox_Ubuntu_20_10_2023_19_21_33](https://github.com/CoderZonora/overthewire_bandit_writeup/assets/140229408/18419a68-4a15-458f-9b6e-539c57f771f0)


An approach thought of before reading about the ```strings``` command was using split to create multiple files of 33 characters size and grep for **'====='** but that did not work as writing is not allowed for the current user on the server.

![VirtualBox_Ubuntu_20_10_2023_19_20_54](https://github.com/CoderZonora/overthewire_bandit_writeup/assets/140229408/7e5831c3-1336-44d3-a8a6-5f5733a03a08)


Password for bandit10:G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s
