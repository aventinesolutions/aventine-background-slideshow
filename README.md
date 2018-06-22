## Raw Images
* 17122016-DSC04464 (Amsterdam Lights smear) AmsterdamGoldenParachute.jpg
* 28062016-DSC02752 (University of Évora Plato) ÉvoraPlatonic.jpg
* 02072017-DSC04906 (Biogradska Gora Montenegro) BiogradskaGreenEternity.jpg
* 20171021-DSC05517 (National Park Cristoffel, Curação) SpikeyCristoffel.jpg
* 20180303-DSC05733 (Ice on the Brouwersgracht, Amsterdam) LoneSkaterBrouwersgracht.jpg
* 20180628-DSC02714 (Capela dos Ossos, Évora) CapelaDosOssos.jpg
* 20170711-DSC05091 (Dubrovnik, Croacia) LavenderDubrovnikDreams.jpg
* IMG_20170923_155909_20170923160312624 (Haarlemmerdijk, Amsterdam) HaarlemmerdijkPurpleHaze.jpg

## Project Initalization
Use ```yarn```:

```shell
yarn install
```

If using FTP to deploy, you may use the ```rake``` tool.  If so, run
the Ruby Bundler to install gems:

```shell
bundle install
```

Set up your FTP secrets in a ```.env``` file:

```
FTP_SERVER=<host>
FTP_USER=<user>
FTP_PASSWORD=<password>
FTP_DEBUG=<true or false>
```

## Webpack

To build the webpack bundle and watch changes:
```shell
yarn build
```

To build once (while releasing):
```shell
yarn build-once
```

## Deploying with Rake tool (FTP only)

Using your normal FTP client, build the folder structure as follows
(```/public/backgrounds-test``` is the example here):

```
/public/backgrounds-test
/public/pbackgrounds-test/dist
/public/backgrounds-test/dist/font
/public/backgrounds-test/images
/public/backgrounds-test/images/backgrounds
```

Adjust the ```deploy.yml``` configuration according to your structure.

Then run:
```shell
rake --trace
```

## Adobe Lightroom Classic


I have checked in the Lightroom catalog to show how I got from the raw
images to the web background JPEG's.











