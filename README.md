# CaliCubeChamps23

## Introduction

To celebrate the first inaugural [CaliCubeChamps](https://www.eventbrite.com/e/california-cube-championship-tickets-534133837687?aff=eand) in Santa Rosa, CA. This 6/10/23 - 6/11/23, I've created a Python script that scrapes Cubecobra's API and returns a dataset that shows each card per cube!

## Methodology

Following the Jupyter Notebook File and building off of my previous iteration of the [Cubecon Jupyter Analysis](https://github.com/tpugliese/Cubecon-2023) repository I've been working on, this analysis aims on the 14 Main Event cubes for this specific event:

| INDEX | CUBE NAME | ID | URL |
| :---: | :---: | :---: | :---: |
|0|Salt and Pauper cube|saltandpauper|https://cubecobra.com/cube/overview/saltandpauper | 
|1|Golden Gate Cube|ggcube|https://cubecobra.com/cube/overview/ggcube |
|2|The Jund Cube|jund-em-out|https://cubecobra.com/cube/overview/jund-em-out |
|3|aquaone powered|aquaone|https://cubecobra.com/cube/overview/aquaone |
|4|Melded Mardu Monarchy Cube|inclined|https://cubecobra.com/cube/overview/inclined |
|5|Raveyard|raveyard/|https://cubecobra.com/cube/overview/raveyard/ |
|6|Living Legacy cube|2uu|https://cubecobra.com/cube/overview/2uu |
|7|The 1/1 Cube|1-1cube|https://cubecobra.com/cube/overview/1-1cube |
|8|Unspiracy cube|3bx2j|https://cubecobra.com/cube/overview/3bx2j |
|9|Amonkar Desert Cube|amonkardesert|https://cubecobra.com/cube/overview/amonkardesert |
|10|Bloobe|22bp3|https://cubecobra.com/cube/overview/2bp3 |
|11|Artifacts & Enchantments Cube|4mq46|https://cubecobra.com/cube/overview/4mq46 |
|12|Max's Vintage Cube|maxzcube|https://cubecobra.com/cube/overview/maxzcube |
|13|Joe's anarchy cube|joescube|https://cubecobra.com/cube/overview/joescube |

You can find all of the available cubes by their Cubecobra link above.  

In the Jupyter Notebook file, you can review my code of how I turned the above `ID` Field into `.JSON` responses from Cubecobra which I turned into Python DataFrames to return the entire cardlist of the main event cubes.  The cubes were required to be "locked" (no card changes before the event)

You can follow the methodology involved, or peruse the **ccc_export_of_cards.csv** to come up with your own analysis!

Initially I have created a ["Cubemunity"](https://cubecobra.com/cube/overview/61b00e02-905a-4d68-9185-3b8f873f1f8b) of the Cards most frequently appearing in the dataset.


## Data

Quick Bits:
**6460** Unique Cards over **14** Main Event Cubes.

Artifacts & Enchantments have the *most* Cards with **600**, Mardu & Max's Vintage have the least with **360**.

Most Planeswalkers **30** with Joe's Anarchy Cube, the Salt & Pauper Cube has *0* (unsurprisingly).

### Full Export

* **ccc_export_of_cards.csv** = Every Card in Every Cube 

Export.info():
```python
<class 'pandas.core.frame.DataFrame'>
Int64Index: 6460 entries, 0 to 539
Data columns (total 27 columns):
 #   Column                    Non-Null Count  Dtype              
---  ------                    --------------  -----              
 0   index                     6460 non-null   int64              
 1   CUBE NAME                 6460 non-null   object             
 2   Cube Type                 6460 non-null   category           
 3   cardID                    6460 non-null   object             
 4   addedTmsp                 6460 non-null   int64              
 5   added_to_cube_on          6460 non-null   datetime64[ns, UTC]
 6   details_released_at       6460 non-null   object             
 7   details_name              6460 non-null   object             
 8   details_full_name         6460 non-null   object             
 9   details_artist            6460 non-null   object             
 10  details_rarity            6460 non-null   category           
 11  details_color_identity    6460 non-null   object             
 12  details_colors            6460 non-null   object             
 13  details_set               6460 non-null   object             
 14  details_cmc               6460 non-null   int8               
 15  details_parsed_cost       6460 non-null   object             
 16  details_type              6460 non-null   object             
 17  details_elo               6460 non-null   float64            
 18  details_popularity        6460 non-null   float64            
 19  details_cubeCount         6460 non-null   int64              
 20  details_loyalty           166 non-null    object             
 21  details_power             2837 non-null   object             
 22  details_toughness         2837 non-null   object             
 23  is_creature               6460 non-null   bool               
 24  is_land                   6460 non-null   bool               
 25  is_pwer                   6460 non-null   bool               
 26  days_until_added_to_cube  6460 non-null   int64              
dtypes: bool(3), category(2), datetime64[ns, UTC](1), float64(2), int64(4), int8(1), object(14)
memory usage: 1.1+ MB
```

This is just a preliminary analysis, I'd love to hear any thoughts or questions from the community about what they want to see!  

## Exports

[Cubecobra Link of the Cubes](https://cubecobra.com/cube/overview/61b00e02-905a-4d68-9185-3b8f873f1f8b) with **4** or more copies distributed among cubes in the Main Event.

## Acknowledgements

Thanks to [Joe Anderson](https://twitter.com/Fandwick) for putting on Cubecon and [Gwen Dekker](https://twitter.com/GwenDekker) for creating Cubecobra.  And thanks to you for reading!  Find me on Twitter [@tylerpug](https://twitter.com/tylerpug) or Discord (@tylerpug).