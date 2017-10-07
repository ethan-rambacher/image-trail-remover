# image-trail-remover

The goal of this project is to create a way to automatically remove undesirable light trails, such as from planes, from images.

I am dividing the project into 2 parts:
1. Detection
2. Removal

## Detection

My proposed algorithm for detection is as follows:
1. Create "mask" to turn all stars and star trails white and all else black.
2. Locate all contiguous white areas.
3. Determine "length" of all white areas.
4. Filter out white areas determined to be stars, not trails.
5. Somehow "tag" or record location of all areas determined to be trails.

To begin, the detection code will be prototyped in Python. For performance and integration with the removal system, this may ultimately be translated to C++ or Java, or even JavaScript or Lua for Adobe plugins.

## Removal
So far a few options have been brainstormed for removal:
1. Lightroom script/plugin
2. Photoshop script/plugin
3. Homemade "clone" operation