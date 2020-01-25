# Multi-Image Comparison Slider

Compare images with a multiple image slider. 
With this slider, you can compare multiple images all in one slider window. This is a slider that allows users to select and compare multiple images using side panel buttons.


# Features

1. Left and Right buttons to actively change the left and right images on the slider.
   
2. The slider is optimized to fit the screen width and resizes with the browser window.


# Demo

Below is demo gif of the image slider.

![](images/demo/imagery_demo.gif)





# Using it with Your Imagery

1. Replace the images in the images/imagery directory with your images.
You can also create your own folder inside the images/ directory but remember to change the paths in the compare.js and compare.html files.

2. Open the ```compare.html``` file and locate the div with id='sliderbox'. Change the src attributes for the 'img-right' and 'img-left' to the path of the default images you would like to have as the initial slider images. 
For example, changing the initial values to ```edited.jpg``` and ```unedited.jpg``` would change the file to:

```html
    <div id="sliderbox" class="img-container">
        <!-- Right Image -->
        <img class="fitcenter" id="img_right" src="images/imagery/edited.jpg">
        <!-- Left image -->
        <div class="imgholder img-top">
            <img class="fitcenter" id="img_left" src="images/imagery/unedited.jpg">
        </div>
        <span class="handle"></span>
    </div>
```

3. All that is left at this point is to point the left and right buttons to your images. You do this by:

    a. Open the ```compare.js``` file and locate the line with, ```var filenames```.

    b. Inside this filenames, you shall put all the images you want in the slider and their button names. For example, if you have 4 images edited.jpg, unedited.jpg, filtered.jpg and unfiltered. Your filename variable should be changed to:
    ```javascript
    var filenames = [
        ['edited', 'images/imagery/edited.jpg'],
        ['filtered', 'images/imagery/filtered.jpg'],
        ['un-edited', 'images/imagery/unedited.jpg'],
        ['un-filtered', 'images/imagery/unfiltered.jpg']
    ]
    ```

    Note: For each item in the filenames array, the first item is the name that will appear on the button, eg ```'edited'``` and the second item is the path to the image, eg ```'images/imagery/edited.jpg'```.

4. Change the title of the slider in the ```compare.html```, or remove it all together if not needed. 

Once this is done, save your changes and you are good to go!