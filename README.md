## Sample Images
* 17122016-DSC04464 (Amsterdam Lights smear) AmsterdamGoldenParachute.jpg
* 28062016-DSC02752 (University of Évora Plato) EvoraPlatonic.jpg
* 02072017-DSC04906 (Biogradska Gora Montenegro) BiogradskaGreenEternity.jpg
* 20171021-DSC05517 (National Park Cristoffel, Curação) SpikeyCristoffel.jpg
* 20180303-DSC05733 (Ice on the Brouwersgracht, Amsterdam) LoneSkaterBrouwersgracht.jpg
* 20180628-DSC02714 (Capela dos Ossos, Évora) CapelaDosOssos.jpg
* 20170711-DSC05091 (Dubrovnik, Croacia) LavenderDubrovnikDreams.jpg
* IMG_20170923_155909_20170923160312624 (Haarlemmerdijk, Amsterdam) HaarlemmerdijkPurpleHaze.jpg

## LESS Variables

Variables are used to determine the length of the slideshow animation and the URL locations
of the slide images and you will need to provide them in order to transpile the CSS. 

The sample page includes 7 slides using the following variables:

```
@length-animation: 175s;
@total-slides: 7s;

@slide1-url: "../images/backgrounds/AmsterdamGoldenParachute.jpg";
@slide2-url: "../images/backgrounds/CapelaDosOssos.jpg";
@slide3-url: "../images/backgrounds/HaarlemmerdijkPurpleHaze.jpg";
@slide4-url: "../images/backgrounds/LavenderDubrovnikDreams.jpg";
@slide5-url: "../images/backgrounds/LoneSkaterBrouwersgracht.jpg";
@slide6-url: "../images/backgrounds/SpikeyCristoffel.jpg";
@slide7-url: "../images/backgrounds/EvoraPlatonic.jpg";
```

## Changing the Number of Slides

The sample page contains 7 slides.  To change the number of slides, besides changing the
variables, you'll have to change the slideshow LESS. 

For example, this would be the 8th slide:

```css
li:nth-child(8) {
  @delay-slide8: 7s * @length-animation / @total-slides;

  .delay-slide8() {
    -webkit-animation-delay: @delay-slide8;
    -moz-animation-delay: @delay-slide8;
    -o-animation-delay: @delay-slide8;
    animation-delay: @delay-slide8;
  }

  div {
    .delay-slide8();
  }

  span {
    .delay-slide8();
    background-image: url(@slide8-url);
  }
}
```

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











