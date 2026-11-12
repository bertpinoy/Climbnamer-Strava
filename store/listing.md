# Store listing — ClimbNamer for Strava

Texts to paste into the Chrome Web Store Developer Dashboard.

## Basics

| Field | Value |
|---|---|
| Chrome Web Store | Not published separately (publisher limit of 2 extensions): included in ClimbNamer for Garmin Connect and Strava 1.6.0, item `ejokejjhepoeeebomjahihncemjbmfda` |
| Name | ClimbNamer - for Strava *(from the manifest)* |
| Category | *Productivity* (or *Tools*) |
| Language | English |
| Homepage / support URL | https://github.com/bertpinoy/Climbnamer-Strava |
| Support / contact | https://github.com/bertpinoy/Climbnamer-Strava/issues |
| Privacy policy URL | https://github.com/bertpinoy/Climbnamer-Strava/blob/main/PRIVACY.md |
| Icon | `extension/icons/icon-128.png` (from the zip) |
| Small promo tile (440×280) | `store/promo-tile-440x280.png` |
| Marquee promo tile (1400×560) | `store/marquee-1400x560.png` |
| Screenshots | `store/screenshots/*.png` (1280×800), see below |

## Short description (manifest, max 132 characters)

> Finds and names the climbs on your Strava routes, using OpenStreetMap. Not affiliated with Strava.

## Detailed description

```
Know which climbs are on your route.

Strava shows the elevation profile of your routes, but not where the climbs are or what they're called. ClimbNamer finds them and names them: Kemmelberg, Koppenberg, Mur de Huy, Col du Galibier.

WHAT IT DOES
When you open a route on strava.com, ClimbNamer detects its climbs from the elevation profile, with criteria similar to Garmin's ClimbPro, and shows a small panel with every climb:
• its name
• length, average gradient and elevation gain
• where on the route it starts

The climbs also appear on Strava's own elevation chart, as orange numbered bands. Hover a climb in the panel to highlight it on the chart; click it to pick it out and see its top on the map.

WHY YOU'LL LIKE IT
• Plan better: see which climbs are on a route before you ride it or send it to your bike computer.
• Your own names: don't agree with a name, or want a local nickname? Rename the climb. Your name is used for that climb on all your routes.
• Fast: climbs named after a summit or pass appear instantly. Summits for Belgium, the Netherlands and Luxembourg are built in; elsewhere they are downloaded once per area. Every climb is looked up only once and remembered.
• Nothing to set up: install it, open a route on Strava, done.

WHERE THE NAMES COME FROM
ClimbNamer uses OpenStreetMap, the free world map made by volunteers:
1. If there is a named hill, summit or mountain pass at the top of the climb, that name is used.
2. Otherwise it uses the road the climb follows. In Flanders that is often the climb's name itself (Koppenberg, Paterberg, Oude Kwaremont).
3. Otherwise it says which village the climb is near.

Is a name wrong or missing? Rename the climb, or improve OpenStreetMap so every rider benefits.

PRIVACY
• No account and no sign-up.
• No tracking, no analytics, no advertising.
• No server of our own: nothing is sent to the developer.
• ClimbNamer only reads the route data that the Strava page already contains in your browser. Only the location of the climbs, and the outline of the area around them, is sent to public OpenStreetMap services to look up names.
• Your own climb names and settings are stored in your browser.
Full privacy policy: https://github.com/bertpinoy/Climbnamer-Strava/blob/main/PRIVACY.md

FAIR TO OPENSTREETMAP
The OpenStreetMap services are free and run by volunteers and non-profits. ClimbNamer is careful with them: each climb is looked up only once, summits are fetched once per area instead of per climb, requests go one at a time, and it pauses when the services are busy.

GOOD TO KNOW
• Works on strava.com route pages in Google Chrome and Microsoft Edge. You need your own Strava account.
• ClimbNamer never changes anything in your Strava account.
• Open source: https://github.com/bertpinoy/Climbnamer-Strava. Questions, ideas or a climb with a wrong name? Open an issue there.
• Also available for the Hammerhead dashboard and Garmin Connect.

ClimbNamer is an independent project and is not affiliated with, endorsed by or sponsored by Strava. Strava is a trademark of Strava, Inc. ClimbPro is a trademark of Garmin Ltd.
Map data © OpenStreetMap contributors, ODbL.
```

## Chrome: Privacy practices tab

**Single purpose description**

```
ClimbNamer finds the climbs on the user's routes on Strava (www.strava.com) and shows their names, looked up in OpenStreetMap, in a panel and on the route's elevation chart.
```

**Permission justifications**

*storage*
```
Stores a cache of climb names so each climb is looked up only once, the named summits of areas the user looked at, the user's own names for climbs, and the extension's settings. Nothing is sent to the developer.
```

*declarativeNetRequestWithHostAccess*
```
Used only to set an identifying User-Agent header ("ClimbNamer/<version> (+https://github.com/bertpinoy/Climbnamer-Strava)") on the extension's own requests to the OpenStreetMap services (overpass-api.de, overpass.kumi.systems, nominatim.openstreetmap.org), as their usage policies require apps to identify themselves. The rule is limited to requests initiated by this extension; it does not block, redirect or modify any other requests.
```

*Host permission use*
```
https://www.strava.com/*: the extension runs only on Strava, where it reads the route data the route page already contains to detect the climbs, and shows their names in the page. It never changes anything in the user's account.
https://overpass-api.de/*, https://overpass.kumi.systems/* and https://nominatim.openstreetmap.org/*: public OpenStreetMap services used to look up the names of summits, passes, roads and villages at the coordinates of each climb. Only climb coordinates are sent.
```

**Remote code:** No, I am not using remote code.

**Data usage:** tick **Location** (climb coordinates are sent to OpenStreetMap services
to look up names); leave the other categories unticked. Tick all three certifications.

## Screenshots

Upload in this order (1280×800 PNG):

1. `screenshots/1-route-climbs-chart.png`: a 24 km route with five climbs (Vidaigneberg,
   Rodeberg, Monteberg, Kemmelberg and a road climb) as numbered bands on Strava's
   elevation chart; climb 5 selected.
2. `screenshots/2-route-many-climbs.png`: an 86 km route with seven climbs, named after
   summits (Scherpenberg, Vidaigneberg, Baneberg, Monteberg, Kraaiberg) and roads.

Originals are scaled to fit 1280×800; thin dark bands fill the rest, so nothing is
cropped.
