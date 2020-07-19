**Deprecated**. The examples in this repo may still be useful, but if you're just interested in viewing a Cardboard Camera photo then check out [stereo-panorama-viewer](https://github.com/bryik/stereo-panorama-viewer). All you need to do is [convert](https://storage.googleapis.com/cardboard-camera-converter/index.html) your Cardboard Camera photo and then drag-and-drop into the viewer.

<hr>

# A-Frame Cardboard Camera Example

Demonstrates how to display Cardboard Camera photos with A-Frame.

## An Easier Way?

**Updated:** August 22nd, 2016.

Rather than use this repository as a boilerplate to deploy your Cardboard Camera images to GitHub Pages, it may be easier to upload to Imgur and CodePen. Step-by-step instructions are available [here](http://bl.ocks.org/bryik/68b4044557f25bd9c578540fc4969b65).

## Use as a Boilerplate

If you want to display your own Cardboard Camera photos, feel free to fork or download this repo and replace the library images with your own.

Instructions:

1) Get vr.jpg source files off your phone and onto your computer.

2) Use [this web service](https://storage.googleapis.com/cardboard-camera-converter/index.html) to convert the vr.jpg to over-under equirectangular.

3) Split the image obtained in step (2) using a tool like ImageMagick. This command works:

```bash
    magick convert <IMAGE.png> -crop 1x2@ +repage +adjoin pano_%d.png
```

Rename the output images "left" and "right".

4) Download or fork this repository and replace the images in the asset folder with your own.

**What follows is copied from the A-Frame starter boilerplate.**

<hr>

### <sup>Option 1:</sup> Download the ZIP kit 📦

[<img src="http://i.imgur.com/UVPZoM0.png" width="200">](https://github.com/bryik/aframe-cardboard-camera/archive/master.zip)

After you have __[downloaded and extracted this `.zip` file](https://github.com/bryik/aframe-cardboard-camera/archive/master.zip)__ containing the contents of this repo, open the resulting directory, and you'll be have your scene ready in these few steps:

    npm install && npm start
    open http://localhost:3000/

<hr>

### <small><sup>Option 2:</sup> Fork this Git repo 🍴🐙

Alternatively, you can __[fork this repo](https://github.com/bryik/aframe-cardboard-camera/fork)__ to get started, if you'd like to maintain a Git workflow.

After you have __[forked this repo](https://github.com/bryik/aframe-cardboard-camera/fork)__, clone a copy of your fork locally and you'll be have your scene ready in these few steps:

    git clone https://github.com/bryik/aframe-cardboard-camera.git
    cd aframe-cardboard-camera && rm -rf .git && npm install && npm start
    open http://localhost:3000/

> :iphone: **Mobile pro tip:** Upon starting the development server, the URL will be logged to the console. Load that URL from a browser on your mobile device. (If your mobile phone and computer are not on the same LAN, consider using [ngrok](https://ngrok.com/) for local development and testing. [Browsersync](https://www.browsersync.io/) is also worth a gander.)

<hr>

## Publishing your scene

If you don't already know, GitHub offers free and awesome publishing of static sites through __[https://pages.github.com/](GitHub Pages)__.

To publish your scene to your personal GitHub Pages:

    npm run deploy

And, it'll now be live at __http://`your_username`.github.io/__ :)

<hr>

To know which GitHub repo to deploy to, the `deploy` script first looks at the optional [`repository` key](https://docs.npmjs.com/files/package.json#repository) in the [`package.json` file](package.json) (see [npm docs](https://docs.npmjs.com/files/package.json#repository) for sample usage). If the `repository` key is missing, the script falls back to using the local git repo's remote origin URL (you can run the local command `git remote -v` to see all your remotes; also, you may refer to the [GitHub docs](https://help.github.com/articles/about-remote-repositories/) for more information).

<hr>

## Still need Help?

### Installation

First make sure you have Node installed.

On Mac OS X, it's recommended to use [Homebrew](http://brew.sh/) to install Node + [npm](https://www.npmjs.com):

    brew install node

To install the Node dependencies:

    npm install


### Local Development

To serve the site from a simple Node development server:

    npm start

Then launch the site from your favourite browser:

[__http://localhost:3000/__](http://localhost:3000/)

If you wish to serve the site from a different port:

    PORT=8000 npm start


## License

This program is free software and is distributed under an [MIT License](LICENSE).
