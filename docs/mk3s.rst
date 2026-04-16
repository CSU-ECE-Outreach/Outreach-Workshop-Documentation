How to Use the Prusa MK3S+
==========================

1. Find the file you want to print. **Already have an STL file? Go to Step 2.**

   Use a pre-designed STL from the internet, for example Printables or Thingiverse.

   Printables by Prusa: https://www.printables.com/

   .. figure:: images-mk3s/image4.png
      :alt: Printables website home page
      :align: center
      :width: 3.81487in

   Search for what you want to print and open the file page.

   .. figure:: images-mk3s/image7.png
      :alt: Printables search and file page
      :align: center
      :width: 3.81508in

   Click **Download**.

   .. figure:: images-mk3s/image2.png
      :alt: Printables download options
      :align: center
      :width: 3.86979in

   Click the file you want to download.

   Ultimaker Thingiverse: https://www.thingiverse.com/

   .. figure:: images-mk3s/image24.png
      :alt: Thingiverse home page
      :align: center
      :width: 4.10938in

   Search for what you want to print.

   .. figure:: images-mk3s/image22.png
      :alt: Thingiverse search results
      :align: center
      :width: 4.13982in

   Click **Thing Files**.

   .. figure:: images-mk3s/image23.png
      :alt: Thingiverse file downloads
      :align: center
      :width: 4.16706in

   Click **Download** for the files you want.

2. **Log on to the machines.**

3. Open PrusaSlicer, or download it here:
   https://www.prusa3d.com/page/prusaslicer_424/

4. Start setup.

   .. figure:: images-mk3s/image19.png
      :alt: PrusaSlicer setup window
      :align: center
      :width: 4.86979in

5. Click **Next**.

6. Continue through the setup wizard.

   .. figure:: images-mk3s/image1.png
      :alt: PrusaSlicer setup options
      :align: center
      :width: 4.83854in

7. Scroll to the **MK3 Family** and select all standard profiles (0.4 mm nozzle).

8. Confirm your printer profile selections.

   .. figure:: images-mk3s/image9.png
      :alt: MK3 profile selection
      :align: center
      :width: 5.75521in

9. Click **Finish**. You are done setting up the default printer settings.

10. Main PrusaSlicer screen:

    .. figure:: images-mk3s/image18.png
       :alt: PrusaSlicer main interface
       :align: center
       :width: 6.5in

11. Press **Ctrl+I** to import a file, then navigate to the model you want.

12. File import dialog:

    .. figure:: images-mk3s/image5.png
       :alt: File import dialog
       :align: center
       :width: 6.5in

13. Your screen should look similar to this.

14. Imported model preview:

    .. figure:: images-mk3s/image13.png
       :alt: Imported model in PrusaSlicer
       :align: center
       :width: 4.35417in

15. On the sidebar, review these settings:

    - **Print settings:** Controls quality and speed. Larger layer heights print faster but reduce quality.
    - **Filament:** Select the material you are using. In the Creator Space we use PLA and PETG. **Make sure this is correct.**
    - **Printer:** Set this to **Original Prusa i3 MK3S & MK3S+**.
    - **Supports:** If your model has overhangs, set supports to **Everywhere**; otherwise leave supports off.
    - **Infill:** Controls part density. For high-load parts, increase infill. **Do not set infill above 80%.**
    - **Brim:** For tall or small-footprint parts, add a brim to improve bed adhesion.

16. Sidebar settings example:

    .. figure:: images-mk3s/image12.png
       :alt: PrusaSlicer print settings sidebar
       :align: center
       :width: 5.07813in

17. After setting everything, click **Slice Now**.

18. Sliced model previews:

    .. figure:: images-mk3s/image28.jpg
       :alt: Sliced preview example 1
       :align: center
       :width: 2.89856in

    .. figure:: images-mk3s/image27.jpg
       :alt: Sliced preview example 2
       :align: center
       :width: 2.89541in

19. Go to the SD card readers/adapters drawer and grab an SD card adapter.

    .. figure:: images-mk3s/image30.jpg
       :alt: SD card adapter drawer
       :align: center
       :width: 2.98438in

20. Example SD card and adapter:

    .. figure:: images-mk3s/image29.jpg
       :alt: SD card adapter
       :align: center
       :width: 3.02604in

21. Take the SD card from the printer you want to use and plug it into your computer.

22. SD card connected to computer:

    .. figure:: images-mk3s/image16.png
       :alt: SD card inserted into computer
       :align: center
       :width: 5.94271in

23. Click the button in the lower-right corner. Save the file to your SD card with a clear name.

24. Save dialog:

    .. figure:: images-mk3s/image20.png
       :alt: Save to SD card dialog
       :align: center
       :width: 4.66667in

25. After saving, click **Eject**.

26. Remove the SD card, return the adapter, and insert the SD card into the printer.

27. If you do not want to change filament, skip to Step 39.

28. To change filament color, press the dial. In the menu, select **Unload Filament** and press the dial again.

29. Printer menu screens:

    .. figure:: images-mk3s/image14.png
       :alt: Printer menu for unloading filament
       :align: center
       :width: 2.81771in

    .. figure:: images-mk3s/image11.png
       :alt: Printer unload filament confirmation screen
       :align: center
       :width: 2.79804in

30. Select the material type currently loaded (PET or PLA). Wait for the extruder to heat until the printer beeps.

31. Heating prompt:

    .. figure:: images-mk3s/image25.png
       :alt: Extruder heating prompt
       :align: center
       :width: 2.59302in

32. When it beeps, press the dial. The old filament will unload from the extruder.

33. Unload complete:

    .. figure:: images-mk3s/image21.png
       :alt: Filament unloaded from extruder
       :align: center
       :width: 3.15104in

34. Load the new filament into the extruder.

35. New filament loading:

    .. figure:: images-mk3s/image3.png
       :alt: Insert new filament step 1
       :align: center
       :width: 2.58853in

    .. figure:: images-mk3s/image8.png
       :alt: Insert new filament step 2
       :align: center
       :width: 2.59896in

36. Select **Autoload Filament**. The printer will purge material and ask if the color is correct. Respond accordingly, then remove purged filament from the nozzle tip.

37. Autoload screens:

    .. figure:: images-mk3s/image26.png
       :alt: Autoload filament prompt
       :align: center
       :width: 2.71354in

    .. figure:: images-mk3s/image15.png
       :alt: Filament color confirmation prompt
       :align: center
       :width: 2.71354in

38. Return to the printer main menu.

    .. figure:: images-mk3s/image14.png
       :alt: Printer main menu
       :align: center
       :width: 5.25in

39. Open the menu and select **Print from SD**.

40. Print from SD screen:

    .. figure:: images-mk3s/image6.png
       :alt: Select file from SD card
       :align: center
       :width: 4.73958in

41. Select the file you sliced earlier.

42. **Congratulations.** If all steps were followed correctly, the printer will heat the bed and extruder, then begin printing.

43. For more information, see the Prusa MK3S+ handbook:
   https://cdn.prusa3d.com/downloads/manual/prusa3d_manual_mk3s_en.pdf

44. **If you need help with a print, need advice, or something went wrong, email**
   ece_labs@colostate.edu **and we will respond as soon as possible.**
