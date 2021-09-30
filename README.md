Gliding waypoints and turnpoints for the Cape (and possibly South Africa) for XCSoar, Oudie, etc.

#### Project aims:
1. One, [single point of truth](https://en.wikipedia.org/wiki/Single_source_of_truth)
for [waypoints](https://xkcd.com/927/), locations, unique short codes, and descriptions.
2. Version controlled, with full history.
3. Open source, open data, including all history, versions, changes, and motivations.
4. Anybody can contribute (and anybody can fork).
5. Automatically incorporated into XCSoar, Oudie, etc.

---
An easily editable version of the waypoints can be found on this 
[spreadsheet](https://docs.google.com/spreadsheets/d/13YJ6NrfoLhxTgeO8fi1aIT0n_nm4z0_ixXWjndgwzjE/edit#gid=364570956).

A map version of the waypoints can be found
[here](https://www.google.com/maps/d/u/0/edit?mid=1OdQ9Jp9IcUgXAMa7qQpaBRQReOhAuitc&usp=sharing).

---
#### Precedents
The BGA waypoint policy:

1. [Policy](http://www.newportpeace.co.uk/turningpoints.htm)

Arizona gliding community waypoint documentation:

1. [Instructions for updating and editing](https://docs.google.com/presentation/d/1pMjyXVpgSP-2waq6FuD5_nyMrU_6ApVSMYG6YpMSBvM/edit?usp=sharing)
1. [Map](https://www.google.com/maps/d/u/0/edit?mid=1kHawbgbNa_hPMl5rvOVMP27UdMX1PvQ_&ll=32.39213804431958%2C-111.49211784793266&z=11)
1. [Waypoint repository](https://github.com/DavisChappins/AZTurnpoints).

---
### User Instructions

To use the waypoint file on your glide computer (that supports CUP files):

1. Download or copy the 
[South_Africa_Cape.cup](https://raw.githubusercontent.com/csindle/waypointsZA/master/South_Africa_Cape.cup)
file to the correct location.
2. Activate it.

(In future, we will have official time based releases, to ensure strict version synchronisation. 
E.g. `South_Africa_Cape_2022-01-15.cup`).

---
### Contributor Instructions

*Contributions, comments, requests, and suggestions are very welcome.*

1. Click on `South_Africa_Cape.cup` file. 
2. Click on the pencil icon in the top right corner.
3. Modify the file as necessary, try to keep changes to a single function or turnpoint so that a history is easily viewable.
4. At the bottom of the page, write a quick summary of changes. E.g. "Deleted duplicate waypoint." and click "Propose changes".
5. Click "Create pull request" (twice). 
6. A maintainer with write access to the master branch can then approve and merge changes.

For a more detailed step-by-step walk through, see Davis from Arizona's instructions
[here](https://docs.google.com/presentation/d/1pMjyXVpgSP-2waq6FuD5_nyMrU_6ApVSMYG6YpMSBvM/edit?usp=sharing
).

---
### Maintainer Instructions

#### Convert CSV (spreadsheet) 🠪 CUP:

1. Download the [Google Sheet](https://docs.google.com/spreadsheets/d/13YJ6NrfoLhxTgeO8fi1aIT0n_nm4z0_ixXWjndgwzjE/edit#gid=364570956)
as a CSV file.
2. Remove all Columns after K (i.e. keep only the first 11 columns).
3. Run `./sanitise.py in.cup` to create a verified output .cup file.
4. Rename output file appropriately and commit, push, and publish.

#### Convert CUP 🠪 KML (Google Earth):

1. `gpsbabel -i xcsv,style=script/name_cup.style -f South_Africa_Cape.cup  -o kml -F South_Africa_Cape.cup.kml`
2. Import the KML file as a new layer on the [Google Map](https://www.google.com/maps/d/u/0/edit?mid=1OdQ9Jp9IcUgXAMa7qQpaBRQReOhAuitc&usp=sharing)
 layer.
3. Rename, and delete the old layer.

---
#### Resources:

1. [CUP file specification](https://downloads.naviter.com/docs/CUP-file-format-description.pdf)

