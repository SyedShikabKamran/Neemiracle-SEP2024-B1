# Quotes Guessing Game

## Overview
This Python script is a console-based game where players guess the author of a randomly selected quote from a website. It scrapes quotes from the [quotes.toscrape.com](https://quotes.toscrape.com) website, provides hints, and tracks game statistics.

## Requirements
- **Python Version:** 3.x
- **Libraries:**
  - requests (`pip install requests`)
  - beautifulsoup4 (`pip install beautifulsoup4`)
  - pandas (`pip install pandas`)

## How It Works

### Scraping Quotes

- Fetches a random page of quotes from the [Quotes to Scrape](https://quotes.toscrape.com) website.
- Extracts quotes, authors, and author links.

### Game Functionality

- A random quote is selected for the player to guess.
- The player has 5 attempts to guess the author.
- Hints are provided after certain numbers of incorrect guesses:
  - 3 attempts remaining: Author's birthdate and place.
  - 2 attempts remaining: Author's first name initial.
  - 1 attempt remaining: Author's last name initial.

### Game Tracking

- Tracks game results (win/loss, number of attempts remaining).
- Allows the game to continue based on the player's choice.

### Data Storage

- Saves game data to a CSV file in the Downloads folder.

## Usage

1. Run the script in a Python environment.
2. Follow the prompts to guess the author of the displayed quote.
3. After the game ends, you will be asked if you want to play again.

## Code Explanation

- **`scrappingQuoteDetails()`**: Scrapes a random page for quotes and their details.
- **`quoteForDisplay()`**: Selects a random quote and fetches author details.
- **`lastNameHint(auth)`**: Provides a hint for the last name's initial.
- **`timeNow()`**: Returns the current time for game logging.
- **`wonOrlost(tries)`**: Determines the result based on remaining attempts.
- **Game Loop**: Manages game flow, user input, and hinting.
- **Data Storage**: Saves game results to a CSV file in the Downloads folder.

## Customization

To change the location of the CSV file, modify the `path` variable in the code.
