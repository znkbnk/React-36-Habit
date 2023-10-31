Step 1: Commence Deletion.

- Begin by removing the following buttons:
edit, favorite, delete, complete, and any
associated functionality from HabitList.js

Step 2: Delete showCompletedHabits.

- Remove the const showCompletedHabits = 
!showUnfinished; line since we won't
need it anymore.

Step 3: Modify Filtering Logic. This will
address the problem of toggling between
finished and unfinished states.

- Use the showUnfinished state to determine
whether to show finished or unfinished habits.
When showUnfinished is true, filter and
show only unfinished habits (where goalDays
is greater than 0). When showUnfinished is
false, filter and show only finished habits
(where goalDays is 0).

Step 4: Handling Habit Deletion. To ensure 
the data remains in the history.

- Check if the goalDays of the habit is
equal to 0.
- If the habit can be deleted, create an
updated list of habits by filtering out the
habit to be deleted using the filter method.
It uses the key property to identify the
habit to be removed.
- Update the habits state and store the
updated habit list in local storage using
localStorage.setItem.
- If the habit can be deleted, create a
copy of the habit with its goalDays reset
to its initial value and add it to the
completedHabits state.
- Save the updated completed habits
list to storage.
- Display a toast message to inform the
user about the outcome of the deletion.
- Create the button code to trigger the
handleDeleteHabit function when clicked
and disable it if the habit's goalDays
is greater than 0

