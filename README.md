# Degrees of Separation

This Python project finds the shortest connection between two actors based on the movies they've acted in, inspired by the "Six Degrees of Kevin Bacon" concept. It uses breadth-first search to determine the minimal number of shared movie links between any two actors using data from CSV files.

## Features

- Calculates the shortest path (degrees of separation) between two actors.
- Uses breadth-first search for efficient pathfinding.
- Loads actor and movie data from CSV files.
- Handles ambiguous actor names interactively.

## Project Structure

```
degrees.py
util.py
large/
    movies.csv
    people.csv
    stars.csv
small/
    movies.csv
    people.csv
    stars.csv
```

- `degrees.py`: Main program logic and data loading.
- `util.py`: Utility classes for search algorithms.
- `large/` and `small/`: Sample datasets.

## Usage

1. **Install Python 3** if you haven't already.
2. The required datasets are already included in the `large/` and `small/` directories—no need to provide your own CSV files.
3. Run the program:

    ```sh
    python degrees.py
    ```

    By default, this uses the data in the `large` directory. To use the smaller dataset, run:

    ```sh
    python degrees.py small
    ```

4. Enter the names of two actors when prompted. The program will output the shortest connection between them.

## Example

```
$ python degrees.py small
Loading data...
Data loaded.
Name: Emma Watson
Name: Daniel Radcliffe
2 degrees of separation.
1: Emma Watson and Daniel Radcliffe starred in Harry Potter and the Prisoner of Azkaban
2: Daniel Radcliffe and James McAvoy starred in Victor Frankenstein
3: James McAvoy and Jennifer Lawrence starred in X-Men: First Class
```
