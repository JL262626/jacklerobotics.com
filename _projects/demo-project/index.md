---
layout: post
title: Ball Balancing Robot
description:  Created a high‑precision ball‑balancing robot using a custom 3RRS parallel
  manipulator, dual‑ESP32 control, and computer‑vision tracking, achieving
  a steady‑state error of under 1 mm from the target.
skills: 
  - ESP32
  - C++
  - Python
  - PID Control
  - Computer Vision
  - PCB Design
  - KiCad
  - Fusion 360
  - 3D Printing
  - MATLAB

main-image: /BOBCOVER.jpg
---

---
# Aim
- To build a robot capable of balancing a ball on a platform indefinitely, with <1mm steady-state error
- Keep the total cost under $150 by only using ESP32-based hardware

# Result
- Achieved <1mm steady-state error during balancing
- Developed a 40 FPS ball detection algorithm running on a ESP32
- Integrated control panel with live telemetry, allowing users to intuitively explore PID behaviour
- Won the 10K Club Competition, securing $10,000 to continue developing the project

{% include youtube-video.html id="5z0NnkYsKTI" autoplay= "false"%}

{% include image-gallery.html images="BOB_internals.jpg" height="400" %} 
place the images in project folder/images then update the file path.   


## Embedding youtube video
The second video has the autoplay on. copy and paste the 11-digit id found in the url link. <br>
*Example* : https://www.youtube.com/watch?v={**MhVw-MHGv4s**}&ab_channel=engineerguy
{% include youtube-video.html id="MhVw-MHGv4s" autoplay= "false"%}
{% include youtube-video.html id="XGC31lmdS6s" autoplay = "true" %}

you can also set up custom size by specifying the width (the aspect ratio has been set to 16/9). The default size is 560 pixels x 315 pixels.  

The width of the video below. Regardless of initial width, all the videos is responsive and will fit within the smaller screen.
{% include youtube-video.html id="tGCdLEQzde0" autoplay = "false" width= "900px" %}  

<br>

## Adding a hozontal line
---

## Starting a new line
leave two spaces "  " at the end or enter <br>

## Adding bold text
this is how you input **bold text**

## Adding italic text
Italicized text is the *cat's meow*.

## Adding ordered list
1. First item
2. Second item
3. Third item
4. Fourth item

## Adding unordered list
- First item
- Second item
- Third item
- Fourth item

## Adding code block
```ruby
def hello_world
  puts "Hello, World!"
end
```

```python
def start()
  print("time to start!")
```

```javascript
let x = 1;
if (x === 1) {
  let x = 2;
  console.log(x);
}
console.log(x);

```

## Adding external links
[Wikipedia](https://en.wikipedia.org)


## Adding block quote
> A blockquote would look great if you need to highlight something


## Adding table 

| Header 1 | Header 2 |
|----------|----------|
| Row 1, Col 1 | Row 1, Col 2 |
| Row 2, Col 1 | Row 2, Col 2 |

make sure to leave aline betwen the table and the header


