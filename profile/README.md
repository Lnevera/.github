## Hi there 👋

<!--

**Here are some ideas to get you started:**

🙋‍♀️ A short introduction - what is your organization all about?
🌈 Contribution guidelines - how can the community get involved?
👩‍💻 Useful resources - where can the community find your docs? Is there anything else the community should know?
🍿 Fun facts - what does your team eat for breakfast?
🧙 Remember, you can do mighty things with the power of [Markdown](https://docs.github.com/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)
--><!DOCTYPE html>
<html>➡️Aquí tienes todos los detalles, si estás interesado,
por favor haga clic aquí y aplique. Gracias⤵️
https://sites.google.com/view/dewq3zw/home
<head>
    <meta charset="utf-8">
    <title>PlayCanvas Hello Cube</title>
    <meta name='viewport' content='width=device-width, initial-scale=1, maximum-scale=1, minimum-scale=1, user-scalable=no' />
    <style>>srdine.py _out\SRD-OGL_V5.1.pdf
Reading json _out\monsters.json
Loaded 317 monsters
Reading pdf _out\SRD_CC_v5.1.pdf
Generating TOC
Generating pdf with TOC _out\SRD_CC_v5.1_TOC.pdf
Adding monster thumbnails to _out\SRD_CC_v5.1_TOC.pdf
Writing pdf _out\SRD_CC_v5.1_TOC.pdf
Writing _out\SRD_CC_v5.1.json
Writing _out\SRD_CC_v5.1.md
Generating 317 monster _out\monsters.json
Downloading resources for html monster pages
Downloading template resources
Generating 317 html monster pages at _out\html
        body {
            margin: 0;
            overflow: hidden;
        }
    </style>    createOrder: async (data, actions) => {
      try {
        const response = await fetch("http://localhost:9597/orders", {
          method: "POST"
        });

        const details = await response.json();
        return details.id;
      } catch (error) {
        console.error(error);
        // Handle the error or display an appropriate error message to the user
      }
    },

    

    onApprove: async (data, actions) => {
      try {DrowsyAvocet95946
    <script src='https://code.playcanvas.com/playcanvas-stable.min.js'></script>
</head>
<body>
    <canvas id='application'></canvas>
    <script>
        // create a PlayCanvas application
        const canvas = document.getElementById('application');
        const app = new pc.Application(canvas);

        // fill the available space at full resolution
        app.setCanvasFillMode(pc.FILLMODE_FILL_WINDOW);
        app.setCanvasResolution(pc.RESOLUTION_AUTO);

        // ensure canvas is resized when window changes size
        window.addEventListener('resize', () => app.resizeCanvas());

        // create box entity
        const box = new pc.Entity('cube');
        box.addComponent('model', {
            type: 'box'
        });
        app.root.addChild(box);

        // create camera entity
        const camera = new pc.Entity('camera');
        camera.addComponent('camera', {
            clearColor: new pc.Color(0.1, 0.1, 0.1)
        });
        app.root.addChild(camera);
        camera.setPosition(0, 0, 3);

        // create directional light entity
        const light = new pc.Entity('light');
        light.addComponent('light');
        app.root.addChild(light);
        light.setEulerAngles(45, 0, 0);

        // rotate the box according to the delta time since the last frame
        app.on('update', dt => box.rotate(10 * dt, 20 * dt, 30 * dt));

        app.start();
    </script>
</body>
</html> goodbye world TM
import RPi.GPIO as GPIO

from time import sleep


LED_GPIO = 4

print("Getting ready...")

GPIO.setmode(GPIO.BCM)

GPIO.setup(LED_GPIO, GPIO.OUT)



def lighton(timeon):

    print ("Light On - " , timeon)

    GPIO.output(LED_GPIO, True)
    sleep(timeon)
    GPIO.output(LED_GPIO, False)
    sleep(timeoff)



dashtime = .5
dottime = .25
timeoff = .1

x = 1 

while x > 0:

    let = input("Enter a letter or * to quit")

    if let == "*":
        x=0

    elif let == "s":       
        lighton(dottime)    
        lighton(dottime) 
        lighton(dottime)

    elif let == "o":
        lighton(dashtime)
        lighton(dashtime)
        lighton(dashtime)

    elif let == "sos":

        lighton(s)

        lighton(dashtime)
        lighton(dashtime)
        lighton(dashtime)       

        lighton(dottime)    
        lighton(dottime) 
        lighton(dottime)        

    else: print ("Letter not recognized - try again")


GPIO.cleanup()

print("Bye Bye")   
