# Ex.08 Design of Interactive Image Gallery
## Date:04-10-2025

## AIM:
To design a web application for an inteactive image gallery with minimum five images.

## DESIGN STEPS:
```
. Plan the Requirement

Decide what you want the images to do:

Enlarge on click ✅

Blink on click ✅

Or both together.

2. Set Up Basic HTML

Use <img> tags for your images.

Add a common class (e.g., clickable-image) so you can target them with CSS & JavaScript.

Example:

<img class="clickable-image" src="image1.png" alt="Image 1" />

3. Style Images with CSS

Give them a default size.

Add cursor: pointer; to indicate they are clickable.

Add smooth effects using transition.

Example:

.clickable-image {
  width: 150px;
  cursor: pointer;
  transition: transform 0.3s ease;
}

4. Create CSS Effects

For enlarging, use a .enlarged class with transform: scale(2).

For blinking, use a .blinking class with an @keyframes blink animation.

Example:

.enlarged {
  transform: scale(2);
  position: relative;
  z-index: 10;
}

@keyframes blink {
  0%, 100% { opacity: 1; }
  50% { opacity: 0; }
}

.blinking {
  animation: blink 0.5s linear infinite;
}

5. Write JavaScript for Interaction

Select all images with document.querySelectorAll().

Add click event listeners.

Toggle CSS classes (.enlarged or .blinking) on click.

Example:

const images = document.querySelectorAll('.clickable-image');

images.forEach(img => {
  img.addEventListener('click', () => {
    img.classList.toggle('blinking'); // or .enlarged
  });
});

6. Test the Functionality

Open in a browser.

Click an image → it should enlarge or blink.

Click again → it should return to normal.

7. Enhance (Optional)

Allow both enlarge + blink together by toggling both classes.

Add a close button or double click reset option.

Add a hover preview effect.
```
### Step 1:
Clone the github repository and create Django admin interface.

### Step 2:
Change settings.py file to allow request from all hosts.

### Step 3:
Use CSS for positioning and styling.

### Step 4:
Write JavaScript program for implementing interactivity.

### Step 5:
Validate the HTML and CSS code.

### Step 6:
Publish the website in the given URL.

## PROGRAM :
```
zoom.html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>Multiple Images Enlarge on Click</title>
<style>
  .clickable-image {
    width: 150px;
    height: auto;
    margin: 10px;
    cursor: pointer;
    transition: transform 0.3s ease;
  }
  .enlarged {
    transform: scale(2);
    z-index: 10;
    position: relative;
  }
</style>
</head>
<body>

<img class="clickable-image" src="Screenshot 2025-10-04 143141.png" alt="Image 1" />
<img class="clickable-image" src="Screenshot 2025-10-04 143233.png" alt="Image 2" />
<img class="clickable-image" src="Screenshot 2025-10-04 143340.png" alt="Image 3" />
<img class="clickable-image" src="Screenshot 2025-10-04 143426.png" alt="Image 4" />

<script>
  const images = document.querySelectorAll('.clickable-image');

  images.forEach(img => {
    img.addEventListener('click', () => {
      img.classList.toggle('enlarged');
    });
  });
</script>

</body>
</html>
```
## OUTPUT:
![alt text](<Screenshot 2025-10-04 144503.png>)
## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
