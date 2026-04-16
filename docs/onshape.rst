Onshape Tutorial
=================
Within this workshop, we will be using Onshape, a cloud-based CAD software. You can access it at https://www.onshape.com/.

Creating an Account & and a new Document
-------------------
go to https://www.onshape.com/ and click on "Get Started". You can create a free account using your email address or sign up with Google. Follow the prompts to complete the registration process.

click on "Create" then "Document". You can name your document.
figure:: images-onshape/create_doc.png
        :alt: Creating a new document in Onshape
        :align: center

 Name it and click create

  check your settings to make sure you have the correct units selected
figure:: images-onshape/os_settings.png
    :alt: Setting units in Onshape
    :align: center

Basic Controls
-------------------
*Left click on an entity you want to select 
You will know if something is selected if its highlighted yelllow
*click it again to deselect it
*Hold down the right mouse button to pan the view
*use the scroll wheel to zoom in and out

Starting a Sketch
-------------------
Right click on the plane you want to sketch on and select "New Sketch"
figure:: images-onshape/selectd_plane.png
    :alt: selecting a plane for sketching in Onshape
    :align: center

The plane you select will be the plane that your sketch is on. You can select the top, front, or right plane to start your sketch.
    Note: you can click on the box with the planes labeled to reorient your view to look directly at the plane you want to sketch on.

Click the Sketch button to in the tool bar to start sketching. (it will the fist option furthest to the left)

Sketching
-------------------
When making your sketch your goal is to create a 2D fully defined base for your 3D object
 This is done by use of Onshape's sketching tools to make create the lines of your sketch and defining it with dimensions and relations.

Using most of the sketching tools in onshape involes selecting the tool you want to use and then selecting the point on your sketch plane you want your starting point to be, dragging your mouse to modify the shape or size of the entity you are creating, and then clicking again to set the end point of the entity.

Dimensioning
 You can use the dimension tool to set any dimension within your sketch. 


For learning purposes, let's make a cube without using the rectangle tool.

1. Select the line tool and make an enclosed shape with 4 sides that is intentionally asemetric and weird 
 (start at the orgin to make it easier to dimension later)
 you will know if your shape is enclosed if the inside of the shape is shaded gray

2. Use relations and dimensions to turn that weird shape into a square. 
    * To add a relation, select all of the entities you want to relate and then click on the relation you want to add in the toolbar. For example, to make two lines parallel, select the two lines and then click on the "Parallel" relation in the toolbar.
    * To add a dimension, select the entities you want to dimension and then click on the dimension tool in the toolbar. Click again to place the dimension and then enter the desired value.

Your sketch is fully defined when all of the lines in your sketch turn from blue to black. This means that you are unable to move any of the lines in your sketch without changing the dimensions or relations you have set.
 Your sketch being fully defined is important because it ensures that it cannot be accidentally modified and fits the specifications you want it to. 

3. Once your sketch is fully defined, you can now extrude it
    *to extrude a shape you'll want to make sure that its fully enclosed
    *select the shape you want to extrude and then click the extrude tool
     this will open a menu where you can control modify the settings of your extrusion.
        *for a simple extrusion, make sure you have have 'add' selected and select blind for an extrusion with a specific depth. You can also swap the direction of your extrusion by clicking the arrow indicating the direction the extrusion is going.


You did it!!!


With your cube that you made you can now use some of onshape's 3d tools to modify it.
    *fillet- rounds the edge of your cube
    *chamfer- creates a beveled edge on your cube
    *shell- hollows out your cube and creates a wall thickness that you can specify
You can also use the sketch tool on any face of your cube to add more features to it. 

Try putting a hole through your cube
    1. select the face you want to start the hole from and start a new sketch
    2. make sure you have a centered hole make use of some contruction geometry. This are lines that you designate as "imaginary" and use to build other goemetry off of. 
     We're going to make two contruction lines by making a line that goes from the top of the cube to the bottom and making its starting point the midpoint of the top edge.
     To make it a construction line, press the the 'i' key.
    3. Now use the circle tool to make the outline of your hole, making the center of the cicle to be the midpoint of the contruction line you just made.
    4. To make the cut in the cube select the circle and then click the extrude tool. To remove material instead of adding material, select "remove" instead of "add" in the extrude menu.
    5. Specify how far through the cube you want the hole to go. If you want to make the hole go all the way through, select "through all" instead of "blind".

    Congratualatios you made a cube with a hole in it!!

If you want to try and make something more complicated here is a part that is used during the 