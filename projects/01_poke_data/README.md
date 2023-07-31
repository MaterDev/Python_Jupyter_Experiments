# Pokémon Data Retrieval and Analysis

![Poke Data Cover](./images/cover.png)

This project retrieves data for 1281 Pokémon from the PokéAPI and saves it as a CSV file. The data includes each Pokémon's name, ID, types, and stats (HP, Attack, Defense, Special Attack, Special Defense, and Speed). The project also includes statistical analysis and data visualization components.

## Function: `get_pokemon_data()`

This function retrieves Pokémon data from the PokéAPI, stores it in a pandas DataFrame, and saves it as a CSV file at `./data/pokemon.csv`.

### Process:

1. **API Request:** The function sends a GET request to `'https://pokeapi.co/api/v2/pokemon?limit=1281'` to retrieve the Pokémon data.
2. **Dataframe Creation:** An empty pandas DataFrame is created with the columns `['name', 'id', 'type1', 'type2', 'hp', 'attack', 'defense', 'special_attack', 'special_defense', 'speed']`.
3. **Data Retrieval Loop:** The function loops through each Pokémon returned by the API, sending an additional GET request to the specific URL of each Pokémon to retrieve detailed data. 

    For each Pokémon, it retrieves:
    - Name
    - ID
    - Types (Type1 and Type2; if the Pokémon only has one type, Type2 is set to None)
    - Stats (HP, Attack, Defense, Special Attack, Special Defense, Speed)
4. **Dataframe Concatenation:** The retrieved data is concatenated to the DataFrame.
5. **CSV File Creation:** The DataFrame is saved as a CSV file at `./data/pokemon.csv`.

To run this function, uncomment the line `# get_pokemon_data()`.

## Data Analysis and Visualization

This project includes several analysis and visualization methods:

- **Pokémon Type Distribution**: A bar chart that shows the distribution of the primary Pokémon types.

- **Statistical Comparison of Pokémon Types**: Uses box plots to compare the distribution of different stats (like HP, Attack, Defense, etc.) across Pokémon types.

- **Pokémon Stat Comparison (Radar Plot)**: A function that takes two Pokémon names as input and produces a radar chart comparing their stats.

- **Pokémon Team Stat Comparison (Radar Plot)**: A function that takes multiple Pokémon names as input and produces a radar chart comparing their stats.

## Dependencies

This project requires Python 3 and the following Python libraries installed:

- [Requests](https://docs.python-requests.org/en/latest/)
- [Pandas](https://pandas.pydata.org/)
- [Matplotlib](https://matplotlib.org/)
- [Seaborn](https://seaborn.pydata.org/)

## Usage

To use this script, you need to run the Python file in your terminal or command prompt. You can also import the `get_pokemon_data()` function and the visualization functions into your own Python script or Jupyter notebook.
