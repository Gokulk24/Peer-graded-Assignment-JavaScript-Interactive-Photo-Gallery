# Peer-graded-Assignment-JavaScript-Interactive-Photo-Gallery

Several thumbnail images.

A div with the ID image where the large image and alt text will be shown.

Example:
<div id="image">Hover over an image below to display here.</div>

<img class="preview" src="img1.jpg" alt="Description 1" onmouseover="upDate(this)" onmouseout="undo()">
<img class="preview" src="img2.jpg" alt="Description 2" onmouseover="upDate(this)" onmouseout="undo()">
<!-- Add more images as needed -->

2. Write the JavaScript Code
You need two functions: upDate(previewPic) and undo().


function upDate(previewPic) {
    // Log to check function triggers
    console.log("Mouse over image");
    console.log("Alt text:", previewPic.alt);
    console.log("Image source:", previewPic.src);

    // Update the #image div's background and text
    let displayDiv = document.getElementById('image');
    displayDiv.style.backgroundImage = "url('" + previewPic.src + "')";
    displayDiv.innerHTML = previewPic.alt;
}

function undo() {
    // Reset the background image and text
    let displayDiv = document.getElementById('image');
    displayDiv.style.backgroundImage = "url('')";
    displayDiv.innerHTML = "Hover over an image below to display here.";
}
