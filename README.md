# QwikLabs - Detect Labels, Faces, and Landmarks in Images with the Cloud Vision API
Lab completed by Pat Sweetman during Google Cloud OnAir: The Journey From Big Data to AI. Sources include:
* QwikLabs
* Google

## Languages
* JSON
## Uses
This repository should be used as a reference. This does not build, and is not an application. Any attempt to build this as an application will almost certainly fail :)
## API Usage
Curl request can be used to with json payload including Image URL string or Google Storage URL
1. Be sure to `export API_KEY={your-api-key}` for this curl command to work
2. You should be located in the same directory as `request.json`
```
curl -s -X POST -H "Content-Type: application/json" --data-binary @request.json  https://vision.googleapis.com/v1/images:annotate?key=${API_KEY}
```
* search the Internet for additional details on our image.
* find emotions of the faces and their location in the image.
* Logo detection: identify common logos and their location in an image.
* Safe search detection: determine whether or not an image contains explicit content.
* return a list of labels (words) of what's in your image.
* identify landmarks - the name of the landmark, its latitude longitude coordinates, and the location of where the landmark was identified in an image.
