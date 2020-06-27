---
layout: post
title: Image alignment when batch scanning with SilverFast and the Reflecta RPS 10M film scanner
image: 
tags: [photography, scanning]
---

If you're like me, you read the reviews of the Reflecta RPS 10M scanner and had visions of being able to feed a complete roll of film into the scanner and come back in a couple of hours with a folder full of images. But then you started working with the SilverFast interface and reading through the documentation, searching YouTube for tutorial videos that weren't about flatbed scanners, and being baffled by the UI. 

It might be helpful, but I didn't want to pay an additional $30 for an eBook of documentation for an already expensive piece of software. So, I've been doing some experimenting to learn how to use the tool.

One of the most initially frustrating challenges was getting the negatives from a film strip to line up. The scanner should be able to detect edges, but using the Overview tool and clicking on "Adjust offset" didn't seem to do anything. The arrows under each thumbnail shown in the help pages don't appear in the Overview window.

I finally figured out how I think frame alignment is supposed to work with the RPS 10M:

- Start the software
- Insert film
    - Software restarts to use th film feed "holder"
- Click Overview and select the images you want to scan. (Blue highlight is selected, no highlight is unselected.)
- When completed, click OK
    - Prescans the first image
- When finished, click Overview again
- Click Adjust Offset
    - The mouse pointer changes from a black to a white cursor. This indicates that it is now in Adjust Offset mode.
- Click the left edge of the preview image, just inside the black frame border.
    - Prescans image again.
- If you want to confirm the framing, click Overview again.
- Click Refresh thumbnails again
    - Confirm the aligned images are in the thumbnails.

The RPS 10M can't align individual frames, so SilverFast suggests aligning on an image somewhere in the middle of a filmstrip. If your camera produces variable image spacing, you might run into problems with an entire roll.

(I think a lot of confusion could be avoided with a popup dialog after clicking Adjust Offset, instructing the user to click on the image frame. There could be a "click this box to not show again" once the user understands the workflow.)

Once you have confirmed that the film frames are properly aligned, you can scan:
- Set the frame size and resolution. If you want to scan all the frames at 5000 dpi, you may have to use a custom image size (e.g, not A4).
- In Preferences, you can turn Perform Auto Frame Detection *on*, so SilverFast finds the border of the image for each individual frame.
- In Preferences, you can also turn Auto frame inset *off*, if you want the software to try to go to the edge of each image (at the risk of incorporating some of the black frame and biasing the Auto Correction with low values).
- Select all the image corrections you want to do on the prescanned image frame.
- Long-click on Scan and select Batch Scan. Give it a filename and a sequence number, and SilverFast should use your Auto settings, find each frame, and save the selected frame scans to disk.
- If you have SilverFast Ai Studio (which is **not** required for batch scanning), you can alternatively go to Overview, highlight the images you want, and click Add Selection to add them to the Job Manager, where you can edit the individual frame settings one at a time.

I hope this helps someone else, and please let me know if you think I've gotten any of this incorrect.