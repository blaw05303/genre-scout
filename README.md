# Genre-Scout
My app helps a small indie game studio decide which genre to make its next game in by comparing genres’ ratings, player counts, number of competing games, and typical prices in Steam’s most-reviewed games.
 A course project for **MIST 4600: Computer Programming in Business** at the University of Georgia's Terry College of Business (Fall 2026).

## Problem
My user is indie game developers, these developers need to decide what genre their next game should be, and why it's hard without your app. (2-3 sentences)

## What it does
My app answers three questions:
1. **Quality:** Which genres have the best rated games, and what do the best-rated games in those genres have in common? 
2. **Room to grow:** Which genres have many players but few games?
3. **Price:** In the most promising genres, what price do the best-rated games charge?
4. **Timing:** Which genres have the most top games released in recent years, so the studio can tell growing genres from fading ones?

## Data
The [Steam Games Dataset](https://www.kaggle.com/datasets/artermiloff/steam-games-dataset) on Kaggle, collected in March 2025. The dataset is shared under the MIT License by its creator, artermiloff. This repo uses `steam_games.csv`, a smaller file made for the course: the 1,000 games with the most reviews.

## Built with
- Python and pandas, in Google Colab
- [Google Gemini API](https://ai.google.dev/) through the `google-genai` library: listing 3 distinct similarities between top genres

## How to run it
1. Click **Open in Colab** above, or open `Genre_Scout.ipynb` from this repository in [Google Colab](https://colab.research.google.com).
2. Put `steam_games.csv` (in this repository) in your Google Drive, in the same folder as the notebook.
3. Get a free Gemini API key at [aistudio.google.com](https://aistudio.google.com) (use a personal Gmail account). In Colab, click the key icon on the left (Secrets), add a secret named `GOOGLE_API_KEY` with your key as its value, and turn on **Notebook access**.
4. Choose **Runtime → Run all**. Allow access to Google Drive when Colab asks.

Never type your Gemini key into the notebook: this repository is public.

## Example output
**Sub-question 1:** Which genres have the best rated games, and what do the best-rated games in those genres have in common?

```
       genre  pct_pos_total
0       Indie           89.6
1      Casual           88.6
2  Simulation           86.7
3   Adventure           86.2
4    Strategy           85.1
```
* **Player Agency and Open-Ended Design:** Most of these titles emphasize sandbox elements, survival, or player-driven choices rather than forcing participants down a strictly linear narrative path.
* **Multiplayer and Social Interaction:** The vast majority of these games feature robust online, cooperative, or competitive multiplayer modes designed to be played with friends or large groups of strangers.
* **Resource and Systems Management:** Players are consistently required to gather materials, manage inventories, build structures, or upgrade equipment to progress and survive within their respective environments.

**Sub-question 2:** Which genres have many players but few games?


## AI Use Disclosure
Coming soon

## Author
Brooks Lawson 
[Connect With Me!](https://www.linkedin.com/in/brooks-lawson-29a8ab357/)
