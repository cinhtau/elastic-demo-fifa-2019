
The dataset is from [Kaggle](https://www.kaggle.com/karangadiya/fifa19) and contains over 18k+ football player information.

* The Elasticsearch Type column reflects the field type in Elasticsearch.
* The Action column describes the action for Logstash.

For instance the current market value is `€110.5M` human readable, but problematic for number ranges and comparison.
The default strategy is to keep the original value and add an additional field with the real numeric (long) value.

| Column                   | Example Value                                  | Description                        | Elasticsearch Type | Action   | 
|--------------------------|------------------------------------------------|------------------------------------|--------------------|----------| 
|                          | 0                                              | row number                         |                    | drop     | 
| ID                       | 158023                                         | unique id for every player         | internal           |          | 
| Name                     | L. Messi                                       | name                               | multi-field        |          | 
| Age                      | 31                                             | age                                | short              |          | 
| Photo                    | https://cdn.sofifa.org/players/4/19/158023.png | url to the player's photo          | keyword            |          | 
| Nationality              | Argentina                                      | nationality                        | keyword            |          | 
| Flag                     | https://cdn.sofifa.org/flags/52.png            | url to players's country flag      | keyword            |          | 
| Overall                  | 94                                             | overall rating                     | short              |          | 
| Potential                | 94                                             | potential rating                   | short              |          | 
| Club                     | FC Barcelona                                   | current club                       | keyword            |          | 
| Club Logo                | https://cdn.sofifa.org/teams/2/light/241.png   | url to club logo                   | keyword            |          | 
| Value                    | €110.5M                                        | current market value               | keyword            | convert  | 
| Wage                     | €565K                                          | current wage                       | keyword            | convert  | 
| Special                  | 2202                                           | Preferred Foot                     | integer            |          | 
| Preferred Foot           | Left                                           | left/right                         | keyword            |          | 
| International Reputation | 5                                              | rating on scale of 5               | byte               |          | 
| Weak Foot                | 4                                              | rating on scale of 5               | byte               |          | 
| Skill Moves              | 4                                              | rating on scale of 5               | byte               |          | 
| Work Rate                | Medium/ Medium                                 | attack work rate/defence work rate | multi-field        |          | 
| Body Type                | Messi                                          | body type of player                | keyword            |          | 
| Real Face                | Yes                                            |                                    | keyword            |          | 
| Position                 | RF                                             | position on the pitch              | keyword            |          | 
| Jersey Number            | 10                                             | jersey number                      | byte               |          | 
| Joined                   | "Jul 1, 2004"                                  | joined date                        | keyword            |          | 
| Loaned From              |                                                | club name if applicable            | keyword            |          | 
| Contract Valid Until     | 2021                                           | contract end date                  | short              |          | 
| Height                   | 5'7                                            | height of the player               | keyword            |          | 
| Weight                   | 159lbs                                         | weight of the player               | keyword            |          | 
| LS                       | 88+2                                           | rating on scale of 100             | keyword            |          | 
| ST                       | 88+2                                           | rating on scale of 100             | keyword            |          | 
| RS                       | 88+2                                           | rating on scale of 100             | keyword            |          | 
| LW                       | 92+2                                           | rating on scale of 100             | keyword            |          | 
| LF                       | 93+2                                           | rating on scale of 100             | keyword            |          | 
| CF                       | 93+2                                           | rating on scale of 100             | keyword            |          | 
| RF                       | 93+2                                           | rating on scale of 100             | keyword            |          | 
| RW                       | 92+2                                           | rating on scale of 100             | keyword            |          | 
| LAM                      | 93+2                                           | rating on scale of 100             | keyword            |          | 
| CAM                      | 93+2                                           | rating on scale of 100             | keyword            |          | 
| RAM                      | 93+2                                           | rating on scale of 100             | keyword            |          | 
| LM                       | 91+2                                           | rating on scale of 100             | keyword            |          | 
| LCM                      | 84+2                                           | rating on scale of 100             | keyword            |          | 
| CM                       | 84+2                                           | rating on scale of 100             | keyword            |          | 
| RCM                      | 84+2                                           | rating on scale of 100             | keyword            |          | 
| RM                       | 91+2                                           | rating on scale of 100             | keyword            |          | 
| LWB                      | 64+2                                           | rating on scale of 100             | keyword            |          | 
| LDM                      | 61+2                                           | rating on scale of 100             | keyword            |          | 
| CDM                      | 61+2                                           | rating on scale of 100             | keyword            |          | 
| RDM                      | 61+2                                           | rating on scale of 100             | keyword            |          | 
| RWB                      | 64+2                                           | rating on scale of 100             | keyword            |          | 
| LB                       | 59+2                                           | rating on scale of 100             | keyword            |          | 
| LCB                      | 47+2                                           | rating on scale of 100             | keyword            |          | 
| CB                       | 47+2                                           | rating on scale of 100             | keyword            |          | 
| RCB                      | 47+2                                           | rating on scale of 100             | keyword            |          | 
| RB                       | 59+2                                           | rating on scale of 100             | keyword            |          | 
| Crossing                 | 84                                             | rating on scale of 100             | byte               |          | 
| Finishing                | 95                                             | rating on scale of 100             | byte               |          | 
| HeadingAccuracy          | 70                                             | rating on scale of 100             | byte               |          | 
| ShortPassing             | 90                                             | rating on scale of 100             | byte               |          | 
| Volleys                  | 86                                             | rating on scale of 100             | byte               |          | 
| Dribbling                | 97                                             | rating on scale of 100             | byte               |          | 
| Curve                    | 93                                             | rating on scale of 100             | byte               |          | 
| FKAccuracy               | 94                                             | rating on scale of 100             | byte               |          | 
| LongPassing              | 87                                             | rating on scale of 101             | byte               |          | 
| BallControl              | 96                                             | rating on scale of 102             | byte               |          | 
| Acceleration             | 91                                             | rating on scale of 103             | byte               |          | 
| SprintSpeed              | 86                                             | rating on scale of 104             | byte               |          | 
| Agility                  | 91                                             | rating on scale of 105             | byte               |          | 
| Reactions                | 95                                             | rating on scale of 106             | byte               |          | 
| Balance                  | 95                                             | rating on scale of 107             | byte               |          | 
| ShotPower                | 85                                             | rating on scale of 108             | byte               |          | 
| Jumping                  | 68                                             | rating on scale of 109             | byte               |          | 
| Stamina                  | 72                                             | rating on scale of 110             | byte               |          | 
| Strength                 | 59                                             | rating on scale of 111             | byte               |          | 
| LongShots                | 94                                             | rating on scale of 112             | byte               |          | 
| Aggression               | 48                                             | rating on scale of 113             | byte               |          | 
| Interceptions            | 22                                             | rating on scale of 114             | byte               |          | 
| Positioning              | 94                                             | rating on scale of 115             | byte               |          | 
| Vision                   | 94                                             | rating on scale of 116             | byte               |          | 
| Penalties                | 75                                             | rating on scale of 117             | byte               |          | 
| Composure                | 96                                             | rating on scale of 118             | byte               |          | 
| Marking                  | 33                                             | rating on scale of 119             | byte               |          | 
| StandingTackle           | 28                                             | rating on scale of 120             | byte               |          | 
| SlidingTackle            | 26                                             | rating on scale of 121             | byte               |          | 
| GKDiving                 | 6                                              | rating on scale of 122             | byte               |          | 
| GKHandling               | 11                                             | rating on scale of 123             | byte               |          | 
| GKKicking                | 15                                             | rating on scale of 124             | byte               |          | 
| GKPositioning            | 14                                             | rating on scale of 125             | byte               |          | 
| GKReflexes               | 8                                              | rating on scale of 126             | byte               |          | 
| Release Clause           | €226.5M                                        | release clause value               | keyword            | convert  | 

