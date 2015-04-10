# PoPI_TestChamber
Test setup for evaluation of the Position of Participant Indicator (PoPI), a glyph design to support collaborative filtering around an interactive tabletop.

Introduces participants with glyph designs. Then draws 2 screens per glyph design for evaluation purposes with a specific task.

Can also be run from http://svencharleer.com/dev/popi/ 

## Requirements
2 versions: 

mouse https://github.com/svencharleer/PoPI_TestChamber/releases/tag/MOUSE_VERSION

TUIO https://github.com/svencharleer/PoPI_TestChamber/releases/tag/TUIO_VERSION

TUIO requires http://fe9lix.github.io/Tuio.js/ to be running on local machine. Deploy on (local) webserver and open index.html file.

## Data for evaluation
Data for evaluation is available at https://github.com/svencharleer/PoPI_TestChamber/blob/master/data/testData.json. It contains the data for 5 users around a tabletop.

E.g.

    {
        "users":["0xCC8CFF6B","0xCCfff3a2","0xCCff1313","0xCC00deff","0xCCff03f0"],
        "userLocations":[[0,0],[0.3,0],[1,0.2],[0,0.8],[0.7,1]],
        "polis":[
            {"x":0.25,"y":0.5, "size": 10,"users":[1,2]},
            {"x":0.15,"y":0.20, "size": 5,"users":[0,1]},
            {"x":0.15,"y":0.40, "size": 5,"users":[2,4]},
            {"x":0.30,"y":0.5, "size": 5,"users":[0,2,3]},
            {"x":0.40,"y":0.5, "size": 5,"users":[0,1,4]},
            {"x":0.65,"y":0.2, "size": 5,"users":[3,1]},
            {"x":0.75,"y":0.6, "size": 5,"users":[1,2,3,4]},
            {"x":0.8,"y":0.5, "size": 5,"users":[3,5]}
         ],
        "type":"static",
        "showAll":true,
        "title":"Which datapoints belong to user A?"
    },

*users*: contains the color codings for the user

*userLocations*: the position around the tabletop, defined within [0,0]-[1,1]

*polis*: positions of the PoPI glyphs (i.e. data points) (x,y) and indices of users that are highlighted for the PoPI (size: not used)

*type*: static (A), flake (B1/B2), table (C1,C2), direction (B3)

*showall*: true (B1, C1), false (B2, C2) (i.e. do not show users who are not higlighted)

*title*: task description to show evaluation test user before showing the next glyph screen



## Contact

If you wish to run this experiment, or have any questions, contact me at sven.charleer [at] gmail.com.

