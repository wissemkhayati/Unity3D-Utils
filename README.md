# Sample file downloader

Make downloading and displaying files through Unity3D apps easy, clean and useful.

## Getting Started

The project has two classes.

* [Test.cs](https://github.com/wissemkhayati/File-loader/blob/master/Assets/Scripts/Test.cs) - Used to test functionalities.
* [FileLoader.cs](https://github.com/wissemkhayati/File-loader/blob/master/Assets/Scripts/FileLoader.cs) - Has two functions.


## Class FileLoader

#### Function LoadImage()

Through this method the UnityWebRequestTexture Class is used to download an image and convert it to a Texture.


#### Function LoadVideo()

For downloading the data of video which is array of bytes the UnityWebRequest Class is used.


## Running the tests

Instantiate an object of FileLoader then call its method.

Firt example downloading an image from external url.

```
FileLoader loader1 = new FileLoader("downloadedImage", "http://vps587231.ovh.net/static/cocacola.png");
yield return StartCoroutine(loader1.LoadImage());
image.texture = loader1.Source_texture;
```
Second example downloading a video from external url.

```
FileLoader loader2 = new FileLoader("downloadedVideo","http://vps587231.ovh.net/static/TVPub/Stories/cocacola1.mp4");
yield return StartCoroutine(loader2.LoadVideo());
video.url = loader2.Source_video;
```
